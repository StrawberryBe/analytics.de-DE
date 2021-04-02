---
description: Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.
title: Linktracking-Methode
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: f9d9c7dbaf5fde5bd51c929d927d4cd3f61cb63b
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 99%

---


# Linktracking-Methode

Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.

>[!IMPORTANT]
>
>Bei der Implementierung von Links, deren Text (nicht href) personenbezogene Daten (PII-Daten) enthalten könnte, sollte [s_objectID](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/page-variables.html) verwendet oder die Activity Map-Linkerfassung mit [s.ActivityMap.linkExclusions oder s.ActivityMap.regionExclusions](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#configuration-vars) ausgeschlossen werden. Weitere Informationen zum Sammeln von PII-Daten durch Activity Map finden Sie [hier](/help/analyze/activity-map/lnk-tracking-overview.md).

In Activity Map basiert Linktracking auf diesen beiden IDs:

* Primäre ID: Dies ist der erkennbare Parameter des Links.
* Linkregion: Dies ist ein sekundärer Parameter, der es Benutzern ermöglicht, eine Zeichenfolge anzugeben, die für den gesamten Linkbereich der Seite oder der Region repräsentativ ist. Dieser Parameter kann automatisch generiert werden, wenn er nicht vom Benutzer bereitgestellt wird.

## Primäre ID  {#section_E8705CC1BDBC47FB8A4FE02293BACFE6}

Wenn der HTML-Code eine s_objectid enthält, dann wird diese standardmäßig als primäre ID verwendet. Andernfalls werden folgende Parameter als primäre ID verwendet (hier in der Reihenfolge der Priorität aufgeführt):

* Innertext
* Alttext
* Anrede/Titel
* Src
* Aktion

## Verwenden von InnerText im Vergleich zur Linkaktion (URL)   {#section_70C3573E22274522A8CC035BF18EC468}

Die Linkaktion (URL) ist die Aktion, die von der Webseite beim Klicken auf den Link ausgeführt wird. Normalerweise wird die URL angegeben, die nach dem Klicken auf den Link aufgerufen wird. Einige der Probleme, die bei der Verwendung der Linkaktion auftreten, sind:

* Mehrere unterschiedliche Links können die gleiche ID haben.
* Lesbarkeit des Links
* Ein Link kann mehrere Aktionen haben (abhängig vom Gerät, auf dem der Link angezeigt wird).

Daher wird InnerText verwendet, um von folgenden Vorteilen gegenüber der Linkaktion (URL) zu profitieren:

* InnerText ist repräsentativ für die Linkidentität. Es gibt deutlich weniger doppelte primäre IDs, da mehrere Links normalerweise nicht den gleichen Text enthalten.
* Die Konsistenz der primären ID wird über Geräte- und Browsertypen hinweg gewährleistet.
* Wenn ein Link auf der Seite neu positioniert wird, hat dies keine Auswirkungen auf InnerText.
* Die Lesbarkeit wird verbessert, sodass Benutzer Linktracking-Berichte außerhalb von Activity Map analysieren können.

## Linkregion {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

Dieses neue Attribut ermöglicht Benutzern, eine Zeichenfolge anzugeben, die für die Seitenregion, in der sich der Link befindet, repräsentativ ist.

Beispiel: Für den Link „Kontaktaufnahme“ im Menübereich der Webseite kann der Benutzer einen Regionsparameter „Menu“ übergeben. Befindet sich der Link „Kontaktaufnahme“ in der Fußzeile der Webseite, kann der Regionsparameter auf „footer“ gesetzt werden.

Der Wert der Linkregion wird nicht im Link selbst festgelegt, sondern in einem übergeordneten HTML-Element der DOM-HTML-Hierarchie für diese Region.
Die Verwendung der Linkregion hat diese Vorteile:

* Sie hilft, Links mit der gleichen primären ID zu unterscheiden.
* Die Trends einer Region sind weniger vom dynamischen Aspekt einer Webseite betroffen.
* Benutzer können die beliebtesten Links in einer Region sehen. Mit der Region als Anker können Überlagerungen für Links angezeigt werden, die aktuell auf der Seite nicht sichtbar sind (Ajax, Targeting).
* Eine Region kann Seiten ersetzen, da sie über viele Webseiten hinweg verwendet werden kann. Sie hilft, Fragen zu beantworten wie: „Erzielt die Region mit meinem Produktangebot auf der Landingpage für Frauen oder Männer bessere Ergebnisse?“
* Die Region ist eine nützliche Dimension, um hochdynamische Webseiten zu analysieren. Der Grund ist, dass Verzerrungen durch ständig wechselnde Links vermieden werden: In einer Region namens „Neueste Nachrichten“ auf der Landingpage eines Nachrichtensenders ändern sich die Links wahrscheinlich sehr häufig. Aber die Region bleibt immer dieselbe. Deshalb kann es interessant sein, Trends auf Regionsebene über mehrere Tage hinweg zu beobachten.

**Benutzerdefinierte Verfolgung von Regionen**

Sie können den Regionsparameter für einen Link (Standard ist Link-ID) anpassen: Ein auf „ID“ gesetztes Tag verwendet alle HTML-Elemente mit dem Parameter „id“ als Region. Wenn Sie daher das Regions-Tag auf „id“ setzen, führt dies wahrscheinlich zu sehr vielen Regionen (so viele, wie es unterschiedliche IDs auf der Seite gibt). Für eine spezifischere Implementierung können Sie das Regions-Tag alternativ auch auf einen genauer bestimmten Parameter setzen, beispielsweise auf „region_id“.

Der folgende Abschnitt enthält ein Beispiel für HTML-Code, in dem das standardmäßige Attribut für die ID einer Region, „id“, verwendet wird:

```
<div id="content">
  <div id="breaking_news">
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

Sie können Elemente auch mit einer frei gewählten Zeichenfolge-ID markieren, in diesem Fall „lpos“, und dann Attribute mit dem Namen „lpos“ hinzufügen.

```
<script language="JavaScript" type="text/javascript">
s.ActivityMap.regionIDAttribute = "lpos";
</script>
<div id="nav" lpos="navbar">
  <ul>
    <li>Menu Category A
      <ul>
        <li><a href="">Menu Item A 1</a>
        <li><a href="">Menu Item A 2</a>
      </ul>
    </li>
    <li>Menu Category B
      <ul>
        <li><a href="">Menu Item B 1</a>
        <li><a href="">Menu Item B 2</a>
      </ul>
    </li>
  </ul>
</div> 
  
<div id="content">
  <div id="breaking_news" lpos="breaking_news>
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

## Konfigurationsvariablen {#configuration-vars}

Beachten Sie, dass diese Variablen nur zu Referenzzwecken aufgelistet werden. Activity Map sollte standardmäßig korrekt konfiguriert sein, Sie können Ihre Implementierung jedoch mit diesen Variablen anpassen.

<table id="table_7BC8DC3F35CF49288D94BA707F06B283"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablenname </th> 
   <th colname="col2" class="entry"> Beispiel </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s.ActivityMap.regionIDAttribute </td> 
   <td colname="col2"> Standardeinstellung ist der Parameter „id“. Sie können auch einen anderen Parameter einstellen. </td> 
   <td colname="col3"> Zeichenfolge, die angibt, dass als Tag-Attribut die Regions-ID eines übergeordneten Elements (parent, parent.parent...) von s.linkObject verwendet werden soll, d. h. <b>das Element, auf das geklickt wurde</b> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.link </td> 
   <td colname="col2"> 
    <code>//&nbsp;only&nbsp;ever&nbsp;use&nbsp;"title"&nbsp;attributes&nbsp;from&nbsp;A&nbsp;tags</code><br/>
    <code>function(clickedElement)&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;var&nbsp;linkId;</code><br/>
    <code>&nbsp;&nbsp;if&nbsp;(clickedElement&nbsp;&amp;&amp;&nbsp;clickedElement.tagName.toUpperCase()&nbsp;===&nbsp;'A')&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;linkId&nbsp;=&nbsp;clickedElement.getAttribute('title');</code><br/>
    <code>&nbsp;&nbsp;}</code><br/>
    <code>&nbsp;&nbsp;return&nbsp;linkId;</code><br/>
    <code>}</code> </td>
   <td colname="col3"> Funktion, die das HTML-Element erhält, auf das geklickt wurde, und einen Zeichenfolgewert zurückgeben soll, der <b>dem Link, auf den geklickt wurde</b>, entspricht. <br/>
      <br/>
     Wenn der Rückgabewert „false“ lautet („null“, „undefined“, leere Zeichenfolge, 0) wird kein Link verfolgt. </td>
  </tr>
  <tr>
   <td colname="col1"> s.ActivityMap.region </td> 
   <td colname="col2"> 
        <code>//&nbsp;only&nbsp;ever&nbsp;use&nbsp;lowercase&nbsp;version&nbsp;of&nbsp;tag&nbsp;name&nbsp;concatenated&nbsp;with&nbsp;first&nbsp;className&nbsp;as&nbsp;the&nbsp;region</code><br/>
    <code>function(clickedElement)&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;var&nbsp;regionId,&nbsp;className;</code><br/>
    <code>&nbsp;&nbsp;while&nbsp;(clickedElement&nbsp;&amp;&amp;&nbsp;(clickedElement&nbsp;=&nbsp;clickedElement.parentNode))&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;regionId&nbsp;=&nbsp;clickedElement.tagName;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;if&nbsp;(regionId)&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;regionId.toLowerCase();</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;}</code><br/>
    <code>&nbsp;&nbsp;}</code><br/>
    <code>}</code> </td> 
   <td colname="col3"> Funktion, die das geklickte HTML-Element erhält und einen Zeichenfolgewert für <b>die Region, in der sich der Link befand, als auf ihn geklickt wurde</b>, zurückgeben soll. <br/>
      <br/>
     Wenn der Rückgabewert „false“ lautet („null“, „undefined“, leere Zeichenfolge, 0) wird kein Link verfolgt. </td>
  </tr>
  <tr>
   <td colname="col1"> s.ActivityMap.linkExclusions </td> 
   <td colname="col2"> 
     <code>//&nbsp;Exclude&nbsp;links&nbsp;tagged&nbsp;with&nbsp;a&nbsp;special&nbsp;linkExcluded&nbsp;CSS&nbsp;class</code><br/>
    <code>&lt;style&gt;</code><br/>
    <code>.linkExcluded&nbsp;{</code><br/>
    <code>&nbsp;&nbsp;display:&nbsp;block;</code><br/>
    <code>&nbsp;&nbsp;height:&nbsp;1px;</code><br/>
    <code>&nbsp;&nbsp;left:&nbsp;-9999px;</code><br/>
    <code>&nbsp;&nbsp;overflow:&nbsp;hidden;</code><br/>
    <code>&nbsp;&nbsp;position:&nbsp;absolute;</code><br/>
    <code>&nbsp;&nbsp;width:&nbsp;1px;</code><br/>
    <code>}</code><br/>
    <code>&lt;/style&gt;</code><br/>
    <code>&lt;a&nbsp;href="next-page.html"&gt;</code><br/>
    <code>&nbsp;&nbsp;Link&nbsp;is&nbsp;tracked&nbsp;because&nbsp;link&nbsp;does&nbsp;not&nbsp;have&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter.&nbsp;</code><br/>
    <code>&lt;/a&gt;</code><br/>
    <code>&lt;a&nbsp;href="next-page.html"&gt;</code><br/>
    <code>&nbsp;&nbsp;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.linkExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;has&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter.</code><br/>
    <code>&nbsp;&nbsp;&lt;span&nbsp;class="linkExcluded"&gt;exclude-link1&lt;/span&gt;</code><br/>
    <code>&lt;/a&gt;</code><br/>
    <code>&lt;a&nbsp;href="next-page.html"&gt;</code><br/>
    <code>&nbsp;&nbsp;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.linkExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;has&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter.</code><br/>
    <code>&nbsp;&nbsp;&lt;span&nbsp;class="linkExcluded"&gt;exclude-link2&lt;/span&gt;</code><br/>
    <code>&lt;/a&gt;</code><br/>
    <code>&lt;script&gt;</code><br/>
    <code>&nbsp;&nbsp;var&nbsp;s&nbsp;=&nbsp;s_gi('samplersid');</code><br/>
    <code>&nbsp;&nbsp;s.ActivityMap.linkExclusions&nbsp;=&nbsp;'exclude-link1,exclude-link2';</code><br/>
    <code>&lt;/script&gt;</code> </td> 
   <td colname="col3"> Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um im Link nach Text zu suchen: Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden. </td>
  </tr>
  <tr>
   <td colname="col1"> s.ActivityMap.regionExclusions </td> 
   <td colname="col2"> 
    <code>//&nbsp;Exclude&nbsp;regions&nbsp;on&nbsp;the&nbsp;page&nbsp;from&nbsp;its&nbsp;links&nbsp;being&nbsp;trackable&nbsp;by&nbsp;ActivityMap</code><br/>
    <code>&lt;div&nbsp;id="links-included"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;a&nbsp;href="next-page.html"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;Link&nbsp;is&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.regionExclusions&nbsp;is&nbsp;set&nbsp;but&nbsp;does&nbsp;not&nbsp;match&nbsp;the&nbsp;filter.</code><br/>
    <code>&nbsp;&nbsp;&lt;/a&gt;</code><br/>
    <code>&lt;/div&gt;</code><br/>
    <code>&lt;div&nbsp;id="links-excluded"&gt;&nbsp;</code><br/>
    <code>&nbsp;&nbsp;&lt;a&nbsp;href="next-page.html"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.regionExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;matches&nbsp;the&nbsp;filter.</code><br/>
    <code>&nbsp;&nbsp;&lt;/a&gt;</code><br/>
    <code>&lt;/div&gt;</code><br/>
    <code>&lt;script&gt;</code><br/>
    <code>&nbsp;&nbsp;var&nbsp;s&nbsp;=&nbsp;s_gi('samplersid');</code><br/>
    <code>&nbsp;&nbsp;s.ActivityMap.regionExclusions&nbsp;=&nbsp;'links-excluded';</code><br/>
    <code>&lt;/script&gt;</code> </td> 
   <td colname="col3"> Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um in der Region nach Text zu suchen. Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden. </td>
  </tr>
 </tbody>
</table>
