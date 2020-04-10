---
description: Adobe Analytics-Angebot verwenden verschiedene Besuchszeitmetriken und -dimensionen. Finden Sie heraus, was sie sind und wie sie berechnet werden.
title: Besuchszeit
topic: Metrics
translation-type: tm+mt
source-git-commit: 8df1fdfb048dd69b4926b7b812ec5dfea4a97b89

---


# [!UICONTROL Time spent]

Various [!UICONTROL 'time spent'] metrics and dimensions are offered across Adobe Analytics products.

## [!UICONTROL 'Time spent'] Metriken

| Metrik | Definition | Verfügbar in |
|---|---|---|
| [!UICONTROL Total seconds spent] | Zeigt den Zeitraum an, über den Besucher insgesamt mit einem bestimmten Dimensionselement agieren. Enthält die Instanz eines Wertes sowie die Persistenz über alle folgenden Treffer hinweg. Bei Props wird die Besuchszeit auch über die nachfolgenden Verknüpfungsereignisse hinweg berechnet. | Analysis Workspace, Reports &amp; Analytics, Report Builder (als „Gesamtbesuchszeit“ bezeichnet), Data Warehouse, Ad Hoc Analysis |
| [!UICONTROL Time spent per visit] (Sekunden) | *Gesamtbesuchszeit in Sekunden/(Besuchsabsprünge)*<br>Stellt die durchschnittliche Zeit dar, die Besucher bei jedem Besuch mit einem bestimmten Dimensionselement interagieren. | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |
| [!UICONTROL Time spent per visitor] (Sekunden) | *Gesamtbesuchszeit in Sekunden/Unique Visitors *<br>Stellt die durchschnittliche Zeit dar, die Besucher mit einem bestimmten Dimensionselement über die Lebensdauer des Besuchers (Cookie-Laufzeit) hinweg interagieren. | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |
| [!UICONTROL Average time spent on site] (Sekunden) | Stellt die Gesamtdauer dar, die Besucher mit einem bestimmten Dimensionselement pro Sequenz mit einem Dimensionselement interagieren. Es ist nicht nur auf &quot;Site&quot;-Durchschnittswerte beschränkt, wie der Name nahe legt. Weitere Informationen über Sequenzen finden Sie im Bereich „Berechnung der Besuchszeit“.<br>**Hinweis **: Diese Metrik unterscheidet sich auf der Dimensionselement-Ebene mit hoher Wahrscheinlichkeit von „Zeit pro Besuch“, da bei der Berechnung ein anderer Nenner verwendet wird. | Analysis Workspace, Reports &amp; Analytics (in Minuten angezeigt), Report Builder (in Minuten angezeigt), Ad Hoc Analysis |
| [!UICONTROL Average time spent on page] | Veraltete Metrik.<br> Stattdessen empfehlen wir Ihnen die Verwendung von „Durchschnittliche Besuchszeit pro Site“, wenn Sie die durchschnittliche Zeit für ein Dimensionselement in Erfahrung bringen möchten. | Report Builder (wenn sich eine Dimension in der Anforderung befindet) |
| [!UICONTROL Total session length], alias [!UICONTROL Previous session length] | Nur SDK für Mobilanwendungen. <br>Wird beim nächsten Start der App für die vorangegangene Sitzung bestimmt. In Sekunden berechnet, zählt diese Metrik nicht, wenn die App im Hintergrund ist, sondern nur, wenn sie verwendet wird. Es handelt sich um eine Metrik auf Sitzungsebene.<br>Beispiel: Wir installieren die App ABC, starten die App und verwenden sie 2 Minuten lang, bevor wir die App schließen. Es werden keine Daten über diese Sitzungsdauer gesendet. The next time we launch the app, [!UICONTROL Previous Session Length] will be sent with a value of 120. | Analysis Workspace, Reports &amp; Analytics, Report Builder, Mobile Services |
| [!UICONTROL Average session length] (mobile) | *Gesamtsitzungslänge/(Starts – Erste Starts)*<br>Nur Mobile App-SDK. Es handelt sich um eine Metrik auf Sitzungsebene. | Report Builder, Mobile Services, Ad Hoc Analysis |

