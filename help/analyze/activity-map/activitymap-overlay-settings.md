---
description: Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.
title: Activity Map-Einstellungen konfigurieren
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
translation-type: tm+mt
source-git-commit: 700d3b21a238af23719b291fe60df207e916bb87
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 50%

---

# Activity Map-Einstellungen konfigurieren

Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.

Rufen Sie das Activity Map-Einstellungsbedienfeld durch Klicken auf das Zahnradsymbol in der Activity Map-Symbolleiste auf.

## Allgemeine Einstellungen {#section_697A12F099494D699A4BF498598178C5}

![](assets/settings_other.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Unternehmen]** | Wählen Sie die entsprechende Firma aus. |
| **[!UICONTROL Report Suite]** | Die für Sie verfügbare Liste mit Report Suites ist nicht mehr beschränkt auf die im Web-Seiten-Tag definierten Report Suites. Sie können nun die ausgewählte Report Suite (die zu einem der Tags auf der Seite gehört) durch eine andere Report Suite ersetzen. Diese neue Report Suite muss nicht mit einem Tag auf der Seite verbunden sein. Wenn Sie die ausgewählte Report Suite in den Activity Map-Einstellungen ändern, werden beim Speichern alle betroffenen Analytics-Berichte aktualisiert.<br>**Wichtig**:  [!UICONTROL Virtual Report ] Suites sind nicht mit dem  [!UICONTROL Livemodus] kompatibel, sondern nur mit dem  [!UICONTROL Standardmodus]. Wenn Sie sich für eine Standard-Report Suite im Livemodus befinden, aber [!UICONTROL Virtual Report Suite] in diesem Dialogfeld auswählen, wird der Standardmodus angezeigt, sobald Sie **[!UICONTROL OK]** hier klicken.  Darüber hinaus wird das Kalendersteuerelement neu initialisiert, um dem Kalendertyp der Report Suite (Gregorianisch, Handel, Benutzerspezifisch...) zu entsprechen. |
| **[!UICONTROL Seitenname]** | Die Seite, auf die diese Einstellungen angewendet werden. |
| **[!UICONTROL Sprache]** | Die Auswahl entspricht den angebotenen Sprachen für Adobe Analytics. |
| **[!UICONTROL Overlays bezeichnen als]** | <ul><li>**[!UICONTROL Kein Label]**: nur für Verlaufsüberlagerungen In diesem Fall vermittelt die Farbe der Überlagerung einen Sinn für die Rangordnung des Links</li><li>**[!UICONTROL Wert]**: Der unverarbeitete Gesamtwert der Metrik für den Link</li><li>**[!UICONTROL Prozent]**: Prozentsatz der Metrik für diesen Link im Vergleich zum Gesamtwert der Metrik für die Seite.</li><li>**[!UICONTROL Rang]**: Rang dieses Links im Vergleich zu allen Links auf der gerenderten Seite</li></ul> |
| **[!UICONTROL Schriftgröße Beschriftung]** | Ermöglicht Ihnen, die Schriftgröße der Überlagerungsbeschriftung zur besseren Lesbarkeit mithilfe eines Reglers zu erhöhen oder zu verringern. |
| **[!UICONTROL Verlaufs-/Blasenfarbe]** | Um die Rangfolge der Überlagerungsverknüpfungen für Verlaufs- oder Blasenüberlagerungsvisualisierungen anzuzeigen, wählen Sie eine aus einem Farbbereich aus. |
| **[!UICONTROL Farbverlauf auf Grundlage von]** | <ul><li>**[!UICONTROL Top-30-Bewertungen]**: Die Farbintensität wird für die 30 höchsten Werte vereinheitlicht.</li><li>**[!UICONTROL Absoluter Metrikwert]**: Die Farbintensität ist eine Funktion des absoluten Metrikwerts.</li></ul> |
| **[!UICONTROL Verlaufstransparenz]** | Wählen Sie die Transparenzstufe für Verlaufsüberlagerungen. Diese Einstellung hat keine Auswirkungen auf die Überlagerungen [!UICONTROL Textfeld]. |

## Standardeinstellungen {#section_24DB95376E1A448494ECF3F57743FC19}

Diese Einstellungen gelten für die Standardmodus-Überlagerung.

![](assets/settings_standard.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Dynamische Datenfilterung]** | Mit dieser Dropdownliste können Sie Überlagerungen für<ul><li>(Standard) Alle Links auf der Seite</li><li>Die obere (höchste) oder untere (niedrigste) Anzahl der Links mit Rangansicht auf der Seite, wobei # eine Auswahl von 1, 10, 50 oder 100 sein kann.</li></ul> |
| **[!UICONTROL Überlagerungen für Links ausblenden, die keine Treffer]** erhalten haben. | Ein Kontrollkästchen, das die Sichtbarkeit von Überlagerungen für Links ohne Daten umschaltet.<ul><li>(Standard) Wenn das Kontrollkästchen aktiviert ist, wird keine Überlagerung angezeigt, wenn ein Link keine Activity Map-Linkdaten enthält.</li><li>Wenn das Kontrollkästchen deaktiviert ist und ein Link keine Activity Map-Link-Daten enthält, wird eine Überlagerung angezeigt und hat die Beschriftung &quot;-&quot;, d. h. &quot;K/A&quot;(nicht zutreffend). |

## Live-Einstellungen {#section_D30F6E62FB5D404090B588F396A460AF}

Diese Einstellungen gelten für die Überlagerung im Livemodus.

![](assets/settings_live.png)

| Einstellung | Beschreibung |
|---|---|
| **[!UICONTROL Anzeige oben]** | Um **[!UICONTROL Gewinner]** oder **[!UICONTROL Verlierer]** (oder beide) als Überlagerungen anzuzeigen, wählen Sie die Anzahl der Links aus. |
| **[!UICONTROL Unterste ausschließen (%)]** | Wählen Sie diese Option, um Links für Gewinner oder Verlierer auszuschließen, für die wenig Daten vorhanden sind. Wenn Sie diesen Prozentsatz der Links ausschließen, werden nur noch die Links angezeigt, für die genug Daten vorhanden sind, um relevante Gewinne oder Verluste anzuzeigen. Der Prozentsatz wird anhand der Anzahl der Links auf der Seite berechnet. Wenn Sie beispielsweise die unteren 10 % einer Liste mit 200 Links herausfiltern, werden die unteren 20 Links herausgefiltert. |
| **[!UICONTROL Automatische Aktualisierung von Daten]** | Hier können Sie entscheiden, ob die auf der Oberfläche angezeigten Analytics-Daten automatisch aktualisiert werden, wenn ein neuer Zeitraum berechnet wird. |
| **[!UICONTROL Zeitraum für automatische Aktualisierung]** | Wenn dieses Kontrollkästchen aktiviert wird, wird die Webseite jedes Mal aktualisiert, wenn neue Daten abgerufen werden. Dadurch können die Links auf der Seite genauer mit den erfassten Daten synchronisiert werden. |
