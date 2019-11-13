---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 82060388a9a2122b66c57725cafa0eb4ce54e147

---


# s.linkTrackEvents

Die Variable ist eine kommagetrennte Liste von Ereignissen, die mit einem benutzerspezifischen, Ausstiegs- oder Download-Link gesendet werden. The `linkTrackEvents` parameter should include each event you want to track with every file download, exit link, and custom link. Wenn auf einen Link dieser Typen geklickt wird, wird der aktuelle Wert der einzelnen Variablen als nachverfolgt identifiziert. Diese Variable wird nur berücksichtigt, wenn `linkTrackVars` „Ereignisse“ enthält.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Konversion | "Keine" |

If an event is not in `linkTrackEvents`, it is not sent to Analytics, even if it is populated in the `onClick` event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

The values of [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) and `linkTrackEvents` override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link. Die Einstellungen für beide wirken sich auf jeden Datei-Download, Ausstiegslink und benutzerspezifischen Link aus. In Fällen, in denen die Variable (oder das Ereignis) auf die aktuelle Seite angewendet wird, jedoch nicht auf den jeweiligen Dateidownload, Ausstiegslink oder benutzerspezifischen Link, können die Instanzen jeder Variablen und jedes Ereignisses zu hoch sein.

Um sicherzustellen, dass die richtigen Variablen mit benutzerspezifischem Linkcode eingestellt werden, empfiehlt Adobe die Festlegung *`linkTrackVars`* und *`linkTrackEvents`* Verwendung des benutzerspezifischen Linkcodes wie folgt:

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

Im obigen Beispiel wird der Wert für "prop1"im benutzerspezifischen Linkcode selbst festgelegt. Der Wert für „prop2“ stammt aus dem aktuellen Wert, den die Variable auf der Seite hat.

*Hinweis: Wenn`linkTrackVars`(oder`linkTrackEvents`) null ist (oder eine leere Zeichenfolge wie ""), werden alle Analytics-Variablen (oder -Ereignisse), die für die aktuelle Seite definiert sind, verfolgt. Mit anderen Worten, alle Variablen mit Werten werden mit Linkdaten gesendet. Dadurch werden die Instanzen der einzelnen Variablen höchstwahrscheinlich in die Höhe getrieben. Um das zu hohe Ansteigen von Instanzen oder Seitenaufrufen zu vermeiden, die mit anderen Variablen verknüpft sind, empfiehlt Adobe das Ausfüllen von`linkTrackVars`und`linkTrackEvents`in dem[!UICONTROL onClick]-Ereignis eines Links, der für das Linktracking verwendet wird.*

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Exitlinks) müssen in `linkTrackVars` aufgeführt sein. Wenn `linkTrackEvents` verwendet wird, muss `linkTrackVars` „Ereignisse“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Alle | "Keine" |

When populating `linkTrackEvents`, do not use the 's.' prefix for variables. Anstatt es beispielsweise mit "s.event1"zu füllen, sollten Sie es mit "event1"füllen. Das folgende Beispiel zeigt, wie es verwendet werden sollte.

```js
s.linkTrackVars="eVar1,events" 
s.linkTrackEvents="event1" 
s.events="event1" 
s.eVar1="value A" 
s.eVar2="value B" 
s.t() // eVar1, event1 and event2 are recorded 
<a href="https://google.com">event1 and eVar1 are recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.eVar1='value C';s.events='';s.tl(this,'o')">eVar1 is recorded</a> 
```

Beachten Sie im ersten Link, dass die Variable events den Wert beibehält, der vor dem Klicken auf den Link festgelegt wurde. Dadurch kann „event1“ mit dem benutzerspezifischen Link gesendet werden. In the second example, the link to event2 is not recorded because it is not listed in `linkTrackEvents`.

Um Verwirrung und mögliche Probleme zu vermeiden, empfiehlt Adobe das Ausfüllen von [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) und `linkTrackEvents` in dem `onClick`-Ereignis eines Links, der für das Linktracking verwendet wird.

## Syntax und mögliche Werte

Die Variable *`linkTrackEvents`* ist eine kommagetrennte Liste mit Ereignissen (ohne Leerzeichen).

```
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

In `linkTrackEvents`. Eine Liste dieser Ereignisse finden Sie unter [Ereignisse](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html). Wenn vor oder nach dem Ereignisnamen ein Leerzeichen angezeigt wird, kann das Ereignis nicht mit Bildanforderungen für Links gesendet werden.

## Beispiele

To track `prop1`, `eVar1`, and `event1` with every file download, exit link, and custom link, use the following settings within the global JS file:

```
s.linkTrackVars="prop1,eVar1,events"
```

```
s.linkTrackEvents="event1"
```

**Weitere Beispiele**

```
s.linkTrackEvents="purchase,event1"
```

```
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Die JavaScript-Datei verwendet nur `linkTrackEvents`, wenn `linkTrackVars` die Variable „Ereignisse“ enthält. „Ereignisse“ sollte nur in `linkTrackVars` enthalten sein, wenn `linkTrackEvents` definiert ist.

* Vorsicht, wenn ein Ereignis auf einer Seite ausgelöst wird, das in `linkTrackEvents`. Das Ereignis wird dann bei jedem [!UICONTROL Exit-], [!UICONTROL Download-] oder [!UICONTROL benutzerspezifischen] Link erneut aufgezeichnet, wenn die „events“-Variable nicht zuvor zurückgesetzt wird (im [!UICONTROL onClick]-Ereignis eines Links oder nach Aufruf der Funktion `t()`).

* Wenn bei `linkTrackEvents` zwischen Ereignisnamen Leerzeichen stehen, werden die Ereignisse nicht aufgezeichnet.
