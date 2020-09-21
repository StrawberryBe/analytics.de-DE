---
description: Verwenden Sie Feldbeschreibungen im Dynamic Tag Management zur Anpassung des Seiten-Codes bei der Bereitstellung von Analytics.
keywords: Dynamic Tag Management;customize page code;open editor;execute
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Seiten-Code anpassen
uuid: b7cad069-3eb8-4388-b0b0-34f54001e05f
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '101'
ht-degree: 100%

---


# Seiten-Code anpassen

Verwenden Sie Feldbeschreibungen im Dynamic Tag Management zur Anpassung des Seiten-Codes bei der Bereitstellung von Analytics.

**[!UICONTROL `Property`]** > **[!UICONTROL Tool bearbeiten]** ![](assets/settings_gear.png) > **[!UICONTROL Seiten-Code anpassen]**

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
   <td colname="col2"> <p>Sie können einen beliebigen JavaScript-Aufruf einfügen, der vor dem finalen <code> s.t()</code>-Aufruf ausgelöst werden muss, der im <code> s_code</code> enthalten ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Starte </p> </td> 
   <td colname="col2"> <p> <b>Vor UI-Einstellungen</b>: Benutzeroberflächeneinstellungen haben Priorität vor dem benutzerdefinierten Code (beispielsweise wenn Sie eine eVar aufheben möchten, wenn eine Einstellung in der Benutzeroberfläche aktiviert wurde). </p> <p> <b>Nach UI-Einstellungen</b>: Benutzerdefinierter Code hat Priorität vor Benutzeroberflächeneinstellungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

