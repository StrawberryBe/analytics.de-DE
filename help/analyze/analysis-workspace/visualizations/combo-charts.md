---
description: Ermöglicht Ihnen die einfache Visualisierung von Vergleichsdaten in Analysis Workspace, z. B. das Erstellen von Vergleichen mit dem letzten Monat, dem letzten Jahr usw.
title: Visualisierung von Combo-Diagrammen
feature: Visualizations
role: User, Admin
exl-id: 08e49857-aa58-4527-bdfd-b1663a75a02b
source-git-commit: 46a3fc5170f4b445cf3cafd2c4cc01a40d522bd3
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 34%

---

# Kombinationsdiagramm

>[!NOTE]
>
>Diese Funktion wird derzeit [eingeschränkt getestet](/help/release-notes/releases.md).

Die [!UICONTROL Combo-Diagramm] Visualisierung erleichtert das schnelle Erstellen einer Vergleichsvisualisierung, ohne dass zunächst eine Tabelle erstellt werden muss. Sie können Trends in Ihren Daten einfach in einer Zeilen-/Balkenkombination anzeigen.

Verwenden Sie eine [!UICONTROL Combo-Diagramm] nach

* Vergleichen Sie die Bestellungen dieser Woche zur gleichen Zeit im letzten Monat (und im letzten Jahr) - alle mit wenigen Klicks.

* Schnelles Analysieren und Vergleichen mehrerer Metriken (z. B. [!UICONTROL Unique Visitors] und [!UICONTROL Umsatz]) im selben Diagramm miteinander verglichen.

* Eine Metrik mit einer Funktion analysieren (z. B. [!UICONTROL Kumulativer Durchschnitt]).

Bedenken Sie, dass Sie

* Mehrere Vergleiche in einem einzigen [!UICONTROL Combo-Diagramm].
* Wenn Sie einen oder mehrere Vergleiche hinzufügen, müssen diese vom gleichen Typ sein, z. B. [!UICONTROL Zeitvergleich].
* Sie können bis zu 5 Vergleiche hinzufügen.
* Sie können bis zu 3 Filter (Segmente) auf eine Metrik anwenden.

## Erstellen eines Combo-Diagramms

1. Ziehen Sie aus der Dropdownliste Visualisierungen in der linken Leiste die [!UICONTROL Combo-Diagramm] Visualisierung in ein leeres Bedienfeld.

   ![](assets/combo-chart-build.png)

1. Wählen Sie aus den Dropdownlisten eine Dimension für die X-Achse und eine Metrik für die Y-Achse aus.

1. Wählen Sie den Typ [!UICONTROL Zeilenvergleich] Sie verwenden möchten.

   | Kantenvergleichstyp | Definition |
   | --- | --- |
   | **[!UICONTROL Zeitvergleich]** | Der häufigste Vergleichstyp - z. B. Vergleich dieses Zeitraums mit dem vor 4 Wochen. Wenn Sie [!UICONTROL Zeitvergleich], wählen Sie eine sekundäre Auswahl, um welchen Zeitraum Sie vergleichen möchten.<p>![](assets/combo-time-period.png) |
   | **[!UICONTROL Funktion]** | Sie können eine Funktion wie [!UICONTROL Durchschnittlich] in den Vergleich ein. Eine Liste der unterstützten Funktionen finden Sie unten.<p>![](assets/combo-functions.png) |
   | **[!UICONTROL Sekundäre Metrik]** | Sie können beispielsweise [!UICONTROL Umsatz] zu einer anderen Metrik hinzu.<p>![](assets/combo-2metrics.png) |

   {style=&quot;table-layout:auto&quot;}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Die Ausgabe sieht in etwa so aus:

   ![](assets/combo-output.png)

   Der aktuelle Zeitraum wird im Balkendiagramm angezeigt und der Vergleichszeitraum wird durch das Liniendiagramm dargestellt. Die Punkte im Liniendiagramm werden als &quot;Balkenglocken&quot;bezeichnet.

