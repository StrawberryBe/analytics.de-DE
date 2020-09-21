---
description: Die Importdatei-Vorlage hilft Ihnen, mit dem Import zu beginnen.
subtopic: Data sources
title: Importdatei-Vorlage generieren
topic: Developer and implementation
uuid: bcd90e34-42e6-4cd1-b67e-87586dea25d8
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '596'
ht-degree: 100%

---


# Importdatei-Vorlage generieren

Die Importdatei-Vorlage hilft Ihnen, mit dem Import zu beginnen.

Sie sind nicht auf die in der Vorlage definierten Spalten beschränkt. Sie können bei Bedarf weitere Spalten hinzufügen, solange die Metrik oder Definition für den ausgewählten Datenverarbeitungstyp unterstützt wird. Sie können die für jeden Typ unterstützten Metriken und Dimensionen in den folgenden Abschnitten anzeigen:   [Webprotokoll](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md), [Traffic](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md), [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md), [Transaktions-ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md), [Besucher-ID](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md), [Vollständige Verarbeitung](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md)). Für einen Traffic-Datentyp können Sie beispielsweise eine Spalte für eine Metrik oder Dimension hinzufügen, die im Abschnitt [Traffic](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) aufgeführt wird.

Nach dem Erstellen können Sie die Vorlage herunterladen, Daten in die Vorlage eingeben und dann die Daten auf die Data Sources-FTP-Site hochladen. Nach der Verarbeitung durch den Data Sources-Server stehen die importierten Daten in Ihren Analytics-Berichten zur Verfügung.

Die Datenquelle-Vorlage ist eine .txt-Datei, die Sie mit einem beliebigen Texteditor öffnen können. Am einfachsten ist es jedoch, wenn Sie in Microsoft Excel oder einer anderen Tabellenkalkulationsanwendung mit der Vorlage arbeiten. Der Vorlageninhalt ist von der Auswahl im Datenquelle-Aktivierungsassistent abhängig.

Siehe  [Importdatei-Referenz](/help/import/c-data-sources/datasrc-template/datasrc-import-file-reference.md) für weitere Details.

1. Bei Analytics anmelden.
1.  Wählen Sie in der Suite-Kopfzeile **[!UICONTROL Admin]** > **[!UICONTROL Data Sources]** aus.
1. Wählen Sie unter Data Sources auf der Registerkarte **[!UICONTROL „Erstellen“]** eine Vorlagenkategorie und einen Typ aus.
1. Überprüfen Sie die Aktivierungsanweisungen/-informationen und klicken Sie auf **[!UICONTROL „Aktivieren“]**. 

   Schritt Ergebnis 1. Wählen Sie die Optionen zur Vorlagenerstellung im Datenquelle-Aktivierungsassistenten aus.

   | Assistentenseite | Feld | Beschreibung |
   |--- |--- |--- |
   | 1 | Name | Der Vorlagenname, der von Analytics im Data Sources-Manager angezeigt wird. |
   | 1 | E-Mail | Die E-Mail-Adresse, die alle Benachrichtigungen hinsichtlich der Nutzung dieser Datenquelle-Vorlage erhält. |
   | 1 | Kontrollkästchen für relevante Gebühren | Aktivieren Sie das Kontrollkästchen, um die Annahme der Gebühren für die Nutzung dieser Datenquellenvorlage zu kennzeichnen. |
   | 2 | Metrik auswählen | Wählen Sie die mit dieser Datenquelle zu importierenden Metriken aus. Analytics empfiehlt bestimmte Metriken basierend auf der Datenquellenkategorie und dem Datenquellentyp, die Sie in Schritt 3 ausgewählt haben. Um eine andere Metrik auszuwählen, geben Sie den Namen in ein leeres Feld ein und aktivieren Sie das Kontrollkästchen, um die Metrik zu aktivieren. |
   | 3 | Metrik zuordnen | Wählen Sie ein Analytics-Ereignis aus, um jede auf Seite 2 des Assistenten ausgewählte importierte Metrik abzurufen.  Dabei sollte es sich um neue, nicht zugewiesene Ereignisse handeln, denen Sie zuvor Namen zugeordnet haben, die den importierten Metrikdaten entsprechen, die sie über Data Sources erhalten.  Wenn eine eVar-, Produkt- oder Trackingcode-Variable eine Zielvariable ist und die hochgeladenen Werte vorhandenen erfassten Werten entsprechen, fügen die hochgeladenen Ereignisse im Grunde den vorhandenen Werten Metriken hinzu. Sie können beispielsweise die Metrik „Offline-Bestellungen“ erstellen mit einer Produkte-Datendimension, die als Metriken bereits über Produktansichten, Kassengänge und Bestellungen verfügt. |
   | 4 | Datendimensionen auswählen | Wählen Sie die Datendimensionen aus, um die importierten Metriken aus dieser Datenquelle zu unterteilen. Analytics empfiehlt bestimmte Datendimensionen basierend auf dem Datenquellentyp, den Sie in Schritt 3 ausgewählt haben.  Um eine andere Datendimension auszuwählen, geben Sie den Namen in ein leeres Feld ein und aktivieren Sie das Kontrollkästchen, um die Datendimension zu aktivieren. |
   | 5 | Datendimensionen zuordnen | Wählen Sie einen Standardbericht oder eine eVar aus, um jede auf Seite 4 des Assistenten ausgewählte importierte Datendimension zu erhalten. |

1. Nachdem die Vorlage erstellt wurde, kopieren Sie die Daten in die entsprechenden Spalten aus der Datenquelle-Vorlage und stellen Sie dabei sicher, dass Sie das für diese Datenspalte erforderliche Datenformat berücksichtigen.

   Schritt Ergebnis 1. Speichern Sie die Data Sources-Datei unter einem Namen gemäß der von Ihnen ausgewählten Namensgebungskonvention. Adobe empfiehlt, eine konsistente Namensgebungskonvention für alle Data Sources-Dateien zu verwenden. Verwenden Sie eine gemeinsame Dateierweiterung wie .txt oder .tsv (oder verwenden Sie gar keine Erweiterung).

