---
description: Dateidownloads und Exitlinks können automatisch anhand von Parametern verfolgt werden, die in der AppMeasurement für JavaScript-Datei festgelegt sind.
keywords: Analytics-Implementierung
seo-description: Dateidownloads und Exitlinks können automatisch anhand von Parametern verfolgt werden, die in der AppMeasurement für JavaScript-Datei festgelegt sind.
seo-title: Die s.tl()-Funktion – Linktracking
solution: Analytics
subtopic: Linktracking
title: Die s.tl()-Funktion – Linktracking
topic: Entwickler und Implementierung
uuid: f 28 f 071 a -8820-4 f 74-89 cd-fd 2333 a 21 f 22
translation-type: tm+mt
source-git-commit: acaea784c977d7ff438f84faf8af5a3c605e3cf5

---


# Die s.tl()-Funktion – Linktracking

File downloads and exit links can be automatically tracked based on parameters set in the [!DNL AppMeasurement] for JavaScript file.

## Die s.tl()-Funktion – Linktracking {#concept_EA13689CB8EE4F308FC89A1293046D5E}

File downloads and exit links can be automatically tracked based on parameters set in the [!DNL AppMeasurement] for JavaScript file.

Bei Bedarf können Links dieser Typen manuell verfolgt werden, indem benutzerspezifischer Linkcode (wie unten erklärt) eingesetzt wird. Außerdem lässt sich benutzerspezifischer Linkcode zur Verfolgung generischer benutzerspezifischer Links einsetzen, was für verschiedene Verfolgungs- und Berichterstellungsanforderungen nützlich ist.

## s.tl() – Parameterreferenz {#section_DDF19EE3ACE24EFAB2D65CD4B0D7DBC4}

<!-- Meike, I converted a table within to table to this section. Please check against orginal file -Bob -->

**this**

Das erste Argument sollte immer entweder auf „this“ (Standardeinstellung) oder „true“ festgelegt werden. Das Argument verweist auf das Objekt, auf das geklickt wird. Wenn „this“ festgelegt ist, bezieht es sich auf die HREF-Eigenschaft des Links.

Wenn Sie Linktracking für ein Objekt implementieren, das keine HREF-Eigenschaft besitzt, sollten Sie dieses Argument immer auf &quot;this&quot; setzen.

Da das Klicken auf einen Link oft zum Verlassen der aktuellen Seite führt, wird durch eine Verzögerung von 500 ms sichergestellt, dass eine Bildanforderung an Adobe gesendet wird, bevor der Besucher die Seite verlässt. Diese Verzögerung ist nur beim Verlassen der Seite erforderlich, jedoch ist sie für gewöhnlich vorhanden, wenn die s.tl()-Funktion aufgerufen wird. Wenn Sie die Verzögerung deaktivieren möchten, übergeben Sie beim Aufrufen der s.tl()-Funktion das Keyword „true“ als ersten Parameter.

**„linkType“**

`s.tl(this,linkType,linkName, variableOverrides, doneAction)`

Bei „linkType“ sind drei Werte möglich, je nachdem, welcher Typ von Link erfasst werden soll. Wenn der Link kein Download- oder Exitlink ist, sollten Sie die Option „Benutzerspezifische Links“ wählen.

| Typ | linkType-Wert |
|--- |--- |
| Dateidownloads | &#39;d&#39; |
| Exitlinks | &#39;e&#39; |
| Benutzerspezifische Links | &#39;o&#39; |

**linkName**

Das kann ein beliebiger benutzerdefinierter Wert mit einer Länge von bis zu 100 Zeichen sein. Davon hängt ab, wie der Link im entsprechenden Bericht angezeigt wird.

**variableOverrides**

(Optional) Hiermit können Sie Variablenwerte für diesen einen Aufruf ändern. Ist ähnlich wie bei anderen [!DNL AppMeasurement]-Bibliotheken. Wenn nicht verwendet, „null“ übergeben.

**useForcedLinkTracking**

Dieses Flag deaktiviert die erzwungene Linktracking für einige Browser. Bei Firefox 20+ und WebKit-Browsern ist die erzwungene Linktracking standardmäßig aktiviert.

Standardwert = true

Beispiel: `s.useForcedLinkTracking& = false`

**forcedLinkTrackingTimeout**

