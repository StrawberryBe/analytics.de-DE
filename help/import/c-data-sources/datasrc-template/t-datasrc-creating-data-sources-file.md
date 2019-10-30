---
description: Die Importdatei-Vorlage hilft Ihnen, mit dem Import zu beginnen.
seo-description: Die Importdatei-Vorlage hilft Ihnen, mit dem Import zu beginnen.
seo-title: Importdatei-Vorlage generieren
solution: Analytics
subtopic: Datenquellen
title: Importdatei-Vorlage generieren
topic: Entwickler und Implementierung
uuid: bcd90e34-42e6-4cd1-b67e-87586dea25d8
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Importdatei-Vorlage generieren

Die Importdatei-Vorlage hilft Ihnen, mit dem Import zu beginnen.

Sie sind nicht auf die in der Vorlage definierten Spalten beschränkt. Sie können bei Bedarf weitere Spalten hinzufügen, solange die Metrik oder Definition für den ausgewählten Datenverarbeitungstyp unterstützt wird. Sie können die für jeden Typ unterstützten Metriken und Dimensionen in den folgenden Abschnitten anzeigen: [Webprotokoll](../../../import/c-data-sources/c-datasrc-types/datasrc-web-log.md#concept_E25D89C8B90A41FEB7DF4E936CACEE2B), [Traffic](../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC), [Konversion](../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0), [Transaktions-ID](../../../import/c-data-sources/c-datasrc-types/datasrc-transactionid.md#concept_A97302E9EC45468A8F30285FACE8C776), [Besucher-ID](../../../import/c-data-sources/c-datasrc-types/datasrc-visitorid.md#concept_1CFAA61D57A84B22A41F7A8E0DFCAAB5)[](../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED),Full Processing). For example, for a traffic data type, you can add a column for any metric or dimensions listed in [Traffic](../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC).

Nach dem Erstellen können Sie die Vorlage herunterladen, Daten in die Vorlage eingeben und dann die Daten auf die Data Sources-FTP-Site hochladen. Nach der Verarbeitung durch den Data Sources-Server stehen die importierten Daten zur Verwendung in Ihren Analytics-Berichten zur Verfügung.

Die Datenquelle-Vorlage ist eine .txt-Datei, die Sie mit einem beliebigen Texteditor öffnen können. Am einfachsten ist es jedoch, wenn Sie in Microsoft Excel oder einer anderen Tabellenkalkulationsanwendung mit der Vorlage arbeiten. Der Vorlageninhalt ist von der Auswahl im Datenquelle-Aktivierungsassistent abhängig.

Siehe [Importdatei-Referenz](../../../import/c-data-sources/datasrc-template/datasrc-import-file-reference.md#concept_472095E1D011434D98A21C101A4618BD) für weitere Details.

1. Bei Analytics anmelden.
1. In the Suite header, select **[!UICONTROL Admin]** &gt; **[!UICONTROL Data Sources]**.
1. On the **[!UICONTROL Data Sources Create]** tab, select a template category and type.
1. Review the Activation Instructions/Information, then click **[!UICONTROL Activate]**.

   Schritt Ergebnis 1. Wählen Sie die Optionen zur Vorlagenerstellung im Datenquelle-Aktivierungsassistenten aus.

   | Assistentenseite | Feld | Beschreibung |
   |--- |--- |--- |
   | 1 | Name | Der Vorlagenname, den Analytics im Datenquellen-Manager anzeigt. |
   | 1 | E-Mail | Die E-Mail-Adresse, die alle Benachrichtigungen hinsichtlich der Nutzung dieser Datenquelle-Vorlage erhält. |
   | 1 | Kontrollkästchen für relevante Gebühren | Aktivieren Sie das Kontrollkästchen, um Ihre Annahme der Gebühren für die Verwendung dieser Datenquelle-Vorlage anzugeben. |
   | 2 | Metrik auswählen | Wählen Sie die mit dieser Datenquelle zu importierenden Metriken aus. Analytics empfiehlt bestimmte Metriken basierend auf der in Schritt 3 ausgewählten Datenquellen-Kategorie und -Typ.  Um eine andere Metrik auszuwählen, geben Sie den Namen in ein leeres Feld ein und aktivieren Sie das Kontrollkästchen, um die Metrik zu aktivieren. |
   | 3 | Metrik zuordnen | Wählen Sie ein Analytics-Ereignis aus, um jede importierte Metrik zu erhalten, die auf Seite 2 des Assistenten ausgewählt wurde.  Dabei sollte es sich um neue, nicht zugewiesene Ereignisse handeln, denen Sie zuvor Namen zugeordnet haben, die den importierten Metrikdaten entsprechen, die sie über Data Sources erhalten.  Wenn eine eVar-, Produkt- oder Trackingcode-Variable eine Zielvariable ist und die hochgeladenen Werte vorhandenen erfassten Werten entsprechen, fügen die hochgeladenen Ereignisse im Grunde den vorhandenen Werten Metriken hinzu. Sie können beispielsweise eine Metrik für "Offline-Bestellungen"mit einer Produktdatendimension erstellen, die bereits über Produktansichten, Checkouts und Bestellungen als vorhandene Metriken verfügt. |
   | 4 | Datendimensionen auswählen | Wählen Sie die Datendimensionen aus, um die importierten Metriken aus dieser Datenquelle zu unterteilen. Analytics empfiehlt bestimmte Datendimensionen basierend auf dem in Schritt 3 ausgewählten Datenquellentyp.  Um eine andere Datendimension auszuwählen, geben Sie den Namen in ein leeres Feld ein und aktivieren Sie das Kontrollkästchen, um die Datendimension zu aktivieren. |
   | 5 | Datendimensionen zuordnen | Wählen Sie einen Standardbericht oder eine eVar aus, um jede auf Seite 4 des Assistenten ausgewählte importierte Datendimension zu erhalten. |

1. Nachdem die Vorlage erstellt wurde, kopieren Sie die Daten in die entsprechenden Spalten aus der Datenquelle-Vorlage und stellen Sie dabei sicher, dass Sie das für diese Datenspalte erforderliche Datenformat berücksichtigen.

   Schritt Ergebnis 1. Speichern Sie die Data Sources-Datei unter einem Namen gemäß der von Ihnen ausgewählten Namensgebungskonvention. Adobe empfiehlt, eine konsistente Namensgebungskonvention für alle Data Sources-Dateien zu verwenden. Verwenden Sie eine allgemeine Dateierweiterung wie .txt oder .tsv (oder verwenden Sie keine Erweiterung).

