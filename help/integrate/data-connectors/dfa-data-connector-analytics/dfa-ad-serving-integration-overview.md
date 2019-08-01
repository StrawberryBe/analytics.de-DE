---
description: 'Diese Integration erfasst Daten über Besucher, deren Aktionen von Anzeigen bestimmt werden, auf viele verschiedene Wege. Zunächst gibt es den so genannten Clickthrough, das heißt Besucher klicken auf eine Anzeige und werden auf eine getaggte Landingpage weitergeleitet '
keywords: DFA
seo-description: 'Diese Integration erfasst Daten über Besucher, deren Aktionen von Anzeigen bestimmt werden, auf viele verschiedene Wege. Zunächst gibt es den so genannten Clickthrough, das heißt Besucher klicken auf eine Anzeige und werden auf eine getaggte Landingpage weitergeleitet '
seo-title: Übersicht zur AdServing-Integration
solution: Analytics
title: Übersicht zur AdServing-Integration
topic: Data Connectors
uuid: e 286 f 61 e -4 b 90-48 b 5-b 1 e 9-3 c 07 b 6 face 24
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Übersicht zur AdServing-Integration{#ad-serving-integration-overview}

Diese Integration erfasst Daten über Besucher, deren Aktionen von Anzeigen bestimmt werden, auf viele verschiedene Wege. Zunächst gibt es den so genannten Clickthrough, das heißt Besucher klicken auf eine Anzeige und werden auf eine getaggte Landingpage weitergeleitet:

![](assets/Diagram1.png)

Besucher gelangen zur Site eines Herausgebers, auf der die Anzeige gehostet wird. Diese Anzeige verfügt über die so genannte einzigartige Anzeigen-ID. Eine Anzeige besteht aus einer Platzierung sowie dem zugehörigen kreativen Inhalt. Sie beschreiben den Anzeigeort auf der Site des Herausgebers und den angezeigten Inhalt für Besucher. Rufen Besucher diese Anzeige, diese Platzierung oder diesen kreativen Inhalt von den DFA-Inhaltsservern ab, wird auf den DFA Floodlight-Servern für sie eine Impression getrackt (1).

Klicken Besucher auf die Anzeige (2), wird der Floodlight-Server kontaktiert, was als Klick zählt. Anschließend werden Besucher durch 302 auf die Landingpage weitergeleitet (3). Befinden sich die Besucher dann auf der Landingpage, wird dies als Clickthrough bezeichnet. Diese Seite enthält Adobe-Trackingcode, durch den Daten vom DFA Floodlight-Server abgerufen werden.

Gelangen die Besucher nach dem Tracken eines Klicks durch den Floodlight-Server nicht auf die Landingpage, wird nicht von einem Clickthrough gesprochen. Bei einigen Anzeigen oder Implementierungen kann es vorkommen, dass der Besucherbrowser nicht durch 302 weitergeleitet wird. Weiteres dazu finden Sie unter [Abgleich von Metrikdiskrepanzen](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies/dfa-reconciling-metric-discrepancies.md#concept-8c31ebe761ca4b3fab1e3a18ef5d098f).

Eine weitere Metrik, die von dieser Integration erfasst wird, tritt ein, wenn Besucher die Anzeigenimpression erhalten, nicht klicken, aber doch auf anderem Weg kurze Zeit nach der Impression auf die Landingpage gelangen.

![](assets/Viewthrough.png)

In diesem Fall wird von einer Durchsicht gesprochen. Der Unterschied zwischen diesem Szenario und dem Clickthrough besteht darin, dass Besucher nicht auf die Anzeige klicken, sondern erst andere Aktivitäten durchführen und anschließend anderweitig zur Landingpage gelangen (2). Der einfachste Fall besteht darin, dass Besucher die URL der Landingpage in ihre Adresszeile im Browser eingeben. In anderen Fällen fahren die Besucher mit dem Browsen fort, verwenden später aber eine Suchmaschine, durch die sie auf die Landingpage gelangen. Die Besucher gelangen in jedem Fall auf die Landingpage.
