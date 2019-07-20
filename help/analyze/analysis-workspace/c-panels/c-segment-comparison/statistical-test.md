---
description: Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.
keywords: Analysis Workspace; Segment-IQ
seo-description: Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.
seo-title: Statistische Tests, die im Segmentvergleich verwendet werden
solution: Analytics
title: Statistische Tests, die im Segmentvergleich verwendet werden
topic: Reports and Analytics
uuid: c 3 f 52470-5 bfc -4 e 6 b -8638-1 c 142 b 08 d 013
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Statistische Tests, die im Segmentvergleich verwendet werden

Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.

Der Wert 0 besagt, dass es keine Unterschiede zwischen den beiden Segmenten gibt. Der Wert 1 besagt, dass es einen sehr großen Unterschied zwischen den beiden Segmenten gibt. Es werden zwei Typen von statistischen Tests verwendet, um diese Differenzwerte zu generieren: Für die Tabelle der Top-Metriken wird ein Mann-Whitney-U-Test verwendet, für die Tabellen der Top-Dimensionselemente und der Top-Segmente wird ein Vergleich der Risikodifferenz verwendet.

## Top metrics difference score {#section_5E8047464EB945C78543B25F8F30F17A}

In der Tabelle „Top Metriken“ verwendet das Segmentvergleichswerkzeug einen Mann-Whitney-U-Test mit zwei Stichproben, bei dem es sich um einen nichtparametrischen Gleichheitstest handelt, mit dem die eindimensionalen Wahrscheinlichkeitsverteilungen der einzelnen Metriken für jedes betrachtete Segment verglichen werden. Der Differenzwert in der Tabelle der Metriken ist eine Kombination aus dem p-Wert der berechneten U-Statistik (der angibt, wie stochastisch unterschiedlich die beiden Segmente innerhalb einer bestimmten Metrik verteilt sind) und der relativen Größenordnung der beobachteten Differenz. Ein hoher Differenzwert (nahe an 1) besagt, dass eine bestimmte Metrik eine große relative Differenz sowie eine hohe statistische Genauigkeit besitzt, dass die Segmente unterschiedlich sind.

## Top dimension items and top segments difference scores {#section_8073ADA6053B44C9A23FDC5ED4AF2AC4}

Für die Berechnung des Differenzwerts der Tabelle der Top-Dimensionselemente und der Top-Segmente wird ein relativer Risikodifferenz-Algorithmus verwendet (vergleichbar mit dem Risikoverhältnis, auch wenn anstelle eines Verhältnisses eine Differenz verwendet wird). Eine Risikodifferenz wird durch Subtraktion der kumulierten Häufigkeiten eines Dimensionselements (oder der Überschneidung mit einem Segment der Segmenttabelle) eines ausgewählten Segments von der eines anderen berechnet. Ein hoher Differenzwert (nahe an 1) besagt, dass ein bestimmtes Dimensionselement oder ein drittes Segment in einem der ausgewählten Segmente sehr stark vorhanden ist und in dem anderen nicht.

>[!NOTE]
>
>In allen drei Tabellen basiert die Differenzstatistik auf einem geeigneten Besuchermuster, damit der Prozess so schnell wie möglich ausgeführt wird, während er statistisch genau bleibt. Während der Differenzwert auf einer Stichprobe basiert, handelt es sich bei den in der Tabelle angezeigten Ergebnissen nicht um eine Stichprobe. Damit die statistische Bedeutung sichergestellt ist, basiert jeder statistische Test auf einem dynamischen Zuteilungsalgorithmus, sodass das kleinere Segment eine Stichprobengröße enthält, die eine Fehlergrenze von unter 3 % gewährleistet. Wenn ein Segment sehr wenige Besucher enthält (weniger als 1.000), werden für die Berechung des Differenzwerts alle verfügbaren Daten verwendet und es wird keine Stichprobe gebildet.

