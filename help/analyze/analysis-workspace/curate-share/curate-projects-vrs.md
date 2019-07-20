---
title: VRS und Projektkuratierung
seo-title: Kuratieren von Projekten und Virtual Report Suites im Analysis Workspace
description: Hier erfahren Sie, wie Sie vrs-Komponenten und -projekte kuratieren.
seo-description: Kuratieren von VRS und Kuratieren von Projekten
translation-type: tm+mt
source-git-commit: 0b56838e966aaf4cfa5c2685dd8335adbbbf11a7

---


# VRS und Projektkuratierung

Wenn Sie Projekte oder Virtual Report Suites (VRSs) kuratieren, filtern Sie im Wesentlichen Komponenten heraus, sodass Ihre Zielgruppe nur die von Ihnen gewünschten Projekte/VRS-Komponenten (Abmessungen, Kennzahlen, Segmente, Datumsbereiche) sehen.

>[!Note]
>Komponentenberechtigungen sind der primäre Mechanismus für die Komponenten, die ein Benutzer sehen kann. Sie werden über die Admin Tools verwaltet. Kuratierung ist ein Sekundärfilter.

Ab sofort können Sie eine verbesserte Kuratierungserfahrung genießen. Hier finden Sie eine Übersicht darüber, was die Schaltfläche **[!UICONTROL Alle anzeigen]in verschiedenen Kuratierungserfahrungen und nach Berechtigungsstufe zusätzlich zu den bereits verfügbaren kuratierten Komponenten zeigt:**

| Kuratierungstyp | Admins | Projektinhaber ohne Administratorrechte | Ohne Administratorrechte |
|---|---|---|---|
| Kuratierte VRS | Alle nicht kuratierten VRS-Komponenten | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in kuratierte VRS | Alle nicht kuratierten Komponenten, aufgeführt unter **[UICONTROL nicht ausgewählte Projektkomponenten]** und **[UICONTROL nicht kuratierte VRS-Komponenten]** | Alle nicht kuratierten und nicht kuratierten VRS-Komponenten, die diese Rolle besitzt oder die für sie freigegeben wurden | Nicht kuratierte VRS- und Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |

>[!IMPORTANT]
>Die VRS-Kuration wird immer vor der Projektkuratierung angewendet. Auch wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, werden sie herausgefiltert, wenn sie die kuratierten VRS nicht enthalten.
