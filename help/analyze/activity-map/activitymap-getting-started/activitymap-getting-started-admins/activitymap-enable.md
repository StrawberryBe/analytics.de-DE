---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
title: Activity Map aktivieren
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: d4caf0ddc5cf5402bfef94a64db1c00e1c725658
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 74%

---

# Activity Map aktivieren{#enable-activity-map}

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. Implementierungscode aktualisieren {#section_5D1586289DF2489289B1B6C1C80C300D}

Das Activity Map-Modul ist Teil der AppMeasurement.js und des Web SDK (Version 2.15.0 oder höher).
Die AppMeasurement-Bibliothek oder das Web-SDK lädt das Activity Map-Modul bei der Instanziierung.

>[!NOTE]
>
>Activity Map-Daten können nur erfasst werden, wenn Sie auf **AppMeasurement** **Version 1.6** oder höher oder **Web SDK** **Version 2.15.0** oder höher.


1. Laden Sie die neueste JavaScript-Bibliothek herunter, je nachdem, ob Sie AppMeasurement oder Web SDK verwenden.

   - **AppMeasurement** Code (AppMeasurement_Javascript-1.6.zip), indem Sie  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Code-Manager]** und [implementieren](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=de).

     Der verfügbare [Beispiel-Implementierungscode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) veranschaulicht die Änderungen, die am Code durch Einbindung des Activity Map-Moduls vorgenommen wurden.

   - **Web SDK** Code (legierung.js). Siehe [Installieren des SDK - Option 2: Installieren der vordefinierten eigenständigen Version](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de#option-2%3A-installing-the-prebuilt-standalone-version) für weitere Informationen. Stellen Sie sicher, dass Sie Version 2.15 oder höher verwenden.

     Siehe [Links verfolgen](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de) für Informationen zur Implementierung des Linktrackings und zur Aktivierung der Aktivitätszuordnung durch Erfassen der `region` des angeklickten HTML-Elements.

     >[!NOTE]
     >
     >Durch die Aktivierung von Linktracking mit dem Web SDK werden derzeit Link-Ereignisse gesendet, wenn eine Kundin oder ein Kunde von einer Seite zur nächsten navigiert. Dies unterscheidet sich von der Funktionsweise von AppMeasurement und kann möglicherweise zu zusätzlichen abrechnungsfähigen Treffern führen, die an Adobe gesendet werden.


1. Validieren Sie die Implementierung:

   1. Wenn auf ein klickbares Element geklickt wird, werden Daten in einem Cookie namens s_sq gespeichert.
   1. Die Activity Map-Daten sind in der Abfragezeichenfolge des Tracking-Aufrufs sichtbar. Beispiel:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Schlüsseln Sie diesen Bericht mit **[!UICONTROL Activity Map – Link nach Region]** auf, um den Link/die Region für diese Seite zu sehen:  ![](assets/am_breakdown.png){width="400px"}

## Schritt 2. Activity Map-Berichte aktivieren {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Zunächst müssen Sie Activity Map-Berichte auf einer Report Suite-Ebene aktivieren.

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suites auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map – Berichterstattung]**.
1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. Zur Aktivierung müssen Sie zunächst die Variablen aktivieren, indem Sie auf **[!UICONTROL Activity Map-Berichte aktivieren]** klicken.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

1. Nach etwa einer Stunde können Sie sich den [Activity Map-Seitenbericht](/help/analyze/activity-map/activitymap-reporting-analytics.md) ansehen, der alle Seiten enthält, auf denen Benutzer auf einen Link geklickt haben.

## Schritt 3. Benutzer zur Activity Map Access Group hinzufügen {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klicken Sie auf **[!UICONTROL Benutzer zur Gruppe hinzufügen]**.

   Dies bringt Sie zur Gruppenverwaltungsseite in der Admin Console.

1. [Fügen Sie Benutzer dieser Gruppe hinzu](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-groups/groups.html?lang=de) und klicken Sie auf **[!UICONTROL Gruppe speichern]**.

1. Dadurch können Ihre Admin-Benutzer Activity Map über **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Werkzeuge]** > **[!UICONTROL Activity Map]** herunterladen.

>[!NOTE]
>
>Wenn Sie möchten, dass Benutzer, die keine Administratoren sind, Activity Map herunterladen können, erstellen Sie eine neue Benutzergruppe, die Berechtigungen für „Tools“ und „Legacy ClickMap Installation“ bereitstellt. Diese Berechtigungsstufe in Verbindung mit dem Activity Map-Zugriff bietet Berechtigungen zum Herunterladen und Verwenden des Tools.
