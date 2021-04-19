---
description: Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Bereitstellung planen.
subtopic: Dashboards
title: Dashboard-Manager
uuid: 380fd148-2ed9-43bf-9d42-46e373e788e4
feature: Grundlagen zu Reports & Analysen
role: Business Practitioner, Administrator
exl-id: abd5acf5-f743-4c94-81fb-fc6cc69e8f26
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 99%

---

# Dashboard-Manager

Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Bereitstellung planen.

>[!IMPORTANT]
>
>Als Best Practice für den Dashboard-Manager wird empfohlen, für einen Benutzer nicht mehr als 300 Dashboards zu verwenden. Beachten Sie auch, dass der Manager alle unten aufgeführten freigegebenen Dashboards lädt. Achten Sie daher auf eine sinnvolle Freigabe von Dashboards.

Klicken Sie auf **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Dashboards]**.

| Element | Beschreibung |
|--- |--- |
| Freigegeben | Zeigt an, ob das Dashboard freigegeben ist. |
| Eingeplant | Damit können Sie die Bereitstellung eines Dashboards einplanen. |
| Archiv anzeigen | Diese Funktion ist nicht mehr verfügbar. |
| An Benutzer senden | Hiermit können Sie ein Dashboard freigeben. |
| Verwalten | Hiermit können Sie ein Dashboard bearbeiten, kopieren und löschen. |

## Freigegebene Dashboards verwalten

Schritte, in denen beschrieben wird, wie Sie die Verwaltungsoptionen für freigegebene Dashboards verwenden.

1. Gehen Sie zu **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Dashboards]**.
1. Suchen Sie unter [!UICONTROL „Freigegebene Dashboards“] das freigegebene Dashboard (oder Legacy-Dashboard), das Sie verwalten möchten, und wählen Sie eine oder mehrere der folgenden Optionen:

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
  <td class="chdesc stentry"> <p>Die Server von SiteCatalyst 14 reagieren nicht mehr auf Dashboard Player-Datenanforderungen. Alle Dashboards, die derzeit im Dashboard Player angezeigt werden, können über die Standardoberfläche „Reports &amp; Analytics“ aufgerufen oder als Real-Time Dashboard neu erstellt werden. Real-Time Dashboards sind speziell für die kontinuierliche Anzeige konzipiert und enthalten einen Vollbildmodus für die Anzeige auf TV-Geräten oder anderen Geräten mit großen Bildschirmen. </p> <p>Erforderliche Benutzeraktion: Sie müssen aufhören, den Dashboard Player zu verwenden. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Kopier mich</strong></td> 
  <td class="chdesc stentry"> Fügt Ihrer Dashboard-Liste eine Kopie hinzu und verwendet dabei den gleichen Namen wie das Original. Sie können allerdings keine vom Eigentümer des Dashboards vorgenommenen Aktualisierungen/Änderungen sehen. Wenn Sie ein Legacy-Dashboard kopieren, wird ein leeres Dashboard geöffnet, in das Sie dann den Legacy-Inhalt einfügen können. <p>Wichtig: Wenn die von Ihnen am Dashboard vorgenommenen Änderungen für gemeinsame Benutzer nicht sichtbar sind, prüfen Sie Ihren Dashboard-Manager, um zu sehen, ob die Benutzer die Option <span class="uicontrol">Kopier mich</span> ausgewählt haben. Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. Um alle Änderungen/Updates sehen zu können, müssen gemeinsame Benutzer die Option <span class="uicontrol">Im Menü</span> im Dashboard-Manager auswählen. </p> </td> 
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

Sie können vorhandene Legacy-Dashboards weiterhin ausführen, bearbeiten, herunterladen und planen. Neue Legacy-Dashboards können Sie jedoch nicht mehr erstellen. Wir empfehlen Ihnen dringend, vorhandene Legacy-Dashboards auf das neue Dashboard-Format zu aktualisieren.

>[!NOTE]
>
>Sie sollten zukünftig in Erwägung ziehen, [Analysis Workspace-Projekte](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/home.html) und ihre Möglichkeit zum Herunterladen und Planen zu nutzen.

