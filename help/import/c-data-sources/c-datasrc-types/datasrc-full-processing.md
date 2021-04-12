---
description: Data Sources unterstützt die folgenden Variablen bei der Verarbeitung von Daten als Standard-Server-Aufruf („Generisch“ > „Vollständige Verarbeitung“).
title: Vollständige Verarbeitung
topic: Entwickler und Implementierung
exl-id: 9eb8c754-f4de-4483-934e-3f79134516ca
translation-type: tm+mt
source-git-commit: 4e8a79648b0573e68d9059c518f6ec8fb3d9a694
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 96%

---

# Vollständige Verarbeitung

>[!IMPORTANT]
>
>Adobe empfiehlt Kunden, die [Bulk Data Insertion API (BDIA)](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) anstelle von Datenquellen mit vollständiger Verarbeitung zu verwenden. Adobe plant, Datenquellen mit vollständiger Verarbeitung am 31. Juli 2021 zu veraltet. [Weitere Infos](/help/import/c-data-sources/c-datasrc-types/datasrc-fullproc-eol.md)

Data Sources unterstützt die folgenden Variablen bei der Verarbeitung von Daten als Standard-Server-Aufruf („Generisch“ > „Vollständige Verarbeitung“).

Daten aus Datenquellen mit vollständiger Verarbeitung werden so verarbeitet, wie das beim Empfang von Adobe-Servern zum angegebenen Zeitpunkt (jeder Treffer enthält einen Zeitstempel) der Fall wäre.

* [Besucherprofil](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_6065627D0C144506965F562C80AE67F8)
* [Spaltenreferenz](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_92BAE76639E3404E97276B1BE0581078)

## Besucherprofil {#section_6065627D0C144506965F562C80AE67F8}

Daten aus Datenquellen mit vollständiger Verarbeitung werden mit getrennten Besucherprofilen verarbeitet. Das heißt, selbst wenn die Besucher-ID in den hochgeladenen Daten mit den Daten übereinstimmt, die mit JavaScript oder einer anderen AppMeasurement-Bibliothek erfasst wurden, sind die Benutzerprofile aus der Sicht einer eVar-Zuordnung nicht miteinander verbunden.

Beispiel: Ein Benutzer mit der Besucher-ID `"user@example.com"` besucht Ihre Site von einer Marketing-Kampagne mit der Bezeichnung „Spring Sale“ aus, die in der Kampagnenvariable gespeichert ist. Wenn Sie später eine Transaktion mit derselben Besucher-ID hochladen, erhält die Kampagne „Spring Sale“ keine Gutschriften für jegliche Umsätze oder Erfolgsereignisse, die mit Datenquellen mit vollständiger Verarbeitung hochgeladen wurden.

## Spaltenreferenz {#section_92BAE76639E3404E97276B1BE0581078}

