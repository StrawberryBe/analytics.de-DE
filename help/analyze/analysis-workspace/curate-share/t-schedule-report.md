---
description: Senden Sie ein Analysis Workspace-Projekt per E-Mail oder planen Sie es für den Versand.
keywords: Analysis Workspace
title: Geplante Projekte
topic: Reports and analytics
uuid: 9244d7b2-1b7e-4323-98ef-cf22de3b666a
translation-type: tm+mt
source-git-commit: 04b5c7af0ac0052d059bea86cae13aa7fb05fff3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 9%

---


# Geplante Projekte

Über das Menü &quot; **Freigeben&quot;in Workspace können Sie Analysis Workspace-Projekte per E-Mail an ausgewählte Empfänger senden**. Dateien können im CSV- oder PDF-Format gesendet werden.

## Datei jetzt senden

So senden Sie eine Datei sofort per E-Mail an Empfänger:

1. Click **Share > Send File Now**.
1. Geben Sie den Dateityp an (CSV oder PDF).
1. (Optional) Hinzufügen eine Beschreibung, die in der E-Mail enthalten ist, um die empfangene Datei zu erklären.
1. hinzufügen Empfänger oder Gruppen. E-Mail-Adressen können auch eingegeben werden.
1. Klicken Sie auf **Jetzt senden**.
1. (Optional) Click **Show scheduling options** to specify a delivery schedule.

## Datei planmäßig senden

To send a file on a recurring schedule to recipients via email:

1. Click **Share > Send File on Schedule**.
1. Specify the file type (CSV or PDF).
1. (Optional) Hinzufügen eine Beschreibung, die in der E-Mail enthalten ist, um die empfangene Datei zu erklären.
1. hinzufügen Empfänger oder Gruppen. E-Mail-Adressen können auch eingegeben werden.
1. Geben Sie den Bereich an, über den der Zeitplan bereitgestellt werden soll, indem Sie die Einstellungen &quot;Start am&quot;und &quot;Ende bei Eingabe&quot;ändern. Das Enddatum muss innerhalb eines Jahres ab dem Tag liegen, an dem der Plan erstellt oder geändert wird.
1. Geben Sie die Häufigkeit des Versands an. Jede Frequenz ermöglicht unterschiedliche Anpassungen.
1. Klicken Sie auf Planmäßig **senden**.

## Manager für geplante Projekte

Geplante Analysis Workspace-Projekte können unter **Analytics > Komponenten > Geplante Projekte** verwaltet werden.

In the Scheduled Projects Manager, you can edit and delete recurring project schedules. Suchen Sie nach einem Zeitplan in der Suchleiste oder mithilfe der Filteroptionen in der linken Leiste. Sie können nach Tag, genehmigten Zeitplänen, Inhabern und mehr filtern.

Im Manager für geplante Projekte werden häufig folgende Aktionen ausgeführt:

| Aktion | Beschreibung |
|---|---|
| **Zeitplan bearbeiten** | Klicken Sie auf den Titel des Zeitplans, um seine Versand-Einstellungen zu aktualisieren. |
| **Zeitplan löschen** | Wählen Sie das geplante Projekt in der Liste aus und klicken Sie dann im Menü auf Löschen. Dadurch wird der ausgewählte Zeitplan für das Projekt gelöscht. das Projekt selbst wird nicht gelöscht. |
| **hinzufügen** | Wählen Sie das geplante Projekt in der Liste aus und wählen Sie dann &quot;Taggen&quot;oder &quot;Genehmigen&quot;, um Ihre Zeitpläne zu organisieren und die Suche zu vereinfachen. |
| **Ansicht fehlgeschlagene Zeitpläne** | Navigate to the left rail > Other filters > Failed to see schedules that have failed. |
| **View expired schedules** | Navigate to the left rail > Other filters > Expired to see schedules that have expired. Click the title of the schedule to setup a new deliery schedule. |
| **View schedule ID** | Navigate to column options in the top right and add the Schedule ID column to the table. The scheduled ID is often useful for debugging. |

Im Manager für geplante Projekte werden die Elemente angezeigt, die von einem bestimmten Benutzer erstellt wurden. Wenn das Benutzerkonto in der Anwendung deaktiviert wird, werden alle geplanten Bereitstellungen gestoppt. Scheduled project ownership can be **transferred** to a new user under **Admin > Analytics Users &amp; Assets > Transfer Assets**.
