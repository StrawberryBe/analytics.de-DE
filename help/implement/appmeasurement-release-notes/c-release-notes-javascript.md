---
description: Gesammelte Versionshinweise für JavaScript H-Code – Legacy.
seo-description: Gesammelte Versionshinweise für JavaScript H-Code – Legacy.
seo-title: JavaScript H-Code – Legacy
solution: Analytics
subtopic: Versionshinweise
title: JavaScript H-Code – Legacy
topic: Entwickler und Implementierung
uuid: 4586 b 250-0 f 1 b -45 b 8-829 c -18 dc 1201956 f
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# JavaScript H-Code – Legacy{#javascript-h-code-legacy}

Gesammelte Versionshinweise für JavaScript H-Code – Legacy.

>[!NOTE]
>
>To find the current library version, use [DigitalPulse Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=debugger_about).

<!-- 

https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=omtrcache&title=AppMeasurement+Change+Log

 -->

## H.27.5 - Update {#section_DB9535C7EC4A4DDE9BA56B6C02BE8327}

Releasedatum: **16. Juni 2016**

Aufnahme der Visitor API 1.5.7.

## H.25.5 - Update {#section_B10151D7718F4568AE523BE1553FCCB7}

Releasedatum: **19. Mai 2016**

Aufnahme der Visitor API 1.5.5.

## H.27.5 - Update {#section_AD73ECD5CDAB4E158B509BA7B4B8CC1F}

Releasedatum: **5. November 2015**

* Aufnahme der Visitor API 1.5.3.

## H.27.5 - Update {#section_8A94D8A74A39486AAE248A22D661A261}

Releasedatum: **17. September 2015**

* Aufnahme der Visitor API 1.5.2.

## H.27.5 - Update {#section_62D1787F90FB4730B5F0C79EC1EF84B1}

Releasedatum: **20. August 2015**

* Aufnahme der Visitor API 1.5.1.

## H.27.5 - Update {#section_F58AF8B7FAE9470ABCBF2AAD9E7AF881}

Releasedatum: **18. Juni 2015**

* Aufnahme der Visitor API 1.5.

## H.27.5 - Update {#section_B3E310AFF909480BAD59A7F87D298348}

Releasedatum: **21. Mai 2015**

* Aufnahme der Visitor API 1.4

## H.27.5 - Update {#section_E7006FC903064376A85D3EC2AC1D2544}

Releasedatum: **16. April 2015**

* Added Integrate module to s_code.js in legacy [!DNL AppMeasurement] for [!DNL JavaScript] H.X ZIP file. (AN-101001)

## H.27.5 {#section_22DCF43169614B28BC17F46426C5D5B6}

Releasedatum: **19. Februar 2015**

* Aufnahme der Visitor API 1.3.5.
* Geändert, sodass kein automatisches Referrer-Tracking nach dem ersten Tracking-Aufruf stattfindet. Der zweite, dritte usw. Tracking-Aufruf (im Regelfall Linktracking) zählen somit den Referrer nicht doppelt, wenn *`s.referrer`* vor dem ersten Tracking-Aufruf manuell eingestellt wurde. (AN-92647)

## H.27.4 - Update {#section_ED38D59E83B4417180877F7C10BE4582}

Releasedatum: **15. Januar 2015**

* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.4.

Releasedatum: **18. September 2014**

* Es wurde eine `tagContainerMarker`-Variable hinzugefügt, die in der Implementierung die Angabe von bis zu 4 Zeichen ermöglicht. Diese Zeichen werden zusammen mit einer zusätzlichen Gedankenstrich-Zeichenbegrenzung an die Versionszeichenfolge angehängt. Diese Variable wird im dynamischen Tag-Management verwendet.

```js
  //  
<keyword>
  JavaScript 
</keyword> 
  s.tagContainerMarker = "D1.0"; 
    
  // Data Collection request 
  //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
```

## H.27.3 {#section_B38C61EE3BEA49CAA7A664395C85E4CF}

Releasedatum: **21. August 2014**

* Es wurden interne Veränderungen zur Unterstützung neuer Funktionen vorgenommen.

