---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.linkTrackVars

Die Variable ist eine kommagetrennte Liste von Variablen, die bei benutzerspezifischen, Download- und Exitlinks gesendet werden.

Der Parameter [`linkTrackVars`](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) soll alle Variablen enthalten, die Sie bei jedem Dateidownload, Exitlink und benutzerspezifischen Link verfolgen möchten.

Die Einstellungen für `linkTrackVars` und `linkTrackEvents` in der JS-Datei wirken sich auf jeden Datei-Download, Exitlink und benutzerspezifischen Link aus. In Fällen, in denen eine Variable (oder ein Ereignis) für die aktuelle Seite, aber nicht für den betreffenden Dateidownload, Exitlink oder benutzerspezifischen Link gilt, kann es zu einer Aufblähung von Instanzen der einzelnen Variablen und Ereignisse kommen.

Um sicherzustellen, dass die korrekten Variablen mit dem benutzerspezifischen Linkcode eingestellt sind, empfiehlt Adobe, `linkTrackVars` und `linkTrackEvents` im benutzerspezifischen Linkcode wie folgt festzulegen:

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

Im oben gezeigten Beispiel ist der Wert für „prop1“ direkt innerhalb des benutzerspezifischen Linkcodes festgelegt. Der Wert für „prop2“ stammt aus dem aktuellen Wert, den die Variable auf der Seite hat.

Die Werte von `linkTrackVars` und `linkTrackEvents` überschreiben die Einstellungen in der JS-Datei und stellen sicher, dass nur die im benutzerspezifischen Linkcode angegebenen Variablen und Ereignisse für den betreffenden Link festgelegt werden.

*Hinweis: Wenn`linkTrackVars`(oder`linkTrackEvents`) null (oder eine leere Zeichenfolge) ist, werden alle für die aktuelle Seite festgelegten Analytics-Variablen (bzw. Analytics-Ereignisse) verfolgt. Mit anderen Worten: Alle Variablen mit Werten werden mit Linkdaten gesendet. Dadurch werden die Instanzen der einzelnen Variablen höchstwahrscheinlich verfälscht. Um das zu hohe Ansteigen von Instanzen oder Seitenaufrufen, die mit anderen Variablen verknüpft sind, zu vermeiden, empfiehlt Adobe das Ausfüllen von`linkTrackVars`und`linkTrackEvents`in dem[!UICONTROL onClick]-Ereignis eines Links, der für das Linktracking verwendet wird.*

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Exitlinks) müssen in `linkTrackVars` aufgeführt sein. Wenn `linkTrackEvents` verwendet wird, muss `linkTrackVars` „Ereignisse“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | Alle | „Keine“ |

Verwenden Sie beim Angeben von `linkTrackVars` bei Variablen nicht das Präfix „.s“. Anstatt beispielsweise `linkTrackVars` mit „s.prop1“ auszufüllen, müssen Sie „prop1“ eingeben. Das folgende Beispiel zeigt, wie `linkTrackVars` verwendet werden muss.

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

Da der Link zu „google.com“ ein Exitlink ist (es sei denn, Sie sind Google), werden mit den Ausstiegslinkdaten „event1“ und „eVar1“ gesendet. Dadurch nehmen die Instanzen zu, die mit „eVar1“ verknüpft sind, sowie die Anzahl der Auslösungen von „event1“. In dem Link zu [!DNL test.php] wird [!UICONTROL eVar1] mit dem Wert „value C“ gesendet, da dies der aktuelle Wert ist, den eVar1 zu dem Zeitpunkt hat, zu dem `tl()` abgerufen wird.

## Syntax und mögliche Werte

Die Variable `linkTrackVars` ist eine kommagetrennte Liste mit Variablennamen ohne den vorangestellten Objektnamen. Außerdem ist bei den Variablennamen auf die richtige Groß-/Kleinschreibung zu achten. Anstelle von „s.eVar1“ müssen Sie also „eVar1“ verwenden.

```
s.linkTrackVars="variable_name[,variable_name[...]]"
```

Die Variable `linkTrackVars` darf nur Variablen enthalten, die an [!DNL Analytics] gesendet werden: `events`, `campaign`, `purchaseID`, `products`, `eVar1-75`, `prop1-75`, `hier1-5`, `channel`, `server`, `state`, `zip` und `pageType`.

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
