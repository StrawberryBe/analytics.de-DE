---
description: Ermöglicht Ihnen die einfache Visualisierung von Vergleichsdaten in Analysis Workspace, z. B. das Erstellen von Vergleichen mit dem letzten Monat, dem letzten Jahr usw.
title: Visualisierung von Combo-Diagrammen
feature: Visualizations
role: User, Admin
source-git-commit: e2cd08ae4109e037f8b54edf21239fa6fa659896
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 32%

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
* Wenn Sie einen oder mehrere Vergleiche hinzufügen, müssen diese vom gleichen Typ sein, z. B. Zeitraum.
* Sie können bis zu 5 Vergleiche hinzufügen.
* Sie können einen Filter auf eine Metrik anwenden.

## Erstellen eines Combo-Diagramms

1. Ziehen Sie aus der Dropdownliste Visualisierungen in der linken Leiste die [!UICONTROL Combo-Diagramm] Visualisierung in ein leeres Bedienfeld.

   ![](assets/combo-chart-build.png)

1. Wählen Sie aus den Dropdownlisten eine Dimension für die X-Achse und eine Metrik für die Y-Achse aus.

1. Wählen Sie den Typ [!UICONTROL Zeilenvergleich] Sie verwenden möchten.

   | Kantenvergleichstyp | Definition |
   | --- | --- |
   | Zeitraum | Der häufigste Vergleichstyp - z. B. Vergleich dieses Zeitraums mit dem vor 4 Wochen. Wenn Sie den Zeitraum ausgewählt haben, wählen Sie eine sekundäre Auswahl, mit welchem Zeitraum Sie vergleichen möchten.<p>![](assets/combo-time-period.png) |
   | Zusätzliche Metrik | Sie können beispielsweise [!UICONTROL Umsatz] zu einer anderen Metrik hinzu.<p>![](assets/combo-2metrics.png) |
   | Funktion | Sie können eine Funktion wie [!UICONTROL Durchschnittlich] in den Vergleich ein. Eine Liste der unterstützten Funktionen finden Sie unten.<p>![](assets/combo-functions.png) |

   {style=&quot;table-layout:auto&quot;}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Die Ausgabe sieht in etwa so aus:

   ![](assets/combo-output.png)

   Der aktuelle Zeitraum wird im Balkendiagramm angezeigt und der Vergleichszeitraum wird durch das Liniendiagramm dargestellt. Die Punkte im Liniendiagramm werden als &quot;Balkenglocken&quot;bezeichnet.

## Unterstützte Funktionen

Wenn Sie **[!UICONTROL Funktion]** als [!UICONTROL Kantenvergleichstyp], wird eine Funktion der gewählten Metrik zurückgegeben.

| Funktion | Definition |
| --- | --- |
| **[!UICONTROL Kumulativer Durchschnitt]** | Gibt den Durchschnitt der letzten N Zeilen zurück. |
| **[!UICONTROL Summe]** | Addiert alle numerischen Werte für eine Metrik innerhalb einer Spalte (über die Elemente einer Dimension hinweg) |
| **[!UICONTROL Exponent]** | Gibt *e* hoch eine angegebene Zahl zurück. |
| **[!UICONTROL Mittel]** | Gibt das arithmetische Mittel (oder den Durchschnitt) einer Metrik zurück. |
| **[!UICONTROL Quartil]** | Gibt das Quartil der Werte für eine Metrik zurück. Anhand von Quartilen können Sie beispielsweise die oberen 25 % der Produkte finden, die den meisten Umsatz generieren. |

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
| **[!UICONTROL Allgemein]** |  |
| **[!UICONTROL Prozentsätze]** | Zeigt Werte als Prozentzahlen an. |
| **[!UICONTROL Legende eingeblendet]** | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung von Combo-Diagrammen. |
| **[!UICONTROL Granularität]** | Für Trend-Visualisierungen können Sie die Zeitgranularität (Tag, Woche, Monat usw.) aus dieser Dropdown-Liste ändern. |
| **[!UICONTROL Überlagerungen]** | Ein- oder Ausblenden von Grillen auf Linien. |
| **[!UICONTROL Achse]** |  |
| **[!UICONTROL Zwei-Achsen-Display]** | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| **[!UICONTROL Normalisierung]** | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| **[!UICONTROL X-Achse anzeigen]** | Zeigen Sie die X-Achse an oder blenden Sie sie aus. |
| **[!UICONTROL y-Achse anzeigen]** | Zeigen Sie die Y-Achse an oder blenden Sie sie aus. |
| **[!UICONTROL Y-Achse bei null verankern]** | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |

{style=&quot;table-layout:auto&quot;}


