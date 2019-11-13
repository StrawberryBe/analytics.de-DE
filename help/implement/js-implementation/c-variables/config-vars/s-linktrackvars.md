---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 82060388a9a2122b66c57725cafa0eb4ce54e147

---


# s.linkTrackVars

Die Variable ist eine kommagetrennte Liste von Variablen, die bei benutzerspezifischen, Download- und Exitlinks gesendet werden.

The [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) parameter should include each variable that you want to track with every file download, exit link, and custom link.

The settings for `linkTrackVars` and `linkTrackEvents` within the JS file affect every file download, exit link, and custom link. In Fällen, in denen eine Variable (oder ein Ereignis) für die aktuelle Seite, aber nicht für den betreffenden Dateidownload, Exitlink oder benutzerspezifischen Link gilt, kann es zu einer Aufblähung von Instanzen der einzelnen Variablen und Ereignisse kommen.

Um sicherzustellen, dass die richtigen Variablen mit benutzerspezifischem Linkcode eingestellt werden, empfiehlt Adobe die Festlegung `linkTrackVars` und `linkTrackEvents` Verwendung des benutzerspezifischen Linkcodes wie folgt:

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

The values of `linkTrackVars` and `linkTrackEvents` override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link.

*Hinweis: Wenn`linkTrackVars`(oder`linkTrackEvents`) null ist (oder eine leere Zeichenfolge wie ""), werden alle Analytics-Variablen (oder -Ereignisse), die für die aktuelle Seite definiert sind, verfolgt. Mit anderen Worten, alle Variablen mit Werten werden mit Linkdaten gesendet. Dadurch werden die Instanzen der einzelnen Variablen höchstwahrscheinlich in die Höhe getrieben. Um das zu hohe Ansteigen von Instanzen oder Seitenaufrufen zu vermeiden, die mit anderen Variablen verknüpft sind, empfiehlt Adobe das Ausfüllen von`linkTrackVars`und`linkTrackEvents`in dem[!UICONTROL onClick]-Ereignis eines Links, der für das Linktracking verwendet wird.*

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Exitlinks) müssen in `linkTrackVars` aufgeführt sein. Wenn `linkTrackEvents` verwendet wird, muss `linkTrackVars` „Ereignisse“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Alle | "Keine" |

When populating `linkTrackVars`, do not use the 's.' prefix for variables. Anstatt beispielsweise `linkTrackVars` mit „s.prop1“ auszufüllen, müssen Sie „prop1“ eingeben. Das folgende Beispiel zeigt, wie `linkTrackVars` verwendet werden muss.

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

Da der Link zu „google.com“ ein Exitlink ist (es sei denn, Sie sind Google), werden mit den Ausstieglinkdaten „event1“ und „eVar1“ gesendet. Dadurch nehmen die Instanzen zu, die mit „eVar1“ verknüpft sind, sowie die Anzahl, wie oft „event1“ ausgelöst wurde. In dem Link zu [!DNL test.php] wird [!UICONTROL eVar1] mit dem Wert „value C“ gesendet, da dies der aktuelle Wert ist, den eVar1 zu dem Zeitpunkt hat, wenn `tl()` abgerufen wird.

## Syntax und mögliche Werte

Die Variable `linkTrackVars` ist eine kommagetrennte Liste mit Variablennamen ohne den vorangestellten Objektnamen. Außerdem ist bei den Variablennamen auf die richtige Groß-/Kleinschreibung zu achten. Anstelle von „s.eVar1“ müssen Sie also „eVar1“ verwenden.

```
s.linkTrackVars="variable_name[,variable_name[...]]"
```

Die Variable `linkTrackVars` variable may contain only variables that are sent to [!DNL Analytics], namely: `events`, `campaign`, `purchaseID`, `products`, `eVar1-75`, `prop1-75`, `hier1-5`, `channel`, `server`, `state`, `zip`, and `pageType`.

## Beispiele

```
s.linkTrackVars="events,prop1,eVar49"
```

```
s.linkTrackVars="products"
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Wenn `linkTrackVars` leer ist, werden alle Variablen, die Werte enthalten, bei allen Server-Aufrufen verfolgt.
* Jede Variable, die in `linkTrackVars` aufgeführt ist und einen Wert zum Zeitpunkt des Herunterladens, Beendens oder eines benutzerdefinierten Links hat, wird nachverfolgt.
* Bei Verwendung von `linkTrackEvents` muss `linkTrackVars` „Ereignisse“ enthalten.

* Lassen Sie bei Variablen das Präfix „s.“ oder „s_objektname“. weg.
