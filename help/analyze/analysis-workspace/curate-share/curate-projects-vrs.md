---
title: VRS und Projektkuratierung
description: Hier erfahren Sie, wie Sie vrs-Komponenten und -Projekte kuratieren.
translation-type: tm+mt
source-git-commit: db983980a6ec3db4d60bbc8fc3ba57a4e1219287

---


# VRS und Projektkuratierung

Wenn Sie Projekte oder Virtual Report Suites (VRSs) kuratieren, filtern Sie im Wesentlichen Komponenten heraus, sodass Ihre Zielgruppe nur die von Ihnen gewünschten Projekte/VRS-Komponenten (Abmessungen, Kennzahlen, Segmente, Datumsbereiche) sehen.

>[!NOTE]
>
>Produktprofile bestimmen als Hauptmechanismen, welche Komponenten ein Anwender sehen kann. Sie werden über die [Admin Console](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html#createproductprofiles) verwaltet. Kuratierung ist ein Sekundärfilter.

Ab sofort können Sie eine verbesserte Kuratierungserfahrung genießen. Here is an overview of what the **[!UICONTROL Show All]** button reveals, in addition to the curated components already available, in different curated experiences and by permission level:

| Kuratierungstyp | Admins | Projektinhaber ohne Administratorrechte | Ohne Administratorrechte |
|---|---|---|---|
| Kuratierte VRS | Alle nicht kuratierten VRS-Komponenten | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in kuratierte VRS | Alle nicht kuratierten Komponenten, aufgeführt unter  **[!UICONTROL Non-Curated Project Components]** und **[!UICONTROL Non-Curated VRS Components]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten VRS-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte VRS- und Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |

>[!IMPORTANT]
>
>Die VRS-Kuratierung wird immer vor der Projektkuratierung ausgeführt. Das bedeutet, dass selbst wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, werden diese herausgefiltert, wenn die kuratierte VRS diese nicht enthält.