Beim Kopieren eines Legacy-Dashboards öffnet das System dieses zur Bearbeitung, wobei Sie Legacy-Inhalt oder neuen Inhalt hinzufügen können. Wenn Sie ein Legacy-Dashboard kopieren, bleibt das Original in der Liste der Legacy-Dashboards erhalten.

>[!NOTE]
>
>Durch das Hinzufügen von Legacy-Inhalt zu einem Dashboard wird ein Dashboard erstellt, das auf der aktuellen Dashboard-Funktion basiert. Das Legacy-Reportlet enthält jedoch eventuell Daten, die auf der vorherigen Datenplattform basieren.

**So migrieren Sie ein Legacy-Dashboard der Version 14.x**

1. Klicken Sie auf **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Dashboards verwalten]**.
1. Klicken Sie in der Spalte [!UICONTROL Verwalten] unter [!UICONTROL Legacy-Dashboards] auf **[!UICONTROL In neues Dashboard kopieren]**.

   Das kopierte Dashboard wird im Dashboard-Layout-Bearbeiter geöffnet.

   Siehe  [Bearbeiten von Dashboard- und Reportlet-Daten](/help/analyze/reports-analytics/dashboard.md).

## Dashboard freigeben

In diesen Schritten wird beschrieben, wie ein Administrator ein Dashboard für mehrere Benutzer freigeben (oder auf diese übertragen) kann. Wenn Sie Benutzern Dashboards senden, stehen die Dashboards diesen Benutzern in deren [!UICONTROL freigegebenen Dashboards] zur Verfügung.

1. Suchen Sie im [!UICONTROL Dashboard-Manager] das Dashboard und aktivieren Sie anschließend **[!UICONTROL Freigegeben]**.
1. Klicken Sie auf **[!UICONTROL An Benutzer senden]**.  ![](assets/push.png)

1. Wählen Sie auf der Seite [!UICONTROL Dashboard verschieben] die Zielbenutzer aus oder klicken Sie auf **[!UICONTROL Alle markieren]**.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn die von Ihnen am Dashboard vorgenommenen Änderungen für gemeinsame Benutzer nicht sichtbar sind, prüfen Sie Ihren Dashboard-Manager, um zu sehen, ob die Benutzer die Option **[!UICONTROL Kopier mich]** ausgewählt haben. Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. Um alle Änderungen/Updates sehen zu können, müssen gemeinsame Benutzer die Option **[!UICONTROL Im Menü]** im Dashboard-Manager auswählen.

## Bereitstellung eines Dashboards planen

Im [!UICONTROL Dashboard-Manager] können Sie sehen, ob ein Dashboard für die Auslieferung eingeplant ist, sowie den Plan bearbeiten. Die Dashboard-Auslieferungsoptionen sind identisch mit den Optionen für die Berichtsauslieferung.

1. Öffnen Sie ein Dashboard.
1. Klicken Sie auf **[!UICONTROL Mehr]** > **[!UICONTROL Senden]**.

   Weitere Informationen finden Sie unter [Planung und Verteilung](/help/analyze/reports-analytics/scheduling.md).

## Dashboard archivieren

>[!NOTE]
>
>Diese Funktion ist ab Januar 2020 nicht mehr verfügbar.

In diesen Schritten wird beschrieben, wie Sie ein gesendetes Dashboard als PDF-Datei archivieren können. Das System speichert die archivierte Datei zwei Jahre lang oder bis das 4-GB-Limit für archivierte Berichte erreicht wurde, je nachdem, was zuerst eintritt.

1. Öffnen Sie ein Dashboard.
1. Klicken Sie auf **[!UICONTROL Mehr]** > **[!UICONTROL Senden]**.
1. Aktivieren Sie in der Gruppe [!UICONTROL Bericht per E-Mail] die Option **[!UICONTROL Archiv]**.
1. Legen Sie die gewünschten Übermittlungsoptionen fest und klicken Sie anschließend auf **[!UICONTROL Senden]**.

   Archivierte Dashboards können Sie im Dashboard-Manager anzeigen. Alternativ können Sie ein Dashboard öffnen und auf **[!UICONTROL Mehr]** > **[!UICONTROL Archiv anzeigen]** klicken.
