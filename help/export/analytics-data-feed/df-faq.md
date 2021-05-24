---
description: Häufig gestellte Fragen zu Daten-Feeds
keywords: Daten-Feed;Auftrag;vor Spalte;nach Spalte;Groß-/Kleinschreibung
title: Häufig gestellte Fragen zu Daten-Feeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
source-git-commit: 7312b61b8d73f45afa3eb9aac73cc4d5fd39bc82
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 54%

---

# Häufig gestellte Fragen zu Daten-Feeds

Häufig gestellte Fragen zu Daten-Feeds.

## Müssen Feed-Namen eindeutig sein?{#section_EF38BB51A7E240D69DAD4C07A34D9AD5}

Datenfeed-Dateinamen umfassen die Report Suite-ID und das Datum. Zwei Feeds, die für dieselbe RSID und denselben Termin bzw. dieselben Termine konfiguriert sind, haben denselben Dateinamen. Wenn diese Feeds in dasselbe Verzeichnis gesendet werden, überschreibt eine Datei die andere. Um das Überschreiben einer Datei zu verhindern, können Sie keinen Feed erstellen, der einen vorhandenen Feed im selben Verzeichnis überschreiben könnte.

Wenn Sie versuchen, einen Feed mit dem Dateinamen eines anderen Feeds zu erstellen, führt dies zu der folgenden Meldung:

Wenn dieser Fehler vorliegt, ziehen Sie die folgenden Fehlerumgehungen in Erwägung:

* Bereitstellungspfad ändern
* Termine ändern, falls möglich
* Report Suite ändern, falls möglich

## Wann werden die Daten verarbeitet? {#section_6346328F8D8848A7B81474229481D404}

Bevor stündliche oder tägliche Daten verarbeitet werden, warten die Daten-Feeds, bis alle Treffer, die innerhalb des Zeitrahmens (Tag oder Stunde) in die Datenerfassung eingehen, in Data Warehouse geschrieben wurden. Anschließend erfassen die Daten-Feeds die Daten mit Zeitstempeln, die in diesen Zeitrahmen fallen, komprimieren die Daten und senden sie per FTP. Bei stündlichen Feeds werden die Daten normalerweise innerhalb von 15 bis 30 Minuten nach Ablauf der entsprechenden Stunde aus dem Data Warehouse geschrieben, es gibt jedoch keinen festgelegten Zeitraum. Wenn es keine Daten mit Zeitstempeln gibt, die in diesen Zeitrahmen passen, erfolgt der Prozess im nächsten Zeitrahmen erneut. Der aktuelle Daten-Feed-Prozess nutzt das Feld `date_time`, um zu ermitteln, welche Treffer zur entsprechenden Stunde gehören. Dieses Feld basiert auf der Zeitzone der Report Suite.

## Was ist der Unterschied zwischen Spalten mit `post_`-Präfix und Spalten ohne `post_`-Präfix?

Spalten ohne das Präfix `post_` enthalten Daten, die exakt so sind, wie sie an die Datenerfassung gesendet wurden. Spalten mit dem Präfix `post_` enthalten den Wert nach der Verarbeitung. Beispiele, die einen Wert ändern können, sind Variablenpersistenz, Verarbeitungsregeln, VISTA-Regeln, Währungsumrechnung oder andere serverseitige Logik, die Adobe anwendet. Adobe empfiehlt, nach Möglichkeit die `post_`-Version einer Spalte zu verwenden.

Wenn für eine Spalte keine `post_`-Version vorliegt (z. B. bei `visit_num`), kann die Spalte als Post-Spalte betrachtet werden.

## Wie gehen Daten-Feeds mit Groß-/Kleinschreibung um?

In Adobe Analytics wird bei den meisten Variablen beim Reporting nicht zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise werden „schnee“, „Schnee“, „SCHNEE“ und „sChnee“ alle als gleicher Wert betrachtet. Die Groß-/Kleinschreibung wird in Daten-Feeds beibehalten.

Wenn Sie unterschiedliche Schreibweisen desselben Werts zwischen Nicht-Post- und Post-Spalten sehen (z. B. „schnee“ in der Pre-Spalte und „Schnee“ in der Post-Spalte), verwendet Ihre Implementierung auf Ihrer Site sowohl Groß- als auch Kleinbuchstaben. Die Variante in der Post-Spalte wurde entweder zuvor eingereicht und ist in einem virtuellen Cookie gespeichert, oder sie wurde etwa zur selben Zeit für diese Report Suite verarbeitet.

