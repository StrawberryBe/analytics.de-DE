---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.linkTrackVars

Die Variable „“ ist eine kommagetrennte Liste von Variablen, die bei benutzerspezifischen, Download- und Ausstiegslinks gesendet werden.

If *`linkTrackVars`* is set to "", all variables that have values are sent with link data. To avoid inflation of instances or page views associated with other variables, Adobe recommends populating  and  in the onClick event of a link that is used for link tracking.*`linkTrackVars`**`linkTrackEvents`*

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Ausstiegslinks) sind in *`linkTrackVars`*. If  is used,  should contain "events."*`linkTrackEvents`**`linkTrackVars`*

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Alle | „None“ |

Verwenden Sie beim Eintragen von Werten in *`linkTrackVars`*, do not use the 's.' prefix for variables. For example, instead of populating  with "s.prop1," you should populate it with "prop1." *`linkTrackVars`* The following example illustrates how  should be used.*`linkTrackVars`*

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

Da der Link zu „google.com“ ein Exitlink ist (es sei denn, Sie sind Google), werden mit den Ausstieglinkdaten „event1“ und „eVar1“ gesendet. Dadurch nehmen die Instanzen zu, die mit „eVar1“ verknüpft sind, sowie die Anzahl, wie oft „event1“ ausgelöst wurde. In the link to [!DNL test.php], [!UICONTROL eVar1] is sent with a value of 'value C' because that is the current value of [!UICONTROL eVar1] at the time that *`tl()`* is called.

## Syntax und mögliche Werte

The *`linkTrackVars`* variable is a case-sensitive, comma-separated list of variable names, without the object name prefix. Anstelle von „s.eVar1“ müssen Sie also „eVar1“ verwenden.

```js
s.linkTrackVars="variable_name[,variable_name[...]]"
```

Die Variable  variable may contain only variables that are sent to , namely: , , , , eVar1-75, prop1-75, hier1-5, , , , , and .*`linkTrackVars`*[!DNL Analytics]*`events`**`campaign`**`purchaseID`**`products`**`channel`**`server`**`state`**`zip`**`pageType`*

## Beispiele

```js
s.linkTrackVars="events,prop1,eVar49"
```

```js
s.linkTrackVars="products"
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* If *`linkTrackVars`* is blank, all variables that have values are tracked with all server calls.
* Any variable listed in *`linkTrackVars`* that has a value at the time of any download, exit, or custom link, are tracked.
* If  is used,  must contain "events."*`linkTrackEvents`**`linkTrackVars`*

* Lassen Sie bei Variablen das Präfix „s.“ oder „s_objektname“. weg.