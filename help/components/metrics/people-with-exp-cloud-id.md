---
title: Personen mit Experience Cloud ID
description: Die Anzahl der Personen in der geräteübergreifenden Analyse, die über eine Experience Cloud ID verfügen.
source-git-commit: eaf0c3b751a5fbdc70ad6bef501dbf9e8400339c
workflow-type: ht
source-wordcount: '130'
ht-degree: 100%

---

# Personen mit Experience Cloud ID

„Personen mit Experience Cloud-ID“ ist eine Metrik der [geräteübergreifenden Analyse](../cda/overview.md), die die Anzahl der [Personen](people.md) anzeigt, die von Adobe mithilfe des [Experience Cloud ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) identifiziert wurden.

## Berechnung dieser Metrik

Bei jedem [Personen](people.md)-Treffer (identifiziert oder nicht identifiziert) erhöht sich diese Metrik, wenn der Treffer die Abfragezeichenfolge `mid` enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de)-Cookie).

Sie können die berechnete Metrik `[People with ECID] ÷ [People]` erstellen, um mithilfe des ID-Service den Prozentsatz der Besucher Ihrer Site festzustellen.

Weitere Informationen zur Bedeutung der Experience Cloud-ID und zum Debugging Ihres Setups finden Sie unter der entsprechenden Metrik der nicht-geräteübergreifenden Analyse [Besucher mit Experience Cloud ID](visitors-with-ecid.md).
