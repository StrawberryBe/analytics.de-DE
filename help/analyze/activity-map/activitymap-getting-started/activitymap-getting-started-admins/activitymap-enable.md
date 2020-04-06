---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
title: Activity Map aktivieren
topic: Activity map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Activity Map aktivieren {#enable-activity-map}

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. AppMeasurement-Code (Javascript) auf Version 1.6 (oder höher) aktualisieren {#section_5D1586289DF2489289B1B6C1C80C300D}

Das Modul &quot;Aktivität Map&quot;ist Teil der Datei AppMeasurement.js (befindet sich oben in der Datei). Die AppMeasurement-Bibliothek lädt das Aktivität Map-Modul, wenn es instanziiert wird.

Aktivität Map-Daten können nur erfasst werden, wenn Sie auf diese Version (oder höher) von AppMeasurement aktualisieren.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** and [implement it](https://marketing.adobe.com/resources/help/de_DE/sc/implement/js_implementation.html).

   Wir haben einen [Beispielimplementierungscode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) eingebunden, der Ihnen bei der Visualisierung der Codeänderungen hilft, indem Sie das Aktivität Map-Modul einbeziehen.

1. Validieren Sie die Implementierung:

   1. Wenn auf ein anklickbares Element geklickt wird, werden die Daten in einem Cookie mit dem Namen s_sq gespeichert.
   1. Die Daten der Aktivität Map können in der Abfrage-Zeichenfolge des Verfolgungsaufrufs angezeigt werden. Beispiel:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL Activity Map Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## Schritt 2: Activity Map-Berichte aktivieren {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Zunächst müssen Sie Activity Map-Berichte auf einer Report Suite-Ebene aktivieren.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites >[select report suite]> Edit Settings > Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. For the activation to happen, you must first activate the variables by clicking **[!UICONTROL Enable Activity Map Reports]**.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

1. Überprüfen Sie nach etwa einer Stunde den Bericht [&quot;](/help/analyze/activity-map/activitymap-reporting-analytics.md)Seitenzuordnungsseite&quot;, der alle Seiten anzeigt, auf die Benutzer auf einen Link geklickt haben.

## Schritt 3. Benutzer zur Activity Map Access Group hinzufügen {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klicken Sie auf **[!UICONTROL Add Users to Group]**.

   Dies bringt Sie zur Gruppenverwaltungsseite in der Admin Console.

1. [Hinzufügen Benutzer zu dieser Gruppe](https://marketing.adobe.com/resources/help/de_DE/reference/groups.html) und **[!UICONTROL Save Group]**.

1. This allow your Admin users to download Activity Map from  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE] Wenn Sie möchten, dass Benutzer, die keine Administratoren sind, Activity Map herunterladen können, erstellen Sie eine neue Benutzergruppe, die Berechtigungen für „Tools“ und „Legacy ClickMap Installation“ bereitstellt. Diese Berechtigungsstufe in Verbindung mit dem Activity Map-Zugriff bietet Berechtigungen zum Herunterladen und Verwenden des Tools.
