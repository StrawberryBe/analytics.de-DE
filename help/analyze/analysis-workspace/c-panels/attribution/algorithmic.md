---
title: Algorithmische Attribution
description: Details zum algorithmischen Zuordnungsmodell in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 5c5e442face936ccf1ff2a3d1580e362d42e0acb
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 2%

---


# Algorithmische Attribution

>[!IMPORTANT]
>
>**[!UICONTROL Die algorithmische Zuordnung]** wird derzeit nur eingeschränkt getestet. [Mehr Infos](https://docs.adobe.com/content/help/en/analytics/landing/an-releases.html)

Das algorithmische [Zuordnungsmodell](attribution.md) in Analyse Workspace unterscheidet sich von anderen Modellen insofern, als es mithilfe statistischer Verfahren Gutschriften über die Dimensionswerte in Ihrem Bericht oder Ihrer Freiformtabelle zuweist. Wie alle anderen Zuordnungsmodelle in Analyse Workspace kann es für jede Dimension oder Metrik verwendet werden und unterstützt eine unbegrenzte Segmentierung und Aufschlüsselung und verteilt 100 % der Konversionen auf die Dimension(en) in der Tabelle (auch als &quot;Bruchzuordnung&quot;bezeichnet).

Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi Dividend aus der Genossenschaftsspieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde), um die Kreditvergabe an Spieler in einem Spiel mit ungleichen Beiträgen zum Ausgang zu verteilen.

Auf hoher Ebene betrachtet die Zuordnungsberechnung des Konversionsguthabens für jeden Touchpoint jeden Marketing-Touchpoint innerhalb eines Lookback-Fensters als eine Koalition von Akteuren, auf die ein Überschuss gleichmäßig verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionswerten) rekursiv erzeugt wurde. Weitere Informationen finden Sie in den Originaldokumenten von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. (1953). Ein Wert für persönliche Spiele. *Beiträge zur Theorie der Spiele, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Ein vereinfachtes Verhandlungsmodell für das persönliche Genossenschaftsspiel. *International Economic Review 4(2)*, 194-220.

>[!NOTE] Das Ergebnis der algorithmischen Zuordnung unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Umrechnungen mit einem einzigen Touchpoint erhalten eine Gutschrift von 100 % unabhängig vom Zuordnungsmodell.