## Enthalten Daten-Feeds Bots, die nach Admin Console-Bot-Regeln gefiltert wurden?

Daten-Feeds enthalten keine Bots, die nach [Admin Console-Bot-Regeln](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/bot-removal/bot-removal.html) gefiltert wurden.

## Warum werden in der Daten-Feed-Spalte `event_list` oder `post_event_list` mehrere `000`-Werte angezeigt?

Einige Tabellen-Editoren, insbesondere Microsoft Excel, runden automatisch große Zahlen. Die Spalte `event_list` enthält viele kommagetrennte Zahlen, was manchmal dazu führt, dass Excel sie als eine große Zahl behandelt. Die letzten Ziffern werden auf `000` gerundet.

Adobe empfiehlt deswegen, `hit_data.tsv`-Dateien nicht automatisch in Microsoft Excel zu öffnen. Verwenden Sie stattdessen das Excel-Dialogfeld „Daten importieren“ und stellen Sie sicher, dass alle Felder als Text behandelt werden.

## Warum fehlen bei einigen Betreibern Informationen in der Spalte &quot;Domain&quot;? {#section_B7508D65370442C7A314EAED711A2C75}

Einige Mobilnetzbetreiber (wie T-Mobile und O1) bieten keine Domänen mehr für Reverse-DNS-Lookups an. Daher sind die Daten nicht für die Domänenberichterstellung verfügbar.

## Warum kann ich &quot;stündliche&quot;Dateien nicht aus Daten extrahieren, die älter als sieben Tage sind?

Bei Daten, die älter als 7 Tage sind, werden die &quot;stündlich&quot;-Dateien eines Tages zu einer einzigen &quot;Täglich&quot;-Datei zusammengefasst.

Beispiel: Am 9. März 2021 wird ein neuer Daten-Feed erstellt und die Daten vom 1. Januar 2021 bis zum 9. März werden als &quot;Stündlich&quot;bereitgestellt. Die &quot;Stündlich&quot;-Dateien, die vor dem 2. März 2021 vorlagen, werden jedoch in einer einzigen &quot;Täglich&quot;-Datei zusammengefasst. Sie können &quot;Stündliche&quot;Dateien nur aus Daten extrahieren, die weniger als 7 Tage nach dem Erstellungsdatum alt sind. In diesem Fall vom 2. März bis 9. März.

## Welche Auswirkungen hat die Sommerzeit auf stündliche Daten-Feeds? {#section_70E867D942054DD09048E027A9474FFD}

In bestimmten Zeitzonen ändert sich die Zeit zweimal jährlich aufgrund von Sommerzeitdefinitionen. Die Datenfeeds berücksichtigen die Zeitzone, für die die Report Suite konfiguriert ist. Wenn die Zeitzone für die Report Suite keine DST-Nutzung ist, wird die Dateibereitstellung normal wie an jedem anderen Tag fortgesetzt. Wenn die Zeitzone der Report Suite DST verwendet, wird die Dateibereitstellung für die Stunde geändert, in der die Zeitänderung erfolgt (normalerweise 2:00 Uhr morgens).

Bei der Umstellung von Normalzeit auf Sommerzeit (&quot;Spring Forward&quot;) erhält der Kunde nur 23 Dateien. Die Stunde, die in der DST-Transition übersprungen wird, wird weggelassen. Wenn die Umstellung beispielsweise um 2 Uhr erfolgt, erhalten sie eine Datei für 1:00 Uhr und eine Datei für 3:00 Uhr. Es gibt keine 2:00-Datei, da sie um 2:00 Uhr Normalzeit zu 3:00 Uhr Sommerzeit wird.

Bei der Umstellung von Sommerzeit auf Normalzeit (im Herbst) erhält der Kunde 24 Dateien. Die Stunde der Transition enthält jedoch Daten von zwei Stunden. Wenn die Umstellung beispielsweise um 2:00 Uhr erfolgt, wird die Datei für 1:00 Uhr um eine Stunde verzögert, sie enthält jedoch Daten für zwei Stunden. Es enthält Daten von 1:00 Uhr Sommerzeit bis 2:00 Uhr Normalzeit (was 3:00 Uhr Sommerzeit gewesen wäre). Die nächste Datei beginnt um 2:00 Uhr Normalzeit.

