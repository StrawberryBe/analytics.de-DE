---
title: VRS und Projektkuratierung
description: Hier erfahren Sie, wie Sie vrs-Komponenten und -Projekte kuratieren.
translation-type: tm+mt
source-git-commit: 3a00162c5899ba2d5bb1b5aaed448b2abe93d56d

---


# VRS und Projektkuratierung

Wenn Sie Projekte oder Virtual Report Suites (VRSs) kuratieren, filtern Sie im Wesentlichen Komponenten heraus, sodass Ihre Zielgruppe nur die von Ihnen gewünschten Projekte/VRS-Komponenten (Abmessungen, Kennzahlen, Segmente, Datumsbereiche) sehen.

>[!Note]
>Produktprofile sind der primäre Mechanismus, der bestimmt, welche Komponenten ein Benutzer sehen kann. They are managed through the [Admin Console](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html#createproductprofiles). Kuratierung ist ein Sekundärfilter.

Ab sofort können Sie eine verbesserte Kuratierungserfahrung genießen. Hier finden Sie eine Übersicht darüber, was die Schaltfläche **[!UICONTROL Alle anzeigen]**in verschiedenen Kuratierungserfahrungen und nach Berechtigungsstufe zusätzlich zu den bereits verfügbaren kuratierten Komponenten zeigt:

| Kuratierungstyp | Admins | Projektinhaber ohne Administratorrechte | Ohne Administratorrechte |
|---|---|---|---|
| Kuratierte VRS | Alle nicht kuratierten VRS-Komponenten | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in kuratierte VRS | Alle nicht kuratierten Komponenten, aufgeführt unter **[!UICONTROL Non-Curated Project Components]**and**[!UICONTROL  Non-Curated VRS Components]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten VRS-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte VRS- und Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |

>[!IMPORTANT]
>VRS-Kuratierung wird immer vor der Projektkuratierung angewendet. Das bedeutet, dass selbst wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, diese herausgefiltert werden, wenn die kuratierte VRS diese nicht enthält.
