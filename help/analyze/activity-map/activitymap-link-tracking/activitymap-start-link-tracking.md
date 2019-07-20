---
description: Hier werden die Schritte zum Starten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.
seo-description: Hier werden die Schritte zum Starten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.
seo-title: Linktracking starten
solution: Analytics
title: Linktracking starten
topic: Activity Map
uuid: 425 cb 287-f 76 e -4430-802 f -288499711 ba 9
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Linktracking starten

Hier werden die Schritte zum Starten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.

<table id="table_1745199B3105467CBA26F50B3B1CCE99"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zum Starten von Linktracking in ... </th> 
   <th colname="col2" class="entry"> gehen Sie wie folgt vor: </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity Map </td> 
   <td colname="col2"> Fügen Sie den folgenden Inhalt aus der Datei Appmeasurement.js ein: 
    <code>/* START Activity Map MODULE Das folgende Modul aktiviert Activity Map-Verfolgung in Adobe Analytics.Mit Activity Map können Sie Datenüberlagerungen in Ihren Links und Inhalten anzeigen, um zu verstehen, wie Benutzer mit Ihrer Website interagieren.Wenn Sie Activity Map nicht verwenden möchten, können Sie den folgenden Codeblock aus Ihrer appmeasurement. js-Datei entfernen.
  Additional documentation on how to configure Activity Map is available at:
      https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/getting-started-admins.html
     */
     function AppMeasurement_Module_Activity Map(g){func
     ...
     /* END Activity Map MODULE */
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ClickMap (früher Besucher-ClickMap) </td> 
   <td colname="col2"> <p>Setzen Sie die Variable <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/trackInlineStats.html" format="https" scope="external">trackInlineStats</a> auf „true“. The syntax reads as follows: 
     <code>
       s.trackInlineStats=true
     </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

