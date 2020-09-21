---
description: Die Dimensionen, die Sie mithilfe von Verarbeitungsregeln lesen und schreiben können (sofern nicht anderweitig vermerkt).
subtopic: Processing rules
title: Für Verarbeitungsregeln verfügbare Dimensionen
topic: Admin tools
uuid: ba73ab59-a8cf-491c-8757-5fb03d6b0745
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 86%

---


# Für Verarbeitungsregeln verfügbare Dimensionen

Die Dimensionen, die Sie mithilfe von Verarbeitungsregeln lesen und schreiben können (sofern nicht anderweitig vermerkt).

## Benutzerspezifische Werte und Kontextdaten  {#section_7A5E1810CAC34B0BBC69F8F5F7C75AA5}

<table id="table_5011C501D5DC489E87A42FFC51DEB40D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wert </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierter Wert </p> </td> 
   <td colname="col2"> <p>Benutzerspezifischer Text oder Werte, die direkt bei der Aktion einer Verarbeitungsregel eingegeben wurden. Diese Werte stehen in nachfolgenden Bedingungen und Regeln zur Verfügung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verketteter Wert </p> </td> 
   <td colname="col2"> <p>Werte, die durch Kombination zweier Werte erstellt werden. So können beispielsweise Kategorie und Seitenname zum Erstellen einer Unterkategorie kombiniert werden. Diese Werte stehen in nachfolgenden Bedingungen und Regeln zur Verfügung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modifizierte Werte </p> </td> 
   <td colname="col2"> <p>Wenn ein Variablenwert mithilfe von Verarbeitungsregeln geändert wird, wird der geänderte Wert in nachfolgenden Bedingungen und Regeln verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kontextdatenvariablen </p> </td> 
   <td colname="col2"> <p>Benannte Variablen, die bei einem Hit versendet werden. </p> <p>Hinweis: Alle Daten, die in einer Kontextdatenvariablen enthalten sind, müssen in eine Berichterstellungsvariable kopiert werden, damit sie in einem Bericht angezeigt werden können. Kontextdatenvariablen sind in den Berichtsoberflächen nicht anzeigbar, auch nicht in den Clickstream-Daten-Feeds. </p> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md"> Kopieren einer Kontextdatenvariable in eine eVar </a> </p> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md"> Festlegen eines Ereignisses mit einer Kontextdatenvariablen </a> </p> <p> <a href="/help/implement/vars/page-vars/contextdata.md"> Kontextdatenvariablen</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Traffic-Variablen {#section_225156106F8B41F8BC1E68D58DDC2652}

<table id="table_575F618C59DC4933BC77F935518EAE39"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variable </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>prop 1-75 </p> </td> 
   <td colname="col2"> <p> <code> prop1 - prop75</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hierarchie 1-5 </p> </td> 
   <td colname="col2"> <p> <code> hier1 - hier5</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Website-Bereich </p> </td> 
   <td colname="col2"> <p> <code> s.channel </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server </p> </td> 
   <td colname="col2"> <p> <code> s.server </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Hit-Attribute {#section_07E69A86A47741A083FD84F112EB80D0}

<table id="table_9011B1FA462B4DBBAA58FC2D6D638DA1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Report Suite-ID (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Die Report Suite, auf der die Verarbeitungsregel ausgeführt wird (möglicherweise nicht die ursprünglich in AppMeasurement spezifizierte Report Suite). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Website-Name </p> </td> 
   <td colname="col2"> <p> <code> s.pageName</code> </p> <p>Hinweis:  Linktracking-Aufrufe entfernen die <code>pageName</code> Variable, bevor sie Verarbeitungsregeln erreichen. Wenn Sie einen Seitennamenwert mithilfe von Verarbeitungsregeln erneut einfügen, wird der Treffer als Ansicht der Seite und nicht als Linkverfolgungsaufruf betrachtet. Adobe empfiehlt eine Überprüfung, um sicherzustellen, dass der Seitenname bereits festgelegt ist, bevor Sie ihn ändern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seiten-URL </p> </td> 
   <td colname="col2"> <code> s.pageURL</code> oder die aktuelle Seiten-URL, wenn <code> s.pageURL</code> nicht spezifiziert ist. <p>Hinweis:  Linktracking-Aufrufe entfernen die <code>pageURL</code> Variable, bevor sie Verarbeitungsregeln erreichen. Wenn Sie einen Seiten-URL-Wert mithilfe von Verarbeitungsregeln erneut einfügen, wird der Treffer als Ansicht der Seite und nicht als Linkverfolgungsaufruf betrachtet. Adobe empfiehlt eine Überprüfung, um sicherzustellen, dass die Seiten-URL bereits festgelegt ist, bevor Sie sie ändern. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Abfragezeichenfolgenparameter </p> </td> 
   <td colname="col2"> <p>Der Wert eines spezifizierten Abfragezeichenfolgenparameters in der aktuellen URL oder Null, wenn kein Parameter existiert. Für die URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b> ist der Wert des Abfragezeichenfolgenparameters <span class="syntax codeph"> cid</span> <b>ad1</b> und der Wert des Abfragezeichenfolgenparameters <span class="syntax codeph"> node</span> ist <b>4</b>. </p> <p>Wenn Sie mit JavaScript AppMeasurement H.25.2 oder früher arbeiten, wird die Seiten-URL unter Umständen nach 255 Zeichen abgeschnitten. JavaScript AppMeasurement H.25.3 (Januar 2013) und höher liefert den Verarbeitungsregeln die vollständige URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitenpfad </p> </td> 
   <td colname="col2"> <p>Der Pfad der Seiten-URL. Der Pfad der URL <b>https://www.example.com/news/a.html?cid=ad1</b> ist <span class="syntax codeph">news/a.html</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitendomäne </p> </td> 
   <td colname="col2"> <p>Der vollständige Hostname, spezifiziert in der URL. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitenstammdomäne </p> </td> 
   <td colname="col2"> <p>Die letzten beiden Abschnitte im Hostnamen der Seite. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitenabfragezeichenfolge </p> </td> 
   <td colname="col2"> <p>Die volle Abfragezeichenfolge der URL. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Referrer* (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>HTTP-Verweis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisabfragezeichenfolgenparameter (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Der Wert eines spezifizierten Abfragezeichenfolgenparameters in der verweisenden URL oder Null, wenn kein Parameter existiert. Für die URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b> ist der Wert des Abfragezeichenfolgenparameters <span class="syntax codeph"> cid</span> <b>ad1</b> und der Wert des Abfragezeichenfolgenparameters <span class="syntax codeph"> node</span> ist <b>4</b>. </p> <p>Wenn Sie mit JavaScript AppMeasurement H.25.2 oder früher arbeiten, wird die Seiten-URL unter Umständen nach 255 Zeichen abgeschnitten. JavaScript AppMeasurement H.25.3 (Januar 2013) und höher liefert den Verarbeitungsregeln die vollständige URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisdomäne (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Der vollständige Hostname des Referrers. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisstammdomäne (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Die letzten beiden Abschnitte im Hostnamen des Referrers. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisabfragezeichenfolge (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Abfragezeichenfolgenparameter, die in der Verweis-URL enthalten sind. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP-Adresse (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>IP-Adressen, wie vom Browser gemeldet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzeragent (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Benutzeragent, wie vom Browser gemeldet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AppMeasurement-Code-Version (schreibgeschützt) </p> </td> 
   <td colname="col2"> <p>Die Version der AppMeasurement-Bibliothek, die zum Stellen der Anfrage verwendet wird. Bei der Verwendung von Bild-Beacons können Sie diese durch einen benutzerspezifischen Wert auffüllen, der mithilfe von Verarbeitungsregeln gelesen wird. Dieser Wert wird an der folgenden Position in der URL aufgeführt: </p> <p>https://server.net/b/ss/report-suite-ID/1/<span class="syntax codeph"> CODEVERSION</span>/... </p> </td> 
  </tr> 
 </tbody> 
</table>

## Konversionsvariablen {#section_311856B21B3B49DBAA0539CFA06C409F}

<table id="table_E28729026EDA485989178A3B887B5983"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variable </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>eVar 1-N </p> </td> 
   <td colname="col2"> <p> <code> evar1</code> - <code> evarN</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kampagnen-Trackingcode </p> </td> 
   <td colname="col2"> <p> <code> s.campaign</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Währungscode </p> </td> 
   <td colname="col2"> <p> <code> s.currencyCode</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Listenvariablen 1-3 </p> </td> 
   <td colname="col2"> <p> <code> s.list1</code> - <code> s.list3</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kauf-ID </p> </td> 
   <td colname="col2"> <p> <code> s.purchaseID</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Transaktions-ID </p> </td> 
   <td colname="col2"> <p> <code> s.transactionID </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bundesland des Besuchers </p> </td> 
   <td colname="col2"> <p> <code> s.state</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Postleitzahl des Besuchers </p> </td> 
   <td colname="col2"> <p> <code> s.zip</code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Erfolgsereignisse {#section_C1946FEB64FC4F579671EC5E0D06AE8A}

Verarbeitungsregeln können Ereignisse einstellen, diese aber nicht als Bedingungen lesen.

<table id="table_926ED12B58CA4FB685D799DC6EE567C0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ereignis- </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ereignis-  1-1000 </p> <p>(Für Kunden mit SiteCatalyst 15: Ereignis 1–100.) </p> </td> 
   <td colname="col2"> <p> <code> event1</code> - <code> event1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>purchase, scView, scAdd und andere Warenkorb-Ereignisse </p> </td> 
   <td colname="col2"> <p>Vordefinierte Ereignisse. </p> </td> 
  </tr> 
 </tbody> 
</table>

