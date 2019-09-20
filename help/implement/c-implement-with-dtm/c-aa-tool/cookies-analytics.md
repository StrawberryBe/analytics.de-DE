---
description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden
keywords: Dynamisches Tag-Management;Cookies;Besucher-ID;Besucher-Namespace;Domänenzeiträume;fp-Domänenzeiträume;Transaktions-ID;Cookie-Lebensdauer
seo-description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden
seo-title: Cookies
solution: Experience Cloud, Analytics, Dynamisches Tag-Management
title: Cookies
uuid: 9c81ecbb-0f02-4c1a-a5a5-426cdea57f38
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Cookies

Field descriptions for the Cookies global settings used for deploying [!UICONTROL Dynamic Tag Management] in Adobe Analytics.

**[!UICONTROL *`Property`*]** &gt; **[!UICONTROL ![](assets/settings_gear.png)

Edit Tool]** &gt; **[!UICONTROL Cookies]**

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Visitor ID </td> 
   <td colname="col2"> <p>Ein eindeutiger Wert, der in Online- und Offline-Systemen einen Kunden kennzeichnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchernamespace </td> 
   <td colname="col2"> <p>Variable zur Angabe der Domäne, bei der Cookies gesetzt werden </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> Domänenpunkte </td> 
   <td colname="col2"> <p>Die Domäne, in der die Analytics-Cookies <code>s_cc</code> und <code>s_sq</code> abgelegt sind. Es wird bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP-Domänenpunkte </td> 
   <td colname="col2"> <p>Die Variable <span class="term"> fpCookieDomainPeriods</span> variable is for cookies set by JavaScript (<code> s_sq</code>, <code> s_cc</code>, plug-ins) that are inherently first-party cookies, even if your implementation uses the third-party <span class="filepath"> 2o7.net</span> or <span class="filepath"> omtrdc.net</span> domains. </p> <p>Siehe <a href="../../../implement/js-implementation/c-variables/configuration-variables.md#concept_8FCA630706334F54B4DCB607378BCD00" format="dita" scope="local"> s.fpCookieDomainPeriods</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transaktions-ID </td> 
   <td colname="col2"> <p>Ein eindeutiger Wert, der eine Online-Transaktion kennzeichnet, die zu einer Offline-Aktivität geführt hat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Cookie-Lebensdauer </td> 
   <td colname="col2"> <p>Gibt die Lebensdauer eines Cookies an. </p> </td> 
  </tr> 
 </tbody> 
</table>

