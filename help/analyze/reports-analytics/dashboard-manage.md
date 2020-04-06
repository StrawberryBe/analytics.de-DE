---
description: Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.
subtopic: Dashboards
title: Dashboard-Manager
topic: Reports and analytics
uuid: 380fd148-2ed9-43bf-9d42-46e373e788e4
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Dashboard-Manager

Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.

>[!IMPORTANT]
>
>Als Best Practice für den Dashboard-Manager wird empfohlen, für einen Benutzer nicht mehr als 300 Dashboards zu verwenden. Beachten Sie auch, dass der Manager alle unten aufgeführten freigegebenen Dashboards lädt. Achten Sie daher auf eine sinnvolle Freigabe von Dashboards.

## Dashboard-Manager

Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.

Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Dashboards]**.

| Element | Beschreibung |
|--- |--- |
| Freigegeben | Zeigt an, ob das Dashboard freigegeben wurde. |
| Eingeplant | Hier können Sie das Dashboard für den Versand planen. |
| Archiv anzeigen | Diese Funktion ist nicht mehr verfügbar. |
| An Benutzer senden | Ermöglicht die Freigabe eines Dashboards. |
| Verwalten | Hiermit können Sie ein Dashboard bearbeiten, kopieren und löschen. |

## Freigegebene Dashboard verwalten

In diesen Schritten wird beschrieben, wie Sie die Verwaltungsoptionen für freigegebene Dashboards verwenden.

1. Öffnen von **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Dashboards]**.
1. Under [!UICONTROL Shared Dashboards], locate the shared dashboard (or legacy dashboard) you want to manage and choose one or more of the following options:

<table id="choicetable_857E0E816D63404683D4E24DC8D7FC69"> 
 <thead class="chhead sthead"> 
  <th class="choptionhd"> Option </th> 
  <th class="chdeschd"> Beschreibung </th> 
 </thead> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Archiv anzeigen</strong></td> 
  <td class="chdesc stentry"> Diese Funktion ist nicht mehr verfügbar. </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Dashboard-Player</strong></td> 
  <td class="chdesc stentry"> <p>Die Server von SiteCatalyst 14 reagieren nicht mehr auf Datenanforderungen von Dashboard Player. Alle Dashboard, die derzeit im Dashboard Player angezeigt werden, können auf der Benutzeroberfläche von Reports &amp; Analysen aufgerufen oder als Echtzeit-Dashboard neu erstellt werden. Real-Time-Dashboard sind speziell für die kontinuierliche Anzeige konzipiert und enthalten einen Vollbildmodus, mit dem Sie auf TV-Geräten oder anderen Geräten mit großem Bildschirm anzeigen können. </p> <p>Erforderliche Benutzeraktion: Sie müssen die Verwendung von Dashboard Player einstellen. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Kopier mich</strong></td> 
  <td class="chdesc stentry"> Fügt Ihrer Liste Dashboards eine Kopie hinzu, die denselben Namen wie das Original trägt. Sie können jedoch keine vom Eigentümer des Dashboards vorgenommenen Aktualisierungen/Änderungen sehen. Durch Kopieren eines älteren Dashboards wird ein leeres Dashboard geöffnet, in dem Sie Legacy-Inhalte hinzufügen können. <p>Wichtig: Wenn die von Ihnen am Dashboard vorgenommenen Änderungen für gemeinsame Benutzer nicht sichtbar sind, prüfen Sie Ihren Dashboard-Manager, um zu sehen, ob die Benutzer die Option <span class="uicontrol">Kopier mich</span> ausgewählt haben. Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. Um alle Änderungen/Updates sehen zu können, müssen gemeinsame Benutzer die Option <span class="uicontrol">Im Menü</span> im Dashboard-Manager auswählen. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Im Menü</strong></td> 
  <td class="chdesc stentry"> Damit können Sie vom Dashboard-Eigentümer vorgenommene Änderungen/Aktualisierungen anzeigen. </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Freigabe aufheben</strong></td> 
  <td class="chdesc stentry"> Entfernt das Dashboard aus Ihrer Liste freigegebener Dashboards. </td> 
 </tr> 
</table>

## Legacy-Dashboard migrieren

