---
description: Hier werden die Schritte zum Anhalten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.
title: Linktracking beenden
topic: Activity map
uuid: e17fb7bd-d6ed-45c3-a006-9150d5718cff
translation-type: ht
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16
workflow-type: ht
source-wordcount: '74'
ht-degree: 100%

---


# Linktracking beenden

Hier werden die Schritte zum Anhalten der Linktracking-Funktion in Activity Map oder der älteren Version ClickMap aufgeführt.

<table id="table_1745199B3105467CBA26F50B3B1CCE99"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zum Anhalten von Linktracking in... </th> 
   <th colname="col2" class="entry"> Führen Sie folgende Schritte aus... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity Map </td> 
   <td colname="col2"> Entfernen Sie den folgenden Inhalt aus der Datei Appmeasurement.js: 
     
    <code>
     /*
     &nbsp;START&nbsp;Activity&nbsp;Map&nbsp;MODULE&nbsp;The&nbsp;following&nbsp;module&nbsp;enables&nbsp;Activity&nbsp;Map&nbsp;tracking&nbsp;in&nbsp;Adobe&nbsp;Analytics.&nbsp;Activity&nbsp;Map
     &nbsp;allows&nbsp;you&nbsp;to&nbsp;view&nbsp;data&nbsp;overlays&nbsp;on&nbsp;your&nbsp;links&nbsp;and&nbsp;content&nbsp;to&nbsp;understand&nbsp;how
     &nbsp;users&nbsp;engage&nbsp;with&nbsp;your&nbsp;web&nbsp;site.&nbsp;If&nbsp;you&nbsp;do&nbsp;not&nbsp;intend&nbsp;to&nbsp;use&nbsp;Activity&nbsp;Map,&nbsp;you
     &nbsp;can&nbsp;remove&nbsp;the&nbsp;following&nbsp;block&nbsp;of&nbsp;code&nbsp;from&nbsp;your&nbsp;AppMeasurement.js&nbsp;file.
     &nbsp;Additional&nbsp;documentation&nbsp;on&nbsp;how&nbsp;to&nbsp;configure&nbsp;Activity&nbsp;Map&nbsp;is&nbsp;available&nbsp;at:
     &nbsp;https://docs.adobe.com/content/help/en/analytics/analyze/activity-map/getting-started/get-started-admins/activitymap-enable.html
     */
     function&nbsp;AppMeasurement_Module_Activity&nbsp;Map(g){func
     ...
     /*&nbsp;END&nbsp;Activity&nbsp;Map&nbsp;MODULE&nbsp;*/
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ClickMap (früher Besucher-ClickMap) </td> 
   <td colname="col2"> <p>Setzen Sie die Variable <a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/config-vars/configuration-variables.html"  >trackInlineStats</a> auf „false“ (Standardeinstellung). Die Syntax lautet wie folgt: 
     <code>
       s.trackInlineStats=false
     </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