## Wie behandelt Analytics FTP-Übertragungsfehler? {#section_4BD44E9167F0494FB2B379D2BA132AD8}

Im Falle eines FTP-Übertragungsfehlers (Anmeldung verweigert, Verbindung unterbrochen, Kontingent überschritten usw.) versucht Adobe automatisch, eine Verbindung herzustellen und sendet die Daten bis zu dreimal separat. Sollten die Fehler weiterhin bestehen, wird der Feed als fehlgeschlagen markiert und es wird eine E-Mail-Benachrichtigung gesendet.

Wenn eine Übertragung fehlschlägt, können Sie einen Auftrag erneut ausführen, bis er erfolgreich ist.

Wenn Sie Probleme haben, einen Daten-Feed auf Ihrer FTP-Site anzuzeigen, finden Sie weitere Informationen unter [Fehlerbehebung bei Aufträgen](jobs-troubleshooting.md).

## Wie sende ich einen Job erneut? {#section_BFD4447B0B5946CAAEE4F0F03D42EDFD}

Nachdem Sie das Bereitstellungsproblem überprüft/korrigiert haben, führen Sie den Vorgang erneut aus, um die Dateien abzurufen.

## Was ist die BucketOwnerFullControl-Einstellung für Amazon S3-Datenfeeds? {#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D}

Bei einer üblichen Verwendung von Amazon S3 erstellt der Kontoinhaber eines Amazon Web Services (AWS)-Kontos zunächst einen Bucket. Dann erstellt er einen Benutzer, der dazu berechtigt ist, Objekte in diesem Bucket zu erstellen. Schließlich stellt der Kontoinhaber die Anmeldeinformationen für diesen Benutzer zur Verfügung. In diesem Fall gehören die Objekte eines Benutzers zum selben Konto, und der Kontoinhaber hat implizit die volle Kontrolle über das Objekt (Lesen, Löschen usw.). Dieser Prozess ähnelt der Funktionsweise der FTP-Bereitstellung.

AWS ermöglicht es Benutzern auch, Objekte in einem Behälter zu erstellen, der zu einem anderen Benutzerkonto gehört. Beispiel: Zwei AWS-Benutzer, Benutzer A und Benutzer B, verfügen über kein gemeinsames AWS-Konto, möchten aber in einem anderen Bucket Objekte erstellen. Erstellt Benutzer A einen Bucket, beispielsweise Bucket A, so kann Benutzer A eine Bucket-Richtlinie festlegen, die Benutzer B explizit erlaubt, in Bucket A Objekte zu erstellen, auch wenn der Bucket nicht Benutzer B gehört. Diese Richtlinie kann von Vorteil sein, da es nicht erforderlich ist, dass Benutzer A und Benutzer B Anmeldeinformationen austauschen. Stattdessen stellt Benutzer B Benutzer A die Nummer seines Benutzerkontos zur Verfügung und Benutzer A erstellt eine Bucket-Richtlinie, die im Wesentlichen aussagt, dass „Benutzer B Objekte in Bucket A erstellen darf“.

**BucketOwnerFullControl** beinhaltet kontenübergreifende Berechtigungen zum Erstellen von Objekten in anderen Buckets. Wenn Benutzer B ein Objekt in den Bucket von Benutzer A hochlädt, &quot;besitzt&quot;Benutzer B dieses Objekt weiterhin und Benutzer A erhält standardmäßig keine Berechtigungen für dieses Objekt, obwohl Benutzer A Eigentümer des Buckets ist. Dies liegt daran, dass Objekte keine Berechtigungen vom übergeordneten Behälter erben. Benutzer B muss Benutzer A explizit Berechtigungen einräumen, da Benutzer B immer noch der Eigentümer des Objekts ist. Um diese Berechtigung zu erteilen, muss Benutzer B das Objekt mit einer BucketOwnerFullControl-ACL hochladen, die angibt, dass dem Bucket-Eigentümer (Benutzer A) vollständige Berechtigungen für das Objekt (Lesen, Schreiben, Löschen usw.) gewährt werden, auch wenn das Objekt Benutzer B &quot;gehört&quot;.

>[!MORELIKETHIS]
>
>* [Fehlerbehebung bei Aufträgen](jobs-troubleshooting.md)

