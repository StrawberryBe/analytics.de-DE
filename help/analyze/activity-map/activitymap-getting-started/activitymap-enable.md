---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
title: Activity Map aktivieren
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: 7f7f6347561d51671bbcb20959895178f3428314
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 40%

---


# Aktivieren und Aktivieren von Activity Map

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. Activity Map aktivieren {#update_code}

Das Activity Map-Modul ist Teil der AppMeasurement.js-, Adobe Experience Platform-Tags- und Web-SDK (legierte.js). Activity Map-Daten können nur erfasst werden, wenn Sie auf **Web SDK-Version 2.15.0** oder höher oder **Adobe Analytics tags-Erweiterung v1.90** oder höher oder **AppMeasurement-Version 1.6** oder höher.

+++Web SDK (Tags-Erweiterung)

Navigieren Sie in Adobe Experience Platform-Tags zu der Eigenschaft, für die Sie Analytics implementieren. under [!UICONTROL Erweiterungen] -> [!UICONTROL Adobe Experience Platform Web SDK]auswählen **[!UICONTROL Aktivieren der Klickdatenerfassung]** wie unten hervorgehoben. Erstellen Sie dann die Bibliothek mit den Änderungen und veröffentlichen Sie die Bibliothek in der Produktion.

![](assets/web_sdk.png)

+++

++ + Manuelle Web SDK-Implementierung

Siehe [Links verfolgen](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de) für Informationen zur Implementierung des Linktrackings und zur Aktivierung der Aktivitätszuordnung durch Erfassen der `region` des angeklickten HTML-Elements.

>[!NOTE]
>
>Durch die Aktivierung von Linktracking mit dem Web SDK werden derzeit Link-Ereignisse gesendet, wenn eine Kundin oder ein Kunde von einer Seite zur nächsten navigiert. Dies unterscheidet sich von der Funktionsweise von AppMeasurement und kann möglicherweise zu zusätzlichen abrechnungsfähigen Treffern führen, die an Adobe gesendet werden.

+++

+ + Analytics-Erweiterung (Adobe Experience Platform-Tags)

Navigieren Sie in Adobe Experience Platform-Tags zu der Eigenschaft, für die Sie Analytics implementieren. Im [!UICONTROL Installieren der Erweiterung] Dialogfeld auswählen **[!UICONTROL Activity Map verwenden]**.

![](assets/aa_extension.png)

+++

+++AppMeasurement

1. Laden Sie die neueste JavaScript-Bibliothek für AppMeasurement herunter.
Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Code-Manager]**.
1. Implementieren Sie es wie folgt [diese Anweisungen](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=de).

+++

## Schritt 2. Activity Map-Berichte aktivieren {#enable}

Zunächst müssen Sie Activity Map-Berichte auf Report Suite-Ebene aktivieren.

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suites auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map – Berichterstattung]**.

1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. Zur Aktivierung müssen Sie zunächst die Variablen aktivieren, indem Sie auf **[!UICONTROL Activity Map-Berichte aktivieren]** klicken.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

   ![](assets/enable.png)

1. Nach etwa einer Stunde können Sie sich den [Activity Map-Seitenbericht](/help/analyze/activity-map/activitymap-reporting-analytics.md) ansehen, der alle Seiten enthält, auf denen Benutzer auf einen Link geklickt haben.

## Schritt 3. Benutzer hinzufügen zu [!UICONTROL Activity Map-Zugriff] Produktprofil {#add_users}

1. Klicken Sie auf **[!UICONTROL Benutzer zur Gruppe hinzufügen]**.

   Dadurch gelangen Sie zur Produktprofilseite im [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview).

1. Wenn Sie keine [!UICONTROL Activity Map-Zugriff] Produktprofil verwenden, tun Sie dies jetzt. Die für dieses Profil erforderlichen Berechtigungselemente sind [!UICONTROL Analytics-Tools] > [!UICONTROL Activity Map] und [!UICONTROL Analytics-Tools] > [!UICONTROL Segmentveröffentlichung].

1. Fügen Sie diesem Produktprofil Benutzer hinzu. Dadurch können Ihre Benutzer Activity Map von herunterladen  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Instrumente]** > **[!UICONTROL ActivityMap]** .

