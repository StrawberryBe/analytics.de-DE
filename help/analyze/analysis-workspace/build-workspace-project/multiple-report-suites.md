---
title: 'Mehrere Report Suites in Workspace '
description: Erfahren Sie, wie und warum Sie in Workspace Projekte mit mehreren Report Suites erstellen
translation-type: tm+mt
source-git-commit: 03ab0edc60f4e858acd98f14390d058387af67fa

---


# Mehrere Report Suites in Workspace 

Sie können jetzt in Analysis Workspace Projekte mit Daten aus mehr als einer Report Suite erstellen. Report Suites werden jetzt auf Bedienfeldebene ausgewählt, sodass Sie für jedes Bedienfeld innerhalb desselben Workspace-Projekts eine andere Report Suite auswählen können.

Diese Funktion ist beispielsweise hilfreich, wenn Sie:

* Daten aus zwei verschiedenen Regionen vergleichen und sich die Daten in zwei verschiedenen Report Suites befinden. Sie können Tabellen und Visualisierungen erstellen, um die Daten nebeneinander zu vergleichen.

* ein Dashboard mit Metriken und Visualisierungen erstellen, um Berichte an andere Organisationen zu senden. Sie können jetzt Daten aus verschiedenen Report Suites in dasselbe Projekt ziehen.

## Report Suite auf alle Bereiche anwenden

Sie können eine Report Suite auf alle Bereiche gleichzeitig anwenden, indem Sie mit der rechten Maustaste auf eine beliebige Bereichsüberschrift klicken und **[!UICONTROL Apply Report Suite to All Panels]** diese auswählen.

![](assets/apply-rs-all-panels.png)

## Aktives Bedienfeld

Mit dieser Funktion führen wir das Konzept des „aktiven Bedienfelds“ im Vergleich zum „interaktiven Bedienfeld“ ein. Sie können das aktive Bedienfeld am hellblauen Rand erkennen. Durch einfaches Klicken in ein Bedienfeld wird dieses Bedienfeld zum aktiven Bedienfeld.

>[!IMPORTANT]
>Sie können per Drag &amp; Drop in ein beliebiges Bedienfeld ziehen, das sich in derselben Report Suite wie das aktive Bedienfeld befindet. Durch Ziehen in einen inaktiven Bereich derselben Report Suite wird das Bedienfeld aktiv.

| Aufgabe | Aktives Bedienfeld | Inaktives Bedienfeld |
|---|---|---|
| Report Suite ändern | Ja | Nein |
| Komponenten per Drag &amp; Drop verschieben | Ja | Ja, für alle Bereiche, die sich in derselben Report Suite wie Ihr aktiver Bereich befinden. |
| Visualisierungen per Drag &amp; Drop verschieben | Ja | Ja, für alle Bereiche, die sich in derselben Report Suite wie Ihr aktiver Bereich befinden. |

## Arbeiten mit mehreren Report Suites

![](assets/mrs-ui.png)

1. Erstellen Sie ein neues Projekt mit zwei oder mehr Bedienfeldern im Workspace.

1. Verschieben Sie Komponenten (Metriken, Dimensionen, Segmente, Datumsbereiche) per Drag &amp; Drop in den Bereich. Stellen Sie sicher, dass Bedienfelder über Daten und Visualisierungen verfügen, die für ihre Report Suite spezifisch sind.


   >[!NOTE]
   >Manchmal wird beim Laden eines Projekts (oder beim Wechsel zu einer Report Suite) ein Banner angezeigt, bei dem nicht alle im Projekt enthaltenen Komponenten in der Report Suite enthalten sind. Die fehlenden Komponenten werden aufgelistet. Befolgen Sie [diese Anweisungen](/help/admin/admin-console/permissions/product-profile.md), um Berechtigungen für die erforderlichen Metriken/Dimensionen festzulegen.

   ![](assets/incompat-rs.png)

   Sie haben 3 Optionen, um mit dieser Inkompatibilität umzugehen:
   * Erforderliche Dimensionen/Metriken aktivieren
   * Ändern Sie die Report Suite.
   * Fahren Sie mit einigen fehlenden Komponenten fort. Dies führt dazu, dass für diese Komponenten keine Daten verfügbar sind und/oder zu leeren Visualisierungen.

1. Wechseln Sie die Report Suite für das Bedienfeld und beachten Sie, wie die Bezeichnung der Komponente (derzeit aktive Report Suite) und die aufgelisteten Komponenten basierend auf der neuen Report Suite aktualisiert werden.

1. Use a keyboard shortcut (`shift` while dragging) to turn an inactive panel to an active panel.

1. (Optional) Sie können auch andere Komponenten-Builder in Analytics aufrufen und sicherstellen, dass ihnen nun eine Report Suite-Bezeichnung angezeigt wird, die angibt

   * wo ein Segment erstellt wird: [Segment Builder](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-build.html).
   * wo eine berechnete Metrik erstellt wird: [Generator für berechnete Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).
   * wo eine Warnung erstellt wird: [Warnhinweiserstellung](https://docs.adobe.com/content/help/de-DE/analytics/components/alerts/alert-builder.html).