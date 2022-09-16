---
description: Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.
title: Activity Map-Einstellungen konfigurieren
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: User, Admin
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 50%

---

# Activity Map-Einstellungen konfigurieren

Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.

Rufen Sie das Activity Map-Einstellungsbedienfeld durch Klicken auf das Zahnradsymbol in der Activity Map-Symbolleiste auf.

## Allgemeine Einstellungen {#section_697A12F099494D699A4BF498598178C5}

![](assets/settings_other.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Unternehmen]** | Wählen Sie die entsprechende Unternehmensanmeldung aus. |
| **[!UICONTROL Report Suite]** | Die für Sie verfügbare Liste mit Report Suites ist nicht mehr beschränkt auf die im Web-Seiten-Tag definierten Report Suites. Sie können nun die ausgewählte Report Suite (die zu einem der Tags auf der Seite gehört) durch eine andere Report Suite ersetzen. Diese neue Report Suite muss nicht mit einem Tag auf der Seite verbunden sein. Wenn Sie die ausgewählte Report Suite in den Activity Map-Einstellungen ändern, werden beim Speichern alle betroffenen Analytics-Berichte aktualisiert.<br>**Wichtig**: [!UICONTROL Virtual Report Suites] sind nicht kompatibel mit [!UICONTROL Livemodus], nur mit [!UICONTROL Standardmodus]. Wenn Sie [!UICONTROL Livemodus] für eine Standard-Report Suite, aber wählen Sie eine [!UICONTROL Virtual Report Suite] in diesem Dialogfeld, sobald Sie auf **[!UICONTROL OK]** hier wird der Standardmodus angezeigt. Darüber hinaus wird das Kalendersteuerelement neu initialisiert, um dem Kalendertyp der Report Suite (Gregorianisch, Einzelhandel, benutzerdefiniert..) zu entsprechen. |
| **[!UICONTROL Seitenname]** | Die Seite, auf die diese Einstellungen angewendet werden. |
| **[!UICONTROL Sprache]** | Die Auswahl entspricht den angebotenen Sprachen für Adobe Analytics. |
| **[!UICONTROL Overlays bezeichnen als]** | <ul><li>**[!UICONTROL Kein Label]**: nur für Verlaufsüberlagerungen In diesem Fall vermittelt die Farbe der Überlagerung einen Sinn für den Rang des Links</li><li>**[!UICONTROL Wert]**: Der unverarbeitete Gesamtwert der Metrik für den Link</li><li>**[!UICONTROL Prozent]**: Prozentsatz der Metrik für diesen Link im Vergleich zum Gesamtwert der Metrik für die Seite.</li><li>**[!UICONTROL Rang]**: Rang dieses Links im Vergleich zu allen Links auf der gerenderten Seite</li></ul> |
| **[!UICONTROL Schriftgröße Beschriftung]** | Ermöglicht Ihnen, die Schriftgröße der Überlagerungsbeschriftung zur besseren Lesbarkeit mithilfe eines Reglers zu erhöhen oder zu verringern. |
| **[!UICONTROL Verlaufs-/Blasenfarbe]** | Um die Rangfolge von Überlagerungslinks für Verlaufs- oder Blasen überlagerungsvisualisierungen anzuzeigen, wählen Sie aus einem Farbbereich aus. |
| **[!UICONTROL Farbverlauf auf Grundlage von]** | <ul><li>**[!UICONTROL Top-30-Bewertungen]**: Die Farbintensität wird für die 30 höchsten Werte vereinheitlicht.</li><li>**[!UICONTROL Absoluter Metrikwert]**: Die Farbintensität ist eine Funktion des absoluten Metrikwerts.</li></ul> |
| **[!UICONTROL Verlaufstransparenz]** | Wählen Sie die Transparenzstufe für Verlaufsüberlagerungen. Diese Einstellung wirkt sich nicht auf die [!UICONTROL Blase] Überlagerungen. |

## Standardeinstellungen {#section_24DB95376E1A448494ECF3F57743FC19}

Diese Einstellungen gelten für die Überlagerung im Standardmodus.

![](assets/settings_standard.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Dynamische Datenfilterung]** | Mit diesem Dropdown-Menü können Sie Überlagerungen für<ul><li>(Standard) Alle Links auf der Seite</li><li>Die obere (höchste) oder untere (niedrigste) Anzahl der Ranglinks auf der Seite, wobei # eine Auswahl von 1, 10, 50 oder 100 sein kann.</li></ul> |
| **[!UICONTROL Überlagerungen für Links ausblenden, die keine Treffer erhalten haben]**. | Ein Kontrollkästchen, mit dem Überlagerungen für Links ohne Daten sichtbar werden.<ul><li>(Standard) Wenn das Kontrollkästchen aktiviert ist, wird keine Überlagerung angezeigt, wenn ein Link keine Activity Map-Linkdaten enthält.</li><li>Wenn das Kontrollkästchen deaktiviert ist und ein Link keine Activity Map-Linkdaten enthält, wird eine Überlagerung angezeigt, die die Bezeichnung &quot;-&quot;trägt, was bedeutet (nicht zutreffend). |

## Live-Einstellungen {#section_D30F6E62FB5D404090B588F396A460AF}

Diese Einstellungen gelten für die Überlagerung im Livemodus.

![](assets/settings_live.png)

| Einstellung | Beschreibung |
|---|---|
| **[!UICONTROL Anzeige oben]** | So zeigen Sie die **[!UICONTROL Gewinner]** oder **[!UICONTROL Verlierer]** (oder beides) als Überlagerungen festlegen, wählen Sie die Anzahl der Links aus. |
| **[!UICONTROL Unterste ausschließen (%)]** | Wählen Sie diese Option, um Links für Gewinner oder Verlierer auszuschließen, für die wenig Daten vorhanden sind. Wenn Sie diesen Prozentsatz der Links ausschließen, werden nur noch die Links angezeigt, für die genug Daten vorhanden sind, um relevante Gewinne oder Verluste anzuzeigen. Der Prozentsatz wird anhand der Anzahl der Links auf der Seite berechnet. Wenn Sie beispielsweise die unteren 10 % einer Liste mit 200 Links herausfiltern, werden die unteren 20 Links herausgefiltert. |
| **[!UICONTROL Automatische Aktualisierung von Daten]** | Hier können Sie entscheiden, ob die in der Benutzeroberfläche angezeigten Analytics-Daten bei der Berechnung eines neuen Zeitraums automatisch aktualisiert werden. |
| **[!UICONTROL Zeitraum für automatische Aktualisierung]** | Wenn dieses Kontrollkästchen aktiviert wird, wird die Webseite jedes Mal aktualisiert, wenn neue Daten abgerufen werden. Dadurch können die Links auf der Seite genauer mit den erfassten Daten synchronisiert werden. |
