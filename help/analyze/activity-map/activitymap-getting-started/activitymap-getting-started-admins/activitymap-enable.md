---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
title: Activity Map aktivieren
topic: Activity map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Activity Map aktivieren {#enable-activity-map}

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. AppMeasurement-Code (Javascript) auf Version 1.6 (oder höher) aktualisieren {#section_5D1586289DF2489289B1B6C1C80C300D}

Das Activity Map-Modul ist Bestandteil der Datei AppMeasurement.js (befindet sich oben in der Datei). Die AppMeasurement-Bibliothek lädt das Activity Map-Modul nach der Instanziierung.

Activity Map-Daten können erst erfasst werden, nachdem AppMeasurement auf diese Version (oder höher) aktualisiert wurde.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** and [implement it](https://docs.adobe.com/content/help/de-DE/analytics/implementation/js/overview.html).

   Der verfügbare [Beispiel-Implementierungscode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) veranschaulicht die Änderungen, die am Code durch Einbindung des Activity Map-Moduls vorgenommen wurden.

1. Validieren Sie die Implementierung:

   1. Wenn auf ein klickbares Element geklickt wird, werden Daten in einem Cookie namens s_sq gespeichert.
   1. Die Activity Map-Daten sind in der Abfragezeichenfolge des Tracking-Aufrufs sichtbar. Beispiel:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL Activity Map Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## Schritt 2: Activity Map-Berichte aktivieren {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Zunächst müssen Sie Activity Map-Berichte auf einer Report Suite-Ebene aktivieren.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites >[select report suite]> Edit Settings > Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. For the activation to happen, you must first activate the variables by clicking **[!UICONTROL Enable Activity Map Reports]**.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

1. Nach etwa einer Stunde können Sie sich den [Activity Map-Seitenbericht](/help/analyze/activity-map/activitymap-reporting-analytics.md) ansehen, der alle Seiten enthält, auf denen Benutzer auf einen Link geklickt haben.

## Schritt 3. Benutzer zur Activity Map Access Group hinzufügen {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klicken Sie auf **[!UICONTROL Add Users to Group]**.

   Dies bringt Sie zur Gruppenverwaltungsseite in der Admin Console.

1. [Hinzufügen Benutzer zu dieser Gruppe](https://docs.adobe.com/content/help/de-DE/analytics/admin/user-product-management/user-groups/groups.html) und **[!UICONTROL Save Group]**.

1. This allow your Admin users to download Activity Map from  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE] Wenn Sie möchten, dass Benutzer, die keine Administratoren sind, Activity Map herunterladen können, erstellen Sie eine neue Benutzergruppe, die Berechtigungen für „Tools“ und „Legacy ClickMap Installation“ bereitstellt. Diese Berechtigungsstufe in Verbindung mit dem Activity Map-Zugriff bietet Berechtigungen zum Herunterladen und Verwenden des Tools.