Die maximale Zeitdauer (in Millisekunden), in der auf die Fertigstellung der Verfolgung gewartet wird, bevor die doneAction-Aktion durchgeführt wird, die in `s.tl` übergeben wurde. Dieser Wert gibt die maximale Wartezeit an. Wenn der Verfolgungslink-Aufruf vor dieser Zeitdauer abgeschlossen ist, wird doneAction sofort ausgeführt. Wenn Sie bemerken, dass Verfolgungslink-Aufrufe nicht abgeschlossen werden, müssen Sie den Wert für diese Zeitüberschreitung eventuell erhöhen.

Standardwert = 250

Beispiel: `s.forcedLinkTrackingTimeout&nbsp;=&nbsp;500`

**doneAction**

Ein optionaler Parameter zur Angabe einer Navigationsaktion, die nach Abschluss des Verfolgungslink-Aufrufs ausgeführt werden soll, wenn useForcedLinkTracking aktiviert ist.

Syntax:

`s.tl(linkObject,linkType,linkName,variableOverrides,doneAction)`

doneAction: (optional) Gibt die Aktion an, die ausgeführt werden soll, nachdem der Linkverfolgungsaufruf gesendet wurde oder abgelaufen ist, je nach dem Wert, der wie folgt festgelegt wurde:

`s.forcedLinkTrackingTimeout`

Die Variable doneAction kann die Zeichenfolge „navigate“ sein, wodurch die Methode den `document.location` auf das „href“-Attribut von linkObject festlegt . Die Variable doneAction kann auch eine Funktion sein, die eine erweiterte Anpassung ermöglicht.

Wenn Sie für doneAction in einem onClick-Ankerereignis einen Wert angeben, müssen Sie nach dem `s.tl`-Aufruf „false“ zurückgeben, um die standardmäßige Browsernavigation zu verhindern.

Um das Standardverhalten zu imitieren und der vom „href“-Attribut angegebenen URL zu folgen, müssen Sie als doneAction eine „navigate“-Zeichenfolge angeben.

Optional können Sie zur Verarbeitung des Navigationsereignisses auch eine eigene Funktion angeben, die Sie dann als doneAction übergeben .

Beispiele:

```js
<a href="..." onclick="s.tl(this,'o','MyLink',null,'navigate');return false">Click Here</a> <a href="#" onclick="s.tl(this,'o','MyLink',null,function(){if(confirm('Proceed?'))document.location=...});return false">Click Here</a>
```

**Beispiel**

Im folgenden Beispiel zu einem Aufruf der [!UICONTROL s.tl()]-Funktion wird mittels der standardmäßigen Verzögerung von 500 ms sichergestellt, dass vor dem Verlassen der Seite alle Daten erfasst werden.

```js
s.tl(this,'o','link name');
```

Im nächsten Beispiel wird die Verzögerung von 500 ms deaktiviert, wenn der Benutzer die Seite nicht verlässt oder wenn das Objekt, das angeklickt wird, kein HREF besitzt.

```js
s.tl(true,'o','link name');
```

Die maximale Verzögerung beträgt 500 ms. Wenn das angeforderte Bild schon vor Ablauf der 500 ms zurückgegeben wird, endet die Verzögerung sofort. Dadurch kann der Besucher zur nächsten Seite wechseln oder eine weitere Aktion auf der gleichen Seite durchführen.

Die folgenden Beispiele zeigen, wie benutzerspezifische Links in WebKit-Browsern verarbeitet werden:

```js
<a href="..." onclick="s.tl(this,'o','MyLink',null,'navigate');return false">Click Here</a>
```

```js
<a href="#"  onclick="s.tl(this,'o','MyLink',null,  
function(){if(confirm('Proceed?'))document.location=...});return false">Click Here</a>
```

>[!NOTE]
>
>Die Verwendung von benutzerspezifischem Linkcode ist oft sehr spezifisch für Ihre Website und Ihre Berichterstellungsanforderungen. Wenn Sie wissen möchten, welche Möglichkeiten Ihnen zur Verfügung stehen und wie Sie die vorhandenen Features am besten für Ihre geschäftlichen Anforderungen einsetzen können, wenden Sie sich vor der Implementierung an Ihren Adobe-Berater oder an den Adobe-Kundendienst.

Das folgende Beispiel zeigt den Basis-Code zur Verfolgung eines Links mithilfe von benutzerspezifischem Linkcode:

```js
<a href="index.html" onClick="s.tl(this,'o','Link Name')">My Page</a>
```

