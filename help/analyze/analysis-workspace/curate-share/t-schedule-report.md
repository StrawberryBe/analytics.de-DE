---
description: Versenden Sie ein Projekt aus Analysis Workspace per E-Mail oder planen Sie die Bereitstellung.
keywords: Analysis Workspace
title: Planen von Projekten
feature: Curate and Share
role: User, Admin
exl-id: 2d6854f7-8954-4d55-b2be-25981cfb348b
source-git-commit: bf9f04ce6ff057ca66bcf0d9cf66540cea160444
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 88%

---

# Planen von Projekten

Über das Menü **Freigeben** in Workspace können Sie Analysis Workspace-Projekte per E-Mail an ausgewählte Empfänger senden. Dateien können im CSV- oder PDF-Format gesendet werden.

## Datei jetzt senden

So senden Sie eine Datei sofort per E-Mail an die Empfänger:

1. Klicken **[!UICONTROL Freigeben] > [!UICONTROL Datei jetzt senden]**.
1. Geben Sie den Dateityp an (CSV oder PDF).
1. (Optional) Fuegen Sie eine Beschreibung hinzu, die in der E-Mail enthalten sein wird, um die empfangene Datei zu erklären.
1. Fügen Sie Empfänger oder Gruppen hinzu. E-Mail-Adressen können auch eingegeben werden.
1. Klicken Sie auf **[!UICONTROL Jetzt senden]**.
1. (Optional) Klicken Sie auf **[!UICONTROL Planungsoptionen anzeigen]**, um einen Zeitplan für den Versand festzulegen.

![Datei jetzt senden](assets/send-file-now.png)

## Datei planmäßig senden

So senden Sie eine Datei basierend auf einem wiederkehrenden Zeitplan per E-Mail an die Empfänger:

1. Klicken **[!UICONTROL Freigeben] > [!UICONTROL Datei planmäßig senden]**.
1. Geben Sie den Dateityp an (CSV oder PDF).
1. (Optional) Fuegen Sie eine Beschreibung hinzu, die in der E-Mail enthalten sein wird, um die empfangene Datei zu erklären.
1. Fügen Sie Empfänger oder Gruppen hinzu. E-Mail-Adressen können auch eingegeben werden.
1. Geben Sie den Datumsbereich an, über den anhand des Zeitplans gesendet werden soll, indem Sie die Einstellungen „Start am“ und „Ende am“ ändern. Das Enddatum muss innerhalb eines Jahres ab dem Tag liegen, an dem der Zeitplan erstellt oder geändert wurde.
1. Geben Sie die Versandhäufigkeit an. Jede Häufigkeit ermöglicht unterschiedliche Anpassungen.
1. Klicken Sie auf **[!UICONTROL Planmäßig senden]**.

![](assets/send-on-schedule.png)

## Manager für geplante Projekte

Geplante Analysis Workspace-Projekte können unter **Analytics > Komponenten > Geplante Projekte** verwaltet werden.

Im Manager für geplante Projekte können wiederkehrende Projektzeitpläne bearbeitet und gelöscht werden. Suchen Sie in der Suchleiste oder mithilfe der Filteroptionen in der linken Leiste nach einem Zeitplan. Sie können nach Tag, genehmigten Zeitplänen, Inhabern und mehr filtern.

![](assets/scheduled-project-manager2.png)

| Feld | Beschreibung |
| --- | --- |
| [!UICONTROL Favoriten] | Wenn Sie das Sternsymbol auswählen, wird dieser Zeitplan zu einem Favoriten. |
| [!UICONTROL Zeitplan-ID] | Diese ID wird hauptsächlich zum Debugging verwendet. |
| [!UICONTROL Titel und Beschreibung] | Titel und Beschreibung dieses Projekts. |
| [!UICONTROL Inhaber] | Die Person, die das Projekt erstellt hat und dafür verantwortlich ist. |
| [!UICONTROL Tags] | (Optional) Mit Tagging können Projekte praktisch organisiert werden. Alle Benutzer können Tags erstellen und eines oder mehrere Tags auf ein Projekt anwenden. Sie sehen Tags jedoch nur für die Projekte, deren Verantwortlicher Sie sind oder die für Sie freigegeben wurden. |
| [!UICONTROL Gesendet an] | Der/die Empfänger dieses geplanten Projekts. |
| [!UICONTROL Ablaufdatum] | Das standardmäßige Ablaufdatum hängt von der Häufigkeit des Zeitplans ab. Siehe &quot;Ablaufdaten für geplante Projekte&quot;unten. |
| [!UICONTROL Häufigkeit] | Wie oft Sie dieses geplante Projekt an den/die Empfänger senden möchten. |
| [!UICONTROL Durchführungszeit] | Zu welcher Tageszeit dieses geplante Projekt gesendet wird.  |
| [!UICONTROL Anzahl der Abfragen] | Die Anzahl der Abfragen für dieses Projekt. |

## Allgemeine Aktionen

Die folgenden Aktionen werden im Manager für geplante Projekte häufig ausgeführt:

| Aktion | Beschreibung |
|---|---|
| **[!UICONTROL Zeitplan bearbeiten]** | Klicken Sie auf den Titel des Zeitplans, um seine Versandeinstellungen zu aktualisieren. |
| **[!UICONTROL Zeitplan löschen]** | Wählen Sie das geplante Projekt in der Liste aus und klicken Sie dann im Menü auf „Löschen“. Dadurch wird der ausgewählte Zeitplan für das Projekt gelöscht. Das Projekt selbst wird nicht gelöscht. |
| **[!UICONTROL Tags hinzufügen]** | Wählen Sie das geplante Projekt in der Liste aus und wählen Sie dann „Taggen“ oder „Genehmigen“ aus, um Ihre Zeitpläne zu organisieren und die Suche zu vereinfachen. |
| **[!UICONTROL Fehlgeschlagene Zeitpläne anzeigen]** | Navigieren Sie zur linken Leiste > „Andere Filter“ > „Fehlgeschlagen“, um Zeitpläne anzuzeigen, die fehlgeschlagen sind. |
| **[!UICONTROL Abgelaufene Zeitpläne anzeigen]** | Navigieren Sie zur linken Leiste > „Andere Filter“ > „Abgelaufen“, um Zeitpläne anzuzeigen, die abgelaufen sind. Klicken Sie auf den Titel des Zeitplans, um einen neuen Versandzeitplan einzurichten. |
| **[!UICONTROL Zeitplan-ID anzeigen]** | Navigieren Sie oben rechts zu den Spaltenoptionen und fügen Sie der Tabelle die Spalte „Zeitplan-ID“ hinzu. Die Zeitplan-ID ist oft zum Debugging nützlich. |

Im Manager für geplante Projekte werden die Elemente angezeigt, die von einem bestimmten Benutzer erstellt wurden. Wenn das Benutzerkonto in der Anwendung deaktiviert wird, werden alle geplanten Bereitstellungen gestoppt. Die Eigentuemerschaft eines geplanten Projekts kann unter **Admin > Analytics-Benutzer und -Assets > Assets übertragen** **übertragen** werden.

## Ablaufdaten für geplante Projekte

Die Ablaufdaten für geplante Projekte hängen von der geplanten Versandhäufigkeit ab:

* Stündliche Sendungen laufen in einer Woche ab.
* Die täglichen Sendungen laufen in einem Monat ab.
* Wöchentliche Sendungen laufen in 6 Monaten ab.
* Die monatlichen/jährlichen Sendungen laufen in einem Jahr ab.
