---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: 0e03379550808e5be3e86f0f9ddbbedd026d4910
workflow-type: tm+mt
source-wordcount: '1593'
ht-degree: 24%

---

# Berichtsaktivität im Reporting Activity Manager anzeigen

{{release-limited-testing}}

Die [!UICONTROL Reporting Activity Manager] ermöglicht es Administratoren, während Spitzenzeiten der Berichterstellung schnell Probleme mit der Berichtskapazität zu diagnostizieren und zu beheben.

Weitere Informationen zum Reporting Activity Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Übersicht über die Berichterstellung in Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Berichtsaktivität für alle Report Suites anzeigen {#view-all-report-suites}

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

   Eine Liste Ihrer aktivierten Basis-Report Suites wird angezeigt.

   ![Berichtswarteschlange](/help/admin/admin/assets/reporting-activity1.png)

1. (Optional) Sie können die Liste der Report Suites durchsuchen oder filtern:

   * Verwenden Sie das Suchfeld, um nach einer bestimmten Report Suite zu suchen. Geben Sie den Namen oder die ID der Report Suite ein und die Liste der Report Suites wird bei der Eingabe aktualisiert.

   * Wählen Sie die [!UICONTROL **Filter**] icon ![Filtersymbol](assets/filter-icon.png) um die Liste der Filteroptionen zu erweitern. Sie können nach [!UICONTROL **Favoriten**] oder [!UICONTROL **Status**].

     Um eine Report Suite als Favoriten zu markieren, wählen Sie das Sternsymbol links neben dem Report Suite-Namen aus.

<!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Zeigen Sie Nutzungsinformationen zu den einzelnen Report Suites an. Sie können eine Spaltenüberschrift auswählen, um die Tabelle nach dieser Spalte zu sortieren.

   Die folgenden Spalten sind verfügbar:

   | UI-Element | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität von Ihnen überwacht wird. |
   | **[!UICONTROL Virtual Report Suites]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites ermöglichen eine höhere Komplexität von Berichtsanfragen aufgrund zusätzlich anwendbarer Filter- und Segmentierungsebenen. Alle Anfragen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite.<p>Beispielsweise ergeben 10 Anfragen, die von 5 Virtual Report Suites kommen, 50 Anfragen auf Seiten der zugrunde liegenden Report Suite. Auf diese Weise können Sie sehr schnell die Kapazitätsgrenzen erreichen. |
   | **[!UICONTROL Kapazitätsauslastung]** | Der Prozentsatz der verwendeten Berichtskapazität der Report Suite in Echtzeit. <p>**Hinweis** Selbst eine Nutzungskapazität von 100 % bedeutet nicht unbedingt, dass Sie mit dem Abbrechen von Berichtsanfragen beginnen sollten. 100 % der Nutzkapazität können gesund sein, wenn die durchschnittliche Wartezeit vernünftig ist. Die 100-%-Nutzungskapazität könnte auf ein Problem hinweisen, wenn auch die Anzahl der Anforderungen in der Warteschlange wächst.</p> |
   | **[!UICONTROL Anfragen in der Warteschlange]** | Die Anzahl der zu verarbeitenden Anforderungen. <!-- ??? --> |
   | **[!UICONTROL Wartezeit in der Warteschlange]** | Die durchschnittliche Wartezeit für die Verarbeitung jeder Anfrage. <!-- ???? --> |
   | **[!UICONTROL Status]** | Folgende Status sind möglich: <ul><li>[!UICONTROL **Aktiv**] (blau): Berichte wurden für die Report Suite ausgeführt und werden auf Aktivität überwacht.</li><li>[!UICONTROL **Inaaktiv**] (grau): Für die Report Suite wurden bisher keine Berichte ausgeführt. Dieser Status wird nur angezeigt, wenn Report Suites zum ersten Mal erstellt werden.</li></ul> |

   {style="table-layout:auto"}

## Berichtsaktivität für eine einzelne Report Suite anzeigen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Reporting Activity Manager**].

1. Wählen Sie den verknüpften Titel der Report Suite aus, für die Sie Details anzeigen möchten.

   Berichtsaktivitätsdaten werden für die von Ihnen ausgewählte Report Suite angezeigt.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. Verwenden Sie die verfügbaren Diagramme und Tabellen, um die Berichtsaktivität in der Report Suite zu verstehen.

   * [Diagramme anzeigen](#view-graphs)

   * [Tabelle anzeigen](#view-data-in-the-table)

### Diagramme anzeigen

Die folgenden Diagramme helfen Ihnen dabei, die Aktivitäten in der Report Suite besser zu verstehen. Wenn keine Diagramme sichtbar sind, wählen Sie die [!UICONTROL **Diagramme anzeigen**] Schaltfläche.

#### Auslastungsdiagramm {#utilization}

Das Nutzungsdiagramm zeigt die Nutzung der Berichte für die ausgewählte Report Suite in den letzten 2 Stunden.

* Die X-Achse zeigt die Berichtsnutzungskapazität der letzten 2 Stunden an.
* Die Y-Achse zeigt den Prozentsatz der Berichtsnutzungskapazität nach Minuten an.
* Sie können mit dem Mauszeiger über das Diagramm fahren, um Zeitpunkte anzuzeigen, an denen der Nutzungsprozentsatz für diese Minute am höchsten war.

  ![Nutzungsdiagramm](assets/utilization-graph.png)

#### Diagramm &quot;Unique Users&quot;

Das Diagramm Unique Users zeigt die Berichtsaktivität für die ausgewählte Report Suite in den letzten 2 Stunden an.

* Die X-Achse zeigt einen 2-Stunden-Zeitrahmen an.
* Die Y-Achse zeigt die Anzahl der Benutzer, die Berichterstellungsanfragen gestellt haben, nach Minuten an.
* Sie können mit dem Mauszeiger über das Diagramm fahren, um die Zeitpunkte anzuzeigen, an denen die maximale Anzahl von Benutzern für diese Minute lag.

  ![Diagramm &quot;Unique Users&quot;](assets/distinct-users-graph.png)

<!--

#### Requests graph

The Requests graph shows the number of processed and completed requests for the selected report suite over the last 2 hours. 

* The x-axis shows a 2-hour time frame.
* The y-axis shows the number of processed requests (in purple) and completed requests (in green), by minute.
* You can hover over the chart to view points in time where the maximum number of requests was highest for that minute.

   ![Distinct Users graph](assets/requests-graph.png)

#### Queueing graph

The Queueing graph shows the average queue wait time (in seconds) for reporting requests for the selected report suite over the last 2 hours. 

* The x-axis shows a 2-hour time frame.
* The y-axis shows the average wait time (in seconds).
* You can hover over the chart to view points in time where the maximum average wait time was highest for that minute.

   ![Distinct Users graph](assets/queueing-graph.png)

-->

### Tabelle anzeigen {#view-table}

Sie können die Anzeige der Daten auf eine der folgenden Registerkarten oben in der Datentabelle einstellen: [!UICONTROL **Anfrage**], [!UICONTROL **Benutzer**], [!UICONTROL **Projekt**] oder [!UICONTROL **Anwendung**].

>[!TIP]
>
>Sie können [!UICONTROL **Ausblenden von Diagrammen**] , um nur die Tabelle anzuzeigen.

![Tabellenregisterkarten](assets/indiv-report-ste-table-tabs.png)

#### Daten nach Anforderung anzeigen

Wenn Sie die [!UICONTROL **Anfrage**] -Tab, stehen in der Tabelle die folgenden Spalten zur Verfügung:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Antrags-ID**] | Kann zur Fehlerbehebung verwendet werden. |
| [!UICONTROL **Ausführungszeit**] | Dauer der Ausführung der Anfrage. |
| [!UICONTROL **Startzeit**] | Der Zeitpunkt, zu dem die Anfrage verarbeitet wurde (basierend auf der Ortszeit des Administrators). |
| [!UICONTROL **Wartezeit**] | Wie lange die Anfrage vor der Verarbeitung gewartet hat. im Allgemeinen bei „0“, wenn genügend Kapazität vorhanden ist. |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Intelligente Warnhinweise</li></ul> |
| [!UICONTROL **Benutzer**] | Der Benutzer, der die Anfrage initiiert hat. Wenn der Wert dieser Spalte [!UICONTROL **Nicht erkannt**], bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben. |
| [!UICONTROL **Projekt**] | Gespeicherte Workspace-Projektnamen, API-Berichts-IDs usw. (Metadaten können von Programm zu Programm variieren.) |
| [!UICONTROL **Status**] | Statusindikatoren: <ul><li>**Läuft**: Die Anfrage wird derzeit verarbeitet.</li><li>**Ausstehend**: Die Anfrage wartet auf die Verarbeitung.</li></ul> |
| [!UICONTROL **Komplexität**] | Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist. Mögliche Werte: <ul><li>[!UICONTROL **Niedrig**]</li><li>[!UICONTROL **Mittel**]</li><li>[!UICONTROL **Hoch**]</li></ul>Dieser Wert wird durch die Werte in den folgenden Spalten beeinflusst:<ul><li>[!UICONTROL **Monatsgrenzen**]</li><li>[!UICONTROL **Spalten**]</li><li>[!UICONTROL **Segmente**]</li></ul> |
| [!UICONTROL **Monatsgrenzen**] | Die Anzahl der Monate, die in einer Anfrage enthalten sind. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL **Spalten**] | Die Anzahl der Metriken und Aufschlüsselungen in der Anforderung. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL **Segmente**] | Die Anzahl der Segmente, die auf die Anforderung angewendet werden. Dies erhöht die Komplexität der Anfrage. |

