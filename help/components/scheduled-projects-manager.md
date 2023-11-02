---
description: Anzeigen und Verwalten von terminierten Berichten in der gesamten Organisation.
title: Manager für geplante Projekte
feature: Admin Tools
exl-id: 8bc8d983-f680-48fa-8483-694c87a9ae4c
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---

# Geplante Projekte

Geplante Analysis Workspace-Projekte können unter **Analytics > Komponenten > Geplante Projekte** verwaltet werden.

Wenn Sie geplante Projekte verwalten, können Sie Zeitpläne von wiederkehrenden Projekten bearbeiten und löschen:

* Dateityp ändern (CSV oder PDF)
* Projektbeschreibung aktualisieren
* Empfängerinnen und Empfänger hinzufügen oder entfernen
* Häufigkeit ändern

Um ein geplantes Projekt zu ändern:

1. Wählen Sie **Analytics > Komponenten > Geplante Projekte** aus.
1. Suchen Sie in der Suchleiste oder mithilfe der Filteroptionen in der linken Leiste nach einem Zeitplan. Sie können nach [!UICONTROL Tags], [!UICONTROL Inhabenden], [!UICONTROL Favoriten] usw. filtern.

![Screenshot mit der Liste der geplanten Projekte, in der die Spalten „Titel“, „Inhaberin bzw. Inhaber“, „Tags“, „Zugestellt an“ und andere Spalten zu sehen sind, die im Abschnitt „Verfügbare Spalten“ beschrieben werden.](assets/scheduled-project-manager2.png)

## Verfügbare Spalten

| Feld | Beschreibung |
| --- | --- |
| [!UICONTROL Favoriten] | Wenn Sie das Sternsymbol auswählen, wird dieser Zeitplan zu einem Favoriten. |
| [!UICONTROL Zeitplan-ID] | Diese ID wird hauptsächlich zum Debugging verwendet. |
| [!UICONTROL Titel und Beschreibung] | Titel und Beschreibung dieses Projekts. |
| [!UICONTROL Inhabende] | Die Person, die das Projekt erstellt hat und dafür verantwortlich ist. |
| [!UICONTROL Tags] | (Optional) Mit Tagging können Projekte praktisch organisiert werden. Alle Benutzer können Tags erstellen und eines oder mehrere Tags auf ein Projekt anwenden. Sie sehen Tags jedoch nur für die Projekte, deren Verantwortlicher Sie sind oder die für Sie freigegeben wurden. |
| [!UICONTROL Gesendet an] | Die Empfängerinnen bzw. Empfänger dieses geplanten Projekts. |
| [!UICONTROL Ablaufdatum] | Für die Häufigkeit eines geplanten Projekts können Sie das Ablaufdatum für bis zu einem Jahr in der Zukunft festlegen. |
| [!UICONTROL Häufigkeit] | Wie oft Sie dieses geplante Projekt an die Empfängerinnen bzw. Empfänger senden möchten. |
| [!UICONTROL Durchführungszeit] | Zu welcher Tageszeit dieses geplante Projekt gesendet wird.  |
| [!UICONTROL Anzahl der Abfragen] | Die Anzahl der Abfragen für dieses Projekt. |

## Allgemeine Aktionen

Die folgenden Aktionen werden im Manager für geplante Projekte häufig ausgeführt:

| Aktion | Beschreibung |
|---|---|
| **[!UICONTROL Bearbeiten]** | Klicken Sie auf den Titel des Zeitplans, um seine Versandeinstellungen zu aktualisieren. |
| **[!UICONTROL Löschen]** | Wählen Sie das geplante Projekt in der Liste aus und klicken Sie dann im Menü auf „Löschen“. Dadurch wird der ausgewählte Zeitplan für das Projekt gelöscht. Das Projekt selbst wird nicht gelöscht. |
| **[!UICONTROL Tag]** | Wählen Sie das geplante Projekt in der Liste aus und wählen Sie dann „Taggen“ oder „Genehmigen“ aus, um Ihre Zeitpläne zu organisieren und die Suche zu vereinfachen. |
| **[!UICONTROL Fehlgeschlagene Zeitpläne anzeigen]** | Navigieren Sie zur linken Leiste > „Andere Filter“ > „Fehlgeschlagen“, um Zeitpläne anzuzeigen, die fehlgeschlagen sind. |
| **[!UICONTROL Abgelaufene Zeitpläne anzeigen]** | Navigieren Sie zur linken Leiste > „Andere Filter“ > „Abgelaufen“, um Zeitpläne anzuzeigen, die abgelaufen sind. Klicken Sie auf den Titel des Zeitplans, um einen neuen Versandplan einzurichten. |
| **[!UICONTROL Zeitplan-ID anzeigen]** | Navigieren Sie oben rechts zu den Spaltenoptionen und fügen Sie der Tabelle die Spalte „Zeitplan-ID“ hinzu. Die Zeitplan-ID ist oft zum Debugging nützlich. |

Im Manager für geplante Projekte werden die Elemente angezeigt, die von einer bestimmten Benutzerin bzw. einem bestimmten Benutzer erstellt wurden. Wenn das Benutzerkonto in der Anwendung deaktiviert wird, werden alle geplanten Bereitstellungen gestoppt. Die Inhaberschaft eines geplanten Projekts kann unter **Admin** > **Analytics-Benutzende und -Assets** > **Assets übertragen** übertragen werden.
