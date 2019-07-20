---
description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden
keywords: Dynamisches Tag-Management; Cookies; Besucher-ID; visitor namespace; Domänenpunkte; fp-Domänenpunkte; Transaktions-ID; Cookie-Lebensdauer
seo-description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden
seo-title: Cookies
solution: Marketing Cloud, Analytics, dynamisches Tag-Management
title: Cookies
uuid: 9 c 81 ecbb -0 f 02-4 c 1 a-a 5 a 5-426 cdea 57 f 38
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Cookies

Field descriptions for the Cookies global settings used for deploying [!UICONTROL Dynamic Tag Management] in Adobe Analytics.

**[!UICONTROL *`Property`*]** &gt;** [! UICONTROL ![](assets/settings_gear.png)

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
   <td colname="col1"> Besucher-ID </td> 
   <td colname="col2"> <p>Ein eindeutiger Wert, der in Online- und Offline-Systemen einen Kunden kennzeichnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchernamespace </td> 
   <td colname="col2"> <p>Variable zur Angabe der Domäne, bei der Cookies gesetzt werden </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> Domänenpunkte </td> 
   <td colname="col2"> <p>Die Domäne, in der die Analytics-Cookies <code>s_cc</code> und <code>s_sq</code> abgelegt sind. Es wird bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins zur Bestimmung der richtigen Domäne für Cookies der Plug-ins verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP-Domänenpunkte </td> 
   <td colname="col2"> <p>Die Variable <span class="term"> Die Variable "fpcookiedomainperiods</span> " dient für Cookies, die von javascript (<code> s_ sq</code>, <code> s_ cc</code>, Plug-Ins) gesetzt werden und von Erstanbietern stammen, selbst wenn Ihre Implementierung die Domänen <span class="filepath"> 2 o 7. net</span> oder <span class="filepath"> omtrdc. net</span> von Drittanbietern verwendet. </p> <p>See <a href="../../../implement/js-implementation/c-variables/configuration-variables.md#concept_8FCA630706334F54B4DCB607378BCD00" format="dita" scope="local"> s.fpCookieDomainPeriods</a>. </p> </td> 
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

