---
title: Algorithmische Zuordnung
description: Details zum algorithmischen Zuordnungsmodell in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 143cbed5f2159b7faab387e10896af836d0780f7

---


# Algorithmische Zuordnung

Das algorithmische [Zuordnungsmodell](attribution.md) in Analysis Workspace unterscheidet sich von anderen Modellen insofern, als es mithilfe statistischer Verfahren Gutschriften über die Dimensionswerte in Ihrem Bericht oder Ihrer Freiformtabelle verteilt. Wie alle anderen Zuordnungsmodelle in Analysis Workspace kann es für jede Dimension oder Metrik verwendet werden und unterstützt unbegrenzte Segmentierung und Aufschlüsselungen und verteilt 100 % der Konversionen auf die Dimension(en) in der Tabelle (auch als &quot;Bruchzuordnung&quot;bezeichnet).

Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi Dividend aus der Genossenschaftsspieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde), um die Kreditvergabe an Spieler in einem Spiel mit ungleichen Beiträgen zum Ausgang zu verteilen.

Auf hoher Ebene betrachtet die Zuordnungsberechnung des Konversionsguthabens für jeden Touchpoint jeden Marketing-Touchpoint innerhalb eines Lookback-Fensters als eine Koalition von Akteuren, auf die ein Überschuss gleichmäßig verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionswerten) rekursiv erzeugt wurde. Weitere Informationen finden Sie in den Originaldokumenten von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. &quot;Ein Wert für persönliche Spiele.&quot; *Beiträge zur Theory of Games 2.28*, 1953, S. 1. 307-317.
* Harsanyi, John C. &quot;Ein vereinfachtes Verhandlungsmodell für das persönliche Genossenschaftsspiel.&quot; *International Economic Review 4.2*, 1963, S. 1. 194-220.

> [!NOTE] Das Ergebnis der algorithmischen Zuordnung unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Umrechnungen mit einem einzigen Touchpoint erhalten eine Gutschrift von 100 % unabhängig vom Zuordnungsmodell.
