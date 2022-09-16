---
description: Best Practices für Power BI.
title: Best Practices
feature: Report Builder
role: User, Admin
exl-id: 2d9447f4-77ac-465b-af93-206dc3ea80f7
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 100%

---

# Best Practices

## Beibehalten von Referenzen in Power BI-Visualisierungen {#section_7ED14FE64D974681A57EB91EF1B47CB6}

Wenn Sie eine Anforderung erstellen, besitzt diese Anforderung immer die gleiche Referenz in Power BI. Wenn Sie jedoch eine Anforderung löschen, wird die Referenz von einer neuen Anforderung verwendet, die Sie für die gleiche Dimension erstellen.

Wenn Sie eine Anforderung in Ihrer Arbeitsmappe löschen, stellen Sie sicher, dass in Power BI keine Visualisierung auf diese Anforderung verweist, da die Visualisierung dadurch beschädigt wird.

* Sofern möglich, löschen Sie keine Anforderungen, die Sie in Report Builder erstellt haben.
* Wenn Sie Anforderungen in Report Builder löschen müssen, löschen Sie auch die entsprechenden Visualisierungen in Power BI.
* Wenn Sie nicht sicher sind, löschen Sie die Anforderungen, die Sie nicht mehr benötigen, führen Sie eine erneute Veröffentlichung durch und wechseln Sie zu Power BI, um festzustellen, welche Visualisierungen beschädigt wurden.
