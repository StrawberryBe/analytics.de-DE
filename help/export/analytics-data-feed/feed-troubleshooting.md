---
description: Dieser Abschnitt enthält Informationen zu allgemeinen Problemen.
keywords: Data Feed;troubleshooting
title: Fehlerbehebung bei Daten-Feeds
uuid: 4be981ab-3a61-4099-9b0d-785d2ac2492a
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '938'
ht-degree: 100%

---


# Fehlerbehebung bei Daten-Feeds

Dieser Abschnitt enthält Informationen zu allgemeinen Problemen.

## Fehler beim Speichern des Feeds  {#section_EF38BB51A7E240D69DAD4C07A34D9AD5}

Datenfeed-Dateinamen umfassen die Report Suite-ID und das Datum. Zwei Feeds, die für dieselbe RSID und denselben Termin bzw. dieselben Termine konfiguriert sind, haben denselben Dateinamen. Wenn diese Feeds in dasselbe Verzeichnis gesendet werden, überschreibt eine Datei die andere. Um das Überschreiben einer Datei zu verhindern, können Sie keinen Feed erstellen, der einen vorhandenen Feed im selben Verzeichnis überschreiben könnte.

Wenn Sie versuchen, einen Feed mit dem Dateinamen eines anderen Feeds zu erstellen, führt dies zu der folgenden Meldung:

Wenn dieser Fehler vorliegt, ziehen Sie die folgenden Fehlerumgehungen in Erwägung:

* Bereitstellungspfad ändern
* Termine ändern, falls möglich
* Report Suite ändern, falls möglich

## BucketOwnerFullControl-Einstellungen für Amazon S3-Datenfeeds  {#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D}

Bei einer üblichen Verwendung von Amazon S3 erstellt der Kontoinhaber eines Amazon Web Services (AWS)-Kontos zunächst einen Bucket. Dann erstellt er einen Benutzer, der dazu berechtigt ist, Objekte in diesem Bucket zu erstellen. Schließlich stellt der Kontoinhaber die Anmeldeinformationen für diesen Benutzer zur Verfügung. In diesem Fall gehören die Objekte eines Benutzers zum selben Konto und der Kontoinhaber hat implizit die vollständige Kontrolle über das Objekt (lesen, löschen, usw.). Dies entspricht der Funktionsweise der FTP-Bereitstellung.

Mit AWS kann ein Benutzer aber auch Objekte in einem Bucket erstellen, die einem völlig anderen Benutzerkonto zugeordnet sind. Beispiel: Zwei AWS-Benutzer, Benutzer A und Benutzer B, verfügen über kein gemeinsames AWS-Konto, möchten aber in einem anderen Bucket Objekte erstellen. Erstellt Benutzer A einen Bucket, beispielsweise Bucket A, so kann Benutzer A eine Bucket-Richtlinie festlegen, die Benutzer B explizit erlaubt, in Bucket A Objekte zu erstellen, auch wenn der Bucket nicht Benutzer B gehört. Dies kann vorteilhaft sein, da es nicht notwendig ist, dass Benutzer A und Benutzer B Anmeldeinformationen austauschen. Stattdessen stellt Benutzer B Benutzer A die Nummer seines Benutzerkontos zur Verfügung und Benutzer A erstellt eine Bucket-Richtlinie, die im Wesentlichen aussagt, dass „Benutzer B Objekte in Bucket A erstellen darf“.

**BucketOwnerFullControl** beinhaltet kontenübergreifende Berechtigungen zum Erstellen von Objekten in anderen Buckets. Lädt Benutzer B ein Objekt in den Bucket von Benutzer A, „gehört“ das Objekt immer noch Benutzer B und Benutzer A hat standardmäßig keine Berechtigungen an dem Objekt, auch wenn der Bucket Benutzer A gehört – Objekte erben keine Berechtigungen des übergeordneten Buckets. Benutzer B muss Benutzer A explizit Berechtigungen einräumen, da Benutzer B immer noch der Eigentümer des Objekts ist. Für dieses kontenübergreifende Hochladen bietet AWS eine BucketOwnerFullControl-ACL, die vom Eigentümer des Behälters (Benutzer A) verwendet werden kann und vollständige Berechtigungen an dem Objekt (lesen, schreiben, löschen, etc.) beinhaltet, auch wenn das Objekt Benutzer B „gehört“.

## Übertragungsfehler {#section_4BD44E9167F0494FB2B379D2BA132AD8}

Im Fall eines FTP-Übertragungsfehlers (Anmeldung verweigert, Verbindung getrennt, Kontingent überschritten usw.) versucht Adobe automatisch, eine Verbindung herzustellen und sendet die Daten bis zu drei Mal separat. Sollten die Fehler weiterhin bestehen, wird der Feed als fehlgeschlagen markiert und es wird eine E-Mail-Benachrichtigung gesendet.