<table id="table_AAC04491D643467B9C80FDEF88130B13"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> JavaScript-Variable </th> 
   <th colname="col2" class="entry"> Variable für Spalte „Volle Verarbeitung“ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>campaign </p> </td> 
   <td colname="col2"> <p>Kampagne </p> </td> 
   <td colname="col3"> <p>Konversion-Kampagnen-Trackingcode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>channel </p> </td> 
   <td colname="col2"> <p>Kanal </p> </td> 
   <td colname="col3"> <p>Kanal-Zeichenfolge (z. B. Sportabteilung). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>currencyCode </p> <p>Hinweis: Diese Variable wird auch von Standarddatenquellen als <code> currency code </code> unterstützt. </p> </td> 
   <td colname="col3"> <p>Währungscode für Umsatz (z. B. USD). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timestamp </p> </td> 
   <td colname="col2"> <p>Datum </p> </td> 
   <td colname="col3"> <p>Verwenden Sie das ISO 8601-Datumsformat <code> YYYY-MM-DDThh:mm:ss±UTC_offset </code> (z. B. <code> 2013-09-01T12:00:00-07:00 </code>) oder das Unix-Zeitformat (d. h. die seit dem 1. Januar 1970 abgelaufenen Sekunden). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eVar<i>N</i> </p> </td> 
   <td colname="col2"> <p>eVar<i>N</i>, z. B. &lt;eVar2&gt;…&lt;/eVar2&gt; </p> </td> 
   <td colname="col3"> <p>Konversion-eVar-Name. Sie können über bis zu 75 eVars verfügen (  <span class="varname"> eVar1 </span> bis <span class="varname"> eVar75 </span>). </p> <p>Sie können den eVar-Namen (eVar12) oder einen benutzerfreundlichen Namen (Werbekampagne 3) festlegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>events </p> </td> 
   <td colname="col2"> <p>Ereignisse </p> </td> 
   <td colname="col3"> <p>Ereigniszeichenfolge, mit derselben Syntax für die Variable <a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/events/event-serialization.html"  >s.events</a> formatiert. </p> <p>Beispiel: </p> 
    <code>
      scAdd,event1,event7 
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hier<i>N</i> </p> </td> 
   <td colname="col2"> <p>hier<i>N</i>, z. B. &lt;hier2&gt;…&lt;/hier2&gt; </p> </td> 
   <td colname="col3"> <p>Hierarchiename. Sie können über bis zu 5 Hierarchien verfügen (  <span class="varname"> hier1</span> - <span class="varname">hier5 </span>). </p> <p>Sie können den Standardhierarchienamen (<span class="varname">hier2</span>) oder einen benutzerfreundlichen Namen (<span class="term">Yankees</span>) festlegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkName </p> </td> 
   <td colname="col2"> <p>linkName </p> </td> 
   <td colname="col3"> <p>Name des Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkType </p> </td> 
   <td colname="col2"> <p>linkType </p> </td> 
   <td colname="col3"> <p>Art des Links. Folgende Werte werden unterstützt: </p> 
    <ul id="ul_E441013055A9447AB6C3FB05B6099F7D"> 
     <li id="li_A33F66F30B60479284F72AE3AD4BF499"> <b>d</b>: Download-Link </li> 
     <li id="li_182F695AA2D044DAB036BAFE38BC3915"> <b>e</b>: Exitlink </li> 
     <li id="li_4FD4D542D1774607860BEF41C1B090D1"> <b>o</b>: Benutzerdefinierter Link. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkURL </p> </td> 
   <td colname="col2"> <p>linkURL </p> </td> 
   <td colname="col3"> <p>HREF des Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageName </p> </td> 
   <td colname="col2"> <p>pageName </p> </td> 
   <td colname="col3"> <p>Seitenname </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageType </p> </td> 
   <td colname="col2"> <p>pageType </p> </td> 
   <td colname="col3"> <p>Seitentyp („Fehlerseite“). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageURL </p> </td> 
   <td colname="col2"> <p>pageURL </p> </td> 
   <td colname="col3"> <p>Seiten-URL (z. B. <code>https://www.example.com/index.html)</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>products </p> </td> 
   <td colname="col2"> <p>products </p> </td> 
   <td colname="col3"> <p>Liste des Produkts (z. B. <code> "Sports;Ball;1;5.95"</code>). Kann maximal 4096 Byte pro Zeile enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prop1 – prop75 </p> </td> 
   <td colname="col2"> <p>prop<i>N</i>, z. B. &lt;prop2&gt;…&lt;/prop2&gt; </p> </td> 
   <td colname="col3"> <p>Property#-Zeichenfolge (z. B.  <span class="term"> Sportbereich </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>purchaseID </p> </td> 
   <td colname="col2"> <p>purchaseID </p> </td> 
   <td colname="col3"> <p>Kauf-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>s_account </p> </td> 
   <td colname="col2"> <p>reportSuiteID </p> </td> 
   <td colname="col3"> <p>Bericht-Suite-ID(s), der der Hit zugeordnet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server </p> </td> 
   <td colname="col2"> <p>server </p> </td> 
   <td colname="col3"> <p>Serverzeichenfolge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>state </p> </td> 
   <td colname="col2"> <p>state </p> </td> 
   <td colname="col3"> <p>Konversion-Status-Zeichenfolge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zip </p> </td> 
   <td colname="col2"> <p>zip </p> </td> 
   <td colname="col3"> <p>Konversion-PLZ. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgende Tabelle enthält Traffic-Variablen, die automatisch ausgefüllt werden, wenn Sie JavaScript-Bibliotheken verwenden. Diesen Eigenschaften sind keine Variablen zugeordnet, aber sie können mit Datenquellen importiert werden.

<table id="table_FDBC5BD225644AA09078C0570BE709FE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Variable für Spalte „Volle Verarbeitung“ </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>browserHeight </p> </td> 
   <td colname="col2"> <p>Browser-Höhe in Pixel (z. B. 768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>browserWidth </p> </td> 
   <td colname="col2"> <p>Browser-Breite in Pixel (z. B. 1024). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>charSet </p> </td> 
   <td colname="col2"> <p>Der für Ihre Website unterstützte Zeichensatz. Beispiel: UTF-8, ISO-8859-1 usw. </p> <p>Eine vollständige Liste finden Sie im Whitepaper <a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/config-vars/configuration-variables.html#concept_E65B9A8F75C3482C87D0D455805F89BD"  >Multi-Byte Character Sets</a> (Internationalisierung). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickAction </p> </td> 
   <td colname="col2"> <p>Objekt-ID für Besucher-ClickMap (oid). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickActionType </p> </td> 
   <td colname="col2"> <p>Objekt-ID-Typ für Besucher-ClickMap (oidt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContext </p> </td> 
   <td colname="col2"> <p>Seiten-ID für Besucher-ClickMap (pid). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContextType </p> </td> 
   <td colname="col2"> <p>Seiten-ID-Typ für Besucher-ClickMap (pidt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickSourceID </p> </td> 
   <td colname="col2"> <p>Quellenindex für Besucher-ClickMap (oi). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickTag </p> </td> 
   <td colname="col2"> <p>Objekt-Tag-Name für Besucher-ClickMap (ot). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>colorDepth </p> </td> 
   <td colname="col2"> <p>Bildschirmfarbtiefe in Bit (z. B. 24) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>connectionType </p> </td> 
   <td colname="col2"> <p>Verbindungstyp des Besuchers ( <span class="term"> LAN </span> oder <span class="term"> Modem </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookiesEnabled </p> </td> 
   <td colname="col2"> <p>Y oder N, ob der Besucher Cookies aus Eigensitzungen unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>Der Standardwährungscode für die Website. </p> <p>Beispiel: USD=US-Dollar, EUR = Euro, JPY = Japanische Yen usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>homePage </p> </td> 
   <td colname="col2"> <p>Y oder N, ist die aktuelle Seite die Homepage des Besuchers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaEnabled </p> </td> 
   <td colname="col2"> <p>Y oder N, hat der Besucher Java aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaScriptVersion </p> </td> 
   <td colname="col2"> <p>JavaScript-Version (z. B. 1.3). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>plugins </p> </td> 
   <td colname="col2"> <p>Durch Semikolon voneinander getrennte Liste mit Namen für Browserzusatzmodule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>propN </p> </td> 
   <td colname="col2"> <p>Eigenschaftswerte für Ihre Eigenschaften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>referrer </p> </td> 
   <td colname="col2"> <p>URL für verweisende Seiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resolution </p> </td> 
   <td colname="col2"> <p>Bildschirmauflösung (z. B. 1024x768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>scXmlVer </p> </td> 
   <td colname="col2"> <p>Marketingberichte-XML-Anforderungsversion (z. B. 1.0). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timezone </p> </td> 
   <td colname="col2"> <p>Zeitzonenversatz des Besuchers zu GMT in Stunden (z. B. -8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>visitorID </p> </td> 
   <td colname="col2"> <p>Besucher-ID. </p> </td> 
  </tr> 
 </tbody> 
</table>
