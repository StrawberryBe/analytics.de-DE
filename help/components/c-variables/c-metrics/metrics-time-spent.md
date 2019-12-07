---
description: Adobe Analytics bietet verschiedene Metriken und Dimensionen zur Besuchszeit. Erfahren Sie mehr über die Funktionsweise und die Berechnung solcher Metriken.
title: Besuchszeit
topic: Metrics
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# [!UICONTROL Besuchszeit]

In Adobe Analytics-Produkten stehen verschiedene [!UICONTROL Besuchszeitmetriken und -dimensionen zur Verfügung] .

## [!UICONTROL "Besuchszeit"] -Metriken

| Metrik | Definition | Verfügbar in |
|---|---|---|
| [!UICONTROL Gesamtbesuchszeit in Sekunden] | Zeigt den Zeitraum an, über den Besucher insgesamt mit einem bestimmten Dimensionselement agieren. Umfasst die Instanz eines Werts und der Persistenz für alle nachfolgenden Treffer. Bei Props wird die Besuchszeit auch über die nachfolgenden Verknüpfungsereignisse hinweg berechnet. | Analysis Workspace, Reports &amp; Analysen, ReportBuilder (als "Gesamtbesuchszeit"bezeichnet), Data Warehouse, Ad-hoc-Analysen |
| [!UICONTROL Zeit pro Besuch] (Sekunden) | *Gesamtdauer pro Besuch / (Besuchsabsprünge)*<br>Stellt die durchschnittliche Zeit dar, die Besucher während jedes Besuchs mit einem bestimmten Dimensionselement interagieren. | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |
| [!UICONTROL Besuchszeit pro Besucher] (Sekunden) | *Gesamtdauer/*<br>individuelle BesucherStellt die durchschnittliche Zeit dar, die Besucher während der gesamten Lebensdauer des Besuchers mit einem bestimmten Dimensionselement interagieren (Länge des Cookies). | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |
| [!UICONTROL Durchschnittliche Besuchszeit pro Site] (Sekunden) | Stellt die gesamte Zeit dar, die Besucher pro Dimensionselement-Sequenz mit einem bestimmten Dimensionselement interagieren. Anders als der Name vermuten lässt, beschränkt sich diese Metrik nicht nur auf Durchschnitte pro „Seite“. Weitere Informationen zu Sequenzen finden Sie im Abschnitt "Berechnung der Besuchszeit".<br>**Hinweis**: Diese Metrik unterscheidet sich sehr wahrscheinlich von "Zeit pro Besuch"auf Dimensionselemensebene aufgrund der Unterschiede im Nenner in der Berechnung. | Analysis Workspace, Reports &amp; Analysen (in Minuten angezeigt), ReportBuilder (in Minuten angezeigt), Ad-hoc-Analysen |
| [!UICONTROL Durchschnittliche Besuchszeit pro Seite] | Veraltete Metrik.<br> Stattdessen sollten Sie "Durchschnittliche Besuchszeit pro Site"verwenden, wenn die durchschnittliche Zeit für einen Dimensionselement erforderlich ist. | Report Builder (wenn sich eine Dimension in der Anforderung befindet) |
| [!UICONTROL Gesamtsitzungslänge], alias Länge der [!UICONTROL vorherigen Sitzung] | Nur SDK für Mobilanwendungen. <br>Wird beim nächsten Start der App für die vorangegangene Sitzung bestimmt. Diese Metrik wird in Sekunden berechnet. Allerdings zählt sie nicht, wenn sie im Hintergrund ausgeführt wird, sondern nur, wenn sie direkt verwendet wird. Es handelt sich um eine Metrik auf Sitzungsebene.<br>Beispiel: Wir installieren die App ABC und starten und verwenden sie für 2 Minuten und schließen dann die App. Zu dieser Sitzungszeit werden keine Daten gesendet. The next time we launch the app, [!UICONTROL Previous Session Length] will be sent with a value of 120. | Analysis Workspace, Reports &amp; Analysen, ReportBuilder, Mobile Services-Benutzeroberfläche |
| [!UICONTROL Durchschnittliche Sitzungslänge] (Mobil) | *Gesamte Sitzungslänge / (Starts - Erste Starts)Nur*<br>Mobile App-SDK. Es handelt sich um eine Metrik auf Sitzungsebene. | ReportBuilder, Mobile Services-Benutzeroberfläche, Ad-hoc-Analysen |

## Dimensionen der "Besuchszeit"

| Dimension | Definition | Verfügbar in |
|---|---|---|
| [!UICONTROL Zeit pro Besuch – präzise] | Die gesamte bei einem Besuch verbrachte Zeit, die auf die nächste Sekunde gekürzt und auf alle Treffer angewendet wird, die Teil des Besuchs waren. Es handelt sich um eine Dimension auf Besuchsebene. | Analysis Workspace, Ad-hoc-Analysen |
| [!UICONTROL Zeit pro Besuch – zusammengefasst] | Die präzise Dimension, die in 9 verschiedene Bereiche zusammengefasst wird. Es handelt sich um eine Dimension auf Besuchsebene. Die Bereiche sind:<ul><li>Weniger als 1 Minute</li><li>1-5 Minuten</li><li>5-10 Minuten</li><li>10-30 Minuten</li><li>30-60 Minuten</li><li>1-2 Stunden</li><li>2-5 Stunden</li><li>5-10 Stunden</li><li>10-15 Stunden</li></ul>**Hinweis**: Es können keine Behälter größer sein, da ein Besuch nach 12 Stunden Aktivität abläuft. | Analysis Workspace, Reports &amp; Analysen, ReportBuilder, Ad-hoc-Analysen |
| [!UICONTROL Besuchszeit pro Seite – präzise] | Die gesamte bei einem Treffer verbrachte Zeit, die auf die nächste Sekunde gekürzt wird. Dies ist eine Dimension auf Trefferebene und umfasst sowohl Seitenansichten als auch Linkereignisse. Trotz seines Namens ist sie nicht auf die Dimension "Seite"beschränkt. | Analysis Workspace, Ad-hoc-Analysen |
| [!UICONTROL Besuchszeit pro Seite – zusammengefasst] | Die präzise Dimension, die in 10 verschiedene Bereiche zusammengefasst wird; die zusammengefasste Dimension zählt jedoch nur Seitenansichten (und schließt Verknüpfungs-Ereignisse aus). Es handelt sich um eine Dimension auf Trefferebene. Die Bereiche sind:<ul><li>weniger als 15 Sekunden</li><li>15–29 Sekunden</li><li>30–59 Sekunden</li><li>1–3 Minuten</li><li>3–5 Minuten</li><li>5–10 Minuten</li><li>10–15 Minuten</li><li>15–20 Minuten</li><li>20–30 Minuten</li><li>Mehr als 30 Minuten</li></ul> | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |

## Berechnung der Besuchszeit

Adobe Analytics verwendet explizite Werte (einschließlich Verknüpfungs-Ereignissen und Videoaufrufen) zur Berechnung der [!UICONTROL Besuchszeit].

>[!NOTE]
>
>Without link events like [!UICONTROL Video Views] or [!UICONTROL Exit Links], time spent on the last hit of a visit cannot be known. For similar reasons, [!UICONTROL Bounce Visits] (i.e. visits with a single hit) also does not have a 'time spent' associated with it.

The **numerator** in all time spent calculations is total seconds spent.

The **denominator** is not available as a separate metric in Adobe Analytics. Bei Metriken zur Besuchszeit auf Trefferebene handelt es sich um Sequenzen. Eine Sequenz ist ein Satz aufeinanderfolgender Treffer, in dem eine beliebige Variable denselben Wert enthält (egal, ob festgelegt, nach vorne verteilt oder permanent gespeichert). "Weitergeben"bezieht sich auf die Persistenz von Props zwischen Seitenansichten (d. h. über nachfolgende Link-Ereignisse) zum Zwecke der Berechnung der Besuchszeit.

* For example, in the case of [!UICONTROL Page Name] or other dimensions at the hit level, the denominator is essentially [!UICONTROL 'Instances'] or [!UICONTROL 'Page Views'], but with reloads and unset values (e.g. link events) counted as a single interaction (a sequence).

* Absprung- und Abbruchtreffer werden auch aus dem Nenner entfernt, da die "Besuchszeit"nicht bekannt ist.

## Häufig gestellte Fragen (FAQ)

**Q1: Können alle "Besuchszeit"-Metriken auf eine Dimension angewendet werden?**

A: Die Metriken zur "Besuchszeit"können auf beliebige Dimensionen angewendet werden:

* [!UICONTROL Gesamtbesuchszeit in Sekunden]

* [!UICONTROL Zeit pro Besuch] (Sekunden)

* [!UICONTROL Besuchszeit pro Besucher] (Sekunden)

* [!UICONTROL Durchschnittliche Besuchszeit pro Site] (Sekunden)

**Q2: Welche Besuchszeit-Dimension wird am besten bei Aufschlüsselungen mit anderen Dimensionen verwendet?**

A: The [!UICONTROL Time Spent on Page – granular] dimension is a hit-level dimension. Wenn Sie diese Dimension anhand einer anderen Dimension aufschlüsseln, können Sie die Sekunden ermitteln, über die sich ein Treffer erstreckte, von dem auch die Aufschlüsselungsdimension betroffen war.
Im Beispiel unten wird der Suchbegriff "klassifiziert"mit Trefferzeiten von 54 Sekunden, 59 Sekunden usw. verknüpft. Dies zeigt möglicherweise an, dass Besucher Zeit mit dem Lesen von Inhalten verbringen, die für diesen Begriff zurückgegeben wurden.

![](assets/time-spent1.png)

**Q3: Welche Metrik eignet sich für die Dimension "[!UICONTROL Besuchszeit pro Seite - granular]"?**

A: Jede Metrik. Die Dimension zeigt die Zeit, die für den exakten Treffer, bei dem das Ereignis auftrat, verbracht wurde. Eine längere Besuchszeit bedeutet, dass ein Besucher mehr Zeit auf einer Seite (Treffer) verbracht hat, auf der es zu dem Ereignis kam.

![](assets/time-spent2.png)

**4. Quartal: Wie unterscheidet sich die[!UICONTROL durchschnittliche Besuchszeit pro Site]von der[!UICONTROL Zeit pro Besuch]?**

A: Die Differenz ist der Nenner in der Metrik:

* [!UICONTROL Die durchschnittliche Besuchszeit pro Site] verwendet die Sequenzen, die ein Dimensionselement enthalten.

* [!UICONTROL Die Zeit pro Besuch] verwendet die Besuchszahl

Aus diesem Grund geben diese Metriken möglicherweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

## Beispiele für [!UICONTROL Besuchszeitberechnungen]

Angenommen, der folgende Satz von Server-Aufrufen gilt für einen einzigen Besucher mit einem einzigen Besuch:

| Besuch – Trefferanzahl | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| **Verstrichene Zeit des Besuchs (in Sekunden)** | 0 | 30 | 80 | 180 | 190 | 230 | 290 |
| **Besuchszeit in Sekunden** | 30 | 50 | 100 | 10 | 40 | 60 | - |
| **Treffertyp** | Seite | Link | Seite | Seite | Seite | Seite | Seite |
| **Seitenname** | Startseite | - | Produkt | Home | Home (neu laden) | Korb | Bestellungsbestätigung |
|  |  |  |  |  |  |  |  |
| **prop1** | A (festgelegt) | A (Spread forward) | nicht festgelegt | B (Set) | B (Set) | A(festgelegt) | C (festgelegt) |
| **prop1 – Besuchszeit in Sekunden** | 30 | 50 | - | 10 | 40 | 60 | - |
|  |  |  |  |  |  |  |  |
| **eVar1** | Rot (festgelegt) | Rot (dauerhaft) | (abgelaufen) | Blau (festgelegt) | Blau (Set) | Blau (dauerhaft) | Rot (Set) |
| **eVar1 Sekunden** | 30 | 50 | - | 10 | 40 | 60 | - |

Auf der Grundlage der oben stehenden Tabelle werden Besuchszeitmetriken wie folgt berechnet:

| prop1 | Gesamtbesuchszeit in Sekunden | Besuchszeit pro Besuch | Besuchszeit pro Besucher | Anzahl der Sequenzen | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| A | 30 + 50 + 60 = 140 | 140 / 1 = 140 | 140 / 1 = 140 | 2 | 140 / 2 = 70 |
| B | 10 + 40 = 50 | 50 / 1 = 50 | 50 / 1 = 50 | 1 | 50 / 1 = 50 |
| C | 0 | 0 | 0 | 0 | 0 |
| Nicht zugewiesene Zeit | 100 | - | - | - | - |

| eVar1 | Gesamtbesuchszeit in Sekunden | Besuchszeit pro Besuch | Besuchszeit pro Besucher | Anzahl der Sequenzen | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| Rot | 30 + 50 = 80 | 80 / 1 = 80 | 80 / 1 = 80 | 1 | 80 / 1 = 80 |
| Blau | 10 + 40 + 60 = 110 | 110 / 1 = 110 | 110 / 1 = 110 | 1 | 110 / 1 = 110 |
| Nicht zugewiesene Zeit | 100 | - | - | - | - |

Besuchszeit pro Besuch (granular): 290Besuchszeit pro Seite (granular): 10, 30, 40, 50, 60, 100

Einige zusätzliche Hinweise, um das Beispiel deutlicher zu machen:

* Alle Berechnungen zur Besuchszeit basieren auf der abgelaufenen Besuchszeit, die beim ersten Treffer des Besuchs bei null beginnt.

* "Sekunden verbracht"ist die Differenz zwischen dem Zeitstempel des aktuellen Treffers und dem Zeitstempel des nächsten Treffers. Aus diesem Grund gibt es für den letzten Treffer des Besuchs (sowie die Absprünge) keine Besuchszeit.

* Eine „Sequenz“ ist ein Satz aufeinanderfolgender Treffer, in dem eine beliebige Variable denselben Wert enthält (egal, ob festgelegt, nach vorne verteilt oder permanent gespeichert). Zum Beispiel verfügt prop1 „A“ über zwei Sequenzen: Treffer 1 und 2 sowie Treffer 6. Werte des letzten Treffers eines Besuchs beginnen keine neue Sequenz, da es für den letzten Treffer keine Besuchszeit gibt. „Durchschnittliche Besuchszeit pro Site“ verwendet Sequenzen im Nenner.

   * Für die Zwecke der Besuchszeit werden Props von Seitenaufrufen auf nachfolgende Link-Treffer wie oben für "prop1"bei Treffer 2 "aufgeschlüsselt". Dadurch kann der für prop1 festgelegte Wert für Treffer 1 („A“) die bei Treffer 2 verbrachte Zeit sammeln.

   * eVars akkumulieren die Zeit, die bei jedem Treffer verbracht wird, bei dem die eVar eingestellt oder beibehalten wird. Die eVar-Persistenz wird durch die eVar-Einstellungen in Analytics &gt; Admin definiert.

