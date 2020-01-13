---
title: VRS und Projektkuratierung
description: Hier erfahren Sie, wie Sie vrs-Komponenten und -Projekte kuratieren.
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# VRS und Projektkuratierung

Wenn Sie Projekte oder Virtual Report Suites (VRSs) kuratieren, filtern Sie im Wesentlichen Komponenten heraus, sodass Ihre Zielgruppe nur die von Ihnen gewünschten Projekte/VRS-Komponenten (Abmessungen, Kennzahlen, Segmente, Datumsbereiche) sehen.

>[!Note]
>Komponentenberechtigungen bestimmen als Hauptmechanismen, welche Komponenten ein Anwender sehen kann. Sie werden durch Admin Tools verwaltet. Kuratierung ist ein Sekundärfilter.

Ab sofort können Sie eine verbesserte Kuratierungserfahrung genießen. Hier finden Sie eine Übersicht darüber, was die Schaltfläche **[!UICONTROL Alle anzeigen]** in verschiedenen Kuratierungserfahrungen und nach Berechtigungsstufe zusätzlich zu den bereits verfügbaren kuratierten Komponenten zeigt:

| Kuratierungstyp | Admins | Projektinhaber ohne Administratorrechte | Ohne Administratorrechte |
|---|---|---|---|
| Kuratierte VRS | Alle nicht kuratierten VRS-Komponenten | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in kuratierte VRS | Alle nicht kuratierten Komponenten, aufgeführt unter **[Nicht kuratierte Projektkomponenten]** und **[nicht kuratierte VRS-Komponenten von UICONTROL]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten VRS-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte VRS- und Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |

>[!IMPORTANT]
>VRS-Kuratierung wird immer vor der Projektkuratierung angewandt. Wenn Ihr kuratiertes Projekt bestimmte Komponenten umfasst, werden diese also herausgefiltert, wenn das kuratierte VRS diese nicht enthält.
