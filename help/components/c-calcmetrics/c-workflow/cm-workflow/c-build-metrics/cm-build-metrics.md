---
description: Der Generator für berechnete Metriken bietet eine Arbeitsfläche, mit der Sie Dimensionen, Segmente und Funktionen per Drag-and-Drop verschieben können, um benutzerdefinierte Metriken basierend auf Containerhierarchielogik, Regeln und Operatoren zu erstellen. Mit diesem integrierten Entwicklungs-Tool können Sie einfache berechnete Metriken oder komplexe, erweiterte berechnete Metriken erstellen und speichern.
title: Metriken erstellen
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: 7722a2f01ff77dfec8ce110fd04fe977f6c627c6
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 46%

---

# Metriken erstellen

Adobe Analytics bietet eine Arbeitsfläche zum Ziehen und Ablegen von Dimensionen, Metriken, Segmenten und Funktionen zum Erstellen benutzerdefinierter Metriken basierend auf Containerhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe berechnete Metriken erstellen und speichern.

## Erstellen einer berechneten Metrik beginnen

Sie können mit der Erstellung einer berechneten Metrik auf eine der folgenden Arten beginnen:

* Öffnen Sie in Analysis Workspace ein Projekt und wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Metrik erstellen]**.
* Öffnen Sie in Analysis Workspace ein Projekt und wählen Sie dann die **Plus** Symbol neben [!UICONTROL **Metriken**] in der linken Leiste.
* In [!DNL Analytics], gehen Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Berechnete Metriken]**, wählen Sie **[!UICONTROL + Hinzufügen]** oben auf der Seite &quot;Berechnete Metrik&quot;angezeigt.

## Bereiche des Generators für berechnete Metriken

Die folgende Abbildung und die zugehörige Tabelle erläutern einige der Hauptbereiche und -funktionen des Generators für berechnete Metriken.

![](assets/cm_builder_ui.png)

