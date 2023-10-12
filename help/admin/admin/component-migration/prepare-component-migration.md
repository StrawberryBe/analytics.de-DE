---
description: Erläutert die erforderlichen Vorbereitungen für die Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics.
title: Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics
feature: Admin Tools
exl-id: a9ff98dc-6568-428d-a8a8-faca5bc76a29
source-git-commit: 03120156e1ba70e50b265da788fa5997fd31c93e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 15%

---

# Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics

Bevor jemand in Ihrer Organisation mit der Migration von Projekten beginnt, siehe [Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics](/help/admin/admin/component-migration/component-migration.md), führen Sie die folgenden Abschnitte aus.

## Voraussetzungen

Bevor Ihre Projekte und die zugehörigen Komponenten migriert werden können, müssen Sie zunächst:

* Verwenden Sie eine der folgenden Methoden, um Daten in Adobe Experience Platform aufzunehmen, um Adobe Analytics-Report Suite-Daten unter Customer Journey Analytics anzuzeigen:

  >[!NOTE]
  >
  >  Wenn Sie das WebSDK zum Erfassen von Daten verwenden, müssen alle Schemafelder manuell zugeordnet werden. (Weitere Informationen zum Zuordnungsprozess finden Sie unter [Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics](/help/admin/admin/component-migration/component-migration.md))


   * Um den Adobe Analytics-Quell-Connector zu verwenden, gehen Sie folgendermaßen vor:

      * [Report Suites für die Aufnahme in Adobe Experience Platform und Customer Journey Analytics einrichten](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [Daten erfassen und verwenden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html?lang=de)

   * Um das WebSDK zu verwenden, müssen Sie:

      * [Report Suites für die Aufnahme in Adobe Experience Platform und Customer Journey Analytics einrichten](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [Daten über das Adobe Experience Platform Web SDK erfassen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk.html)

* Erstellen Sie eine [connection](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=de) und [Datenansicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de) mit den erfassten Daten.

* Stellen Sie sicher, dass Benutzer in Customer Journey Analytics für die Datenansichten bereitgestellt werden, in denen Daten zugeordnet werden.

  Weitere Informationen finden Sie unter [Customer Journey Analytics-Berechtigungen in der Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) in [Zugriffskontrolle auf Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  Die Registerkarte Berechtigungen ist Teil jedes Produktprofils in Admin Console. Benutzende können zu bestimmten Produktprofilen hinzugefügt werden. Anschließend werden Rechte für bestimmte Datenansichten zugewiesen und festgelegt, welche Berechtigungen die Benutzenden in einem Produktprofil haben.

* Entscheiden Sie als Organisation, wie Sie Komponenten zuordnen.

  Weitere Informationen finden Sie im folgenden Abschnitt: [Als Organisation entscheiden, wie Sie Komponenten zuordnen](#decide-as-an-organization-how-you-will-map-components).

## Informationen zu den Funktionen einer Migration

In den folgenden Tabellen wird beschrieben, welche Elemente eines Projekts und einer Komponente in einer Migration enthalten sind:

### Migrierte Komponentenelemente

Dimensionen und Metriken werden im Rahmen des Zuordnungsprozesses migriert, der unter [Migrieren von Adobe Analytics-Projekten auf Customer Journey Analytics](#migrate-adobe-analytics-projects-to-customer-journey-analytics).

Segmente, Datumsbereiche und berechnete Metriken, die noch nicht im Customer Journey Analytics vorhanden sind, werden dort anhand der zugeordneten Dimensionen und Metriken neu erstellt.

|  | „Migriert“ |
|---------|---------|
| **[Inhabende](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)** | Dimensionen und Metriken: nein<p>Segmente und Datumsbereiche: ![Häkchen](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Freigabe](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen und Metriken: nein<p>Segmente und Datumsbereiche: nein</p> |
| **[Beschreibungen](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | Dimensionen und Metriken: nein<p>Segmente und Datumsbereiche: ![Häkchen](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Tags](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen und Metriken: nein<p>Segmente und Datumsbereiche: nein</p> |
| **[Attribution (auf Dimensionen)](/help/analyze/analysis-workspace/attribution/overview.md)** | Dimensionen und Metriken: nein<p>Segmente und Datumsbereiche: nein</p> |

{style="table-layout:auto"}

### Migrierte Projektelemente

|  | „Migriert“ |
|---------|----------|
| **[Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Segmente](/help/components/segmentation/seg-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Schnellsegmente](/help/analyze/analysis-workspace/components/segments/quick-segments.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Dimensionen](/help/components/dimensions/overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Automatisch oder manuell zugeordnet |
| **[Metriken](/help/components/metrics/overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Automatisch oder manuell zugeordnet |
| **[Bedienfelder](/help/analyze/analysis-workspace/c-panels/panels.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Inhabende](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Definiert durch den Benutzer, der die Migration durchführt |
| **[Kuratierung](/help/analyze/analysis-workspace/curate-share/curate.md)** | Nein |
| **[Freigabe](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | Nein |
| **[Anmerkungen](/help/analyze/analysis-workspace/components/annotations/overview.md)** | Nein |
| **[Ordnerstruktur](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | Nein |
| **[Beschreibungen](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Tags](/help/analyze/landing.md)** | Nein |
| **[Favoriten](/help/analyze/landing.md)** | Nein |
| **[Zeitpläne](/help/components/scheduled-projects-manager.md)** | Nein |
| **[Anomalieerkennung](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |

{style="table-layout:auto"}

## Nicht unterstützte Elemente, die Fehler verursachen

Die folgenden Visualisierungen und Bedienfelder werden im Customer Journey Analytics nicht unterstützt. Wenn diese Elemente vor der Migration in ein Projekt einbezogen werden, kann dies entweder dazu führen, dass die Migration fehlschlägt, oder dass nach der Migration des Projekts Fehler auftreten.

Entfernen Sie diese Elemente aus dem Adobe Analytics-Projekt, bevor Sie das Projekt auf Customer Journey Analytics migrieren. Wenn eine Migration fehlschlägt, entfernen Sie diese Elemente, bevor Sie die Migration erneut versuchen.

### Nicht unterstützte Visualisierungen

* [Zuordnung](/help/analyze/analysis-workspace/visualizations/map-visualization.md)

### Nicht unterstützte Bedienfelder

* [Analytics for Target (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [Segmentvergleich](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [Medien-Zielgruppendurchschnitt pro Minute](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [Nächstes oder vorheriges Element](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [Seitenzusammenfassung](/help/analyze/analysis-workspace/c-panels/page-summary.md)

* [Beitragsanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md)

## Als Organisation entscheiden, wie Sie Komponenten zuordnen

>[!IMPORTANT]
>
>Der Migrationsprozess identifiziert Komponenten in Ihrem Adobe Analytics-Projekt, die nicht automatisch Komponenten im Customer Journey Analytics zugeordnet werden können, und ermöglicht es Ihnen, sie manuell zuzuordnen.
>
>**Alle Zuordnungen eines Projekts gelten für alle zukünftigen Projekte in Ihrer gesamten Organisation, unabhängig davon, welcher Benutzer die Migration durchführt. Diese Zuordnungen können nur geändert oder rückgängig gemacht werden, wenn Sie sich an die Kundenunterstützung wenden.**
>
>Aus diesem Grund ist es wichtig, dass Ihr Unternehmen entscheidet, wie Dimensionen und Metriken zugeordnet werden, bevor Projekte migriert werden. Dadurch wird verhindert, dass einzelne Administratoren Entscheidungen in einem Silo treffen, wenn sie nur ein einzelnes Projekt in Betracht ziehen.
>
>Im Folgenden finden Sie eine Liste von Dimensionen und Metriken, die Sie manuell zuordnen müssen, wenn sie in Ihrem Projekt vorhanden sind. Wir empfehlen, diese Liste vor der Migration zu überprüfen. Wenn eine dieser Komponenten in Ihrem Projekt vorhanden ist, entscheiden Sie jetzt, welchen Customer Journey Analytics-Komponenten Sie sie zuordnen möchten.


### Dimensionen, die manuell zugeordnet werden müssen

* averagepagetime
* pagetimeseconds
* singlepagevisits
* visitnumber
* timeprior
* timespent
* category
* connectiontype
* customerloyalty
* customlink
* downloadlink
* Exitlink
* hitdepth
* hittype
* pathlength
* daysbeforefirstpurchase
* dayssincelastpurchase
* daysSinceLastVisit
* identificationstate
* optoutreason
* persistentcookie
* returnfrequency
* searchenginenatural
* searchenginenaturalkeyword
* mobilecarrier
* monitorresolution
* surveybase
* mcaudiences
* tntbase
* targetraw


### Metriken, die manuell zugeordnet werden müssen

* timespentvisit
* timespentvisitor
* Neuladungen
* Absprünge
* bouncerate
* pageevents
* pageviewspervisit
* orderspervisit
* averagepagedepth
* averagetimespentonsite
* exitlinkinstances
* customlinkinstances
* downloadlinkinstances
* darkvisitors
* singlepagevisits
* singlevaluevisits
* visitorhomepage
* visitorsmcvisid
* pagesnotfound
* newengagements
* time_granularität
* concurrent_viewers_visitors
* concurrent_viewers_instances
* Geräten auf
* geschätzte Personen
* Wiedergabedauer_Besuchszeit_Sekunden
* play_time_used_minutes
* average_minute_audience_time_based
* average_minute_audience_media_time
* average_minute_audience_content_time
* video_length
* Zielkonvertierung
* Zielgruppenbestimmung
