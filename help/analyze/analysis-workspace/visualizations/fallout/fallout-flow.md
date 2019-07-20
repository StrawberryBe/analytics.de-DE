---
description: 'null '
seo-description: 'null '
seo-title: Trichteranalyse - Überblick
title: Trichteranalyse - Überblick
uuid: 2 d 98899 e-e 401-4 d 7 a -8 af 0-de 0002 f 84178
translation-type: tm+mt
source-git-commit: e3886b4fda34771c18481eace8facb9bbbc4df70

---


# Trichteranalyse - Überblick

Fallout-Visualisierungen bieten mehr Optionen zum Erstellen Ihrer Fallout-Berichte. Fallout-Berichte zeigen, wo Besucher eine Site verlassen haben (d. h., wo sie abgegangen sind) und wo sie eine vorab definierte Folge von Seiten passiert haben (d. h., wo sie verblieben sind).

Mit Fallout-Visualisierungen können Sie:

* eine Gegenüberstellung zweier verschiedener Segmente im gleichen Bericht vornehmen.
* Trichterschritte (Touchpoints) ziehen, ablegen und neu anordnen.
* Werte aus unterschiedlichen Dimensionen und Metriken mischen und kombinieren
* Einen multidimensionalen Fallout-Bericht erstellen
* Feststellen, wohin Kunden unmittelbar nach dem Ausstieg navigieren

Die Fallout-Funktion zeigt Konversions- und Fallout-Raten zwischen den einzelnen Schritten oder Touchpoints in einer Sequenz an.

So können Sie beispielsweise die Fallout-Punkte eines Besuchers während eines Kaufprozesses nachverfolgen. Wählen Sie einfach einen Start-Touchpoint und einen End-Touchpoint aus und fügen Sie Zwischen-Touchpoints hinzu, um einen Website-Navigationspfad zu erstellen. Sie können aber auch multidimensionale Fallouts vornehmen.

Eine Fallout-Visualisierung ist zur Analyse der folgenden Punkte nützlich:

* Konversionssätze durch bestimmte Abläufe auf Ihrer Site (wie z. B. ein Kauf- oder Registrierungsablauf).
* Allgemeiner, breiter gefasster Trafficfluss: Dieser Fluss zeigt, wie viele Personen, die sich die Homepage ansahen, anschließend eine Suche durchführten und dann ein bestimmtes Element anzeigten.
* Korrelationen zwischen Ereignissen auf Ihrer Site. Korrelationen zeigen, welcher Prozentsatz von Personen, die die Datenschutzrichtlinien durchlasen, ein Produkt kauften.

[Fallout-Visualisierung auf youtube](https://www.youtube.com/watch?v=VcrfHSyIoj8&index=52&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:15)

## Segmentation as a foundation for flow and fallout {#section_654F37A398C24DDDB1552A543EE29AA9}

Auf Workspace-Bedienfelder angewandte Segmente funktionieren ein wenig anders als Segmente, die auf Fallout- und Flussberichte in Reports &amp; Analytics oder Ad Hoc Analysis angewandt wurden. In den meisten Fällen liefern beide genau dieselben Ergebnisse. Der größte Unterschied besteht darin, dass in Reports &amp; Analytics und Ad Hoc Analysis dasselbe Segment auf jeden Schritt der Sequenz angewandt wird. Dies kann zu leichten Abweichungen bei den Ergebnissen führen.

Hier ist ein Beispiel eines Fallouts mit zwei Schritten:

![](assets/fallout_segments1.png)

Wenn Sie dann ein Segment auf Workspace-Bedienfeld-Ebene anwenden, kombiniert das Segment den Fallout folgendermaßen:

![](assets/fallout_segments2.png)

Beim Berechnen des Segments in Reports &amp; Analytics und Ad Hoc Analysis wird das Segment hingegen folgendermaßen kombiniert:

![](assets/fallout_segments3.png)

In Reports &amp; Analytics und Ad Hoc Analysis wird das Segment mit jedem Schritt kombiniert. Wenn sich die Container auf derselben Ebene wie der Fallout befinden (z. B. Besuch- oder Besucherebene), führt dies zu einem Angleich an die Anzahl an Besuchen oder Besuchern.

Wenn sich das auf das Feld angewandte Segment jedoch unterhalb der Fallout-Ebene (d. h. Trefferebene) befindet, werden für das Segment je nach Kombination durch den Bericht unterschiedliche Ergebnisse angezeigt. Wie bereits erwähnt, entsprechen die Zahlen in Analysis Workspace in den meisten Fällen den Zahlen in Reports &amp; Analytics und Ad Hoc Analysis. Nur wenn alle folgenden Punkte zutreffen, stimmen sie **nicht** überein:

* Das Segment befindet sich nicht auf derselben Ebene wie der Fallout.
* Das Segment weist eine Variable auf, bei der der Besucher/Besuch während eines Besuchs/Besuchers mehrere Werte besitzen kann.

Im seltenen Fall, dass Sie in Analysis Workspace Segmente auf dieselbe Weise wie in Reports &amp; Analytics auf Fallout/Fluss anwenden müssen, legen Sie das Segment einfach in jedem Fallout-Schritt in Workspace ab und erhalten dieselben Zahlen.
