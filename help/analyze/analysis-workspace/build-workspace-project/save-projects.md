---
description: Erfahren Sie mehr über die verschiedenen Speicheroptionen, einschließlich automatisches Speichern, Speichern unter und Speichern als Vorlage.
title: Projekte speichern
feature: Grundlagen zu Workspace
role: Business Practitioner, Administrator
exl-id: e8206956-6e24-4a3a-8c3f-8acf1fb9d800
translation-type: tm+mt
source-git-commit: b199eb9b5eea1a6a0f336dbc0898114102f58348
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 69%

---

# Projekte speichern

Um Ihre Änderungen an einem Projekt zu speichern, gehen Sie zum Menü **[!UICONTROL Projekt]** in Workspace. Darüber hinaus speichert Adobe in bestimmten Fällen Projekte automatisch.

## Projektoptionen speichern {#Save}

Es gibt verschiedene Speicheraktionen, die Sie im Menü **[!UICONTROL Projekt]** ausführen können, je nachdem, wie Sie in Zukunft auf Ihre Analyse zugreifen möchten.

| Aktion | Beschreibung |
|---|---| 
| **[!UICONTROL Speichern]** | Speichern Sie die Änderungen an Ihrem Projekt. Wenn das Projekt freigegeben ist, sehen auch die Empfänger des Projekts die Änderungen. Wenn Sie das Projekt zum ersten Mal speichern, werden Sie aufgefordert, dem Projekt einen Namen, eine (optionale) Beschreibung und (optionale) Tags hinzuzufügen. |
| **[!UICONTROL Mit Hinweisen speichern]** | Bevor Sie das Projekt speichern, fügen Sie Notizen zu den Änderungen im Projekt hinzu. Notizen werden mit der Projektversion gespeichert und stehen allen Redakteuren unter Projekt > Vorige Version öffnen zur Verfügung. |
| **[!UICONTROL Speichern unter]** | Erstellen Sie ein Duplikat Ihres Projekts. Das ursprüngliche Projekt bleibt davon unberührt. |
| **[!UICONTROL Als Vorlage speichern]** | Speichern Sie Ihr Projekt als [benutzerdefinierte Vorlage](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html), die für Ihr Unternehmen unter **[!UICONTROL Projekt > Neu]** zur Verfügung steht. |

![](assets/save-project.png)

## Automatisches Speichern {#Autosave}

Bestehende Projekte, d.h. Projekte, die bereits mindestens einmal gespeichert wurden, werden alle zwei Minuten automatisch auf Ihrem lokalen Rechner gespeichert. Neue Projekte, die noch nie gespeichert wurden, werden derzeit nicht automatisch gespeichert.

Es gibt einige Szenarien, in denen Sie nicht gespeicherte Änderungen an einem Projekt verlassen können, was zu verschiedenen verfügbaren Aktionen führt.

### Öffnen eines anderen Workspace-Projekts

Adobe bietet die Möglichkeit, vor dem Verlassen der Seite zu speichern. Nach dem Verlassen eines bestehenden Projekts wird die automatisch gespeicherte lokale Kopie gelöscht.

![](assets/existing-save.png)

### Verlassen oder Schließen einer Registerkarte

Der Browser warnt, dass nicht gespeicherte Änderungen verloren gehen. Sie können entscheiden, ob Sie die Registerkarte verlassen oder abbrechen möchten.

![](assets/browser-image.png)

### Browser-Abstürze oder Zeitüberschreitung der Sitzung

Bei **bestehenden** Projekten wird dem Benutzer nach der Rückkehr zu Workspace ein Modal zur **Projektwiederherstellung** angezeigt. Durch Auswahl von „Ja“ wird das Projekt von der automatisch gespeicherten lokalen Kopie wiederhergestellt. „Nein“ löscht die automatisch gespeicherte lokale Kopie und öffnet die letzte vom Benutzer gespeicherte Version des Projekts.

![](assets/project-recovery.png)

Bei **neuen** Projekten, die noch nie gespeichert wurden, können nicht gespeicherte Änderungen nicht wiederhergestellt werden.

## Vorherige Version öffnen {#previous-version}

>[!NOTE]
>
>Frühere Projektversionen sind derzeit in begrenztem Umfang verfügbar.

So öffnen Sie eine frühere Version eines Projekts:

1. Gehen Sie zu **[!UICONTROL Projekt]** > **[!UICONTROL Frühere Version öffnen]**
1. Überprüfen Sie die Liste der vorherigen verfügbaren Versionen.
   [!UICONTROL Es werden ] Timestampand   Editorare angezeigt, zusätzlich zu   Notesif, wenn sie beim Speichern des   Editors hinzugefügt wurden. Versionen ohne Notizen werden 90 Tage lang gespeichert. Versionen mit Notizen werden für 1 Jahr gespeichert.
1. Wählen Sie eine frühere Version und klicken Sie auf **[!UICONTROL Laden]**.
Die vorherige Version wird dann mit einer Benachrichtigung geladen. Die vorherige Version wird erst dann zur aktuellen gespeicherten Version Ihres Projekts, wenn Sie auf **[!UICONTROL Speichern]** klicken. Wenn Sie von der geladenen Version weg navigieren, sehen Sie bei der Rückkehr die letzte gespeicherte Version des Projekts.
