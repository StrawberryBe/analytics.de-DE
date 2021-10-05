---
title: Algorithmische Attribution
description: Details zum algorithmischen Attributionsmodell.
feature: Attribution
role: User, Admin
exl-id: dd2b2a5b-9c36-4534-999f-f96604f29eab
source-git-commit: 734eb409e7a433147c3536cebc571b38f87ce716
workflow-type: ht
source-wordcount: '257'
ht-degree: 100%

---

# Algorithmische Attribution

Das algorithmische [Attributionsmodell](models.md) in Analysis Workspace unterscheidet sich von anderen Modellen insofern, als es mithilfe statistischer Verfahren Gewichtungen über die Dimensionselemente in Ihrem Bericht oder Ihrer Freiform-Tabelle verteilt. Wie alle anderen Attributionsmodelle in Analysis Workspace kann es für jede Dimension oder Metrik verwendet werden und unterstützt eine unbegrenzte Segmentierung und Aufschlüsselung und verteilt 100 % der Konversionen auf die Dimension(en) in der Tabelle (auch als Teilattribution bezeichnet).

>[!VIDEO](https://video.tv.adobe.com/v/36205/?quality=12)

Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi-Dividende aus der kooperativen Spieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde) zur Verteilung von Gutschriften unter den Spielern in einem Spiel mit ungleichen Beiträgen zum Ergebnis.

Auf hoher Ebene betrachtet die Attributionsberechnung der Konversionsgewichtung für jeden Touchpoint jeden Marketing-Touchpoint innerhalb eines Lookback-Fensters als eine Koalition von Akteuren, auf die ein Überschuss gleichmäßig verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionselementen) rekursiv erzeugt wurde. Weitere Einzelheiten finden Sie in den Originalarbeiten von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. (1953). A value for n-person games. *Contributions to the Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). A simplified bargaining model for the n-person cooperative game. *International Economic Review 4(2)*, 194-220.

>[!NOTE]
>
>Das Ergebnis der algorithmischen Attribution unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Konversionen mit einem einzigen Touchpoint erhalten eine Gewichtung von 100 % unabhängig vom Attributionsmodell.