## H.27.2 {#section_402A4142C4B846DE945FD59DAD9D9298}

Releasedatum: **19. Juni 2014**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* Der Besucher-ID-Dienst 1.3 unterstützt ab sofort neue Funktionen.

## H.27.1 {#section_CC2556C734EE4BAAB71D6A93095DB38F}

Releasedatum: **11. Juni 2014**

* Fixed an issue in the [!DNL Analytics] for [!DNL Target] integration that caused some hits to incorrectly be merged.

## H.27 {#section_023B6267C0DB424F99A23EBB732B8C69}

Releasedatum: **22. Mai 2014**

* Unterstützung des [Marketing Cloud-Besucher-ID-Dienstes](https://marketing.adobe.com/resources/help/en_US/mcvid/).
* Unterstützung der [Integration von Analytics für Target](https://marketing.adobe.com/resources/help/en_US/target/a4t/).

## H.26.2 {#section_DE82C8BC7645400785E5B136565616F1}

Releasedatum: **17. Oktober 2013**

* Added `alt=""` to all Image objects to comply with Accessible Video and Communications Act.

## H.26.1 {#section_C3BDD9A19EF84467A8FDC283AEAE2DB5}

Releasedatum: **18. Juli 2013**

* Hashes/Fragmentbezeichner werden nun beim automatischen Linktracking ignoriert. Previously the following URL was automatically tracked since the entire `href` ended in `.pdf`:

```js
  <a href="index.htm#anchor.pdf">Test Link</a>
```

Nun werden Hashes/Fragmentbezeichner ignoriert, sodass der Link nur verfolgt wird, wenn der Dateiname mit einer passenden Erweiterung endet.

## H.26 {#section_E25814ACC21E41718EE1741A85AE567B}

Releasedatum: **29. April 2013**

* Die Option `useForcedLinkTracking`, die unter [Manual Link Tracking Using Custom Link Code](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_manuallinktrackcustomlink) beschrieben wird, gilt nun für Firefox 20 und höher (bisher galt dies nur für WebKit-Browser).

* Die Bildobjekt-ID-Erstellung ist nun eindeutig zwischen Instanzen. Auf diese Weise werden Konflikte verhindert, wenn sich mehrere Instanzen auf derselben Seite befinden.

## H.25.5 {#section_A528D1D5E84146F9A56680E4427B2750}

Releasedatum: **19. April 2013**

* Fixed an issue in forced link tr [!DNL Windows]acking that caused a [!DNL JavaScript] error on some [!DNL Android] 2.2 Devices.

* Bei der Video-Autoverfolgung für Media Player wurde ein Scrubbing-Fehler behoben, der eine fehlerhafte Anzeige der Abspieldauer verursachte.

## H.25.4 {#section_009AF895C8DD47CABC9A3776D27E8300}

Releasedatum: **Februar 2013**

* Changed automatic exit link tracking to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

* Der Umfang der Klick-Ereignisse, die durch `useForcedLinkTracking` betroffen sind, wurde verfeinert. Das automatische erzwungene Linktracking gilt nur in folgenden Fällen:

   * `<A>` und `<AREA>` Tags

   * Das Tag muss über ein `HREF`-Attribut verfügen.
   * The `HREF` can't start with `#`, `about:`, or `javascript:`

   * The `TARGET` attribute must not be set, or the `TARGET` needs to refer to the current window ( `_self`, `_top`, or the value of `window.name`)

## H.25.3 {#section_FA6A6F9F5D64455DA5A54C007081341A}

Releasedatum: **Januar 2013**

* Es werden nun URLs mit mehr als 255 Byte unterstützt, um die Erweiterung des Felds „Seiten-URL“ in den Adobe-Datenerfassungsservern zu unterstützen. Page URLs longer than 255 bytes are split, with the first 255 bytes appearing in the `g=` parameter, with the remaining bytes appearing later in the query sting in the `-g=` query parameter. Damit wird vermieden, dass lange URLs, die im Browser abgeschnitten werden, Vorrang vor anderen Daten haben, während gleichzeitig lange URLs erfasst werden können.

* Die URL-Decodierung für Zeichenfolgen, die mit einer gemischten Nutzung von `escape` und `encodeURIComponent` codiert sind, wurde korrigiert.

* Ein Problem in den WebKit-Browsern wurde behoben, in denen das Linktracking fehlschlägt, wenn beim ersten Server-Aufruf auf der Seite eine Zeitüberschreitung auftritt.
* Eine neue Methode für den Fallback der Besuchererkennung wurde hinzugefügt. Weitere Informationen finden Sie im Abschnitt [Erkennen Unique Visitors](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_identifying_unique_visitors).
* Es wurde ein neues `abort`-Flag hinzugefügt, das in `doPlugins` eingestellt werden kann. Wird dieses Flag auf „true“ gesetzt, fährt die [!DNL AppMeasurement]-Bibliothek nicht mit dem Rückverfolgungsaufruf fort. Das abort-Flag wird bei jedem Rückverfolgungsaufruf zurückgesetzt. Wenn also auch ein nachfolgender Rückverfolgungsaufruf abgebrochen werden muss, muss das Flag erneut in `doPlugins` eingestellt werden.

```js
  s.doPlugins = function(s) { 
       s.campaign = s.getQueryParam("cid"); 
       if ((!s.campaign) && (!s.events)) { 
            s.abort = true; 
       } 
  };
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.

## H25.2 {#section_647D7638D0C04019B8C9986CD124914E}

Releasedatum: **Oktober 2012**

* Added support for reporting an additional version number in the [!DNL JavaScript] version report. Diese Version war zuvor auf 2 Zeichen (z. B. 1.8) begrenzt. Es werden nun 3-Zeichen-Versionen (z. B. 1.8.5) unterstützt.
* Fixed an issue with [!DNL Tag Manager] that prevented repeated values in Dependant Code blocks from being sent.

## H.25.1 {#section_680CE31CFA9945978F42612B684DB831}

Releasedatum: **September 2012**

* Erzwungene URL-Codierung für folgende Zeichen:

```
  ~ 
  ! 
  * 
  ( 
  ) 
  '
```

This resolves issues with un-escaped characters being stored in the [!DNL ClickMap] `s_sq` cookie.

* Korrektur eines Problems, das dazu führen konnte, dass das Video-beendet-Ereignis nicht gesendet wird, wenn eine benutzerspezifische `media.monitor`-Methode verwendet wird, die das Medium-schließen-Ereignis verfolgt:

```
  If(media.event==”CLOSE”) { 
  … 
  } 
  
```

## H.25 {#section_BE76FEDFE03B44658808B0BDF779DE97}

Releasedatum: **Juli 2012**

Ein Update wurde durchgeführt, um sicherzustellen, dass das Linktracking in WebKit-Browsern (Safari und Chrome) erfolgreich abgeschlossen wird. Nach diesem Update werden automatisch verfolgte Download- und Exitlinks (wie in `s.trackDownloadLinks` und `s.trackExternalLinks` festgelegt) erfolgreich verfolgt. If you are tracking custom links using manual [!DNL JavaScript] calls, you need to modify how these calls are made.

Zum Beispiel werden Ausstiegs- und Downloadlinks häufig mit einem Code ähnlich dem folgenden nachverfolgt:

```js
  <a href="http://anothersite.com" onclick="s.tl(this,'o','link name',null)">
```

Firefox und Internet Explorer führen den Nachverfolgungslink-Aufruf aus und öffnen die neue Seite. WebKit-Browser können jedoch ggf. die Ausführung des Nachverfolgungslink-Aufrufs abbrechen, wenn die neue Seite geöffnet wird. Daher werden Nachverfolgungslink-Aufrufe bei der Verwendung von WebKit-Browsern häufig vor Abschluss abgebrochen.

Um dies zu vermeiden, verfügt H.25 über eine Überlastungs-Nachverfolgungslink-Methode (`s.tl`), mit der WebKit-Browser gezwungen werden, auf den Abschluss des Nachverfolgungslink-Aufrufs zu warten. Mit dieser neuen Methode wird der Nachverfolgungslink-Aufruf und anschließend das Navigationsereignis ausgeführt, anstatt die Standard-Browseraktion auszuführen. Diese Überlastungsmethode erfordert einen zusätzlichen Parameter, genannt `doneAction`, mit der die Aktion festgelegt wird, die durchgeführt werden soll, wenn der Linktracking-Aufruf abgeschlossen wird.

Um die neue Methode einsetzen zu können, müssen an `s.tl` gerichtete Aufrufe um einen zusätzlichen `doneAction`-Parameter ergänzt werden:

```js
  <a href="http://anothersite.com" onclick="s.tl(this,'o','link name',null 
  <codeph outputclass="syntax"> ,'navigate');return false"> 
  </codeph outputclass="syntax">
```

Durch Zuweisung von 'navigate' als `doneAction` wird das Standard-Browserverhalten widergespiegelt und die durch das `href`-Attribut festgelegte URL geöffnet, wenn der Nachverfolgungsaufruf abgeschlossen ist.

In der folgenden Tabelle sind die Konfigurationsvariablen und Aktualisierungen für H.25 zur Unterstützung dieser Funktion zusammengefasst.

<table id="table_E67157D710874146B26EFB7D84762542"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Variable </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>useForcedLinkTracking </p> </td> 
   <td colname="col2"> <p>Dieses Flag deaktiviert das erzwungene Linktracking für WebKit-Browser. Das erzwungene Linktracking ist für WebKit-Browser standardmäßig aktiviert und wird von anderen Browsern ignoriert. </p> <p> <b>Standardwert</b> </p> <p> <code> wahr </code> </p> <p> <b>Beispiel</b> </p> 
    <code class="syntax javascript">s. useforcedlinktracking &amp; amp; nbsp; = &amp; amp; nbsp; false </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>forcedLinkTrackingTimeout </p> </td> 
   <td colname="col2"> <p>Die maximale Zeitdauer (in Millisekunden), in der auf die Fertigstellung der Verfolgung gewartet wird, bevor die <code>doneAction</code>-Aktion durchgeführt wird, die in <code>s.tl</code> übergeben wurde. Dieser Wert gibt die maximale Wartezeit an. Wenn der Verfolgungslinkaufruf vor dieser Zeitüberschreitung abgeschlossen ist, wird <code>doneAction</code> sofort ausgeführt. Wenn Sie bemerken, dass Verfolgungslinkaufrufe nicht abgeschlossen werden, müssen Sie den Wert für diese Zeitüberschreitung eventuell erhöhen. </p> <p> <b>Standardwert</b> </p> <p>250 </p> <p> <b>Beispiel</b> </p> 
    <code class="syntax javascript">s. forcedlinktrackingtimeout &amp; amp; nbsp; = &amp; amp; nbsp; 500 </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trackLink (<code>s.tl </code>) </td> 
   <td colname="col2"> <p>Verfolgt die Links zum Beenden und Herunterladen sowie die benutzerdefinierten Links. Bietet einen optionalen Parameter zur Angabe einer Navigationsaktion, die ausgeführt wird, wenn der Verfolgungslink auf WebKit-Browsern abgeschlossen ist. </p> <p> <b>Syntax</b> </p> 
    <code class="syntax javascript">s. tl (linkobject, linktype, linkname, variableoverrides, doneaction) </code>
  <p> <b>doneAction</b>: (optional) Gibt die Aktion an, die ausgeführt werden soll, nachdem der Linkverfolgungsaufruf gesendet wurde oder abgelaufen ist (basierend auf dem Wert, der unter <code>s.forcedLinkTrackingTimeout</code> angegeben wurde ). Die <code>doneAction</code> kann die Zeichenfolge „navigate“ sein, wodurch die Methode den <code>document.location</code> auf das Attribut <code>href</code> von <code>linkObject</code> festlegt . Die <code>doneAction</code> kann auch eine Funktion sein, die eine erweiterte Anpassung ermöglicht. </p> <p>If providing a value for <code> onclick </code> in an anchor <code> false </code> event, you must return <code> s.tl </code> after the <code> href </code> call to prevent the default browser navigation. </p> <p> To mirror the default behavior and follow the URL specified by the <code> doneAction </code> attribute, provide a string of 'navigate' as the <code> doneAction </code>. </p> <p>Optionally, you can provide your own function to handle the navigation event by passing this function as the <code>$1</code>. </p> <p> <b>Beispiele</b> </p> 
    <code class="syntax javascript">&lt; a &amp; amp; nbsp; href = "…" &amp; amp; nbsp; onclick = "s. tl (this,' o ',' mylink ', null,' navigate '); return &amp; amp; nbsp; false " &gt; Click &amp; amp; nbsp; Hier &lt;/a &gt; </code><code class="syntax javascript">
 
 
 &lt; a &amp; amp; nbsp; href = " #" &amp; amp; nbsp; onclick = "s. tl (this,' o ',' mylink ', null, function () {if (' Continue?' Continue? '))document.location=...});return&amp;nbsp;false"&gt;Click&amp;nbsp;Here&lt;/a&gt; 
    </code> </td> 
  </tr> 
 </tbody> 
</table>

## H.24.4 {#section_1989179F10A34E88968CA5A5290CF17C}

Releasedatum: **April 2012**

Dieses Update wird allen Kunden empfohlen.

* Dank einer Erweiterung kann nun erkannt werden, wenn eine Seite mit Google Chrome Prerender ([https://developers.google.com/chrome/whitepapers/prerender](https://developers.google.com/chrome/whitepapers/prerender)) vorgerendert wird. Since Prerender loads and executes [!DNL JavaScript] and other code, this could result in page views being sent before a user clicks to visit your site. The [!DNL JavaScript] library now waits until the user visits your site before sending server calls for these prerendered pages.
* `timestamp` Die Variable wurde für Kunden, [!DNL JavaScript] die Zeitstempeldaten ähnlich wie andere [!DNL AppMeasurement] Bibliotheken anpassen möchten, zur Bibliothek hinzugefügt.

```js
  s.timestamp=Math.round((new Date()).getTime()/1000); 
  s.timestamp="2012-04-20T12:49:31-0700";
```

## H.24.3 {#section_F3D471B201F54C089320D3CE6D441DC0}

Releasedatum: **Februar 2012**

* Ein Fehler wurde behoben, bei dem zusätzliche Daten in die Bildanforderung für Kunden aufgenommen wurden, die JavaScript `Object.prototype`-Umgehungen nutzten. Jegliche Verwendung von `Object.prototype` wird nun bei der Handhabung von Kontextdatenvariablen übersprungen.
* Ein Fehler wurde behoben, bei dem der Abfrageparameter `pe` unter bestimmten Umständen zweimal mit demselben Wert weitergegeben wurde.
* Ein Fehler bei der [!DNL ClickMap][!DNL JavaScript]-Verfolgung in wurde behoben, sodass Klicks zum Body-Tag ignoriert werden, selbst wenn das Tag über einen `onClick`-Ereignis-Handler verfügt.
* Ein Zeitstempel wurde zu Variablen hinzugefügt, die mit geringeren Verfolgungsaufrufen (`trackLight`) verwendet werden.

## H.24.2 {#section_91CF07C2BC9B4C8BA0235DFDFB95A4D9}

Releasedatum: **Januar 2012**

* Aktualisierung der Video-Nachverfolgung: Neue Methode zur Verfolgung von Videoaufrufen mit vollständiger Wiedergabe.
* Fixed an issue that caused an "Attribute only valid on v:image" [!DNL JavaScript] error for `OnClick` events on VML elements in IE.
* Behebung des Problems, das dazu führte, dass Kontextdatenvariablen nicht in Link-Server-Anrufen enthalten waren, obwohl auf diese in `linkTrackVars`. Kontextdatenvariablen werden für die Verarbeitung von Regeln verwendet.

## H.24.1 {#section_967356D219FE4E9CAA110D03EDF4C8B1}

Releasedatum: **November 2011**

* Aktualisierung der Videoverfolgung zum Kombinieren von Treffern für Segmente und Meilensteine, die zur selben Zeit eintreten.

## H.24 {#section_78FF9B245643406BB7E9967E784A90AE}

Releasedatum: **November 2011**

* Internal updates to support [!DNL Adobe Tag Manager].

## H.23.9 {#section_3834625A639A47428683E08A472359C7}

Releasedatum: **November 2011**

* Internal updates to support [!DNL Adobe Tag Manager].

## H.23.8 {#section_FF3CEEAB6C6744D6B5EE314A0B5841CA}

Releasedatum: **Oktober 2011**

* Fixed an issue that caused the `linkTrackVars=none` and `linkTrackEvents=none` settings to not apply when using automatic exit link tracking. Die Einstellungen gelten nun auch für automatische Exitlinks. Daher werden Props, eVars und Ereignisse nicht mit der Bildanforderung für den Exitlink gesendet.

## H.23.7 {#section_D9D0CF343EBF49D9844C6BDA0C3C7A2E}

Releasedatum: **September 2011**

* Es wurden Rahmenattribute von Bild-Tags auf Mobilgeräten entfernt, um den Wireless Markup Language (WML)-Standards zu entsprechen. Dadurch wurden Renderingprobleme auf einigen mobilen Geräten behoben.

## H.23.6 {#section_461A208BE1B64EDDA87A8D7C4FD5456C}

Releasedatum: **August 2011**

Verbessert die Genauigkeit von Prozentmessungen bei der Videoverfolgung.

## H.23.5 {#section_FCE48EE33C9A42F08386FA30037BF4E0}

Releasedatum: **Juli 2011**

* Hinzugefügte Unterstützung für [!DNL Adobe Tag Manager].

## H.23.4 {#section_E9152B4437C24107A68D264F70361930}

Releasedatum: **Juni 2011**

* Fixed an issue that caused [!DNL JavaScript] errors when accessing certain properties of Vector Markup Language (VML) shape elements.
* Verweiszeichenfolgen mit mehr als 255 Zeichen werden nun dadurch gekürzt, dass der Pfad anstelle der Abfragezeichenfolge verkürzt wird. Dadurch wurden Probleme behoben, die verursacht wurden, weil Abfragezeichenfolgen verkürzt und nicht erfasst wurden.

## H.23.3 {#section_EAB0602E07EE4A5CA6521351F461D22D}

Releasedatum: **Mai 2011**

* Behebung eines Problems, das verhindert hat, dass die Videoverfolgungsvariable (pev3) gesendet wird.
* Behebung eines Problems, durch das verhindert wurde, dass der `s_gi`-Aufruf einen Code aktiviert, der sowohl mit dem G- als auch dem H-Code kompatibel ist. Wenn Sie eine 1 als zweiten Parameter an diesen Aufruf weiterleiten, wird der Code nun so konfiguriert, dass er mit beiden Versionen kompatibel ist.

## H.23.2 {#section_274143E83A8D42F1AD40CAE4326E99CE}

Releasedatum: **April 2011**

* Unterstützung für contextData, welches die Verarbeitungsregeln auf Serverseite (nur v15) aktiviert.
* Unterstützung für leichte Server-Aufrufe (nur v15).
* Unterstützung für die Zuweisung eines anderen Werts als 1 zu einem Zählereignis in der Ereignisliste.
* Unterstützung für neue Methode der Videoverfolgung über die Konversion von eVars und Ereignissen (aktuell in Beta-Version).
* Wegfall der Unterstützung für die Festlegung von Media.trackWhilePlaying auf „false“. Die Einstellung ist nun immer „true“.
* Das debugTracking-Flag wurde hinzugefügt, um die Protokollierung von Anforderungen zu aktivieren, die an die Firebug-Konsole genau wie an andere Plattformen gesendet wird.
* Vergewissern Sie sich, dass „+“ unabhängig vom Browser immer URL-verschlüsselt ist.