Im Fall eines Übertragungsfehlers können Sie  einen Auftrag erneut ausführen, bis der Vorgang erfolgreich ausgeführt wird.

## Optionen zum erneuten Senden {#section_BFD4447B0B5946CAAEE4F0F03D42EDFD}

Nachdem Sie das Bereitstellungsproblem überprüft/korrigiert haben, führen Sie den Vorgang erneut aus, um die Dateien abzurufen.

## Auswirkungen der Sommerzeit auf stündliche Daten-Feeds {#section_70E867D942054DD09048E027A9474FFD}

Für einige Zeitzonen ändert sich zweimal jährlich die Uhrzeit aufgrund der Sommerzeitdefinition. Die Datenfeeds berücksichtigen die Zeitzone, für die die Report Suite konfiguriert ist. Wenn in der für die Report Suite gewählten Zeitzone keine Sommerzeit berücksichtigt wird, erfolgt die Dateibereitstellung ganz normal wie an den anderen Tagen des Jahres. Wenn in der für die Report Suite gewählten Zeitzone jedoch die Sommerzeit berücksichtigt wird, ändert sich die Dateibereitstellung für die Stunde, in der die Zeitumstellung erfolgt (normalerweise 2:00 Uhr morgens).

Bei der Umstellung von Normalzeit auf Sommerzeit (im Frühling) erhält der Kunde nur 23 Dateien. Die Stunde, die bei der Zeitumstellung übersprungen wird, entfällt. Beispiel: Wenn die Umstellung um 2:00 Uhr erfolgt, erhalten die Kunden eine Datei für 1:00 Uhr und eine Datei für 3:00 Uhr. Es gibt keine Datei für 2:00 Uhr, da 2:00 Uhr Normalzeit während der Sommerzeit 3:00 Uhr entspricht.

Bei der Umstellung von Sommerzeit auf Normalzeit (im Herbst) erhält der Kunde 24 Dateien. Die Stunde der Zeitumstellung enthält dabei Daten für insgesamt 2 Stunden. Beispiel: Wenn die Umstellung 2:00 Uhr erfolgt, erhalten die Kunden die Datei für 1:00 Uhr verspätet, diese umfasst jedoch Daten für insgesamt zwei Stunden. Nämlich Daten von 1:00 Uhr Sommerzeit bis 2:00 Uhr Normalzeit (was 3:00 Uhr nach Sommerzeit entspricht). Die nächste Datei beginnt ab 2:00 Uhr Normalzeit.

## Keine Daten für Zeitraum  {#section_72510794694D42A9A75C966B812AEB0F}

Sie können einen Datenfeed optional so konfigurieren, dass eine Manifestdatei bereitgestellt wird, wenn für einen bestimmten Zeitraum keine Daten erfasst werden. Wenn Sie diese Option aktivieren, erhalten Sie eine Manifestdatei, die folgendem Schema entspricht:

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 0
 Data-Files: 0
 Total-Records: 0
```

## Keine Domäneninfo für Domänenberichterstellung  {#section_B7508D65370442C7A314EAED711A2C75}

Einige Mobilnetzbetreiber (wie T-Mobile und O1) bieten keine Domänen mehr für Reverse-DNS-Lookups an. Daher sind die Daten nicht für die Domänenberichterstellung verfügbar.

## Übersicht zu Datenverarbeitung {#section_6346328F8D8848A7B81474229481D404}

Bevor stündliche oder tägliche Daten verarbeitet werden, warten die Daten-Feeds, bis alle Treffer, die innerhalb des Zeitrahmens (Tag oder Stunde) in die Datenerfassung eingehen, in Data Warehouse geschrieben wurden. Anschließend erfassen die Daten-Feeds die Daten mit Zeitstempeln, die in diesen Zeitrahmen fallen, komprimieren die Daten und senden sie per FTP. Bei stündlichen Feeds werden die Daten normalerweise innerhalb von 15 bis 30 Minuten nach Ablauf der entsprechenden Stunde aus dem Data Warehouse geschrieben, es gibt jedoch keinen festgelegten Zeitraum. Wenn es keine Daten mit Zeitstempeln gibt, die in diesen Zeitrahmen passen, erfolgt der Prozess im nächsten Zeitrahmen erneut. Der aktuelle Daten-Feed-Prozess nutzt das Feld `date_time`, um zu ermitteln, welche Treffer zur entsprechenden Stunde gehören. Dieses Feld basiert auf der Zeitzone der Report Suite.