>[!NOTE]
>
>The [!UICONTROL s_gi] function must contain your report suite ID as a function parameter. Denken Sie daran, [!DNL rsid] durch Ihre individuelle Report Suite-ID zu ersetzen.

>[!NOTE]
>
>Wenn der Parameter für den Linknamen nicht definiert ist, wird die URL des Links (anhand des &quot;this&quot; -Objekts ermittelt) als Linkname verwendet.

[!DNL Analytics]-Variablen können als Teil des benutzerspezifischen Linkcodes definiert werden.

## Automatische Verfolgung von Exitlinks und Dateidownloads {#concept_DF078C5C1B004695B3B7C4536C99D4B2}

Die JavaScript-Datei kann auf der Grundlage entsprechender Definitionsparameter für die automatische Verfolgung von Dateidownloads und Exitlinks konfiguriert werden.

<!-- 

link_automatic.xml

 -->

Die Parameter zur Kontrolle der automatischen Verfolgung lauten wie folgt:

```js
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls" 
s.linkInternalFilters="javascript:,mysite.com,[more filters here]" 
s.linkLeaveQueryString=false 
```

Die Parameter *`trackDownloadLinks`* und *`trackExternalLinks`* bestimmen, ob die automatische Verfolgung von Dateidownloads und Exitlinks aktiviert ist. When enabled, any link with a file type matching one of the values in *`linkDownloadFileTypes`* is automatically tracked as a file download. Any link with a URL that does not contain one of the values in *`linkInternalFilters`* is automatically tracked as an exit link.

In JavaScript H.25.4 (released February 2013), automatic exit link tracking was updated to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

## Example 1 {#section_504D163608E14B25A8B4CA9D615C6735}

The file types [!DNL jpg] and [!DNL aspx] are not included in *`linkDownloadFileTypes`* above, therefore no clicks on them are automatically tracked and reported as file downloads.

The parameter *`linkLeaveQueryString`* modifies the logic used to determine exit links. When *`linkLeaveQueryString`*=false, exit links are determined using only the domain, path, and file portion of the link URL. When *`linkLeaveQueryString`*=true, the query string portion of the link URL is also used to determine an exit link.

## Example 2 {#section_25660B64E28248A0BC982B2AF5603C0E}

Mit den folgenden Einstellungen wird das unten stehende Beispiel als Exitlink gezählt:

```js
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=false 
 
//HTML file 
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site!</a> 
```

## Beispiel 3 {#section_2A78D05162D640169844A7D1E9799BAA}

Mit den folgenden Einstellungen wird der unten angegebene Link nicht als Exitlink gezählt:

```js
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=true 
 
//HTML  
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site</a> 
```

>[!NOTE]
>
>Ein einzelner Link kann nur als Datei-Download oder Exitlink verfolgt werden, wobei der Dateidownload Priorität hat. If a link is both an exit link and file download based on the parameters *`linkDownloadFileTypes`* and *`linkInternalFilters`*, it is tracked and reported as a file download and not an exit link. Die folgende Tabelle fasst die automatische Verfolgung von Dateidownloads und Exitlinks zusammen.

## Manuelles Linktracking mit benutzerspezifischem Linkcode {#concept_7113B5D037BE4622B6934554C6D18F96}

Durch Einsatz von benutzerspezifischem Linkcode können Dateidownloads, Exitlinks und benutzerspezifischen Links auch dann verfolgt werden, wenn eine automatische Verfolgung nicht ausreichend oder nicht möglich ist.

<!-- 

link_manual.xml

 -->

Benutzerspezifischer Linkcode wird für gewöhnlich implementiert, indem einem Link ein [!UICONTROL onClick]-Ereignishandler oder einer vorhandenen Routine Code hinzugefügt wird. Für die Implementierung ist im Prinzip jeder JavaScript-Ereignishandler oder jede JavaScript-Funktion geeignet.

Link Tracking consists of calling the [!DNL AppMeasurement] for JavaScript function whenever the user performs actions that generate data you want to capture. Diese Funktion – [!UICONTROL s.tl()] – wird entweder direkt in einem Ereignishandler (wie [!UICONTROL onClick] oder [!UICONTROL onChange]) oder von einer separaten Funktion aus aufgerufen. Die [!UICONTROL s.tl()]-Funktion verfügt über fünf Argumente. Die ersten drei Argumente müssen vorhanden sein:

```js
s.tl(this,linkType,linkName, variableOverrides, doneAction)
```

