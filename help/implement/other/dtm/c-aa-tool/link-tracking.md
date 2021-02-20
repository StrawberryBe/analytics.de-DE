---
description: Beschreibung der Felder des Dynamic Tag Managements für das Linktracking bei der Bereitstellung von Analytics.
keywords: Dynamic Tag Management;Linktracking;ClickMap aktivieren;Downloadlinks verfolgen;Download-Erweiterungen;ausgehende Links verfolgen;URL-Parameter beibehalten
solution: Experience Cloud,Analytics
title: Linktracking
uuid: 982b744b-5696-4c31-b1d1-410486b0eedd
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 100%

---


# Linktracking

Beschreibung der Felder des Dynamic Tag Managements für das Linktracking bei der Bereitstellung von Analytics.

**[!UICONTROL Eigenschaft]** > ![Zahnradsymbol](assets/settings_gear.png) **[!UICONTROL Tool bearbeiten]** > **[!UICONTROL Linktracking]**

<table id="table_F23FB0B284E74B66A107B1D69D22A51C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Element </th>
   <th colname="col2" class="entry"> Beschreibung </th>
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ClickMap aktivieren </td>
   <td colname="col2"> <p>Bestimmt, ob Daten zur Besucherklickzuordnung gesammelt werden. </p> <p>Siehe  <a href="../../../vars/config-vars/trackinlinestats.md">trackInlinestats</a>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Downloadlinks verfolgen </td>
   <td colname="col2"> <p>Verfolgt Links zu Dateien Ihrer Site, die heruntergeladen werden können. </p> <p>Siehe <a href="../../../vars/config-vars/trackdownloadlinks.md">trackDownloadLinks</a>.</p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> Download-Erweiterungen </td> 
   <td colname="col2"> <p>Wenn die Site Links zu Dateien mit einer der genannten Dateierweiterungen enthält, werden die URLs dieser Links im Bericht angezeigt. </p>Siehe <a href="../../../vars/config-vars/linkdownloadfiletypes.md">linkDownloadFileTypes</a>. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> Ausgehende Links verfolgen </td>
   <td colname="col2"> <p>Bestimmt, ob ein angeklickter Link ein Exitlink ist. </p> <p>Siehe <a href="../../../vars/config-vars/trackexternallinks.md">trackExternalLinks</a>. </p> <p><b>Hinweise zu einseitigen Apps:</b> Aufgrund der Art und Weise, auf die einige SPA-Websites codiert sind, kann ein interner Link zu einer Seite der SPA wie ein ausgehender Link aussehen. </p> <p>Sie können eine der folgenden Methoden zur Verfolgung ausgehender Links über SPA-Sites verwenden: </p>
    <ul id="ul_A4179633ED0644C3BA5F548A58CA4EC9">
     <li id="li_1959FBF14E42469FA8724B37EB58BC54"> <p>Sollten Sie über Ihre SPA keinesfalls ausgehende Links verfolgen wollen, machen Sie unter <span class="wintitle">Niemals verfolgen</span> einen entsprechenden Eintrag. </p> <p>Zum Beispiel <span class="filepath">https://testsite.com/spa/#</span> </p> <p>Alle #-Links für diesen Host werden ignoriert. Alle ausgehenden Links zu anderen Hosts wie <span class="filepath">https://www.google.com</span> werden verfolgt. </p> </li>
     <li id="li_37DD4D37887243FB928C9C04ACE9D39E"> <p>Gibt es einige Links, die Sie in Ihrer SPA immer verfolgen möchten, verwenden Sie den Abschnitt <span class="wintitle">Immer verfolgen</span>. </p> <p>Wenn Sie beispielsweise über die Seite <span class="filepath">spa/#/about</span> verfügen, könnten Sie unter <span class="wintitle">Immer verfolgen</span> den Abschnitt „about“ eintragen. </p> <p>Die Seite „about“ ist der einzige ausgehende Link, der verfolgt wird. Alle anderen Links auf der Seite (beispielsweise <span class="filepath">https://www.google.com</span>) werden nicht verfolgt. </p> </li>
    </ul> <p>Beachten Sie, dass sich diese beiden Optionen gegenseitig ausschließen. </p> </td> 
  </tr>
  <tr>
   <td colname="col1"> URL-Parameter beibehalten </td>
   <td colname="col2"> <p>Behält die Abfragezeichenfolge bei. </p> <p>Siehe <a href="../../../vars/config-vars/linkleavequerystring.md">linkLeaveQueryString</a>. </p> </td>
  </tr>
 </tbody>
</table>
