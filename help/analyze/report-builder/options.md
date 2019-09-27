---
description: Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.
seo-description: Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.
seo-title: Report Builder-Optionen
solution: Analytics
title: Report Builder-Optionen
topic: ReportBuilder
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Report Builder-Optionen

Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.

1. Klicken Sie in der Add-ins-Symbolleiste auf **[!UICONTROL Optionen]** ![](assets/options_icon.png):

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL Ausführungsdatum] |  |
| Auf aktuelles Datum festlegen | Sie können das [!UICONTROL Ausführungsdatum] angeben oder so einstellen, dass ReportBuilder das aktuelle Datum verwendet bzw. fragt, welches Datum für eine Aktualisierung verwendet werden soll. |
| Beim Aktualisieren zum Festlegen auffordern | Sie können das [!UICONTROL Ausführungsdatum] beim Aktualisieren einer Anforderung aktualisieren. |
| [!UICONTROL Datenneuigkeit] |  |
| [!UICONTROL Aktuelle Daten einschließen] | Sie können die Datenlatenz (auch als [!UICONTROL Datenneuigkeit] bezeichnet) auf die Minute genau im Bericht anzeigen, manchmal sogar schon, bevor die Daten von Adobe Analytics bearbeitet wurden.<br>When you do not use this option,  finalized mode (processed) is used, which is typically more latent.[](https://marketing.adobe.com/resources/help/en_US/reference/data_latency.html)<br>Diese Einstellungen gelten für alle Anforderungen in dieser Arbeitsmappe, die kompatible aktuelle Daten enthalten. Ist eine Anforderung nicht kompatibel, wird der finalisierte Modus angewendet.<br>Note the following situations for using the Include Current Data mode:Format Options: You can specify whether to display this information (Data Recency) when formatting display headers.<br>****[](../../analyze/report-builder/layout/t-format-display-headers.md)<br>**Aufgliederungen**: Nicht unterstützt. Wenn der [!UICONTROL Datenneuigkeit]-Modus auf „aktuelle Daten“ eingestellt ist und eine der Anforderungen ein Aufgliederungselement enthält, wird der Modus für diese Anforderung wieder auf „nicht aktuell“ zurückgesetzt. Alle anderen Anforderungen nutzen jedoch weiterhin den Modus „Aktuelle Daten“.<br>**Anforderungs-Manager**: Sie können die Spalte „Aktuelle Daten“ im Anforderungs-Manager anzeigen lassen, um zu sehen, welche Einstellung für eine geplante Anforderung gilt.<br>**Geplante Arbeitsmappen**. Dieser Modus wird während der Planung auf Arbeitsmappen-Ebene gespeichert. If you open a scheduled workbook that is using finalized data, and apply [!UICONTROL Include Current Data], current mode is used thereafter.<br>**Berechtigungen**: Diese Option wird nur Benutzern angezeigt, die Zugriff auf die aktuellen Daten haben.  Wenn diese Option aktiviert ist, wird eine Warnung ausgegeben, wenn eine oder mehrere Anforderungen nicht angewendet werden können. |
| Anforderungswarnungen bezüglich inkompatibler aktueller Daten deaktivieren | Mit dieser Option werden Warnungen angezeigt, wenn der Modus [!UICONTROL Aktuelle Daten einschließen] ausgewählt wird, der Datenmodus aber nicht auf die bearbeitete Anforderung übertragen werden kann.  Wenn Sie zum Beispiel [!UICONTROL Aktuelle Daten einschließen] auswählen und dann eine Anforderung bearbeiten, bei der ein Segment ausgewählt wird, so wird eine Warnung angezeigt. |
| ReportBuilder-Anforderungen in lokaler Datei protokollieren (für Fehlerbehebung) | Sie können Anforderungen in einer lokalen Datei protokollieren. Verwenden Sie diese Protokolldatei für die Fehlerbehebung. |
| Eingegebenen Wert interpretieren... | Eingegebenen Wert in Filtersteuerung erst als Zellposition interpretieren und dann als Filterausdruck.<br>Wenn Sie z. B. eine Top 10-Seite-Anforderung mit Filterschuhen erstellen, zeigt die Anforderung eine Zelle an, die Folgendes enthält:   Filter: Top 1-10 Seite, Seite enthält Schuhe |
| Bei Verfügbarkeit einer neuen Version aktualisieren | Sie werden durch das System benachrichtigt, wenn eine neue Version zur Installation bereit steht. |
