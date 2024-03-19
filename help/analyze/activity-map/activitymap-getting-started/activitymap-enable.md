---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
title: Activity Map aktivieren
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 99%

---


# Aktivieren von Activity Map

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. Aktivieren von Activity Map {#update_code}

Das Activity Map-Modul ist Teil von AppMeasurement.js, Adobe Experience Platform-Tags und dem Web SDK (alloy.js). Activity Map-Daten können nur erfasst werden, wenn Sie auf die **Web SDK-Version 2.15.0** oder höher, die **Adobe Analytics-Tags-Erweiterung v1.90** oder höher oder die **AppMeasurement-Version 1.6** oder höher aktualisieren.

+++Web SDK (Adobe Experience Platform-Tags-Erweiterung)

1. Navigieren Sie in Adobe Experience Platform-Tags zu der Eigenschaft, für die Sie Analytics implementieren. Wählen Sie unter [!UICONTROL Erweiterungen] > [!UICONTROL Adobe Experience Platform Web SDK] die Option zum Aktivieren der Klickdatenerfassung **** aus, wie unten hervorgehoben.
1. Erstellen Sie die Bibliothek mit den Änderungen.
1. Veröffentlichen Sie die Bibliothek in der Produktion.

![](assets/web_sdk.png)

**Validierung**

Interaktionsaufrufe über die Registerkarte „Netzwerk“ von Developer Console:

1. Laden Sie das Skript „Development Launch“ auf der Site.
1. Suchen Sie für Klicks auf Elemente auf der Registerkarte „Netzwerk“ nach „/ee“.

   ![](assets/validation1.png)

Adobe Experience Platform Debugger:

1. Laden Sie [Adobe Experience Platform Debugger](https://chromewebstore.google.com/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) herunter und installieren Sie diese Erweiterung.
1. Navigieren Sie zu [!UICONTROL Protokolle] > [!UICONTROL Edge] > [!UICONTROL Mit Edge verbinden].

   ![](assets/validation2.jpg)

**Häufig gestellte Fragen (FAQ)**

* **Der Interaktionsaufruf wird nicht auf der Registerkarte „Netzwerk“ ausgelöst.**
Die Klickdatenerfassung in einem Erfassungsaufruf müssen wir entweder mit „/ee“ oder mit „collect?“ filtern.

* **Es gibt keine Payload-Anzeige für den Erfassungsaufruf.**
Der Erfassungsaufruf ist so konzipiert, dass das Tracking die Navigation zu anderen Sites nicht beeinträchtigen sollte, sodass die Funktion zum Entladen von Dokumenten für die Erfassungsaufrufe gilt. Dies wirkt sich nicht auf Ihre Datenerfassung aus. Wenn Sie jedoch auf der Seite eine Validierung durchführen müssen, fügen Sie target = &quot;_blank&quot; zum entsprechenden Element hinzu. Der Link wird daraufhin auf einer neuen Registerkarte geöffnet.

* **Wie kann ich die Erfassung von personenbezogenen Daten ignorieren?**
Fügen Sie die entsprechenden Bedingungen in &lt;&lt; on before link click send callback>> hinzu und geben Sie „false“ zurück, um diese Werte zu ignorieren. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de)

  Beispiel-Code:

  ![](assets/sample-code.png)

+++

+++Manuelle Web SDK-Implementierung

Weitere Informationen zum Implementieren von Linktracking und Aktivieren von Activity Map durch Erfassen der `region` des angeklickten HTML-Elements finden Sie unter [Verfolgen von Links](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de).

>[!NOTE]
>
>Durch die Aktivierung von Linktracking mit dem Web SDK werden derzeit Link-Ereignisse gesendet, wenn eine Kundin oder ein Kunde von einer Seite zur nächsten navigiert. Dies unterscheidet sich von der Funktionsweise von AppMeasurement und kann möglicherweise zu zusätzlichen abrechnungsfähigen Treffern führen, die an Adobe gesendet werden. 

+++

+++Analytics-Erweiterung (Adobe Experience Platform-Tags)

Navigieren Sie in Adobe Experience Platform-Tags zu der Eigenschaft, für die Sie Analytics implementieren. Wählen Sie im Dialogfeld [!UICONTROL Erweiterung installieren] die Option zum Verwenden von Activity Map **** aus.

![](assets/aa_extension.png)

+++

+++AppMeasurement

1. Laden Sie die neueste JavaScript-Bibliothek für AppMeasurement herunter.
Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Code-Manager]**.
1. Implementieren Sie sie gemäß [diesen Anweisungen](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=de).

+++

## Schritt 2. Activity Map-Berichte aktivieren {#enable}

Sie müssen Activity Map-Berichte auf Report Suite-Ebene aktivieren.

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suites auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map – Berichterstattung]**.

1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. Zur Aktivierung müssen Sie zunächst die Variablen aktivieren, indem Sie auf **[!UICONTROL Activity Map-Berichte aktivieren]** klicken.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

   ![](assets/enable.png)

1. Nach etwa einer Stunde können Sie sich den [Activity Map-Seitenbericht](/help/analyze/activity-map/activitymap-reporting-analytics.md) ansehen, der alle Seiten enthält, auf denen Benutzer auf einen Link geklickt haben.

## Schritt 3. Hinzufügen von Benutzenden zum Produktprofil [!UICONTROL Activity Map-Zugriff] {#add_users}

1. Klicken Sie auf **[!UICONTROL Benutzer zu Gruppe hinzufügen]**.

   Dadurch gelangen Sie zur Produktprofilseite in der [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview).

1. Falls noch nicht geschehen, erstellen Sie jetzt ein Produktprofil [!UICONTROL Activity Map-Zugriff]. Die für dieses Profil erforderlichen Berechtigungselemente sind [!UICONTROL Analytics-Tools] > [!UICONTROL Activity Map] und [!UICONTROL Analytics-Tools] > [!UICONTROL Segmentveröffentlichung].

1. Fügen Sie diesem Produktprofil Benutzende hinzu. Dadurch können Ihre Benutzenden Activity Map über **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** herunterladen.

