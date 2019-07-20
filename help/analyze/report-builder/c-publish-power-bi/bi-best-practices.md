---
description: 'null '
seo-description: 'null '
seo-title: Best Practices
title: Best Practices
uuid: 6 d 55 a 9 aa -030 e -4 e 4 d -963 c-ec 9 cc 38 e 1731
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Best Practices

## Referenzen in Power BI-Visualisierungen beibehalten {#section_7ED14FE64D974681A57EB91EF1B47CB6}

Wenn Sie eine Anforderung erstellen, besitzt diese Anforderung immer die gleiche Referenz in Power BI. Wenn Sie jedoch eine Anforderung löschen, wird die Referenz von einer neuen Anforderung verwendet, die Sie für die gleiche Dimension erstellen.

Wenn Sie eine Anforderung in Ihrer Arbeitsmappe löschen, stellen Sie sicher, dass in Power BI keine Visualisierung auf diese Anforderung verweist, da die Visualisierung dadurch beschädigt wird.

* Sofern möglich, löschen Sie keine Anforderungen, die Sie in ReportBuilder erstellt haben.
* Wenn Sie Anforderungen in ReportBuilder löschen müssen, löschen Sie auch die entsprechenden Visualisierungen in Power BI.
* Wenn Sie nicht sicher sind, löschen Sie die Anforderungen, die Sie nicht mehr benötigen, führen Sie eine erneute Veröffentlichung durch und wechseln Sie zu Power BI, um festzustellen, welche Visualisierungen beschädigt wurden.