{style="table-layout:auto"}

#### Daten nach Benutzer anzeigen

Wenn Sie die [!UICONTROL **Benutzer**] -Tab, stehen in der Tabelle die folgenden Spalten zur Verfügung:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Benutzer**] | Der Benutzer, der die Anfrage initiiert hat. Wenn der Wert dieser Spalte [!UICONTROL **Nicht erkannt**], bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der vom Benutzer initiierten Anfragen. |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit dem Benutzer verknüpften Projekte. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Intelligente Warnhinweise</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität von Anforderungen, die vom Benutzer initiiert wurden. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Dies erhöht die durchschnittliche Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Dies erhöht die durchschnittliche Komplexität. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Dies erhöht die durchschnittliche Komplexität. |

{style="table-layout:auto"}

#### Daten nach Projekt anzeigen

Wenn Sie die [!UICONTROL **Projekt**] -Tab, stehen in der Tabelle die folgenden Spalten zur Verfügung:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Projekt**] | Das Projekt, bei dem die Abfragen eingeleitet wurden. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der mit dem Projekt verknüpften Anforderungen. |
| [!UICONTROL **Anzahl der Benutzer**] | Die Anzahl der mit dem Projekt verknüpften Benutzer. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Intelligente Warnhinweise</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der Anforderungen, die im Projekt enthalten sind. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Dies erhöht die durchschnittliche Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Dies erhöht die durchschnittliche Komplexität. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Dies erhöht die durchschnittliche Komplexität. |

