---
description: Diese Referenztabelle definiert die Trefferattribute, die Sie auf der Seite „Marketingkanalregeln“ auswählen können.
seo-description: Diese Referenztabelle definiert die Trefferattribute, die Sie auf der Seite „Marketingkanalregeln“ auswählen können.
seo-title: Marketingkanal-Verarbeitungsregeln - Definitionen
solution: Analytics
subtopic: Marketingkanäle
title: Marketingkanal-Verarbeitungsregeln - Definitionen
topic: Reports and Analytics
uuid: 4 e 71 ff 5 b -912 a -4 dc 0-9 c 22-4 be 74 c 5 e 3 cc 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Marketingkanal-Verarbeitungsregeln - Definitionen

Diese Referenztabelle definiert die Trefferattribute, die Sie auf der Seite „Marketingkanalregeln“ auswählen können.

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Begriff </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alle </p> </td> 
   <td colname="col2"> <p>Aktiviert diesen Kanal nur, wenn alle Regeln in der nummerierten Regel „true“ sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alle </p> </td> 
   <td colname="col2"> <p>Aktiviert diesen Kanal, wenn eine der Regeln im Regelsatz „true“ ist. Diese Option steht nur zur Verfügung, wenn mehr als eine Regel in der nummerierten Regel vorhanden ist. </p> </td> 
  </tr>
  <tr> 
   <td colname="col1"> <p>AMO-ID </p> </td> 
   <td colname="col2"> <p>Der primäre Rückverfolgungscode, der von den Integrationen von Advertising Cloud und Advertising Analytics verwendet wird. Wenn eine dieser Integrationen aktiviert ist, kann das Verfolgungscode-Präfix verwendet werden, um die Advertising Cloud-spezifischen Kanäle zu identifizieren. Verwenden Sie "AMO ID" mit" AL" für Suche, "AC" für Display oder" AO" für Social. Wenn die AMO-ID in Marketingkanälen verwendet wird, können die Klick-/Kosten-/Impressionsmetriken dem richtigen Kanal zugeordnet werden (wenn diese Metriken nicht konfiguriert sind, gehen diese Metriken zu "Direct" oder" None" ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AMO ED ID </p> </td> 
   <td colname="col2"> <p>Der sekundäre Trackingcode, der von der Advertising Cloud verwendet wird. Der Hauptzweck dieses Trackingcodes dient als Schlüssel zum Zurücksenden von Daten an die Ad Cloud. Sie kann jedoch auch zur Identifizierung von Display-clickthroughs und Display-viewthroughs verwendet werden, wenn Sie diese als zwei verschiedene Marketingkanäle anzeigen möchten. Dies kann durch Festlegen der Marketingkanal-Logik für "AMO EF ID" mit": d "Für Display-clickthroughs oder" AMO EF ID "endet mit: i "für Display-viewthroughs. Wenn Sie nicht möchten, dass die Anzeige in zwei Kanäle aufgeteilt wird, verwenden Sie stattdessen die Dimension AMO ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Konversionsvariablen </p> </td> 
   <td colname="col2"> <p>Setzt sich aus eVars zusammen, die für diese Report Suite aktiviert wurden, und gilt nur, wenn diese Variablen über den Adobe-Code auf der Seite gesetzt wurden. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/oms_sc_implement.pdf" scope="external" format="html">Implementierungshandbuch </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorhanden </p> </td> 
   <td colname="col2"> <p>Mehrere Auswahlmöglichkeiten sind verfügbar, einschließlich: </p> <p> 
     <ul id="ul_FE39B5F36235441FB757CC73CA2C4F51"> 
      <li id="li_6DC09918D69B443091AB94DB773D5189"> <p> <span class="uicontrol">Nicht vorhanden</span>: Gibt an, dass das Trefferattribut nicht in der Anfrage vorhanden ist. Beispiel: Wenn der Benutzer in einer verweisenden Domäne eine URL eingibt oder auf ein Lesezeichen klickt, ist das Attribut für die verweisende Domäne nicht vorhanden. </p> </li> 
      <li id="li_3AB958F997974682824E85014CA266D6"> <p> <span class="uicontrol"> Ist leer</span>: Gibt an, dass ein Trefferattribut vorhanden ist. In der Regel handelt es sich dabei um eine eVar oder einen Abfragezeichenfolgenparameter, doch dem Trefferattribut ist kein Wert zugeordnet. </p> </li> 
      <li id="li_25EDA39748D141BA8173CC4C41035ABA"> <p> <span class="uicontrol"> Enthält </span>nicht: Hier können Sie beispielsweise angeben, dass eine verweisende Domäne keinen bestimmten Wert enthält (anders als die Auswahl <span class="term"> Enthält.</span> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Den Kanal identifizieren als </p> </td> 
   <td colname="col2"> <p>Verbindet die Regel mit dem Marketingkanal, den Sie der Seite <span class="wintitle">Marketingkanal-Manager</span> hinzugefügt haben. </p> <p>See <a href="../../components/c-marketing-channels/c-channels.md#task_98C9D3F5DBBC4B198E0A9ED4D3891E03" type="task" format="dita" scope="local"> Add marketing channels </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Stimmt mit Erkennungsregeln gebührenpflichtiger Suchvorgänge überein </p> </td> 
   <td colname="col2"> <p>Eine von Adobe erkannte, gebührenpflichtige Suche. Gebührenpflichtige Suchvorgänge treten ein, wenn Firmen Gebühren an die Suchmaschine zahlen, damit diese deren Site auflistet. Gebührenpflichtige Suchergebnisse tauchen gewöhnlich oben oder rechts von den Suchergebnissen auf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Stimmt mit Erkennungsregeln kostenloser Suchvorgänge überein </p> </td> 
   <td colname="col2"> <p>Eine von Adobe erkannte, kostenlose Suche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Stelle stimmt mit internen URL-Filtern überein </p> </td> 
   <td colname="col2"> <p> Ein Besuch, dessen Seiten-URL laut der Definition für die Report Suite in „Admin Tools“ mit dem internen URL-Filter übereinstimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Stelle stimmt nicht mit internen URL-Filtern überein </p> </td> 
   <td colname="col2"> <p>Die verweisende URL stimmt laut Definition für die Report Suite in „Admin Tools“ nicht mit dem internen URL-Filter überein. Sie können diese Einstellung mit <span class="term"> Seiten-URL </span> und <span class="term"> Vorhanden </span> zur Einrichtung einer Sammelregel, sodass keine Besuche im Abschnitt <a href="../../components/c-marketing-channels/c-faq.md#section_451E42994DA247A8A7B8559C715A5EE7" type="section" format="dita" scope="local"> Kein Kanal identifiziert </a> des Berichts landen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Treffer ignorieren, die mit internen URL-Filtern übereinstimmen </p> </td> 
   <td colname="col2"> <p>(Für verweisende Stellen) Verfolgt nur Treffer, die von extern verweisenden Stellen stammen. Normalerweise wird diese Option nicht aktiviert, es sei denn, Sie möchten internen Traffic einbeziehen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ist erste Seite des Besuchs </p> </td> 
   <td colname="col2"> <p>Die erste Seite eines Besuchs, die in der Adobe Berichterstellung erkannt wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seite </p> </td> 
   <td colname="col2"> <p>Der Seitenname einer Webseite auf Ihrer Site, die unter Verwendung des Adobe Web-Beacons mit Tags versehen wurde. Dies entspricht <span class="varname"> s.pageName </span>. Examples include <span class="varname"> Home Page </span> and <span class="varname"> About Us </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitendomäne </p> </td> 
   <td colname="col2"> <p>Die Domäne der Seite, auf der der Besucher landet, z. B. <span class="filepath">products.example.co.uk </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seitendomäne und Pfad </p> </td> 
   <td colname="col2"> <p>Die Domäne und der Pfad, z. B. <span class="filepath">products.example.co.uk/mens/pants/overview.html </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Stammdomäne der Seite (TLD+1) </p> </td> 
   <td colname="col2"> <p>Die Stammdomäne der Seite, auf der der Besucher landet, z. B. <span class="filepath">example.co.uk </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seiten-URL </p> </td> 
   <td colname="col2"> <p>Die URL einer Webseite auf Ihrer Site. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Domäne </p> </td> 
   <td colname="col2"> <p>Die Domäne, von der Ihre Besucher kamen, als sie Ihre Site aufriefen; verweisende Stellen können z. B. <span class="filepath">abcsite.com</span> oder <span class="filepath">xyzsite.com</span> sein . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Abfragezeichenfolgenparameter </p> </td> 
   <td colname="col2"> <p>If a page URL on your site looks like <span class="filepath"> https://example.com/?page=12345&amp;cat=1 </span>, then page and cat are both query string parameters. (See <span class="filepath"> https://en.wikipedia.org/wiki/Query_string </span>.) </p> <p>Sie können pro Regelsatz nur einen Abfragezeichenfolgenparameter angeben. Verwenden Sie zum Hinzufügen zusätzlicher Abfragezeichenfolgenparameter <span class="uicontrol">ANY</span> als Ihren Operator und fügen Sie dann der Regel neue Abfragezeichenfolgenparameter hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Stelle </p> </td> 
   <td colname="col2"> <p>Die Webseite (volle URL), auf der sich Besucher befanden, bevor sie zu Ihrer Site kamen. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domäne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Domäne und Pfad </p> </td> 
   <td colname="col2"> <p>Eine Verkettung aus verweisender Domäne und URL-Pfad. Zu den Beispielen gehören: </p> <p> <span class="filepath"> www.example.com/products/id/12345 </span> </p> <p> <span class="filepath"> ad.example.com/foo </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisender Parameter </p> </td> 
   <td colname="col2"> <p>Abfragezeichenfolgenparameter der verweisenden URL. Wenn Ihre Besucher z. B. von <span class="filepath">example.com/?page=12345&amp;cat=1</span> kommen, sind „page“ und „cat“ die verweisenden Parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verweisende Stammdomäne </p> </td> 
   <td colname="col2"> <p>Die Stammdomäne der verweisenden Stelle. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domäne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suchmaschine </p> </td> 
   <td colname="col2"> <p>Eine Suchmaschine wie Google oder Yahoo!, über die Besucher zu Ihrer Site gelangten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Such-Keywords </p> </td> 
   <td colname="col2"> <p>Ein Wort, mit dem in einer Suchmaschine gesucht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suchmaschine + Keywords </p> </td> 
   <td colname="col2"> <p>Eine Verkettung aus Keyword und Suchmaschine, um die Suchmaschine eindeutig zu kennzeichnen. Wenn Sie z. B. nach dem Begriff „computer“ suchen, werden die Suchmaschine und Keyword wie folgt identifiziert: </p> 
    <code>Suchverfolgungscode = " &lt; search_ type &gt;: &lt; Suchmaschine &gt;: &lt; search keyword &gt; "wobei search_ type =" n "oder" p ", search_ engine =" Google "und search_ keyword =" computer " </code>
  <p><b>Hinweis:</b> n = kostenlos; p = gebührenpflichtig </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Den Kanalwert setzen auf </p> </td> 
   <td colname="col2"> <p>Neben der Erkenntnis, welche Marketingkanäle einen Besucher zu Ihrer Site führen, ist es auch von Interesse, welche Bannerwerbung, welcher Keyword und welche E-Mail-Kampagne in dem Kanal die Gutschrift für die Site-Aktivität des Besuchers erhält. Diese ID ist ein Kanalwert, der mit dem Kanal gespeichert wird. Häufig handelt es sich dabei um eine Kampagnen-ID, die in die Landingpage oder die verweisende URL integriert ist. In anderen Fällen ist es eine Kombination aus Suchmaschine und Keyword oder die verweisende URL, die den Besucher aus einem bestimmten Kanal am genauesten identifiziert. </p> </td> 
  </tr> 
 </tbody> 
</table>



