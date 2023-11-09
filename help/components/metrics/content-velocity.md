---
title: Content-Geschwindigkeit
description: Content-Geschwindigkeit misst die Auswirkungen von Inhalten auf nachgeordnete Inhalte.
feature: Metrics
exl-id: 8ba54990-ff7d-4693-92de-7f9d9f916b55
source-git-commit: 26e166e065df90cb327fe1106542e17831069141
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 19%

---

# Content-Geschwindigkeit

Mit der berechneten Metrik &quot;Content-Geschwindigkeit&quot;können Sie messen, wie eine Dimension (normalerweise [[!UICONTROL Seite]](/help/components/dimensions/page.md)) trägt dazu bei, dass Benutzer Zeit auf Ihrer Website oder in Ihrer App verbringen.

Diese Metrik verwendet [Beitragszuordnung](/help/analyze/analysis-workspace/attribution/models.md) auf [Seitenansichten](page-views.md) -Metrik als Teil der Berechnung. Bei der Teilnahme an Besuchen werden bei jedem Treffer einer Seite auch alle Seiten, die zuvor während desselben Besuchs aufgerufen wurden, für die Seitenansicht angerechnet. Diese Formel bedeutet normalerweise, dass je früher ein Seitenaufruf während eines Besuchs erfolgt, desto mehr Gewichtung erhält er. (Siehe [Seitenansichten (Beitrag) | Besuch) oder &quot;Besuchsbeteiligung&quot;](#page-views-participation--visit-or-visit-participation) für weitere Informationen.)

## Berechnung

&#39;Content-Geschwindigkeit&#39; ist eine standardmäßig berechnete [Metrik](overview.md) und verwendet die Formel `Page views (Visit participation)` dividiert durch `Visits`.

![](assets/cont-velo-1.png)

## Häufige Verwendungszwecke

[!UICONTROL Content-Geschwindigkeit] wird häufig bei der Analyse von Inhalten neben anderen Schlüsselmetriken wie [!UICONTROL Seitenansichten], [!UICONTROL Besuche] und [!UICONTROL Absprungrate] verwendet.

![](assets/cont-velo-3.png)

## Beispiel

Im folgenden Beispiel werden die beiden Teile der Content-Geschwindigkeit unterteilt: &quot;Seitenansichten (Beitrag) | Besuch)&quot;und &quot;Besuche&quot;.

### Seitenansichten (Beitrag) | Besuch) oder &quot;Besuchsbeteiligung&quot;

Betrachten Sie das folgende Beispiel, wie die Besuchsbeteiligung die Attribution beeinflusst:

Auf einer Website besucht ein Benutzer die folgenden Seiten in dieser Reihenfolge:

* Seite A
* Seite B
* Seite C
* Seite D

Im obigen Beispiel würde Seite A eine Gutschrift für 4 Treffer, Seite B für 3 Treffer, Seite C für 2 Treffer und Seite D für 1 Treffer erhalten.

Das folgende Beispiel veranschaulicht das gleiche Prinzip, wobei einige Seiten jedoch mehrmals besucht werden.

* Seite A
* Seite B
* Seite C
* Seite B
* Seite D
* Seite A

Im obigen Beispiel würde Seite A die Gutschrift für 7 Treffer, Seite B für 8 Treffer, Seite C für 4 Treffer und Seite D für 2 Treffer erhalten.

### Besuche

Nach der Berechnung der Besuchsbeteiligung wird das Ergebnis durch die Anzahl der Besuche dividiert.
