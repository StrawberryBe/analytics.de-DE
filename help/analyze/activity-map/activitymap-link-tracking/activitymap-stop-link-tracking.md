---
description: Hier werden die Schritte zum Anhalten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.
seo-description: Hier werden die Schritte zum Anhalten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.
seo-title: Linktracking stoppen
solution: Analytics
title: Linktracking stoppen
topic: Activity Map
uuid: e 17 fb 7 bd-d 6 ed -45 c 3-a 006-9150 d 5718 cff
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Linktracking stoppen

Hier werden die Schritte zum Anhalten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.

<table id="table_1745199B3105467CBA26F50B3B1CCE99"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zum Anhalten von Linktracking in ... </th> 
   <th colname="col2" class="entry"> gehen Sie wie folgt vor: </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity Map </td> 
   <td colname="col2"> Entfernen Sie den folgenden Inhalt aus der Datei Appmeasurement.js: 
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
   <td colname="col2"> <p>Setzen Sie die Variable <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/trackInlineStats.html" format="https" scope="external">trackInlineStats</a> auf „false“ (Standardeinstellung). The syntax reads as follows: 
     <code>
       s.trackInlineStats=false
     </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

