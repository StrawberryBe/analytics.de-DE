---
description: 'Power BI: Best Practices.'
title: Best Practices
uuid: 6d55a9aa-030e-4e4d-963c-ec9cc38e1731
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 95%

---


# Best Practices

## Referenzen in Power BI-Visualisierungen beibehalten {#section_7ED14FE64D974681A57EB91EF1B47CB6}

Wenn Sie eine Anforderung erstellen, besitzt diese Anforderung immer die gleiche Referenz in Power BI. Wenn Sie jedoch eine Anforderung löschen, wird die Referenz von einer neuen Anforderung verwendet, die Sie für die gleiche Dimension erstellen.

Wenn Sie eine Anforderung in Ihrer Arbeitsmappe löschen, stellen Sie sicher, dass in Power BI keine Visualisierung auf diese Anforderung verweist, da die Visualisierung dadurch beschädigt wird.

* Sofern möglich, löschen Sie keine Anforderungen, die Sie in Report Builder erstellt haben.
* Wenn Sie Anforderungen in Report Builder löschen müssen, löschen Sie auch die entsprechenden Visualisierungen in Power BI.
* Wenn Sie nicht sicher sind, löschen Sie die Anforderungen, die Sie nicht mehr benötigen, führen Sie eine erneute Veröffentlichung durch und wechseln Sie zu Power BI, um festzustellen, welche Visualisierungen beschädigt wurden.