## Unterstützte Funktionen

Wenn Sie **[!UICONTROL Funktion]** als [!UICONTROL Kantenvergleichstyp], wird eine Funktion der gewählten Metrik zurückgegeben.

| Funktion | Definition |
| --- | --- |
| **[!UICONTROL Spaltensumme]** | Addiert alle numerischen Werte für eine Metrik innerhalb einer Spalte (über die Elemente einer Dimension hinweg) |
| **[!UICONTROL Kumulativer Durchschnitt]** | Gibt den Durchschnitt der letzten N Zeilen zurück. |
| **[!UICONTROL Median]** | Gibt den Medianwert für eine Metrik in einer Spalte zurück. Der Medianwert ist die Zahl in der Mitte eines Zahlensatzes, d. h. die Hälfte der Zahlen hat Werte größer oder gleich dem Medianwert und die Hälfte ist kleiner oder gleich dem Medianwert. |
| **[!UICONTROL Kumulativ]** | Die kumulierte Summe der N Zeilen. |
| **[!UICONTROL Spaltenmaximum]** | Gibt den größten Wert in einem Satz aus Dimensionselementen für eine Metrikspalte zurück. |
| **[!UICONTROL Mittel]** | Gibt das arithmetische Mittel (oder den Durchschnitt) einer Metrik zurück. |
| **[!UICONTROL Spaltenminimum]** | Gibt den kleinsten Wert in einem Satz aus Dimensionselementen für eine Metrikspalte zurück. |

{style=&quot;table-layout:auto&quot;}

Im Folgenden finden Sie ein Beispiel für den kumulativen Durchschnitt der Umsatzmetrik:

![](assets/combo-cumul-avg.png)

Im Folgenden finden Sie ein Beispiel für ein Kombinationsdiagramm mit den Funktionen &quot;Kumulativer Durchschnitt&quot;und &quot;Mittel&quot;:

![](assets/combo-two-functions.png)

## Komprimierte Diagrammeinstellungen

Klicken Sie auf das Zahnradsymbol oben rechts in einem Kombinationsdiagramm, um dessen Einstellungen zu ändern.

![](assets/combo-settings.png)

| Einstellung | Definition |
| --- | --- |
| **[!UICONTROL Visualisierungstyp]** | Hiermit können Sie zu einem anderen Visualisierungstyp wechseln. |
| **[!UICONTROL Granularität]** | Für Trend-Visualisierungen können Sie die Zeitgranularität (Tag, Woche, Monat usw.) aus dieser Dropdown-Liste ändern. |
| **[!UICONTROL Allgemein]** |  |
| **[!UICONTROL Prozentsätze]** | Zeigt Werte als Prozentzahlen an. |
| **[!UICONTROL Legende eingeblendet]** | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung von Combo-Diagrammen. |
| **[!UICONTROL Maximale Elemente begrenzen]** | Reduziert die Anzahl der Elemente auf der X-Achse. Wenn Sie einen Big Data-Datensatz haben, können Sie nur die ersten 10 Elemente anzeigen (oder einen beliebigen Wert). |
| **[!UICONTROL Überlagerungen]** | Ein- oder Ausblenden von Grillen auf Linien. |
| **[!UICONTROL Achse]** |  |
| **[!UICONTROL Zwei-Achsen-Display]** | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. Die Farbe der Doppelachse entspricht der Farbe der Tabelle, es sei denn, es gibt mehrere Vergleiche. In diesem Fall ist die Farbe für alle Vergleiche grau. |
| **[!UICONTROL Normalisierung]** | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| **[!UICONTROL X-Achse anzeigen]** | Zeigen Sie die X-Achse an oder blenden Sie sie aus. |
| **[!UICONTROL y-Achse anzeigen]** | Zeigen Sie die Y-Achse an oder blenden Sie sie aus. |
| **[!UICONTROL Y-Achse bei null verankern]** | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |

{style=&quot;table-layout:auto&quot;}
