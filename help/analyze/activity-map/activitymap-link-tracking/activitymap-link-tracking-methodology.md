---
description: Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.
seo-description: Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.
seo-title: Linktracking-Methode
solution: Analytics
title: Linktracking-Methode
topic: Activity Map
uuid: 67864 bf 9-33 cd -46 fa -89 a 8-4 d 83 d 3 b 81152
translation-type: tm+mt
source-git-commit: 4f313ae50c4d5a0f3bfec493c2d554bc8614aeef

---


# Linktracking-Methode

Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.

>[!IMPORTANT]
>
>Any link where the text (not the href) may contain PII (Personally Identifiable Information) should be implemented explicitly using [s_objectID](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html) or by excluding ActivityMap link collection with [s.ActivityMap.linkExclusions or s.ActivityMap.regionExclusions](../../../analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#section_634197EACD404AC086DF9A03B813C8C3). Weitere Informationen zum Sammeln von PII-Daten durch Activity Map finden Sie [hier](../../../analyze/activity-map/lnk-tracking-overview.md#section_A9F016E64F33446F8916855D8C69A7C6).

In Activity Map basiert Linktracking auf diesen beiden IDs:

* Primäre ID: Dies ist der erkennbare Parameter des Links.
* Linkregion: Dies ist ein sekundärer Parameter, der es Benutzern ermöglicht, eine Zeichenfolge anzugeben, die für den gesamten Linkbereich der Seite oder der Region repräsentativ ist. Dieser Parameter kann automatisch generiert werden, wenn er nicht vom Benutzer bereitgestellt wird.

## Primäre ID {#section_E8705CC1BDBC47FB8A4FE02293BACFE6}

Wenn der HTML-Code eine s_objectid enthält, dann wird diese standardmäßig als primäre ID verwendet. Andernfalls werden folgende Parameter als primäre ID verwendet (hier in der Reihenfolge der Priorität aufgeführt):

* Innertext
* Alttext
* Title
* Src
* Action

## Verwenden von InnerText im Vergleich zur Linkaktion (URL) {#section_70C3573E22274522A8CC035BF18EC468}

Die Linkaktion (URL) ist die Aktion, die von der Webseite beim Klicken auf den Link ausgeführt wird. Normalerweise wird die URL angegeben, die nach dem Klicken auf den Link aufgerufen wird. Einige der Probleme, die bei der Verwendung der Linkaktion auftreten, sind:

* Mehrere unterschiedliche Links können die gleiche ID haben.
* Lesbarkeit des Links
* Ein Link kann mehrere Aktionen haben (abhängig vom Gerät, auf dem der Link angezeigt wird).

Daher wird InnerText verwendet, um von folgenden Vorteilen gegenüber der Linkaktion (URL) zu profitieren:

* InnerText ist repräsentativ für die Linkidentität. Es gibt deutlich weniger doppelte primäre IDs, da mehrere Links normalerweise nicht den gleichen Text enthalten.
* Die Konsistenz der primären ID wird über Geräte- und Browsertypen hinweg gewährleistet.
* Wenn ein Link auf der Seite neu positioniert wird, hat dies keine Auswirkungen auf InnerText.
* Die Lesbarkeit wird verbessert, sodass Benutzer Linktracking-Berichte außerhalb von Activity Map analysieren können.

## Link region {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

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
s.ActivityMap.regionIDAttribute="lpos"; 
   
<div id="nav" lpos="navbar"> 
  <ul> 
     <li> Menu Category A 
    <ul> 
      <li><a href="">Menu Item A 1</a> 
      <li><a href="">Menu Item A 2</a> 
     </ul> 
    </li> 
     <li> Menu Category B 
     <ul> 
      <li><a href="">Menu Item B 1</a>  
      <li><a href="">Menu Item B 2</a> 
  
   </ul> 
</ul> 
</div> 
  
<div id="content" > 
  <div id="breaking_news" lpos="breaking_news> 
      <a href="breaking-news.html">...</a> 
   </div> 
 <div id="todays_top_headlines"> 
      <a href="breaking-news.html">...</a> 
   </div> 
</div>
```

## Configuration variables {#section_634197EACD404AC086DF9A03B813C8C3}

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
   <td colname="col1"> s. activitymap. regionidattribute </td> 
   <td colname="col2"> Standardeinstellung ist der Parameter „id“. Sie können auch einen anderen Parameter einstellen. </td> 
   <td colname="col3"> Zeichenfolge, die angibt, dass als Tag-Attribut die Regions-ID eines übergeordneten Elements (parent, parent.parent...) von s.linkObject verwendet werden soll, d. h. <b>das Element, auf das geklickt wurde</b> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s. activitymap. link </td> 
   <td colname="col2"> 
    <code>// verwendet nur die Attribute "title" aus einer Tag-Funktion (clickedelement) {var linchild; if (clickedelement &amp; &amp; clickedelement. tagname. touppercase () = = =' A ') {linkind = clickedelement. getattribute (' title '); } return linchild; } </code>
  </td> 
   <td colname="col3"> Funktion, die das HTML-Element erhält, auf das geklickt wurde, und einen Zeichenfolgewert zurückgeben soll, der <b>dem Link, auf den geklickt wurde</b>, entspricht. <p>Wenn der Rückgabewert „false“ lautet („null“, „undefined“, leere Zeichenfolge, 0) wird kein Link verfolgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s. activitymap. region </td> 
   <td colname="col2"> 
    <code>// only ever use kleincase version of Tag name verkettet with first classname as the region function (clickedelement) {var regions regionId, classname; classname; while (clickedelement &amp; &amp; (clickedelement = clickedelement. parentnode)) {regionid = clickedelement. tagname; if (regions regionId) {return regions regionid. tolowercase (); }}}} </code>
  </td> 
   <td colname="col3"> Funktion, die das geklickte HTML-Element erhält und einen Zeichenfolgewert für <b>die Region, in der sich der Link befand, als auf ihn geklickt wurde</b>, zurückgeben soll. <p>Wenn der Rückgabewert „false“ lautet („null“, „undefined“, leere Zeichenfolge, 0) wird kein Link verfolgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.linkExclusions </td> 
   <td colname="col2"> 
    <code>// Links ausschließen mit einer speziellen linkexclude CSS-Klasse &lt; style &gt;. linkexclude {display: Block; height: 1 px; left: -9999 px; Überlauf: ausgeblendet; position: absolute; width: 1 px; } &lt;/style &gt; &lt; a href = "next-page.html" &gt; Link wird verfolgt, da der Link keinen ausgeblendeten Text enthält, der dem Filter entspricht.&lt;/a &gt; &lt; a href = "next-page.html" &gt; Link nicht verfolgt, da s. activitymap. linkexclusions eingestellt ist und dieser Link Text ausgeblendet hat, der mit dem Filter übereinstimmt. &lt; span class = "linkexclude" &gt; exclude-link 1 &lt;/span &gt; &lt;/a &gt; &lt; a href = "next-page.html" &gt; Link nicht verfolgt, da s. activitymap. linkexclusions eingestellt ist und dieser Link Text ausgeblendet hat, der dem Filter entspricht.  &lt;span class="linkExcluded"&gt;exclude-link2&lt;/span&gt; &lt;/a&gt; &lt;script&gt;   var s = s_gi('samplersid');   s.ActivityMap.linkExclusions = 'exclude-link1,exclude-link2'; &lt;/script&gt; 
    </code> </td> 
   <td colname="col3"> <p>Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um im Link nach Text zu suchen: Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.regionExclusions </td> 
   <td colname="col2"> 
    <code>// Regionen auf der Seite aus den Links ausschließen, die von activitymap &lt; div id = "links-included" &gt; &lt; a href = "next-page.html" &gt; link verfolgt werden, weil s. activitymap. regionexclusions eingestellt ist, aber nicht mit dem Filter übereinstimmt.&lt;/a &gt; &lt;/div &gt; &lt; div id = "links-exclude" &gt; &lt; a href = "next-page.html" &gt; Link nicht verfolgt, da s. activitymap. regionexclusions eingestellt ist und dieser Link mit dem Filter übereinstimmt.&lt;/a&gt; &lt;/div&gt; &lt;script&gt;   var s = s_gi('samplersid');   s.ActivityMap.regionExclusions = 'links-excluded'; &lt;/script&gt;
    </code> </td> 
   <td colname="col3"> <p>Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um in der Region nach Text zu suchen. Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden. </p> </td> 
  </tr> 
 </tbody> 
</table>
