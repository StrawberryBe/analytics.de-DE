---
description: Beschreibung der Felder des Dynamic Tag Managements für Referrer- und Kampagnenoptionen bei der Bereitstellung des Dynamic Tag Managements in Adobe Analytics.
keywords: Dynamisches Tag-Management;Referrer;Kampagnen;Überschreiben der verweisenden Stelle;Kampagnenvariable;Abfrageparameter
seo-description: Beschreibung der Felder des Dynamic Tag Managements für Referrer- und Kampagnenoptionen bei der Bereitstellung des Dynamic Tag Managements in Adobe Analytics.
seo-title: Referrer und Kampagnen
solution: Experience Cloud, Analytics, Dynamisches Tag-Management
title: Referrer und Kampagnen
uuid: 56580206-a382-4993-9bba-a488da65cf89
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Referrer und Kampagnen

Field descriptions in [!UICONTROL Dynamic Tag Management] for referrers and campaign options when deploying [!UICONTROL Dynamic Tag Management] in Adobe [!DNL Analytics].

**[!UICONTROL *`Property`*]** &gt; Tool ![](assets/settings_gear.png) bearbeiten **[!UICONTROL &gt;]****[!UICONTROL Verweisende Stellen und Kampagnen]**

<table id="table_09AE3BFF0F12442F9C19CD96451F93E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verweisende Stelle überschreiben </td> 
   <td colname="col2"> <p>Überschreibt den Wert, der in der Variable <span class="varname"> s.referrer</span> variable, which is typically populated by the referrer set in the browser. </p> <p>Siehe [Seitenvariablen](/help/implement/js-implementation/c-variables/page-variables.md). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kampagne </td> 
   <td colname="col2"> <p>Eine Variable, die Marketing-Kampagnen kennzeichnet, über die Besucher zu Ihrer Website gelangen. Der Wert einer Kampagne wird normalerweise einem Abfragezeichenfolgen-Parameter entnommen. </p> <p>Siehe [Seitenvariablen](/help/implement/js-implementation/c-variables/page-variables.md). </p> </td> 
  </tr> 
 </tbody> 
</table>

Verwenden Sie die DTM-Oberfläche, um auszuwählen, ob eine Abfragezeichenfolge oder ein Wert (bezogen aus einem Datenelement) verwendet werden soll oder nicht:

![](assets/dtm-queryparam.png)

Sie können entweder die Abfragezeichenfolge direkt über die Oberfläche eingeben oder sich auf ein anderes Datenelement beziehen, wenn Sie Kampagnen auf andere Art und Weise verfolgen.
