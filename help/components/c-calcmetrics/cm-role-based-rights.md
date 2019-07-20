---
description: Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.
seo-description: Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.
seo-title: Rollenbasierte Berechtigungen für berechnete Metriken
title: Rollenbasierte Berechtigungen für berechnete Metriken
uuid: 7 c 14 d 32 d -370 c -4 afa -8 f 80-5 bbd 8 fc 12 ec 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Berechnete Metriken: rollenbasierte Rechte

Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.

<table id="table_13F72FD90C964B86BD4B51E6F51ED292"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col02" class="entry"> Erstellung     </th> 
   <th colname="col2" class="entry"> Freigabe </th> 
   <th colname="col3" class="entry"> Anzeigen/Verwalten </th> 
   <th colname="col4" class="entry"> Genehmigen </th> 
   <th colname="col5" class="entry"> Übernehmen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Benutzer der Administratorebene</b> </td> 
   <td colname="col02"> Administratoren können berechnete Metriken sowie <a href="https://marketing.adobe.com/resources/help/en_US/reference/groups.html" format="https" scope="external">Gruppen</a> erstellen, um die Rechte von Benutzern zur Erstellung berechneter Metriken einzuschränken. </td> 
   <td colname="col2"> Können eine Freigabe für das gesamte Unternehmen, für Benutzergruppen und für einzelne Benutzer durchführen. </td> 
   <td colname="col3"> <span class="keyword"> [! UICONTROL Reports &amp; Analysen] </span>: Kann angezeigt/bearbeitet/gelöscht usw. ihre eigenen berechneten Metriken und die anderer Benutzer anzeigen/bearbeiten/löschen usw. <p> <span class="keyword">Ad Hoc Analysis</span> und <span class="keyword">Report Builder</span>: Können ihre eigenen berechneten Metriken und die, die für sie freigegeben wurden, anzeigen/bearbeiten/löschen usw. </p> </td> 
   <td colname="col4"> Können berechnete Metriken als autorisiert genehmigen. </td> 
   <td colname="col5"> Können beliebige berechnete Metriken innerhalb der gesamten Organisation anwenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Benutzer, die nicht Mitglied der Administratorebene sind</b> </td> 
   <td colname="col02"> Standardmäßig können Benutzer berechnete Metriken erstellen. Diese Rechte können jedoch von Administratoren eingeschränkt werden. </td> 
   <td colname="col2"> Können nur für einzelne Benutzer freigeben. </td> 
   <td colname="col3"> Können nur ihre eigenen berechneten Metriken anzeigen/bearbeiten/löschen usw. <p>Nicht-Administratoren benötigen Zugriff auf alle Komponentenereignisse, um eine freigegebene Metrik anzeigen zu können (die Berechtigungen der Admin Console werden weiterhin durchgesetzt). </p> <p>Wenn ein Dashboard oder ein terminierter Bericht für einen Nicht-Administrator freigegeben wird, die Metrik für diesen Benutzer aber nicht freigegeben wurde, wird der Bericht mit angewendeter Metrik ausgeführt (vorausgesetzt, der Benutzer ist berechtigt, die Ereignisse anzuzeigen). Er kann allerdings nicht die Definition anzeigen oder die Metrik bearbeiten. </p> </td> 
   <td colname="col4"> Können ausschließlich genehmigte berechnete Metriken nutzen. Können keine Metriken als genehmigt markieren. </td> 
   <td colname="col5"> Können ihre eigenen berechneten Metriken und Segmente, die für sie freigegeben wurden, anwenden. </td> 
  </tr> 
 </tbody> 
</table>