Vorhandene ältere Dashboard werden weiterhin ausgeführt und können weiterhin bearbeitet, heruntergeladen und geplant werden. Sie können jedoch keine neuen alten Dashboard mehr erstellen. Es wird dringend empfohlen, vorhandene ältere Dashboard auf das neuere Dashboard-Format zu aktualisieren.

>[!NOTE] Sie sollten zukünftig in Erwägung ziehen, [Analysis Workspace-Projekte](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/) und ihre Möglichkeit zum Herunterladen und Planen zu nutzen.

Wenn Sie das Legacy-Dashboard kopieren, öffnet das System das Legacy-Dashboard zur Bearbeitung, sodass Sie Legacy- oder neue Inhalte hinzufügen können. Wenn Sie ein Legacy-Dashboard kopieren, wird das Original in der Liste älterer Dashboard beibehalten.

>[!NOTE] Durch das Hinzufügen von Legacy-Inhalt zu einem Dashboard wird ein Dashboard erstellt, das auf der aktuellen Dashboard-Funktion basiert. Das Legacy-Reportlet kann jedoch Daten enthalten, die auf der vorherigen Datenplattform basieren.

**So migrieren Sie ein veraltetes Dashboard der Version 14.x**

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Manage Dashboards]**.
1. Klicken Sie in der [!UICONTROL Manage] Spalte unter [!UICONTROL Legacy Dashboards]auf **[!UICONTROL Copy to New Dashboard]**.

   Das kopierte Dashboard wird im Dashboard-Layout-Editor geöffnet.

   See [Editing Dashboard and Reportlet Data](/help/analyze/reports-analytics/dashboard.md).

## Dashboard freigeben

Schritte, die beschreiben, wie ein Administrator ein Dashboard für mehrere Benutzer freigeben (oder senden) kann. Wenn Sie Dashboard an Benutzer senden, stehen die Dashboard im [!UICONTROL Shared Dashboards] Benutzermenü zur Verfügung.

1. Suchen Sie im [!UICONTROL Dashboard Manager]Dashboard nach und aktivieren Sie dann **[!UICONTROL Shared]**.
1. Klicken Sie auf **[!UICONTROL Push To Users]**.  ![](assets/push.png)

1. Wählen Sie auf der [!UICONTROL Push Dashboard] Seite die Zielgruppe aus oder klicken Sie auf **[!UICONTROL Check All]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

If shared users of your dashboard cannot see changes you made in the dashboard, check your Dashboard Manager to see if the users have chosen the **[!UICONTROL Copy Me]** option. Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. To see all the changes/updates, shared users need to select the **[!UICONTROL On Menu]** option in the Dashboard Manager.

## Dashboard für Versand planen

Im [!UICONTROL Dashboard Manager]Fenster können Sie sehen, ob ein Dashboard für den Versand geplant ist, und den Zeitplan bearbeiten. Die Optionen für den Dashboard-Versand sind mit den Optionen für den Report Versand identisch.

1. Öffnen Sie ein Dashboard.
1. Klicken Sie auf **[!UICONTROL More]** > **[!UICONTROL Send]**.

   Weitere Informationen finden Sie unter [Planung und Verteilung](/help/analyze/reports-analytics/scheduling.md).

## Dashboard archivieren

>[!NOTE] Diese Funktion ist ab Januar 2020 nicht mehr verfügbar.

In diesen Schritten wird beschrieben, wie Sie gesendete Dashboards als PDF-Datei archivieren. Das System speichert die archivierte Datei zwei Jahre lang oder bis Sie eine maximale Grenze von 4 GB an archivierten Berichten erreichen, je nachdem, was zuerst eintritt.

1. Öffnen Sie ein Dashboard.
1. Klicken Sie auf **[!UICONTROL More]** > **[!UICONTROL Send]**.
1. Aktivieren Sie in der [!UICONTROL Email Report] Gruppe **[!UICONTROL Archive]**.
1. Specify delivery options, then click **[!UICONTROL Send]**.

   Sie können archivierte Dashboard im Dashboard-Manager Ansicht haben. Alternativ können Sie ein Dashboard öffnen und auf **[!UICONTROL More]** > **[!UICONTROL View Archive]**.