## Besuchszeit-Dimensionen

| Dimension | Definition | Verfügbar in |
|---|---|---|
| [!UICONTROL Time spent per visit - granular] | Die gesamte bei einem Besuch verbrachte Zeit, die auf die nächste Sekunde gekürzt und auf alle Treffer angewendet wird, die Teil des Besuchs waren. Es handelt sich um eine Dimension auf Besuchsebene. | Analysis Workspace, Ad Hoc Analysis |
| [!UICONTROL Time spent per visit - bucketed] | Die granulare Dimension wurde in 9 verschiedenen Bereichen zusammengefasst. Es handelt sich um eine Dimension auf Besuchsebene. Zu den Bereichen gehören:<ul><li>Weniger als 1 Minute</li><li>1–5 Minuten</li><li>5–10 Minuten</li><li>10–30 Minuten</li><li>30–60 Minuten</li><li>1–2 Stunden</li><li>2–5 Stunden</li><li>5–10 Stunden</li><li>10–15 Stunden</li></ul>**Anmerkung**: Längere Zeiträume können nicht erfasst werden, da ein Besuch nach einer Aktivitätsdauer von 12 Stunden abläuft. | Analysis Workspace, Reports &amp; Analytics, Report Builder, Ad Hoc Analysis |
| [!UICONTROL Time spent on page - granular] | Die gesamte bei einem Treffer verbrachte Zeit, gekürzt auf die letzte ganze Sekunde. Hierbei handelt es sich um eine Dimension auf Trefferebene, die sowohl Seitenansichten als auch Verknüpfungs-Ereignisse enthält. Trotz ihres Namens ist sie nicht auf die Dimension „Seite“ beschränkt. | Analysis Workspace, Ad Hoc Analysis |
| [!UICONTROL Time spent on page - bucketed] | die Granularität, die in 10 verschiedenen Bereichen zusammengefasst ist; Die gezeichnete Dimension zählt jedoch nur die Ansichten der Seite (und schließt Link-Ereignis aus). Dies ist eine Dimension auf Trefferebene. Zu den Bereichen gehören:<ul><li>weniger als 15 Sekunden</li><li>15–29 Sekunden</li><li>30–59 Sekunden</li><li>1 bis 3 Minuten</li><li>3 bis 5 Minuten</li><li>5 bis 10 Minuten</li><li>10 bis 15 Minuten</li><li>15 bis 20 Minuten</li><li>20 bis 30 Minuten</li><li>mehr als 30 Minuten</li></ul> | Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis |

## Berechnung der Besuchszeit

Adobe Analytics uses explicit values (including link events and video views) to calculate [!UICONTROL Time Spent].

>[!NOTE]
>
>Without link events like [!UICONTROL Video Views] or [!UICONTROL Exit Links], time spent on the last hit of a visit cannot be known. For similar reasons, [!UICONTROL Bounce Visits] (i.e. visits with a single hit) also does not have a &#39;time spent&#39; associated with it.

Der **Zähler** ist in allen Besuchszeit-Berechnungen die Gesamtbesuchszeit in Sekunden.

Der **Nenner** ist in Adobe Analytics nicht als separate Metrik verfügbar. Bei Besuchszeit-Metriken auf Trefferebene besteht der Nenner in Sequenzen. Eine Sequenz ist ein Satz aufeinanderfolgender Treffer, in dem eine beliebige Variable denselben Wert enthält (egal, ob festgelegt, nach vorne verteilt oder permanent gespeichert). „Nach vorne verteilt“ bezieht sich auf die Persistenz von Eigenschaften zwischen Seitenansichten (d. h. über aufeinanderfolgende Verknüpfungs-Ereignisse hinweg). Dies dient der Berechnung der Besuchszeit.