## Benutzerspezifische Linktracking in Firefox und WebKit-Browsern {#section_F2B9A2A3CC1F4BB9A64456BC39FC50B9}

Zu JavaScript H.25 gibt es ein Update, das einen erfolgreichen Abschluss der Linktracking in WebKit-Browsern (Safari und Chrome) sicherstellen soll. Zu JavaScript H.26 gibt es ein Update, das einen erfolgreichen Abschluss der Linktracking in Firefox 20+ sicherstellen soll.

Nach diesem Update werden automatisch verfolgte Download- und Exitlinks (wie in [!DNL s.trackDownloadLinks] und [!DNL s.trackExternalLinks] festgelegt) erfolgreich verfolgt. Wenn Sie benutzerspezifische Links mithilfe manueller JavaScript-Aufrufe verfolgen, müssen Sie die Art und Weise, in der diese Aufrufe erfolgen, ändern. So werden zum Beispiel Ausstiegs- und Download-Links häufig mit einem Code nachverfolgt, der etwa so aussieht:

```js
<a href="https://anothersite.com" onclick="s.tl(this,'e','AnotherSite',null)">
```

In Internet Explorer werden der Nachverfolgungslink-Aufruf ausgeführt und die neue Seite geöffnet. In anderen Browsern kann die Ausführung des Nachverfolgungslink-Aufrufs unter Umständen abbrechen, wenn die neue Seite geöffnet wird. Dadurch wird verhindert, dass Nachverfolgungslink-Aufrufe erfolgreich abgeschlossen werden.

Um dieses Problem zu vermeiden, enthält die im Juli 2012 veröffentlichte Version H.25 eine überladene Nachverfolgungslink-Methode ([!DNL s.tl]), die problematische Browser zwingt, auf den ordnungsgemäßen Abschluss des Nachverfolgungslink-Aufrufs zu warten. Anstatt die Standard-Browseraktion auszuführen, führt diese neue Methode den Nachverfolgungslink-Aufruf aus und übernimmt die Verarbeitung des Navigationsereignisses. Diese Überlastungsmethode benötigt einen zusätzlichen Parameter ([!UICONTROL doneAction]), in dem die Aktion festgelegt wird, die nach Abschluss des Linktracking-Aufrufs durchzuführen ist.

Um die neue Methode einsetzen zu können, müssen an [!DNL s.tl] gerichtete Aufrufe um einen zusätzlichen [!UICONTROL doneAction]-Parameter ergänzt werden:

```js
<a href="https://anothersite.com"  
onclick="s.tl(this,'e','AnotherSite',null,'navigate');return false">
```

Durch Übergabe von „navigate“ als [!UICONTROL doneAction] wird das Standard-Browserverhalten imitiert, und nach Abschluss des Nachverfolgungsaufrufs wird die im „href“-Attribut festgelegte URL geöffnet.

In JavaScript H.25.4 (im Februar 2013 veröffentlicht) wurden die folgenden Einschränkungen beim Umfang von verfolgten Links bei aktiviertem `useForcedLinkTracking` hinzugefügt. Das automatische erzwungene Linktracking gilt nur in folgenden Fällen:

* `<A>` und `<AREA>` Tags.
* Das Tag muss über ein `HREF`-Attribut verfügen.
* The `HREF` can&#39;t start with `#`, `about:`, or `javascript:`.
* The `TARGET` attribute must not be set, or the `TARGET` needs to refer to the current window ( `_self`, `_top`, or the value of `window.name`).

## Linktracking mithilfe einer Bildanforderung {#concept_FF31C8D1B3DF483D853BF0A9D637F02F}

Links können auch ohne Aufrufen der s.tl()-Funktion nachverfolgt werden, indem Sie eine Bildanforderung erstellen.

<!-- 

link_img.xml

 -->

Bildanforderungen werden programmiert, indem Sie den Parameter „pe“ wie folgt zum Parameter „src“ Ihrer Bildanforderung hinzufügen:

```
pe=[type]
```

Where `[type]` is replaced with the type of link you want to track:

* lnk_d = Downloadlink
* lnk_e = Ausstiegslink
* lnk_o = Benutzerspezifischer Link

Zusätzlich kann eine Link-URL angegeben werden, indem die URL im „pev1“-Parameter übergeben wird:

```
pev1=mylink.com
```

Ein Linkname kann angegeben werden, indem der Name im „pev2“-Parameter übergeben wird:

