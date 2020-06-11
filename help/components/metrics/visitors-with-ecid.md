---
title: Besucher mit Experience Cloud ID
description: Die Anzahl der eindeutigen Besucher, die den Adobe Experience Cloud ID-Dienst verwenden.
translation-type: tm+mt
source-git-commit: 0328de560185e716a3913080feda9cd078e0f206
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 19%

---


# Besucher mit Experience Cloud ID

Die Metrik &quot;Besucher mit Experience Cloud ID&quot;zeigt die Anzahl der eindeutigen Besucher, die von Adobe mithilfe des [Experience Cloud ID-Diensts](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html)identifiziert wurden. Diese Dimension ist hilfreich, um mit der Metrik &quot; [Individuelle Besucher](unique-visitors.md) &quot;zu vergleichen, um sicherzustellen, dass die Mehrzahl der Besucher Ihrer Site den ID-Dienst verwendet. Wenn ein Großteil der Besucher die ID-Dienst-Cookies nicht verwendet, kann dies auf ein Problem in Ihrer Implementierung hindeuten.

>[!NOTE] Diese Metrik ist besonders beim Debugging wichtig, wenn Sie mehrere Experience Cloud-Dienste wie Adobe Zielgruppe oder Adobe Audience Manager verwenden. Segmente, die für alle Experience Cloud-Produkte freigegeben wurden, enthalten keine Besucher ohne Experience Cloud ID.

## Berechnung dieser Metrik

Diese Metrik basiert auf der Metrik &quot; [Individuelle Besucher](unique-visitors.md) &quot;, mit der Ausnahme, dass sie nur die mit der `mid` Abfrage-Zeichenfolge identifizierten Personen enthält (basierend auf dem [`s_ecid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html) Cookie).

## Debuggen der Experience Cloud ID-Einrichtung

Die Metrik &quot;Besucher mit Experience Cloud ID&quot;kann bei der Fehlerbehebung für Experience Cloud-Integrationen oder bei der Identifizierung von Bereichen Ihrer Site nützlich sein, in denen der ID-Dienst nicht bereitgestellt ist.

Ziehen Sie die &quot;Besucher mit Experience Cloud ID&quot;nebeneinander mit &quot;Individuelle Besucher&quot;, um sie zu vergleichen:

![Vergleich individueller Besucher](assets/metric-mcvid1.png)

Beachten Sie in diesem Beispiel, dass jede Seite dieselbe Anzahl von &quot;Individuellen Besuchern&quot;wie &quot;Besucher mit einer Experience Cloud ID&quot;aufweist. Die Gesamtanzahl an Unique Visitors ist dabei größer als die Gesamtanzahl an Besuchern mit Experience Cloud ID. Sie können eine [berechnete Metrik](../c-calcmetrics/cm-overview.md) erstellen, um herauszufinden, welche Seiten den ID-Dienst nicht einrichten. Sie können die folgende Definition verwenden:

![Definition berechneter Metriken](assets/metric-mcvid2.png)

Wenn Sie die berechnete Metrik zum Bericht hinzufügen, können Sie den Seiten-Bericht so sortieren, dass die Seiten mit der größten Anzahl an Besuchern ohne MCID oben angezeigt werden:

![Seiten ohne ID-Dienst](assets/metric-mcvid3.png)

Beachten Sie, dass der Dimensionswert &quot;Produktschnelle Ansichten&quot;nicht ordnungsgemäß mit dem Identitätsdienst implementiert ist. Sie können mit entsprechenden Teams in Ihrem Unternehmen zusammenarbeiten, um diese Seiten so schnell wie möglich zu aktualisieren. Sie können einen ähnlichen Bericht mit einer beliebigen Dimension wie [Browsertyp](../dimensions/browser-type.md), [Site-Abschnitt](../dimensions/site-section.md)oder einer beliebigen [eVar](../dimensions/evar.md)erstellen.
