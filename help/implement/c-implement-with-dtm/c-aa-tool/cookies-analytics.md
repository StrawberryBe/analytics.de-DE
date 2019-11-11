---
description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden.
keywords: Dynamic Tag Management;Cookies;Besucher-ID;Besucher-Namespace;Domänenpunkte;FP-Domänenpunkte;Transaktions-ID;Cookie-Lebensdauer
seo-description: Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des Dynamic Tag Managements in Adobe Analytics verwendet werden.
seo-title: Cookies
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Cookies
uuid: 9c81ecbb-0f02-4c1a-a5a5-426cdea57f38
translation-type: tm+mt
source-git-commit: 9b946238b48fa4532d136d2f7aa0187fdabd005b

---


# Cookies

Beschreibung der Felder für die globalen Cookie-Einstellungen, die für die Bereitstellung des [!UICONTROL Dynamic Tag Managements] in Adobe Analytics verwendet werden.

*`Property`* &gt; Tool bearbeiten &gt; Cookies

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
   <td colname="col2"> <p>Die Domäne, in der die Analytics-Cookies <code> s_cc</code> und <code> s_sq</code> abgelegt sind. Es wird bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP-Domänenpunkte </td> 
   <td colname="col2"> <p>Die Variable <span class="term"> fpCookieDomainPeriods</span> variable is for cookies set by JavaScript (<code> s_sq</code>, <code> s_cc</code>, plug-ins) that are inherently first-party cookies, even if your implementation uses the third-party <span class="filepath"> 2o7.net</span> or <span class="filepath"> omtrdc.net</span> domains. </p> <p>Siehe <a href="/help/implement/js-implementation/c-variables/configuration-variables.md"  > s.fpCookieDomainPeriods</a>. </p> </td> 
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