```
pev2=My%20Link
```

Beispiel:

```
<img src="https://collectiondomain.112.2o7.net/b/ss/reportsuite/1/H.25.3--NS/0?pe=lnk_e&pev1=othersite.com&pev2=Offsite%20Link" width="1" height="1" border="0" />
```

## Festlegen weiterer Variablen für Datei-Downloads, Ausstiegslinks und benutzerspezifische Links {#concept_8DD06387D5234A52A6E361572FAA2DF6}

Two parameters (  and ) control which [!DNL Analytics] variables are set for file downloads, exit links, and custom links.

<!-- 

link_variables.xml

 -->

Diese sind in der JS-Datei standardmäßig wie folgt eingestellt:

```js
s.linkTrackVars="None"
```

```js
s.linkTrackEvents="None"
```

Die Variable *`linkTrackVars`*soll alle Variablen enthalten, die Sie bei jedem Dateidownload, Exitlink und benutzerspezifischen Link verfolgen möchten. The *`linkTrackEvents`* parameter should include each event you want to track with every file download, exit link, and custom link. Wenn auf einen Link dieser Typen geklickt wird, wird der aktuelle Wert der einzelnen Variablen als nachverfolgt identifiziert.

Wenn zum Beispiel „prop1“, „eVar1“ und „event1“ bei jedem Dateidownload, Exitlink und benutzerspezifischen Link verfolgt werden sollen, verwenden Sie die folgenden Einstellungen in der globalen JS-Datei:

```js
s.linkTrackVars="prop1,eVar1,events"
```

```js
s.linkTrackEvents="event1"
```

>[!NOTE]
>
>The variable *`pageName`* cannot be set for a file download, exit link, or custom link, because each of the link types is not a page view and does not have an associated page name.

>[!NOTE]
>
>If *`linkTrackVars`* (or *`linkTrackEvents`*) is null (or an empty string), all [!DNL Analytics] variables (or events) that are defined for the current page are tracked. Dadurch würden es zu einer starken Zunahme der Instanzen der einzelnen Variablen kommen, was vermieden werden sollte.

## Best Practices {#section_DA3CA596792E4BD6B5FFE89BCE0E617D}

The settings for *`linkTrackVars`* and *`linkTrackEvents`* within the JS file affect every file download, exit link, and custom link. In Fällen, in denen eine Variable (oder ein Ereignis) für die aktuelle Seite, aber nicht für den betreffenden Dateidownload, Exitlink oder benutzerspezifischen Link gilt, kann es zu einer Aufblähung von Instanzen der einzelnen Variablen und Ereignisse kommen.

Um sicherzustellen, dass die korrekten Variablen mit dem benutzerspezifischen Linkcode eingestellt sind, empfiehlt Adobe, *`linkTrackVars`* und *`linkTrackEvents`* im benutzerspezifischen Linkcode wie folgt:

```js
<a href="index.html" onClick=" 
var s=s_gi('rsid'); 
s.linkTrackVars='prop1,prop2,eVar1,eVar2,events'; 
s.linkTrackEvents='event1'; 
s.prop1='Custom Property of Link'; 
s.events='event1'; 
s.tl(this,'o','Link Name'); 
">My Page 
```

The values of *`linkTrackVars`* and *`linkTrackEvents`* override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link.

>[!NOTE]
>
>Im obigen Beispiel wird der Wert für &quot;prop 1&quot; im benutzerspezifischen Linkcode selbst festgelegt. Der Wert für „prop2“ stammt aus dem aktuellen Wert, den die Variable auf der Seite hat.

## Verwendung von Funktionsaufrufen mit benutzerspezifischem Linkcode {#concept_DB662C93B3ED415DB72C80270502BE5D}

[!UICONTROL Aufgrund der komplexen Natur von benutzerspezifischem Linkcode können Sie den Code in einer eigenständigen JavaScript-Funktion (die auf der Seite oder in einer verknüpften JavaScript-Datei definiert wird) zusammenfassen und die Funktion innerhalb des „onClick“-Handlers aufrufen.]

<!-- 

link_functions.xml

 -->

For example, you could insert the following two functions in your `AppMeasurement.js` file, just below the `s_doPlugins()` function, and then use them throughout your site:

```js
/* Set Click Interaction values (with timeout - H25 code and higher*/ 

function trackClickInteraction(name){ 
    var s=s_gi('rsid'); 
    s.linkTrackVars='prop42,prop35'; 
    s.prop42=name; 
    s.prop35=s.pageName; 
    s.tl(true,'o','track interaction',null,'navigate'); 
}
```

