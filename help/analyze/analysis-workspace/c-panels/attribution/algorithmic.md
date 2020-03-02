---
description: 'null'
title: Algorithmische Zuordnung
uuid: bb345642-4f45-4fb8-82d0-803248dd52ea
translation-type: tm+mt
source-git-commit: b5418e6321b09ddbab36e0052f75f36067086e3e

---


# Algorithmische Zuordnung

![Algorithmus](assets/algorithmic.png)

Das algorithmische [Zuordnungsmodell](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html#attribution-models) in Analysis Workspace unterscheidet sich von anderen Modellen in Attribution IQ insofern, als es statistische Techniken verwendet, um die Gutschrift über die Dimensionswerte in Ihrem Bericht oder Ihrer Freiform-Tabelle zu verteilen. Wie alle anderen Zuordnungsmodelle in Analysis Workspace kann es für jede Dimension oder Metrik verwendet werden und unterstützt unbegrenzte Segmentierung und Aufschlüsselungen und verteilt 100 % der Konversionen auf die Dimension(en) in der Tabelle (auch als &quot;Bruchzuordnung&quot;bezeichnet).

Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi Dividend aus der Genossenschaftsspieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde), um die Kreditvergabe an Spieler in einem Spiel mit ungleichen Beiträgen zum Ausgang zu verteilen.

Auf hoher Ebene betrachtet die Zuordnungsberechnung des Konversionsguthabens für jeden Touchpoint jeden Marketing-Touchpoint innerhalb eines Lookback-Fensters als eine Koalition von Akteuren, auf die ein Überschuss gleichmäßig verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionswerten) rekursiv erzeugt wurde. Weitere Informationen finden Sie in den Originaldokumenten von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. &quot;Ein Wert für persönliche Spiele.&quot; Beiträge zur Spieltheorie 2.28 (1953): 307-317.

* Harsanyi, John C. &quot;Ein vereinfachtes Verhandlungsmodell für das persönliche Genossenschaftsspiel.&quot; International Economic Review 4.2 (1963): 194-220.

*Hinweis: Das Ergebnis der algorithmischen Zuordnung unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Bei nur einem einzigen Touchpoint werden beispielsweise 100 % der Gutschrift diesem Wert zugeordnet, unabhängig vom ausgewählten Zuordnungsmodell.*