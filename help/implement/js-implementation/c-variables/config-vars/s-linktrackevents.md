---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: ca0797a353661a72d4064aa5aa84c3d9b7eb38a5

---


# s.linkTrackEvents

Die Variable ist eine kommagetrennte Liste von Ereignissen, die mit einem benutzerspezifischen, Ausstiegs- oder Download-Link gesendet werden. Der Parameter `linkTrackEvents` soll alle Ereignisse enthalten, die Sie bei jedem Dateidownload, Exitlink und benutzerspezifischen Link verfolgen möchten. Wenn auf einen Link dieser Typen geklickt wird, wird der aktuelle Wert der einzelnen Variablen als nachverfolgt identifiziert. Diese Variable wird nur berücksichtigt, wenn [`linkTrackVars`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) „Ereignisse“ enthält.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | Konversion | „Keine“ |

Wenn kein Ereignis in `linkTrackEvents` enthalten ist, wird es auch nicht an Analytics gesendet, selbst wenn es im `onClick`-Ereignis eines Links eingetragen ist (wie im nächsten Beispiel gezeigt):

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

Die Werte von [`linkTrackVars`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) und `linkTrackEvents` überschreiben die Einstellungen in der JS-Datei und stellen sicher, dass nur die im benutzerspezifischen Linkcode angegebenen Variablen und Ereignisse für den betreffenden Link festgelegt werden. Die beiden Einstellungen wirken sich auf jeden Datei-Download, Exitlink und benutzerspezifischen Link aus. In Fällen, in denen eine Variable (oder ein Ereignis) für die aktuelle Seite, aber nicht für den betreffenden Dateidownload, Exitlink oder benutzerspezifischen Link gilt, kann es zu einer Aufblähung von Instanzen der einzelnen Variablen und Ereignisse kommen.

Um sicherzustellen, dass die korrekten Variablen mit dem benutzerspezifischen Linkcode eingestellt sind, empfiehlt Adobe, *`linkTrackVars`* und *`linkTrackEvents`* im benutzerspezifischen Linkcode wie folgt festzulegen:

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

Im oben gezeigten Beispiel ist der Wert für `prop1` direkt innerhalb des benutzerspezifischen Linkcodes festgelegt. Der Wert für `prop2` stammt aus dem aktuellen Wert, den die Variable auf der Seite hat.

*Hinweis: Wenn`linkTrackVars`(oder`linkTrackEvents`) null (oder eine leere Zeichenfolge) ist, werden alle für die aktuelle Seite festgelegten Analytics-Variablen (bzw. Analytics-Ereignisse) verfolgt. Mit anderen Worten: Alle Variablen mit Werten werden mit Linkdaten gesendet. Dadurch werden die Instanzen der einzelnen Variablen höchstwahrscheinlich verfälscht. Um das zu hohe Ansteigen von Instanzen oder Seitenaufrufen zu vermeiden, die mit anderen Variablen verknüpft sind, empfiehlt Adobe das Ausfüllen von`linkTrackVars`und`linkTrackEvents`in dem`onClick`-Ereignis eines Links, der für das Linktracking verwendet wird.*

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Exitlinks) müssen in `linkTrackVars` aufgeführt sein. Wenn `linkTrackEvents` verwendet wird, muss `linkTrackVars` „Ereignisse“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | Alle | „Keine“ |

Verwenden Sie beim Angeben von `linkTrackEvents` bei Variablen nicht das Präfix „.s“. Statt beispielsweise „s.event1“ anzugeben, müssen Sie „event1“ eingeben. Das folgende Beispiel zeigt, wie es verwendet werden muss.

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

Im ersten Link sehen Sie, dass die „events“-Variable den Wert behält, der festgelegt war, bevor auf den Link geklickt wurde. Dadurch kann `event1` mit dem benutzerspezifischen Link gesendet werden. Im zweiten Beispiel wird der Link zu `event2` nicht aufgezeichnet, da er in `linkTrackEvents` nicht aufgeführt ist.

Um Verwirrung und mögliche Probleme zu vermeiden, empfiehlt Adobe das Ausfüllen von [`linkTrackVars`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) und `linkTrackEvents` in dem `onClick`-Ereignis eines Links, der für das Linktracking verwendet wird.

## Syntax und mögliche Werte

Die Variable *`linkTrackEvents`* ist eine kommagetrennte Liste mit Ereignissen (ohne Leerzeichen).

```
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

In `linkTrackEvents` sind nur Ereignisnamen zulässig. Eine Liste dieser Ereignisse finden Sie unter [Ereignisse](https://docs.adobe.com/content/help/de-DE/analytics/implementation/analytics-basics/ref-events.html). Wenn vor oder nach dem Ereignisnamen ein Leerzeichen steht, kann das Ereignis bei Bildanforderungen des Links nicht gesendet werden.

## Beispiele

Wenn zum Beispiel `prop1`, `eVar1` und `event1` bei jedem Dateidownload, Exitlink und benutzerspezifischen Link verfolgt werden sollen, verwenden Sie die folgenden Einstellungen in der globalen JS-Datei:

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

* Vorsicht, wenn ein Ereignis auf einer Seite ausgelöst wird, das in `linkTrackEvents` aufgeführt ist. Das Ereignis wird dann bei jedem Exit-, Download- oder benutzerspezifischen Link erneut aufgezeichnet, wenn die „events“-Variable nicht zuvor zurückgesetzt wird (im `onClick`-Ereignis eines Links oder nach Aufruf der Funktion `t()`).

* Wenn bei `linkTrackEvents` zwischen Ereignisnamen Leerzeichen stehen, werden die Ereignisse nicht aufgezeichnet.
