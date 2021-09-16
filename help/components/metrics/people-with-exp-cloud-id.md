---
title: Personen mit Experience Cloud-ID
description: Die Anzahl der Personen in der geräteübergreifenden Analyse, die über eine Experience Cloud-ID verfügen.
source-git-commit: eaf0c3b751a5fbdc70ad6bef501dbf9e8400339c
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 21%

---

# Personen mit Experience Cloud-ID

&quot;Personen mit Experience Cloud-ID&quot;ist eine [geräteübergreifende Analyse](../cda/overview.md) -Metrik, die die Anzahl der [Personen](people.md) anzeigt, die durch Adobe mit dem [Experience Cloud-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) identifiziert wurden.

## Berechnung dieser Metrik

Bei jedem [Personen](people.md) (identifiziert oder nicht identifiziert) erhöht sich diese Metrik, wenn der Treffer die `mid` Abfragezeichenfolge enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de) -Cookie).

Sie können die berechnete Metrik `[People with ECID] ÷ [People]` erstellen, um den Prozentsatz der Besucher Ihrer Site mithilfe des ID-Diensts abzurufen.

Weitere Informationen zur Wichtigkeit der Experience Cloud-ID und zum Debugging Ihres Setups finden Sie unter der entsprechenden Nicht-CDA-Metrik [Besucher mit Experience Cloud-ID](visitors-with-ecid.md) .
