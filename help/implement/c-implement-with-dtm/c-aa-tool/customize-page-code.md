---
description: Verwenden Sie Feldbeschreibungen im Dynamic Tag Management zur Anpassung des Seiten-Codes bei der Bereitstellung von Analytics.
keywords: Dynamisches Tag-Management; Seiten-Code anpassen; Editor öffnen; execute
seo-description: Verwenden Sie Feldbeschreibungen im Dynamic Tag Management zur Anpassung des Seiten-Codes bei der Bereitstellung von Analytics.
seo-title: Seiten-Code anpassen
solution: Marketing Cloud, Analytics, Target, Dynamisches Tag-Management
title: Seiten-Code anpassen
uuid: b 7 cad 069-3 eb 8-4388-b 0 b 0-34 f 54001 e 05 f
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Seiten-Code anpassen

Verwenden Sie Feldbeschreibungen im Dynamic Tag Management zur Anpassung des Seiten-Codes bei der Bereitstellung von Analytics.

Fügen Sie Plugins hinzu, um zu gewährleisten, dass der Code zur gleichen Zeit wie das Analytics-Tool ausgeführt wird. Weitere Informationen zu den Analytics-Plug-ins finden Sie unter [Plug-ins für Implementierungen](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

**[!UICONTROL *`Property`*]** &gt;** [! UICONTROL ![](assets/settings_gear.png)

Edit Tool]** &gt; **[!UICONTROL Customize Page Code]**

<table id="table_A4676A5FEE814DF9A05DA0E56F8B4C6D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Editor öffnen </p> </td> 
   <td colname="col2"> <p>Sie können einen beliebigen JavaScript-Aufruf einfügen, der vor dem finalen <code>s.t()</code>-Aufruf ausgelöst werden muss, der im <code>s_code</code> enthalten ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Starte </p> </td> 
   <td colname="col2"> <p> <b>Vor UI-Einstellungen</b>: Benutzeroberflächeneinstellungen haben Priorität vor dem benutzerdefinierten Code (beispielsweise wenn Sie eine eVar aufheben möchten, wenn eine Einstellung in der Benutzeroberfläche aktiviert wurde). </p> <p> <b>Nach UI-Einstellungen</b>: Benutzerdefinierter Code hat Priorität vor Benutzeroberflächeneinstellungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

