---
description: Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.
title: Linktracking-Methode
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Activity Map
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: a6b38c6e7a34c876524ebe15514ac205898549d0
workflow-type: ht
source-wordcount: '992'
ht-degree: 100%

---

# Linktracking-Methode

Dieser Abschnitt ist an Adobe Analytics-Administratoren gerichtet. Im Vordergrund stehen die neuen Linktracking-Parameter und wie sie dafür sorgen, dass Links über verschiedene Browser und Geräte hinweg eindeutig und konsistent sind und die Vorgehensweise bei der Neupositionierung von Links auf einer Seite verbessern.

>[!IMPORTANT]
>
>Bei der Implementierung von Links, deren Text (nicht href) personenbezogene Daten (PII-Daten) enthalten könnte, sollte [s_objectID](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html?lang=de) verwendet oder die Activity Map-Linkerfassung mit [s.ActivityMap.linkExclusions oder s.ActivityMap.regionExclusions](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#configuration-vars) ausgeschlossen werden. Weitere Informationen zum Sammeln von PII-Daten durch Activity Map finden Sie [hier](/help/analyze/activity-map/lnk-tracking-overview.md).

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

## Verwenden von InnerText im Vergleich zur Linkaktion (URL)  {#section_70C3573E22274522A8CC035BF18EC468}

Die Linkaktion (URL) ist die Aktion, die von der Webseite beim Klicken auf den Link ausgeführt wird. Normalerweise wird die URL angegeben, die nach dem Klicken auf den Link aufgerufen wird. Einige der Probleme, die bei der Verwendung der Linkaktion auftreten, sind:

* Mehrere unterschiedliche Links können die gleiche ID haben.
* Lesbarkeit des Links
* Ein Link kann mehrere Aktionen haben (abhängig vom Gerät, auf dem der Link angezeigt wird).

Daher wird InnerText verwendet, um von folgenden Vorteilen gegenüber der Linkaktion (URL) zu profitieren:

* InnerText ist repräsentativ für die Linkidentität. Es gibt deutlich weniger doppelte primäre IDs, da mehrere Links normalerweise nicht den gleichen Text enthalten.
* Die Konsistenz der primären ID wird über Geräte- und Browsertypen hinweg gewährleistet.
* Wenn ein Link auf der Seite neu positioniert wird, hat dies keine Auswirkungen auf InnerText.
* Die Lesbarkeit wird verbessert, sodass Benutzer Linktracking-Berichte außerhalb von Activity Map analysieren können.

## Link-Region {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

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

### `s.ActivityMap.regionIDAttribute`

Zeichenfolge, die angibt, dass das Tag-Attribut als Regions-ID eines übergeordneten Elements (parent, parent.parent...) von `s.linkObject` verwendet werden soll, d. h. **das Element, auf das geklickt wurde**.

**Beispiel**

Standardeinstellung ist der Parameter „id“. Sie können auch einen anderen Parameter einstellen.

### `s.ActivityMap.link`

Funktion, die das angeklickte `HTMLElement` erhält und einen Zeichenfolgewert zurückgeben sollte, der dem angeklickten Link entspricht. Wenn der Rückgabewert „false“ („null“, „undefined“, leere Zeichenfolge, 0) lautet, wird kein Link verfolgt.

**Beispiel**

```
// only ever use "title" attributes from A tags
function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

### `s.ActivityMap.region`

Funktion, die das angeklickte HTML-Element erhält und einen Zeichenfolgewert für **die Region zurückgeben sollte, in der sich der Link befand, als auf ihn geklickt wurde.** Wenn der Rückgabewert „false“ („null“, „undefined“, leere Zeichenfolge, 0) lautet, wird kein Link verfolgt.

**Beispiel**

```
// only ever use lowercase version of tag name concatenated with first className as the region
function(clickedElement) {
  var regionId, className;
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

### `s.ActivityMap.linkExclusions`

Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um im Link nach Text zu suchen: Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden.

**Beispiel**

```
// Exclude links tagged with a special linkExcluded CSS class
<style>
.linkExcluded {
  display: block;
  height: 1px;
  left: -9999px;
  overflow: hidden;
  position: absolute;
  width: 1px;
}
</style>
<a href="next-page.html">
  Link is tracked because link does not have hidden text matching the filter. 
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link1</span>
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link2</span>
</a>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.linkExclusions = 'exclude-link1,exclude-link2';
</script>
```

### `s.ActivityMap.regionExclusions`

Zeichenfolge, die eine durch Kommas getrennte Liste mit Zeichenfolgen erhält, um in der Region nach Text zu suchen. Wird der Text gefunden, so wird der Link von der Verfolgung durch Activity Map ausgeschlossen. Ist dieser Wert nicht festgelegt, wird kein Versuch unternommen, die Verfolgung des Links durch Activity Map zu beenden.

**Beispiel**

```
// Exclude regions on the page from its links being trackable by ActivityMap
<div id="links-included">
  <a href="next-page.html">
    Link is tracked because s.ActivityMap.regionExclusions is set but does not match the filter.
  </a>
</div>
<div id="links-excluded"> 
  <a href="next-page.html">
    Link not tracked because s.ActivityMap.regionExclusions is set and this link matches the filter.
  </a>
</div>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.regionExclusions = 'links-excluded';
</script>
```
