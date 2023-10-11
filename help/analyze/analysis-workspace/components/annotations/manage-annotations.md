---
title: Verwalten von Anmerkungen
description: Verwalten von Anmerkungen in Workspace.
role: User, Admin
feature: Annotations
exl-id: 37a538cc-9ea7-4cb1-8ee8-e8e474ad5b08
source-git-commit: 4f0bd39b64535be8ba55e97d65177f6ef291ef6c
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 61%

---

# Verwalten von Anmerkungen

Die [!UICONTROL Anmerkungs-Manager] zeigt Ihnen alle Anmerkungen an, die Ihnen gehören oder die für Sie freigegeben wurden. Projektspezifische Anmerkungen werden hier nicht angezeigt. Sie können diese Benutzeroberfläche verwenden, um Ihre Anmerkungen freizugeben, zu filtern, zu taggen, zu kopieren, zu löschen und zu favorisieren. Administratoren können Anmerkungen verwalten und genehmigen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Anmerkungen]**

## Benutzeroberfläche der Anmerkungsverwaltung

![](assets/annotation-mgr.png)

| UI-Element | Beschreibung |
| --- | --- | 
| [!UICONTROL Titel und Beschreibung] | Werden durch den Anmerkungsgenerator bereitgestellt. Klicken Sie auf den Titel-Link, um den Titel und die Beschreibung zu bearbeiten. Dadurch gelangen Sie zurück zum Anmerkungsgenerator. |
| [!UICONTROL Report Suite] | Die Report Suites, für die diese Anmerkung gilt. |
| [!UICONTROL Inhaber] | Zeigt an, wer Inhaber der Anmerkung ist. Wenn Sie kein Administrator sind, können Sie nur Anmerkungen sehen, deren Inhaber Sie sind, sowie Anmerkungen, die für Sie freigegeben wurden. |
| [!UICONTROL Angewendeter Datumsbereich] | Das Datum oder der Datumsbereich, für das bzw. den diese Anmerkung gilt. |
| [!UICONTROL Freigegeben für] | Listet auf, für wie viele Einzelpersonen oder Gruppen Sie die Anmerkung freigegeben haben. Klicken Sie hier, um weitere Details anzuzeigen. |
| [!UICONTROL Änderungsdatum] | Zeigt das Datum und die Uhrzeit der letzten Änderung der Anmerkung an. |

{style="table-layout:auto"}

## Bearbeiten von Anmerkungen

Die Bearbeitung einer Anmerkung bedeutet, dass Sie Datumsbereiche, Farben und den Umfang anpassen können oder ob diese für alle Report Suites oder Projekte gelten. Anmerkungen können auf zwei Arten bearbeitet werden:

* Bewegen Sie in einem Liniendiagramm den Mauszeiger über die Anmerkung und klicken Sie im Popover auf das Stiftsymbol.
* Klicken Sie in der [!UICONTROL Anmerkungsverwaltung] auf den Titel der Anmerkung.

Beide Optionen führen Sie zurück in den [!UICONTROL Anmerkungsgenerator]. Dort können Sie die erforderlichen Anpassungen vornehmen und die neue Version speichern.

## Freigeben von Anmerkungen

Beachten Sie Folgendes beim Freigeben von Anmerkungen oder Arbeiten mit Anmerkungen, die für Sie freigegeben wurden:

* Wenn Sie ein Projekt mit schreibgeschützten Anmerkungen erstellen und das Projekt dann für einen anderen Benutzer freigeben, können Anmerkungen von niemandem bearbeitet oder gelöscht werden, für den Sie das Projekt freigeben.
* Wenn Sie eine Anmerkung speichern und direkt für einen Benutzer freigeben, kann dieser die Anmerkung nur bearbeiten/löschen, wenn er über Administratorrechte verfügt.
* Wenn ein Projekt für Sie mit einer reinen projektbezogenen Anmerkung freigegeben wird, wird es nur in diesem Projekt angezeigt. Wenn die Anmerkung direkt für Sie freigegeben ist, wird sie in allen Projekten angezeigt, in denen diese Anmerkung angezeigt werden kann.

## Anmerkungen und Zeitzonen

Alle Anmerkungen werden mit einem Zeitstempel erstellt, jedoch ohne Stunden- oder Zeitzoneninformationen. Zum Zeitpunkt des Berichts wird immer die Zeitzone der Report Suite des Bedienfelds angewendet. Beispielsweise wird am 25. Dezember unabhängig von der Zeitzone der Report Suite, in der Sie sich befinden, eine Anmerkung für den Weihnachtstag erstellt.

## Sonstige Anmerkungsaufgaben

Mit der Anmerkungsverwaltung können Administratoren Anmerkungen bearbeiten, hinzufügen, taggen, löschen, umbenennen, genehmigen, kopieren, exportieren und filtern. Dies ist für Nicht-Admin-Benutzer nicht sichtbar.

Zusätzliche Optionen sind verfügbar, wenn Sie mindestens eine Anmerkung auswählen:

| Aufgabe | Beschreibung |
| --- | --- |
| [!UICONTROL Hinzufügen] | Sie gelangen zum Generator für Anmerkungen , in dem Sie Anmerkungen erstellen können. |
| [!UICONTROL Tag] | Alle Benutzer können Tags für Anmerkungen erstellen und ein oder mehrere Tags auf eine Anmerkung anwenden. Sie können Tags jedoch nur für Anmerkungen anzeigen, deren Inhaber Sie sind. |
| [!UICONTROL Löschen] | Durch das Löschen einer Anmerkung wird sie aus jedem Projekt in Ihrer Organisation entfernt. |
| [!UICONTROL Umbenennen] | Beim Umbenennen einer Anmerkung wird sie in allen Projekten umbenannt, auf die sie angewendet wurde. |
| [!UICONTROL Kopieren] | Erstellt eine eigenständige Kopie mit einer eigenen neuen Anmerkungs-ID, jedoch mit demselben Namen und derselben Definition. |
| [!UICONTROL In CSV exportieren] | Exportiert die Anmerkungsdefinition in eine CSV-Datei. |
| [!UICONTROL Filter] (linke Leiste) | Filtern Sie nach Tags, Report Suite, Inhabern und anderen Filtern („Meine“, „Genehmigt“, „Favoriten“, „Für mich freigegeben“ und „Alle anzeigen“). |

{style="table-layout:auto"}