* For example, in the case of [!UICONTROL Page Name] or other dimensions at the hit level, the denominator is essentially [!UICONTROL 'Instances'] or [!UICONTROL 'Page Views'], but with reloads and unset values (e.g. link events) counted as a single interaction (a sequence).

* Treffer mit Absprung und Ausstieg werden auch aus dem Nenner entfernt, da die Besuchszeit nicht ermittelt werden kann.

## Häufig gestellte Fragen (FAQ)

**F1: Können alle Besuchszeitmetriken auf jede Dimension angewendet werden?**

A: Die folgenden Besuchszeitmetriken können auf beliebige Dimensionen angewendet werden:

* [!UICONTROL Total seconds spent]

* [!UICONTROL Time spent per visit] (Sekunden)

* [!UICONTROL Time spent per visitor] (Sekunden)

* [!UICONTROL Average time spent on site] (Sekunden)

**F2: Welche Besuchszeitdimension empfiehlt sich am ehesten in Aufschlüsselungen mit anderen Dimensionen?**

A: Die [!UICONTROL Time Spent on Page – granular] Dimension ist eine Dimension auf Trefferebene. Wenn Sie diese Dimension anhand einer anderen Dimension aufschlüsseln, können Sie die Sekunden ermitteln, über die sich ein Treffer erstreckt hat, von dem auch die Aufschlüsselungsdimension betroffen war.
Im Beispiel unten ist der Suchbegriff „classifieds“ mit Treffer-Zeiten von 54 Sekunden, 59 Sekunden etc. verbunden, was möglicherweise anzeigt, dass Besucher Zeit mit dem Lesen von Inhalten verbringen, die für diesen Begriff zurückgegeben werden.

![](assets/time-spent1.png)

**Q3: Welche Metrik eignet sich für die Dimension von[!UICONTROL Time Spent on Page – granular]?**

A: Jede Metrik. Die Dimension zeigt die Besuchszeit für den Treffer an, bei dem es zu dem Ereignis kam. Eine längere Besuchszeit bedeutet, dass ein Besucher mehr Zeit auf einer Seite (Treffer) verbracht hat, auf der es zu dem Ereignis kam.

![](assets/time-spent2.png)

**4. Quartal: Worin unterscheidet[!UICONTROL Average Time Spent on Site]sich das[!UICONTROL Time Spent per Visit]?**

A: Der Unterschied ist der in der Metrik verwendete Nenner:

* [!UICONTROL Average time spent on site] verwendet die Sequenzen, die ein Dimensionselement enthalten.

* [!UICONTROL Time spent per visit] verwendet die Besuchszahl

Aus diesem Grund geben diese Metriken möglicherweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

**Q5: Warum stimmen Aufschlüsselungssummen[!UICONTROL Average Time Spent on Site]nicht mit dem übergeordneten Zeileneintrag überein?**

A: Denn [!UICONTROL Average Time Spent on Site] hängt von ununterbrochenen Sequenzen einer Dimension ab, und der innere Bericht hängt bei der Berechnung dieser Ausführung nicht vom äußeren Bericht ab.

Betrachten Sie zum Beispiel den folgenden Besuch.
|hit#|1|2|3||—|—|—|—||**Sekunden ausgegeben**|30|100|10||**Seitenname**|Home|Produkt|Home||**date**|Jan 1|Jan 1|Jan 1|

Bei der Berechnung des Zeitaufwands für die Homepage wäre es (30+10)/2=20, aber eine Aufschlüsselung nach Tag würde (30+10)/1=40 ergeben, da der Tag eine einzige ununterbrochene Ausführung vom 1. Januar hat.

Aus diesem Grund geben diese Metriken möglicherweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

## Beispiele für [!UICONTROL Time Spent] Berechnungen

Angenommen, der folgende Satz von Server-Aufrufen gilt für einen einzigen Besucher mit einem einzigen Besuch:

| Besuch – Trefferanzahl | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| **Besuch – vergangene Zeit (in Sek.)** | 0 | 30 | 80 | 180 | 190 | 230 | 290 |
| **Sekunden** | 30 | 50 | 100 | 10 | 40 | 60 | – |
| **Treffertyp** | Seite | Link | Seite | Seite | Seite | Seite | Seite |
| **Webseitenname** | Startseite | – | Product | Startseite | Startseite  (neu laden) | Korb | Bestellungsbestätigung |
|  |  |  |  |  |  |  |  |
| **prop1** | A  (festgelegt) | A (nach vorne verteilt) | nicht festgelegt | B (festgelegt) | B (festgelegt) | A (Set) | C  (festgelegt) |
| **prop1 Sekunden verbracht** | 30 | 50 | – | 10 | 40 | 60 | – |
|  |  |  |  |  |  |  |  |
| **eVar1** | Rot (festgelegt) | Rot (beibehalten) | (abgelaufen) | Blau (festgelegt) | Blau (festgelegt) | Blau (beibehalten) | Rot (festgelegt) |
| **eVar1 – Besuchszeit in Sekunden** | 30 | 50 | – | 10 | 40 | 60 | – |

Basierend auf der obigen Tabelle werden Besuchszeitmetriken wie folgt berechnet:

| prop1 | Gesamtbesuchszeit in Sekunden | Zeit pro Besuch | Besuchszeit pro Besucher | Sequenzanzahl | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| A | 30+50+60=140 | 140/1=140 | 140/1=140 | 2 | 140/2=70 |
| B | 10+40=50 | 50/1=50 | 50/1=50 | 1 | 50/1=50 |
| C | 0 | 0 | 0 | 0 | 0 |
| Nicht zugewiesene Zeit | 100 | – | – | – | – |

| eVar1 | Gesamtbesuchszeit in Sekunden | Zeit pro Besuch | Besuchszeit pro Besucher | Sequenzanzahl | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| Rot | 30+50=80 | 80/1=80 | 80/1=80 | 1 | 80/1=80 |
| Blau | 10+40+60=110 | 110/1=110 | 110/1=110 | 1 | 110/1=110 |
| Nicht zugewiesene Zeit | 100 | – | – | – | – |

Zeit pro Besuch (präzise): 290
Besuchszeit pro Seite (präzise): 10, 30, 40, 50, 60, 100

Einige zusätzliche Hinweise, um das Beispiel deutlicher zu machen:

* Alle Besuchszeitberechnungen basieren auf „Besuch – vergangene Zeit“. Dieser Wert beginnt beim ersten Treffer des Besuchs bei null.

* „Besuchszeit in Sekunden“ ist der Unterschied zwischen dem Zeitstempel des aktuellen Treffers und dem Zeitstempel des nächsten Treffers. Daher wird beim letzten Treffer des Besuchs (und der Absprünge) keine Zeit verbracht.

* Eine &quot;Sequenz&quot;ist ein aufeinander folgender Satz von Treffern, bei denen eine bestimmte Variable denselben Wert enthält (ob durch Festlegen, Spulen nach vorne oder Persistenz). Beispielsweise hat prop1 &quot;A&quot;zwei Sequenzen: Treffer 1 &amp; 2 und Treffer 6. Beim letzten Treffer des Besuchs wird keine neue Sequenz Beginn, da der letzte Treffer keine Besuchszeit hat. Die durchschnittliche auf der Site verbrachte Zeit verwendet Sequenzen im Nenner.

   * Für die Besuchsdauer werden Eigenschaften von Seitentreffern an darauffolgende Verknüpfungs-Treffer „nach vorne verteilt“. Dies wird oben für Eigenschaft 1 auf Treffer 2 dargestellt. Dadurch kann der für prop1 festgelegte Wert für Treffer 1 („A“) die bei Treffer 2 verbrachte Zeit sammeln.

   * eVars sammeln die Besuchszeit für jeden Treffer, bei dem der eVar festgelegt oder permanent gespeichert ist. Die eVar-Persistenz wird durch die eVar-Einstellungen unter „Analytics > „Admin“ definiert.

