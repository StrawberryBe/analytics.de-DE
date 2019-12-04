---
title: Mehrere Report Suites in Workspace
description: Erfahren Sie, wie und warum Sie in Workspace Projekte mit mehreren Report Suites erstellen.
translation-type: tm+mt
source-git-commit: 7f79d5c041959e4093b2aaacb64c948b0593262f

---


# Mehrere Report Suites in Workspace

>[!IMPORTANT]
>Diese Funktion befindet sich derzeit im Beta-Test und wird Anfang 2020 veröffentlicht.

Sie können jetzt im Arbeitsbereich für Analysen Projekte mit Daten aus mehr als einer Report Suite erstellen. Report Suites werden jetzt auf Bereichsebene ausgewählt, sodass Sie für jeden Bereich innerhalb desselben Workspace-Projekts eine andere Report Suite auswählen können.

Diese Funktion ist beispielsweise hilfreich, wenn Sie

* Vergleichen Sie Daten aus zwei verschiedenen Regionen, und die Daten befinden sich in zwei verschiedenen Report Suites. Sie können Tabellen und Visualisierungen erstellen, um die Daten nebeneinander zu vergleichen.

* Erstellen Sie ein Dashboard mit Metriken und Visualisierungen, um Berichte an andere Organisationen zu senden. Sie können jetzt Daten aus verschiedenen Report Suites in dasselbe Projekt ziehen.

## Aktives Bedienfeld

Mit dieser Funktion stellen wir das Konzept des "aktiven Panels" gegen "inaktiver Panel" vor. Die aktive Leiste wird durch den hellblauen Rand um sie herum erkennbar. Wenn Sie einfach in einen Bereich klicken, wird dieser Bereich zum aktiven Bereich.

>[!IMPORTANT]
>Sie können Komponenten **nur in das aktive Bedienfeld** ziehen und dort ablegen, auch wenn andere Bedienfelder dieselbe Report Suite haben. Wenn Sie das Bedienfeld beim Ziehen und Ablegen ändern möchten, können Sie einen Kurzschnitt verwenden: Drücken Sie `shift` beim Ziehen die Taste, um einen inaktiven Bereich in einen aktiven Bereich zu ändern.

| Aufgabe | Aktives Bedienfeld | Inaktives Bedienfeld |
|---|---|---|
| Report Suite ändern | Ja | Nein |
| Komponenten ziehen und ablegen | Ja | Nein |
| Visualisierungen per Drag &amp; Drop | Ja | Nein |

## Arbeiten mit mehreren Report Suites

![](assets/mrs-ui.png)

1. Erstellen Sie ein neues Projekt mit zwei oder mehr Bereichen in Workspace.

1. Ziehen Sie Komponenten (Metriken, Dimensionen, Segmente, Datumsbereiche) per Drag &amp; Drop in den Bereich. Stellen Sie sicher, dass Bedienfelder über Daten und Visualisierungen verfügen, die für ihre Report Suite spezifisch sind.


   >[!NOTE]
   >Manchmal wird beim Laden eines Projekts (oder beim Wechsel zu einer Report Suite) die Meldung "Inkompatible Report Suite"angezeigt, wenn nicht alle im Projekt enthaltenen Komponenten in der Report Suite enthalten sind. Die fehlenden Komponenten werden aufgelistet. Befolgen Sie [diese Anweisungen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html#createproductprofiles) , um Berechtigungen für die erforderlichen Metriken/Dimensionen festzulegen.

   ![](assets/incompat-rs.png)

   1. Sie haben 3 Optionen, um mit dieser Inkompatibilität umzugehen:
   * Fahren Sie mit einigen fehlenden Komponenten fort.
   * Rückgängig.
   * Report Suite ändern.

1. Ändern Sie das Bedienfeld in eine andere Report Suite und beachten Sie, wie die Komponentenbeschriftung (derzeit aktive Report Suite) und die aufgelisteten Komponenten basierend auf der neuen Report Suite aktualisiert werden.

1. Verwenden Sie den Tastaturbefehl (`shift` während Sie ziehen), um einen inaktiven Bereich in einen aktiven Bereich umzuwandeln.

1. (Optional) Sie können auch andere Analytics-Komponenten-Builder aufrufen und sicherstellen, dass ihnen nun eine Report Suite-Bezeichnung angezeigt wird, die

   * Wo ein Segment erstellt wird (Segmentaufbau).
   * Wo eine berechnete Metrik erstellt wird (Generator für berechnete Metriken).
   * Wo eine Warnung erstellt wird (Warnhinweiserstellung).