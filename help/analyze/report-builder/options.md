---
description: Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.
title: Report Builder-Optionen
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 99%

---


# Report Builder-Optionen

Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.

1. Klicken Sie in der Add-ins-Symbolleiste auf **[!UICONTROL Optionen]** ![](assets/options_icon.png):

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL Ausführungsdatum] |  |
| Auf aktuelles Datum festlegen | Sie können das [!UICONTROL Ausführungsdatum] angeben oder so einstellen, dass Report Builder das aktuelle Datum verwendet bzw. fragt, welches Datum für eine Aktualisierung verwendet werden soll. |
| Beim Aktualisieren zum Festlegen auffordern | Sie können das [!UICONTROL Ausführungsdatum] beim Aktualisieren einer Anforderung definieren. |
| [!UICONTROL Datenaktualität] |  |
| [!UICONTROL Aktuelle Daten einschließen] | Sie können die Datenlatenz (auch als [!UICONTROL Datenaktualität] bezeichnet) auf die Minute genau im Bericht anzeigen, manchmal sogar schon, bevor die Daten von Adobe Analytics bearbeitet wurden.<br>Wenn Sie diese Option nicht verwenden, wird der finalisierte Modus (verarbeitet) verwendet, der normalerweise eine längere [Latenzzeit](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/current-data.html) hat.<br>Diese Einstellungen gelten für alle Anforderungen in dieser Arbeitsmappe, die kompatible aktuelle Daten enthalten. Ist eine Anforderung nicht kompatibel, wird der finalisierte Modus verwendet.<br>Beachten Sie die folgenden Situationen für die Verwendung des Modus [!UICONTROL Aktuelle Daten einschließen:] <br>**Formatoptionen**: Sie können angeben, ob diese Informationen ([!UICONTROL Datenaktualität]) beim [Formatieren von Anzeigeüberschriften](/help/analyze/report-builder/layout/t-format-display-headers.md) angezeigt werden sollen.<br>**Aufgliederungen**: Nicht unterstützt. Wenn der Modus [!UICONTROL Datenaktualität] auf „aktuelle Daten“ eingestellt ist und eine der Anforderungen ein Aufgliederungselement enthält, wird der Modus für diese Anforderung wieder auf „nicht aktuell“ zurückgesetzt. Alle anderen Anforderungen nutzen jedoch weiterhin den Modus „Aktuelle Daten“.<br>**Anforderungs-Manager**: Sie können die Spalte „Aktuelle Daten“ im Anforderungs-Manager anzeigen lassen, um zu sehen, welche Einstellung für eine geplante Anforderung gilt.<br>**Geplante Arbeitsmappen**. Dieser Modus wird während der Planung auf Arbeitsmappen-Ebene gespeichert. Wenn Sie eine geplante Arbeitsmappe öffnen, die finalisierte Daten nutzt, und die Option [!UICONTROL Aktuelle Daten einschließen] anwenden, wird anschließend der aktuelle Modus verwendet.<br>**Berechtigungen**: Diese Option wird nur Benutzern angezeigt, die Zugriff auf die aktuellen Daten haben.  Wenn diese Option aktiviert ist, wird eine Warnung ausgegeben, wenn eine oder mehrere Anforderungen nicht angewendet werden können. |
| Anforderungswarnungen bezüglich inkompatibler aktueller Daten deaktivieren | Mit dieser Option werden Warnungen angezeigt, wenn der Modus [!UICONTROL Aktuelle Daten einschließen] ausgewählt wird, der Datenmodus aber nicht auf die bearbeitete Anforderung übertragen werden kann.  Wenn Sie zum Beispiel [!UICONTROL Aktuelle Daten einschließen] auswählen und dann eine Anforderung bearbeiten, bei der ein Segment ausgewählt wird, so wird eine Warnung angezeigt. |
| ReportBuilder-Anforderungen in lokaler Datei protokollieren (für Fehlerbehebung) | Sie können Anforderungen in einer lokalen Datei protokollieren. Verwenden Sie diese Protokolldatei für die Fehlerbehebung. |
| Eingegebenen Wert interpretieren... | Eingegebenen Wert in Filtersteuerung erst als Zellposition interpretieren und dann als Filterausdruck.<br>Wenn Sie z. B. eine Anforderung für die Top 10 Seiten mit Schuhen über einen Filter erstellen, wird eine Zelle angezeigt, die in etwa Folgendes enthält: Filter: Top 1–10 Seiten, Seite enthält Schuhe. |
| Bei Verfügbarkeit einer neuen Version aktualisieren | Sie werden durch das System benachrichtigt, wenn eine neue Version zur Installation bereit steht. |
