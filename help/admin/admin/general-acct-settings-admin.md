---
description: Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.
seo-description: Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.
seo-title: Allgemeine Kontoeinstellungen
solution: Analytics
title: Allgemeine Kontoeinstellungen
topic: Admin Tools
uuid: c 1 ab 5 c 44-2 c 41-4 d 12-a 706-0 e 760 dff 8 a 95
translation-type: tm+mt
source-git-commit: 01ac0011f2e47e6798a520df8ffe5d8393ac0c3c

---


# Allgemeine Kontoeinstellungen

Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; Einstellungen **[!UICONTROL bearbeiten]** &gt; **[!UICONTROL Allgemein]** &gt; **[!UICONTROL Allgemeine Kontoeinstellungen]**

Diese Einstellungen umfassen Bearbeitungsoptionen für grundlegende Report Suite-Funktionen wie Name und Zeitzone.

<table id="table_5448A694DC0A48D2B20C7F1332509F6E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Option </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Site-Titel</span> </td> 
   <td colname="col2"> <p>Identifiziert die Website. Legen Sie für jede Report Suite einen eindeutigen Site-Titel fest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basis-URL</span> </td> 
   <td colname="col2"> <p>Gibt die Hauptwebsite der Report Suite an. Die Basis-URL hat keine Auswirkungen auf die Filterung des Referrers. Verwenden Sie stattdessen <a href="../../admin/admin/internal-url-filter-admin.md#concept_D6BB8358DB7643F0B13E5DC9B7607998" format="dita" scope="local"> interne URL-Filter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Zeitzone</span> </td> 
   <td colname="col2"> <p>Dies wirkt sich auf das Datum und die Uhrzeit aus, die mit Ihren Berichtdaten verbunden werden. </p> <p>Durch das Ändern der Zeitzone bei einer Live-Report Suite ergibt sich entweder eine Spitze oder Lücke in den Berichtdaten. Um die Auswirkungen so gering wie möglich zu halten und keine Daten zu verfälschen, empfiehlt Adobe, die Zeitzonen außerhalb der besonders datenintensiven Zeiten zu ändern. </p> <p>Wenn Sie beispielsweise um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Pacific Standard Time“ (US-Westküste) ändern, ändert sich die aktuelle Uhrzeit in 13 Uhr. Da die Berichterstellung bereits Daten für 13 Uhr gesammelt hat, kommt es für den Zeitraum zwischen 13 und 15 Uhr zu Traffic-Spitzen. </p> <p>Wenn Sie umgekehrt um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Eastern Standard Time“ (US-Ostküste) ändern, ändert sich die aktuelle Uhrzeit in 16 Uhr. In diesem Fall werden in den Berichten für den Zeitraum zwischen 15 und 16 Uhr am Tag der Zeitänderung keine Daten angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Konversionsstufe</span> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert E-Commerce-Variablen wie eVars und Kampagnen. Verwenden Sie die Option <span class="uicontrol">Aktiviert, kein Warenkorb</span>, um alle Warenkorbberichte auszublenden, wenn Sie keinen Warenkorb auf Ihrer Site haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Standardseite</span> </td> 
   <td colname="col2"> <p> Wenn der Bericht <span class="wintitle">Bevorzugte Seiten</span> URL-Adressen statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Web-Seite mehrere URL-Adressen angegeben werden. For example, the URLs <span class="filepath"> https://mysite.com</span> and <span class="filepath"> https://mysite.com/index.html</span> are typically the same page. You can remove default filenames so that these two URLs would both show up as <span class="filepath"> https://mysite.com</span>. </p> <p>Wenn Sie das Feld leer lassen, werden folgende Dateinamen aus den URLs entfernt: <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> und <span class="filepath">home.asp</span>. </p> <p>Um das Entfernen von Dateinamen ganz zu deaktivieren, geben Sie einen Wert ein, der in Ihren URLs nicht vorkommt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Letztes Oktett der IP-Adresse durch 0 ersetzen </span> </td> 
   <td colname="col2"> <p>Das letzte Oktett wird vor der IP-Filterung entfernt. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten angepasst werden, um IP-Adressen mit einer Null am Ende zu berücksichtigen. Übereinstimmung * sollte mit 0 übereinstimmen. </p> <p>Wenn Sie diese Option auswählen, wird die IP-Adresse geändert, bevor sie verarbeitet wird. Die IP-Adresse 134.123.567.780 wird beispielsweise auf 134.123.567.0 geändert. Die Geosegmentierungs-Daten sind dann nicht ganz so präzise wie bei Verwendung der vollständigen IP-Adresse. Insbesondere ist die Genauigkeit der Stadt stärker betroffen als die Genauigkeit des Landes oder der Region. Sowohl Bot-Regeln als auch VISTA-Regeln sind davon betroffen, da die vollständige IP-Adresse nicht mehr zur Verfügung steht. Außerdem wirkt sich diese Einstellung auf IP-basierte Verarbeitungsregeln aus, einschließlich der Marketingkanalregeln und der Verarbeitungsregeln für die Report Suite. </p> <p>Hinweis: Diese Einstellung ist standardmäßig für alle neuen Report Suites aktiviert, die ab Januar 2019 im London Data Center erstellt wurden – jedoch nur dann, wenn die Einstellungen für diese Report Suites aus einer Vorlage kopiert werden, die in der Admin Console aufgeführt ist. Report Suites mit Einstellungen, die aus anderen Report Suites dupliziert wurden, erben alle Einstellungen der ausgewählten Report Suite. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> IP-Verschleierung</span> </td> 
   <td colname="col2"> <p>Verwandelt IP-Adressen in nicht erkennbare Zeichenketten, was sie letztendlich aus den Adobe Datenspeichern löscht. Wenn die IP-Verschleierung aktiviert ist, geht die ursprüngliche IP-Adresse dauerhaft verloren. </p> <p>Hinweis: Die IP-Adressen werden überall in Analytics verschleiert, auch im Data Warehouse. Die IP-Einstellung in Target wird jedoch separat gesteuert. Diese Einstellung hat also keine Auswirkung auf Target. </p> <p>Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie IP-Verschleierung aktivieren. </p> <p>Wenn <span class="uicontrol">Deaktiviert</span> ausgewählt wird, bleibt die IP-Adresse in den Daten. </p> <p>Wenn Sie <span class="uicontrol">IP-Adresse verschleiern</span> aktivieren, wird die IP in einen Hash-Wert geändert (z. B. 234abc6493872038). </p> <p>Wenn Sie <span class="uicontrol">IP-Adresse löschen</span> aktivieren, wird die IP-Adresse nach der Geo-Suche in den Daten durch x.x.x.x ersetzt. </p> <p>Hinweis: Diese Einstellung erfordert möglicherweise Änderungen an benutzerdefinierten <a href="../../admin/admin/bot-removal/bot-rules.md#concept_A306689C65EB4D0F9AE65E3FD48ED5F7" format="dita" scope="local"> Bot-Regeln</a> oder<a href="../../admin/admin/exclude-ip.md#concept_265A95A803F740629CAAAA7EB8BE81A4" format="dita" scope="local"> IP-Ausschlüssen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Transaktions-ID-Speicher</span> </td> 
   <td colname="col2"> <p>Ermöglicht die Verwendung von <a href="https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html?f=c_Transaction_ID" format="https" scope="external">Transaktions-ID</a>-Data Sources. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Ad Hoc Analysis aktivieren</span> </td> 
   <td colname="col2"> <p>Gibt an, ob die betreffende Report Suite in Ad Hoc Analysis als verfügbare Report Suite angezeigt wird. Verwenden Sie diese Einstellung, um einzugrenzen, welche Report Suites als eine Option für Ad Hoc Analysis angezeigt werden. Sie können beispielsweise Ad Hoc Analysis für Entwicklungs- und QA-Report Suites deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td><span class="wintitle"> Data Warehouse aktivieren</span> </td> 
   <td colname="col2"> <p>Aktiviert die Data Warehouse-Benutzeroberfläche unter <span class="uicontrol">Tools</span> &gt; <span class="uicontrol">Data Warehouse</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