{style="table-layout:auto"}

#### Daten nach Anwendung anzeigen

Wenn Sie die [!UICONTROL **Anwendung**] -Tab, stehen in der Tabelle die folgenden Spalten zur Verfügung:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Programm**] | Die Anwendung, in der die Abfragen initiiert wurden. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der mit der Anwendung verknüpften Anforderungen. |
| [!UICONTROL **Anzahl der Benutzer**] | Die Anzahl der mit der Anwendung verknüpften Benutzer. <!--???--> |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit der Anwendung verknüpften Projekte. <!--???--> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der mit der Anwendung verknüpften Anforderungen. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:<ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Dies erhöht die durchschnittliche Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Dies erhöht die durchschnittliche Komplexität. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Dies erhöht die durchschnittliche Komplexität. |

{style="table-layout:auto"}

<!--

### Filter

You can filter the table by Application (see list in the table below), by User, and by Project.

![filter](/help/admin/admin/assets/filter.png)

### Summary Numbers {#summary}

![filter](/help/admin/admin/assets/summary_numbers.png)

The Summary Numbers show the following information:

| Summary Number | Description |
| --- | --- |
| [!UICONTROL **Users**] | The number of users that are currently sending reporting requests to this report suite. |
| [!UICONTROL **Projects**] | Workspace projects, Report Builder workbooks, etc.  | 
| [!UICONTROL **Queries**] | The number of queries currently running. |
| [!UICONTROL **Average Wait Time**] | The average wait time for all running queries.  |
| [!UICONTROL **Usage Capacity**] | The current usage capacity for this report suite. |

{style="table-layout:auto"}

-->