```js
/* Set Click Interaction values (without timeout - pre H25 code*/ 
 
function trackClickInteraction(name){ 
    var s=s_gi('rsid'); 
    s.linkTrackVars='prop42,prop35'; 
    s.prop42=name; 
    s.prop35=s.pageName; 
    s.tl(true,'o','track interaction'); 
}
```

>[!NOTE]
>
>Bei Bedarf können Sie den Linktyp und den Linknamen als zusätzliche Parameter für die javascript-Funktion übergeben.

Sie können einen ähnlichen Code wie den folgenden verwenden, um diese Funktionen aufzurufen:

```
<a href=”https://www.your-site.com/some_page.php” onclick=”trackClickInteraction('this.href');”>Link Text</a>
```

## Vermeiden von doppelten Linkzählungen {#section_9C3F73DE758F4727943439DED110543C}

Es kann vorkommen, dass der Link in Fällen, in denen er normalerweise von der automatischen Dateidownload- oder Exitlinktracking erfasst wird, doppelt gezählt wird.

Wenn Sie z. B. PDF-Downloads automatisch nachverfolgen, führt der folgende Code zur doppelten Zählung des Downloads:

```js
function trackDownload(obj) { 
 var s=s_gi('rsid'); 
 s.linkTrackVars='None'; 
 s.linkTrackEvents='None'; 
 s.tl(obj,'d','PDF Document'); 
}
```

Um sicherzustellen, dass der Link nicht doppelt gezählt wird, verwenden Sie die folgende geänderte JavaScript-Funktion:

```js
<script language=JavaScript> 
function linkCode(obj) { 
 var s=s_gi('rsid'); 
 s.linkTrackVars='None'; 
 s.linkTrackEvents='None'; 
 var lt=obj.href!=null?s.lt(obj.href):""; 
 if (lt=="") { s.tl(obj,'d','PDF Document'); } 
}
```

Die letzten beiden Zeilen des oben gezeigten Codes ändern das Verhalten des benutzerspezifischen Linkcodes so, dass nur die automatische Verfolgung stattfindet. Dadurch wird eine mögliche Doppelzählung vermieden.

## Popup-Fenster mit „useForcedLinkTracking“{#concept_0AC4BA3A64B84CCB8D9A6021A022D1C3}

When `useForcedLinkTracking` is enabled, [!DNL AppMeasurement] overrides the default link behavior on some browsers to prevent the track link call from being canceled when the new page opens. [!DNL AppMeasurement]Anstatt die Standard-Browseraktion auszuführen, führt den Nachverfolgungslink-Aufruf aus und übernimmt die Verarbeitung des Navigationsereignisses selbst.

<!-- 

link_popups.xml

 -->

When tracking some links that open a popup window, the Chrome built-in popup blocker might prevent [!DNL AppMeasurement] from opening a popup window that would normally be allowed. To avoid this, add a `target="_blank"` attribute to calls that open a window:

```
<a href="./popup.html" target="_blank" onClick="<a href="./popup.html" onclick="s.tl(this,'o','popup',null,'navigate');javascript:window.open('./popup.html','popup','width=550,height=450'); 
return false;">
```

So kann der Link nachverfolgt und das Popup-Fenster erwartungsgemäß geöffnet werden.

## Links von URL-Verkürzern {#concept_CD792362A8E04448B452BE9A18772024}

Links von URL-Verkürzerservices (wie bit.ly) werden normalerweise nicht als Seitenansichten oder Referrer verfolgt. Diese Services geben 301/302-Umleitungen mit der vollständigen URL an den Webbrowser zurück, der daraufhin eine neue, separate Anforderung an die vollständige URL sendet. Die ursprüngliche verweisende Stelle wird beibehalten, da der Verkürzer nicht mehr in der Schleife enthalten ist und die Anforderung keine Angabe enthält, dass die URL mit einem Umleitungsservice abgerufen wurde.

<!-- 

link_shortener.xml

 -->

Aufgrund der zahlreichen verfügbaren Services wird empfohlen, die speziellen Szenarien bei Ihrer Site zu testen, um den vom Service verwendeten Umleitungsmechanismus zu bestimmen.

## Linktrackingsvariablen in „doPlugins“{#concept_B5AC1D4372AA4A7D8C7871453A4F1215}

