---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die [!DNL Activity Map]-Linksammlung und den Download durch den Benutzer zu aktivieren.
seo-description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die [!DNL Activity Map]-Linksammlung und den Download durch den Benutzer zu aktivieren.
seo-title: '[!DNL Activity Map] aktivieren'
solution: Analytics
title: '[!DNL Activity Map] aktivieren'
topic: Activity Map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: 36637b76b8026fbf87ad48adcfa47386c530e732

---


# Aktivieren [!DNL Activity Map]{#enable-activity-map}

Explains the steps the Analytics Admin needs to complete to enable [!DNL Activity Map] link collection and user download.

## Schritt 1. Update Your AppMeasurement (Javascript) Code to v1.6 (or higher) {#section_5D1586289DF2489289B1B6C1C80C300D}

The [!DNL Activity Map] module is part of the AppMeasurement.js file (located at the top of the file). The AppMeasurement library will load the [!DNL Activity Map] module when instantiated.

[!DNL Activity Map] Daten können nur erfasst werden, wenn Sie auf diese Version (oder höher) von AppMeasurement aktualisieren.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]** and [implement it](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

   We have included some [sample implementation code](../../../../analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md#concept_EC27DA8A62F5411EBED51284CB7E1734) to help you visualize the changes that have been made to the code by including the [!DNL Activity Map] module.

1. Validieren Sie die Implementierung:

   1. Wenn auf ein klickbares Element geklickt wird, werden Daten in einem Cookie namens s_sq gespeichert.
   1. The [!DNL Activity Map] data can be seen in the query-string on the tracking call. Beispiel:

      ```
      …&c.&a.&[!DNL Activity Map].&link=My%20Link&region=My%20Region&page=My%20Page&.[!DNL Activity Map]&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL [!DNL Activity Map]Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width="400px"}

## Schritt 2: Aktivieren [!DNL Activity Map] von Berichten {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

First, you need to enable [!DNL Activity Map] reports at a report-suite level.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin &gt; Report Suites &gt;[select report suite]&gt; Edit Settings &gt;[!DNL Activity Map]]** &gt; **[!UICONTROL [!DNL Activity Map]Reporting]** .
1. [!DNL Activity Map] erfasst die Linkdaten in [!DNL Activity Map] Berichten. For the activation to happen, you must first activate the variables by clicking **[!UICONTROL Enable[!DNL Activity Map]Reports]**.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

1. After about an hour, check the [[!DNL Activity Map] Page report](/help/analyze/activity-map/activitymap-reporting-analytics.md), which shows all the pages where users clicked on a link.

## Schritt 3. Add users to [!DNL Activity Map] access group {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klicken Sie auf **[!UICONTROL Benutzer zur Gruppe hinzufügen]**.

   Dies bringt Sie zur Gruppenverwaltungsseite in der Admin Console.

1. [Fügen Sie Benutzer dieser Gruppe hinzu](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) und klicken Sie auf **[!UICONTROL Gruppe speichern]**.

1. This allow your Admin users to download [!DNL Activity Map] from  **[!UICONTROL Adobe Analytics]** &gt; **[!UICONTROL Tools]** &gt; **[!UICONTROL ActivityMap]** .

<note>
  Wenn Sie möchten, dass Benutzer, die keine Administratoren sind, [!DNL Activity Map] herunterladen können, müssen Sie eine neue Benutzergruppe erstellen, die Zugriff auf <span class="uicontrol"> Tools </span> &gt; <span class="uicontrol"> Legacy ClickMap-Installation hat </span>. Sie können dieser Gruppe dann Benutzer ohne Administratorrechte hinzufügen. Diese Berechtigungsstufe in Verbindung mit dem [!DNL Activity Map] Access bietet umfassende Berechtigungen zum Herunterladen und Verwenden des Tools. 
</note>
