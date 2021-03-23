---
description: Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.
title: 'Berechnete Metriken: Rollenbasierte Rechte'
uuid: 7c14d32d-370c-4afa-8f80-5bbd8fc12ec7
translation-type: ht
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: ht
source-wordcount: '256'
ht-degree: 100%

---


# Berechnete Metriken: Rollenbasierte Rechte

Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.

<table id="table_13F72FD90C964B86BD4B51E6F51ED292"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col02" class="entry"> Erstellung </th> 
   <th colname="col2" class="entry"> Freigeben </th> 
   <th colname="col3" class="entry"> Anzeigen/Verwalten </th> 
   <th colname="col4" class="entry"> Genehmigen </th> 
   <th colname="col5" class="entry"> Übernehmen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Benutzer der Administratorebene</b> </td> 
   <td colname="col02"> Administratoren können berechnete Metriken sowie <a href="https://docs.adobe.com/content/help/de-DE/analytics/admin/user-product-management/user-groups/groups.html"  >Gruppen</a> erstellen, um die Rechte von Benutzern zur Erstellung berechneter Metriken einzuschränken. </td> 
   <td colname="col2"> Können eine Freigabe für das gesamte Unternehmen, für Benutzergruppen und für einzelne Benutzer durchführen. </td> 
   <td colname="col3"> <span class="keyword"> Reports &amp; Analytics </span>: Können ihre eigenen berechneten Metriken und die anderer Benutzer anzeigen/bearbeiten/löschen usw. <p> <span class="keyword"> Report Builder </span>: Hiermit können Sie die eigenen berechneten sowie die freigegeben Metriken anzeigen/bearbeiten/löschen usw. </p> </td> 
   <td colname="col4"> Können berechnete Metriken als autorisiert genehmigen. </td> 
   <td colname="col5"> Können beliebige berechnete Metriken innerhalb der gesamten Organisation anwenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Benutzer, die nicht Mitglied der Administratorebene sind</b> </td> 
   <td colname="col02"> Standardmäßig können Benutzer berechnete Metriken erstellen. Diese Rechte können jedoch von Administratoren eingeschränkt werden. </td> 
   <td colname="col2"> Können nur für einzelne Benutzer freigeben. </td> 
   <td colname="col3"> Können nur nur ihre eigenen berechneten Metriken anzeigen/bearbeiten/löschen usw. <p>Nicht-Administratoren benötigen Zugriff auf alle Komponentenereignisse, um eine freigegebene Metrik anzeigen zu können (die Berechtigungen der Admin Console werden weiterhin durchgesetzt). </p> <p>Wenn ein Dashboard oder ein terminierter Bericht für einen Nicht-Administrator freigegeben wird, die Metrik für diesen Benutzer aber nicht freigegeben wurde, wird der Bericht mit angewendeter Metrik ausgeführt (vorausgesetzt, der Benutzer ist berechtigt, die Ereignisse anzuzeigen). Er kann allerdings nicht die Definition anzeigen oder die Metrik bearbeiten. </p> </td> 
   <td colname="col4"> Können ausschließlich genehmigte berechnete Metriken nutzen. Können keine Metriken als genehmigt markieren. </td> 
   <td colname="col5"> Können ihre eigenen berechneten Metriken und Segmente, die für sie freigegeben wurden, anwenden. </td> 
  </tr> 
 </tbody> 
</table>

