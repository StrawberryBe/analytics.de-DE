---
description: Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.
keywords: Analysis Workspace;Segment IQ
title: Im Segmentvergleich verwendete statistische Tests
feature: Grundlagen zu Reports & Analysen
uuid: c3f52470-5bfc-4e6b-8638-1c142b08d013
role: Business Practitioner, Administrator
exl-id: b1c235ca-2eab-48d2-bf11-e8a8c4067d03
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 98%

---

# Im Segmentvergleich verwendete statistische Tests

Alle Top-Vergleichstabellen zeigen einen Differenzwert, der anhand verschiedener statistischer Tests berechnet wird, die von dem durchgeführten Vergleich abhängen. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert immer als Wert zwischen 0 und 1 angegeben.

Der Wert 0 besagt, dass es keine Unterschiede zwischen den beiden Segmenten gibt. Der Wert 1 besagt, dass es einen sehr großen Unterschied zwischen den beiden Segmenten gibt. Es werden zwei Typen von statistischen Tests verwendet, um diese Differenzwerte zu generieren: Für die Tabelle der Top-Metriken wird ein Mann-Whitney-U-Test verwendet, für die Tabellen der Top-Dimensionselemente und der Top-Segmente wird ein Vergleich der Risikodifferenz verwendet.

## Differenzwert der Top-Metriken {#section_5E8047464EB945C78543B25F8F30F17A}

In der Tabelle „Top Metriken“ verwendet das Segmentvergleichswerkzeug einen Mann-Whitney-U-Test mit zwei Stichproben, bei dem es sich um einen nichtparametrischen Gleichheitstest handelt, mit dem die eindimensionalen Wahrscheinlichkeitsverteilungen der einzelnen Metriken für jedes betrachtete Segment verglichen werden. Der Differenzwert in der Tabelle der Metriken ist eine Kombination aus dem p-Wert der berechneten U-Statistik (der angibt, wie stochastisch unterschiedlich die beiden Segmente innerhalb einer bestimmten Metrik verteilt sind) und der relativen Größenordnung der beobachteten Differenz. Ein hoher Differenzwert (nahe an 1) besagt, dass eine bestimmte Metrik eine große relative Differenz sowie eine hohe statistische Genauigkeit besitzt, dass die Segmente unterschiedlich sind.

## Differenzwerte für Top-Dimensionselemente und Top-Segmente {#section_8073ADA6053B44C9A23FDC5ED4AF2AC4}

Für die Berechnung des Differenzwerts der Tabelle der Top-Dimensionselemente und der Top-Segmente wird ein relativer Risikodifferenz-Algorithmus verwendet (vergleichbar mit dem Risikoverhältnis, auch wenn anstelle eines Verhältnisses eine Differenz verwendet wird). Eine Risikodifferenz wird durch Subtraktion der kumulierten Häufigkeiten eines Dimensionselements (oder der Überschneidung mit einem Segment der Segmenttabelle) eines ausgewählten Segments von der eines anderen berechnet. Ein hoher Differenzwert (nahe an 1) besagt, dass ein bestimmtes Dimensionselement oder ein drittes Segment in einem der ausgewählten Segmente sehr stark vorhanden ist und in dem anderen nicht.

>[!NOTE]
>
>In allen drei Tabellen basiert die Differenzstatistik auf einer geeigneten Stichprobe von Besuchern, damit der Prozess schnellstmöglich ausgeführt werden kann, während er dennoch statistisch genau bleibt. Während der Differenzwert auf einer Stichprobe basiert, handelt es sich bei den in der Tabelle angezeigten Ergebnissen nicht um eine Stichprobe. Damit die statistische Bedeutung sichergestellt ist, basiert jeder statistische Test auf einem dynamischen Zuteilungsalgorithmus, sodass das kleinere Segment eine Stichprobengröße enthält, die eine Fehlergrenze von unter 3 % gewährleistet. Wenn ein Segment sehr wenige Besucher enthält (weniger als 1.000), werden für die Berechung des Differenzwerts alle verfügbaren Daten verwendet und es wird keine Stichprobe gebildet.
