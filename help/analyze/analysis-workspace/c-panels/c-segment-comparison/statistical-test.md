---
description: Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.
keywords: Analysis Workspace;Segment IQ
title: Im Segmentvergleich verwendete statistische Tests
topic: Reports and analytics
uuid: c3f52470-5bfc-4e6b-8638-1c142b08d013
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Im Segmentvergleich verwendete statistische Tests

Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.

Ein Wert von 0 bedeutet, dass es keinen Unterschied zwischen den beiden Segmenten gibt und ein Wert von 1 bedeutet, dass es einen sehr großen Unterschied zwischen den beiden Segmenten gibt. Es werden zwei Arten statistischer Tests verwendet, um diese Differenzwerte zu generieren: Für die Tabelle &quot;Top-Metriken&quot;wird ein Mann-Whitney-U-Test verwendet, und für die Tabelle &quot;Top-Dimensionselemente&quot;und &quot;Top-Segmente&quot;wird ein Vergleich der Risikodifferenz verwendet.

## Differenzwert der Top-Metriken {#section_5E8047464EB945C78543B25F8F30F17A}

In der Tabelle &quot;Top-Metriken&quot;verwendet das Segmentvergleichswerkzeug einen Mann-Whitney-U-Test mit zwei Beispielen, bei dem es sich um einen nicht parametrischen Gleichheitstest handelt, mit dem die eindimensionalen Wahrscheinlichkeitsverteilungen der einzelnen Metriken für jedes betrachtete Segment verglichen werden. Der Differenzwert in der Metriktabelle ist eine Kombination aus dem p-Wert der berechneten U-Statistik (der angibt, wie stochastisch unterschiedlich die beiden Segmente über eine bestimmte Metrik verteilt sind) und der relativen Größenordnung der beobachteten Differenz. Ein großer Differenzwert (nahe an 1) bedeutet, dass die jeweilige Metrik einen großen relativen Unterschied sowie eine hohe statistische Konfidenz aufweist, dass die Segmente unterschiedlich sind.

## Differenzwerte für Top-Dimensionselemente und Top-Segmente {#section_8073ADA6053B44C9A23FDC5ED4AF2AC4}

Zur Berechnung des Differenzwerts in den Tabellen &quot;Top-Dimensionselemente&quot;und &quot;Oberste Segmentdifferenz&quot;wird ein Algorithmus zur Variation des relativen Risikos verwendet (ähnlich dem Risikoverhältnis, wenn auch eine Differenz anstelle eines Verhältnisses verwendet wird). Eine Risikodifferenz wird berechnet, indem die kumulativen Inzidenzen eines Dimensionselements (oder die Überschneidung mit einem Segment aus der Segmenttabelle) eines ausgewählten Segments vom anderen abgezogen werden. Ein hoher Differenzwert (nahe an 1) bedeutet, dass das bestimmte Dimensionselement oder das tertiäre Segment in einem der ausgewählten Segmente sehr hervorgehoben war und nicht in dem anderen.

>[!NOTE]In allen drei Tabellen basiert die Differenzstatistik auf einer geeigneten Stichprobe von Besuchern, damit der Prozess schnellstmöglich ausgeführt werden kann, während er dennoch statistisch genau bleibt. Während der Differenzwert auf einer Stichprobe basiert, werden die in der Tabelle dargestellten Ergebnisse nicht in eine Stichprobe aufgenommen. Zur Gewährleistung der statistischen Signifikanz beruht jeder statistische Test auf einem dynamischen Zuordnungsalgorithmus, sodass das kleinere Segment eine Stichprobengröße enthält, die eine Fehlermarge von weniger als 3 % bietet. Wenn ein Segment nur sehr wenige Besucher enthält (weniger als 1.000), verwenden wir alle verfügbaren Daten und verwenden keine Stichprobe für die Berechnung des Differenzwerts.
