---
title: Algorithmische Zuordnung
description: Details zum algorithmischen Zuordnungsmodell in Adobe Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Algorithmische Zuordnung

>[!NOTE] Algorithmische Zuordnung ist derzeit nur über [Adobe Analytics Labs](https://docs.adobe.com/content/help/de-DE/analytics/analyze/tech-previews/overview.html)verfügbar. Die Funktion wird schließlich Teil einer allgemeinen Version sein.

Das algorithmische [Zuordnungsmodell](attribution.md) in Analyse Workspace unterscheidet sich von anderen Modellen insofern, als es mithilfe statistischer Verfahren Gutschriften über die Dimensionswerte in Ihrem Bericht oder Ihrer Freiformtabelle zuweist. Wie alle anderen Zuordnungsmodelle in Analyse Workspace kann es für jede Dimension oder Metrik verwendet werden und unterstützt eine unbegrenzte Segmentierung und Aufschlüsselung und verteilt 100 % der Konversionen auf die Dimension(en) in der Tabelle (auch als &quot;Bruchzuordnung&quot;bezeichnet).

Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi Dividend aus der Genossenschaftsspieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde), um die Kreditvergabe an Spieler in einem Spiel mit ungleichen Beiträgen zum Ausgang zu verteilen.

Auf hoher Ebene betrachtet die Zuordnungsberechnung des Konversionsguthabens für jeden Touchpoint jeden Marketing-Touchpoint innerhalb eines Lookback-Fensters als eine Koalition von Akteuren, auf die ein Überschuss gleichmäßig verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionswerten) rekursiv erzeugt wurde. Weitere Informationen finden Sie in den Originaldokumenten von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. (1953). Ein Wert für persönliche Spiele. *Beiträge zur Theorie der Spiele, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Ein vereinfachtes Verhandlungsmodell für das persönliche Genossenschaftsspiel. *International Economic Review 4(2)*, 194-220.

>[!NOTE] Das Ergebnis der algorithmischen Zuordnung unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Umrechnungen mit einem einzigen Touchpoint erhalten eine Gutschrift von 100 % unabhängig vom Zuordnungsmodell.
