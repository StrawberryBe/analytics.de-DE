---
description: Beschreibung der Felder des Dynamic Tag Managements für das Linktracking bei der Bereitstellung von Analytics.
keywords: Dynamisches Tag-Management; Linktracking; clickmap aktivieren; Verfolgen von Download-Links; Download-Erweiterungen; Ausgehende Links verfolgen; URL-Parameter beibehalten
seo-description: Beschreibung der Felder des Dynamic Tag Managements für das Linktracking bei der Bereitstellung von Analytics.
seo-title: Linktracking
solution: Marketing Cloud, Analytics, dynamisches Tag-Management
title: Linktracking
uuid: 982 b 744 b -5696-4 c 31-b 1 d 1-410486 b 0 eedd
translation-type: tm+mt
source-git-commit: 1bc1c7a1e00d7b59cd39f368ac9afb745bea9e47

---


# Linktracking

Beschreibung der Felder des Dynamic Tag Managements für das Linktracking bei der Bereitstellung von Analytics.

**[!UICONTROL *`Property`*]** &gt;** [! UICONTROL ![](assets/settings_gear.png)

Edit Tool]** &gt; **[!UICONTROL Link Tracking]**

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
   <td colname="col2"> <p>Bestimmt, ob Daten zur Besucherklickzuordnung gesammelt werden. </p> <p>Siehe  <a href="../../../implement/js-implementation/c-variables/configuration-variables.md#concept_8FCA630706334F54B4DCB607378BCD00" format="dita" scope="local"> s.trackInlineStats</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Downloadlinks verfolgen </td> 
   <td colname="col2"> <p>Verfolgt die Links zu Dateien Ihrer Site, die heruntergeladen werden können. </p> <p>Siehe [Konfigurationsvariablen] (/help/implementing/js-implementation/c-variables/configuration-variables. md).</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download-Erweiterungen </td> 
   <td colname="col2"> <p>Wenn die Site Links zu Dateien mit einer der genannten Dateierweiterungen enthält, werden die URLs dieser Links im Bericht angezeigt. </p>Siehe [Konfigurationsvariablen] (/help/implementing/js-implementation/c-variables/configuration-variables. md). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ausgehende Links verfolgen </td> 
   <td colname="col2"> <p>Bestimmt, ob ein angeklickter Link ein Exitlink ist. </p> <p>Siehe [Konfigurationsvariablen] (/help/implementing/js-implementation/c-variables/configuration-variables. md). </p> <p><b>Hinweise zu einseitigen Apps:</b> Aufgrund der Art und Weise, auf die einige SPA-Websites codiert sind, kann ein interner Link zu einer Seite der SPA wie ein ausgehender Link aussehen. </p> <p>Sie können eine der folgenden Methoden zur Verfolgung ausgehender Links über SPA-Sites verwenden: </p> 
    <ul id="ul_A4179633ED0644C3BA5F548A58CA4EC9"> 
     <li id="li_1959FBF14E42469FA8724B37EB58BC54"> <p>Sollten Sie über Ihre SPA keinesfalls ausgehende Links verfolgen wollen, machen Sie unter <span class="wintitle">Niemals verfolgen</span> einen entsprechenden Eintrag. </p> <p>For example, <span class="filepath"> https://testsite.com/spa/#</span> </p> <p>Alle #-Links für diesen Host werden ignoriert. All outbound links to other hosts are tracked, such as <span class="filepath"> https://www.google.com</span>. </p> </li> 
     <li id="li_37DD4D37887243FB928C9C04ACE9D39E"> <p>Gibt es einige Links, die Sie in Ihrer SPA immer verfolgen möchten, verwenden Sie den Abschnitt <span class="wintitle">Immer verfolgen</span>. </p> <p>Wenn Sie beispielsweise über die Seite <span class="filepath">spa/#/about</span> verfügen, könnten Sie unter <span class="wintitle">Immer verfolgen</span> den Abschnitt „about“ eintragen. </p> <p>Die Seite „about“ ist der einzige ausgehende Link, der verfolgt wird. Any other links on the page (for example, <span class="filepath"> https://www.google.com</span>) are not tracked. </p> </li> 
    </ul> <p>Beachten Sie, dass sich diese beiden Optionen gegenseitig ausschließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URL-Parameter beibehalten </td> 
   <td colname="col2"> <p>Die Abfragezeichenfolgen bleiben erhalten. </p> <p>Siehe [Konfigurationsvariablen] (/help/implementing/js-implementation/c-variables/configuration-variables. md). </p> </td> 
  </tr> 
 </tbody> 
</table>