| Position im Bild | Name und Funktion |
|---|---|
| 1 | **Titel:** Die Benennung der Metrik ist obligatorisch. Sie können nur benannte Metriken speichern. |
| 2 | **Beschreibung:** Geben Sie ihr eine benutzerfreundliche Beschreibung, um zu zeigen, wofür sie verwendet wird, und um sie von ähnlichen zu unterscheiden. <p>Die Beschreibung wird auch in Berichten angezeigt. Sie sollten die Formel NICHT in die Beschreibung aufnehmen. Erläutern Sie stattdessen, wofür diese Metrik verwendet werden sollte und wofür nicht. (Die Formel wird unter der Überschrift „Zusammenfassung“ generiert, während Sie die Metrik erstellen. Daher müssen Sie die Formel nicht noch der Beschreibung hinzufügen.) </p> |
| 3 | **Format:** Zu den Optionen gehören Dezimal, Zeit, Prozent und Währung. |
| 4 | **Dezimalstellen:** Zeigt an, wie viele Dezimalstellen im Bericht angezeigt werden. Sie können maximal 10 Dezimalstellen angeben. |
| 5 | **Aufwärts-Trend anzeigen als:** Diese Metrikpolaritätseinstellung zeigt an, ob Analytics einen Aufwärtstrend der Metrik als positiv (grün) oder negativ (rot) betrachten sollte. Dementsprechend wird ein steigendes Diagramm des Berichts grün oder rot angezeigt. |
| 6 | **Tags:** Tagging bietet eine gute Möglichkeit, Metriken zu organisieren. Alle Benutzer können Tags erstellen und eines oder mehrere Tags auf eine Metrik anwenden. Sie sehen Tags jedoch nur für die Segmente, deren Inhaber Sie sind oder die für Sie freigegeben wurden. Welche Arten von Tags sollten Sie erstellen? Hier finden Sie einige Vorschläge für nützliche Tags:<ul><li>**Teamnamen**, wie Social Marketing, Mobile Marketing.</li><li>**Projekte** (Analyse-Tags), z. B. Entrypage-Analyse.</li><li>**Kategorien**, wie Frauen, Geografie.</li><li>**Workflows** zu genehmigen; Kuratiert für (einen bestimmten Geschäftsbereich)</li></ul> |
| 7 | **Zusammenfassung:** <p>Die Formel unter Zusammenfassung wird jedes Mal, wenn Sie die Metrikdefinition ändern, aktualisiert. Diese Formel wird auch in der Metrikleiste auf der linken Seite angezeigt, wenn Sie den Mauszeiger über eine Metrik bewegen und auf die <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> Symbol. </p> |
| 8 | **Definition:** Hier können Sie Metriken/berechnete Metriken, Segmente und/oder Funktionen einfügen, um die berechnete Metrik zu erstellen. <ul><li>Wenn Sie eine berechnete Metrik hierhin ziehen, wird die zugehörige Metrikdefinition automatisch eingeblendet. </li> <li>Sie können Definitionen mit Containern verschachteln. Im Gegensatz zu Segmentcontainern funktionieren diese Container allerdings wie ein mathematischer Ausdruck und bestimmen die Reihenfolge der Vorgänge. </li> </ul> |
| 9 | **Operator:** Geteilt durch ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) ist der Standardoperator. Außerdem gibt es die Operatoren +, - und x. |
| 10 | **Vorschau:** Bietet einen schnellen Überblick über mögliche Fehler. Die Vorschau deckt die letzten 90 Tage ab. So können Sie schnell einschätzen, ob Sie die richtigen Komponenten für die Metrik ausgewählt haben. Bei einem unerwarteten Ergebnis müssten Sie die Metrikdefinition noch einmal genauer prüfen. |
| 11 | **Produktkompatibilität:** Mit der Produktkompatibilität wird angezeigt, ob die Metrik mit <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html?lang=de"  > Aktuelle Daten </a>, mit vollständig verarbeiteten Daten oder nur mit Marketingkanalberichten (Erstkontaktzuordnung). <p>Hinweis: Bei aktuellen Daten werden nicht alle Metriken unterstützt. Metriken mit Segmenten oder Funktionen sind nicht mit aktuellen Daten kompatibel. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Mehr... </a> </p> </p> |
| 12 | **Hinzufügen:** Für alle Typen von berechneten Metriken können Sie Container und statische Zahlen zur Definition hinzufügen. Für erweiterte berechnete Metriken können Sie auch Segmente und Funktionen hinzufügen. <ul><li>Container funktionieren wie mathematische Ausdrücke und bestimmen die Reihenfolge der Vorgänge. Jedes Element in einem Container wird also vor dem nächsten Vorgang verarbeitet.</li><li>Wenn Sie ein Segment in einen Container ziehen, werden alle Elemente in diesem Container segmentiert. (Nur erweiterte berechnete Metriken)</li><li>Sie können mehrere Segmente in einem Container stapeln.</li></ul> |
| 13 | **Zahnradsymbol (Metriktyp, Attribution):** Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie die <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > Metriktyp und Attributionsmodelle </a>. |
| 14 | **Neu:** Ermöglicht Ihnen die Erstellung einer neuen Komponente, z. B. eines neuen Segments (Sie werden zum <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > Segment Builder </a>. |
| 15 | **Suchkomponenten:** In dieser Suchleiste können Sie nach Dimensionen, Metriken, Segmenten (nur erweiterte berechnete Metriken) und Funktionen (nur erweiterte berechnete Metriken) suchen. |
| 16 | **Liste der Dimensionen:** Anstatt den Generator für berechnete Metriken zu verlassen, um ein einfaches Segment (im Segment Builder) zu erstellen, z. B. &quot;Seite = Homepage&quot;, können Sie die Seite per Drag-and-Drop verschieben und Startseite direkt aus dem Generator für berechnete Metriken auswählen.<p>So profitieren Sie von einem deutlich optimierten Arbeitsablauf bei der Erstellung segmentierter berechneter Metriken.</p> |
| 17 | **Liste der Metriken:** Metriken sind in drei Kategorien unterteilt: <ul> <li>Standardmetriken (<img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li><li>Berechnete Metriken ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li><li id="li_8735E76637ED4C3F983731A66E04C93E">Metrikvorlagen ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg" id="image_D236601511CC4DD3828F223431E27E88" />) - unten in der Liste. </li> </ul> <p>Wenn Sie mit dem Mauszeiger auf eine Metrik zeigen, wird das Infosymbol rechts neben der Metrik angezeigt: <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" width="15px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Durch Klicken auf dieses Symbol erhalten Sie die folgenden Informationen: </p><ul> <li>Die Formel für die Berechnung der Metrik. </li><li>Ein Vorschautrend der Metrik. </li><li>Symbol &quot;Bearbeiten&quot;(Bleistift) <img placement="break" align="center"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg" width="15px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> oben rechts, wo Sie zum Generator für berechnete Metriken gelangen, wo Sie diese berechnete Metrik bearbeiten können. </li></ul> |
| 18 | **Liste von Segmenten:** (Nur erweiterte berechnete Metriken) Als Administrator enthält diese Liste alle Segmente, die in Ihrem Anmeldeunternehmen erstellt wurden. Wenn Sie kein Administrator sind, enthält diese Liste Segmente, deren Eigentümer Sie sind, sowie Segmente, die für Sie freigegeben wurden. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html?lang=de"  > Mehr... </a> |
| 19 | **Liste der Funktionen:** (Nur erweiterte berechnete Metriken) Funktionen sind in zwei Listen unterteilt: <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > Allgemein </a> (am häufigsten verwendet) und <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > Erweitert </a>. |
| 20 | **Report Suite-Auswahl:** Hiermit können Sie zu einer anderen Report Suite wechseln. |

{style="table-layout:auto"}
