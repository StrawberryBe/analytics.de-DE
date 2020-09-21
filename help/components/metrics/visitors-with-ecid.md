---
title: Besucher mit Experience Cloud ID
description: Die Anzahl der Unique Visitors, die den Adobe Experience Cloud Identity Service verwenden.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '376'
ht-degree: 100%

---


# Besucher mit Experience Cloud ID

Die Metrik „Besucher mit Experience Cloud ID“ gibt die Anzahl der Unique Visitors an, die von Adobe mithilfe des [Experience Cloud Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) identifiziert wurden. Sie können diese Dimension mit der Metrik [Unique Visitors](unique-visitors.md) vergleichen, um sicherzustellen, dass die Mehrheit der Besucher Ihrer Site den Identity Service verwendet. Wenn ein Großteil der Besucher die Identity Service-Cookies nicht verwendet, kann dies auf ein Problem in Ihrer Implementierung hindeuten.

>[!NOTE]
>
>Diese Metrik ist besonders wichtig für das Debugging, wenn Sie mehrere Experience Cloud-Dienste wie Adobe Target oder Adobe Audience Manager verwenden. Segmente, die über Experience Cloud-Produkte hinweg gemeinsam genutzt werden, enthalten keine Besucher ohne Experience Cloud ID.

## Berechnung dieser Metrik

Diese Metrik basiert auf der Metrik [Unique Visitors](unique-visitors.md), mit der Ausnahme, dass sie nur die mit der `mid`-Abfragezeichenfolge identifizierten Personen enthält (basierend auf dem [`s_ecid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html)-Cookie).

## Debuggen Ihres Experience Cloud ID-Setups

Die Metrik „Besucher mit Experience Cloud ID“ kann bei der Fehlerbehebung von Experience Cloud-Integrationen oder bei der Identifizierung von Bereichen Ihrer Site hilfreich sein, in denen der Identity Service nicht bereitgestellt wird.

Ziehen Sie die „Besucher mit Experience Cloud ID“ neben „Unique Visitors“, um sie zu vergleichen:

![Vergleich der Unique Visitors](assets/metric-mcvid1.png)

Beachten Sie Folgendes: In diesem Beispiel weist jede Seite eine identische Anzahl an Unique Visitors und Besuchern mit Experience Cloud ID auf. Die Gesamtanzahl an Unique Visitors ist dabei größer als die Gesamtanzahl an Besuchern mit Experience Cloud ID. Sie können eine [berechnete Metrik](../c-calcmetrics/cm-overview.md) erstellen, um herauszufinden, welche Seiten den Identity Service nicht einrichten. Sie können die folgende Definition verwenden:

![Definition berechneter Metriken](assets/metric-mcvid2.png)

Wenn Sie die berechnete Metrik zum Bericht hinzufügen, können Sie den Seitenbericht so sortieren, dass die Seiten mit der größten Anzahl an Besuchern ohne MCID oben angezeigt werden:

![Seiten ohne Identity Service](assets/metric-mcvid3.png)

Beachten Sie, dass das Dimensionselement „Schnellansichten Produkt“ nicht ordnungsgemäß mit dem Identity Service implementiert ist. Sie können mit entsprechenden Teams in Ihrem Unternehmen zusammenarbeiten, um diese Seiten so schnell wie möglich zu aktualisieren. Sie können einen ähnlichen Bericht mit einer beliebigen Dimension wie [Browser-Typ](../dimensions/browser-type.md), [Website-Bereich](../dimensions/site-section.md) oder einer beliebigen [eVar](../dimensions/evar.md) erstellen.