Zwecks einfacherer Verwaltung der Linktracking werden die folgenden Variablen vorab aufgefüllt, bevor die `doPlugins`-Funktion ausgeführt wird.

<!-- 

util_linkhandler.xml

 -->

Innerhalb von `doPlugins` können Sie mithilfe der folgenden Werte das Linktrackingsverhalten beeinflussen. So können Sie beispielsweise die Verfolgung abbrechen oder weitere Variablen zu Verfolgungsanforderungen hinzufügen.

<table id="table_55CCF4F2BF474FD3B703C926B896B392"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variable </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> Wirkung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> linkType </td> 
   <td colname="col2"> <p>Enthält den automatisch ermittelten Linktyp (wenn vorhanden). Kann auf einen der folgenden Werte eingestellt werden: </p> 
    <ul id="ul_81ACB5D00D774E86AFD22C61AD4D0E2C"> 
     <li id="li_52B6F2B124024DEFB422D1E9E97254C0">d (Download) </li> 
     <li id="li_E842C2E64F034181A364C639C30451FD">e (Exit) </li> 
     <li id="li_3263F378CE65407E81B6C5C597CED1E8">o (custom/Other) </li> 
    </ul> <p>Dies ist der Parameter <code>pe</code> in der Bildanforderung. </p> </td> 
   <td colname="col3"> <p>Wenn mit <code>linkURL</code> oder <code>linkName</code> festgelegt, wird ein Server-Aufruf als Downloadlink, Exitlink oder benutzerspezifischer Link gesendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkName </td> 
   <td colname="col2"> <p>Der Name, der im Bericht zum benutzerdefinierten Link, Download- oder Exitlink angezeigt wird. Wird bei einer Länge von 100 Zeichen abgeschnitten. Kann auf jede beliebige Zeichenfolge eingestellt werden. </p> <p>Dies ist der Parameter <code>pev2</code> in der Bildanforderung. </p> </td> 
   <td colname="col3"> <p> Wenn mit <code>linkType</code> festgelegt, wird eine Bildanforderung als Downloadlink, Exitlink oder benutzerspezifischer Link gesendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkURL </td> 
   <td colname="col2"> <p>Die URL des Links, die als Name verwendet wird, wenn „linkName“ nicht verfügbar ist. Kann auf jede beliebige Zeichenfolge eingestellt werden. </p> <p>Dies ist der Parameter <code>pev1</code> in der Bildanforderung. </p> </td> 
   <td colname="col3"> <p>Wenn mit <code>linkType</code> festgelegt, wird eine Bildanforderung als Downloadlink, Exitlink oder benutzerspezifischer Link gesendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkObject </td> 
   <td colname="col2"> <p>Das angeklickte Objekt (für Referenzzwecke). Dieses ist schreibgeschützt. </p> </td> 
   <td colname="col3"> <p>Hat keine direkte Auswirkung auf die Messung. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**

```js
function s_doPlugins(s) { 
    if (s.linkType == "d" && s.linkURL.indexOf(".aspx?f=") { 
        //special tracking for .aspx file download script 
        s.eVar11 = s.linkURL.substring(s.linkURL.lastIndexOf("?f=") + 3, s.linkURL.length); 
    } 
  
    else if (s.linkType == "o" ) { 
        // note: linkType is set to "o" only if you make a custom call 
        // to s.tl() and set the link type to "o". Automatically tracked 
        // links are set to "d" or "e" only. 
        s.eVar10 = s.LinkURL; 
    } 
}
```

## Validierung von Dateidownloads, Exitlinks und benutzerspezifischen Links {#concept_0B43AD582D3E470899FCCB58E44D3D49}

Für eine vollständige Validierung von Download-, Ausstiegs- und benutzerspezifischen Links empfiehlt Adobe die Verwendung eines Paket-Sniffer-Programms, das die Links in Echtzeit überprüft.

<!-- 

downloads_validate.xml

 -->

Da Dateidownloads, Exitlinks und benutzerspezifische Links keine Seitenansichten sind, können Parameter und Variableneinstellungen nicht mit dem [!UICONTROL DigitalPulse-Debugger] überprüft werden. Für die Anzeige von Verfolgungslinkdaten müssen Sie einen [Paket-Analyzer](../../implement/impl-testing/packet-monitor.md#concept_490DF35E06D44234A91B5FC57C0BF258) , um Nachverfolgungslinkdaten anzuzeigen.
