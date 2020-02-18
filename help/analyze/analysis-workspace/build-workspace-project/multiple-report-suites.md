---
title: Mehrere Report Suites in Workspace
description: Erfahren Sie, wie und warum Sie in Workspace Projekte mit mehreren Report Suites erstellen.
translation-type: tm+mt
source-git-commit: 1a08003170ba07a722927e935ecda26e1d189235

---


# Mehrere Report Suites in Workspace

>[!IMPORTANT]
>Mehrere Report Suites in Workspace befinden sich derzeit in einer eingeschränkten Version.

Sie können jetzt im Arbeitsbereich für Analysen Projekte mit Daten aus mehr als einer Report Suite erstellen. Report Suites werden jetzt auf Bereichsebene ausgewählt, sodass Sie für jeden Bereich innerhalb desselben Workspace-Projekts eine andere Report Suite auswählen können.

Diese Funktion ist beispielsweise hilfreich, wenn Sie

* Vergleichen Sie Daten aus zwei verschiedenen Regionen, und die Daten befinden sich in zwei verschiedenen Report Suites. Sie können Tabellen und Visualisierungen erstellen, um die Daten nebeneinander zu vergleichen.

* Erstellen Sie ein Dashboard mit Metriken und Visualisierungen, um Berichte an andere Organisationen zu senden. Sie können jetzt Daten aus verschiedenen Report Suites in dasselbe Projekt ziehen.

## Aktives Bedienfeld

Mit dieser Funktion stellen wir das Konzept des &quot;aktiven Panels&quot; gegen &quot;inaktiver Panel&quot; vor. Sie können das aktive Bedienfeld am hellblauen Rand erkennen. Durch einfaches Klicken in ein Bedienfeld wird dieses Bedienfeld zum aktiven Bedienfeld.

>[!IMPORTANT]
>Sie können per Drag &amp; Drop in ein beliebiges Bedienfeld ziehen, das sich in derselben Report Suite wie das aktive Bedienfeld befindet. Durch Ziehen in einen inaktiven Bereich derselben Report Suite wird das Bedienfeld aktiv.

| Aufgabe | Aktives Bedienfeld | Inaktives Bedienfeld |
|---|---|---|
| Report Suite ändern | Ja | Nein |
| Komponenten ziehen und ablegen | Ja | Jafür alle Bereiche, die sich in derselben Report Suite wie Ihr aktiver Bereich befinden. |
| Visualisierungen per Drag &amp; Drop | Ja | Jafür alle Bereiche, die sich in derselben Report Suite wie Ihr aktiver Bereich befinden. |

## Arbeiten mit mehreren Report Suites

![](assets/mrs-ui.png)

1. Erstellen Sie ein neues Projekt mit zwei oder mehr Bereichen in Workspace.

1. Ziehen Sie Komponenten (Metriken, Dimensionen, Segmente, Datumsbereiche) per Drag &amp; Drop in den Bereich. Stellen Sie sicher, dass Bedienfelder über Daten und Visualisierungen verfügen, die für ihre Report Suite spezifisch sind.


   >[!NOTE]
   >Manchmal wird beim Laden eines Projekts (oder beim Wechsel zu einer Report Suite) ein Banner angezeigt, bei dem nicht alle im Projekt enthaltenen Komponenten in der Report Suite enthalten sind. Die fehlenden Komponenten werden aufgelistet. Befolgen Sie [diese Anweisungen](/help/admin/admin-console/permissions/product-profile.md) , um Berechtigungen für die erforderlichen Metriken/Dimensionen festzulegen.

   ![](assets/incompat-rs.png)

   Sie haben 3 Optionen, um mit dieser Inkompatibilität umzugehen:
   * Erforderliche Dimensionen/Metriken aktivieren
   * Report Suite ändern.
   * Fahren Sie mit einigen fehlenden Komponenten fort. Dies führt zu keinen Daten für diese Komponenten und/oder zu leeren Visualisierungen.

1. Ändern Sie das Bedienfeld in eine andere Report Suite und beachten Sie, wie die Komponentenbeschriftung (derzeit aktive Report Suite) und die aufgelisteten Komponenten basierend auf der neuen Report Suite aktualisiert werden.

1. Verwenden Sie einen Tastaturbefehl (`shift` während Sie ziehen), um einen inaktiven Bereich in einen aktiven Bereich umzuwandeln.

1. (Optional) Sie können auch andere Analytics-Komponenten-Builder aufrufen und sicherstellen, dass ihnen nun eine Report Suite-Bezeichnung angezeigt wird, die

   * Wo ein Segment erstellt wird: [Segmentaufbau](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html).
   * Wo eine berechnete Metrik erstellt wird: Aufbau [berechneter Metriken](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).
   * Wenn eine Warnung erstellt wird: [Warnhinweiserstellung](https://docs.adobe.com/content/help/en/analytics/components/alerts/alert-builder.html).