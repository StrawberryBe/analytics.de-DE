---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.linkTrackEvents

The  variable is a comma-separated list of events that are sent with a [!UICONTROL custom], [!UICONTROL exit], or [!UICONTROL download] link.

If an event is not in *`linkTrackEvents`*, it is not sent to [!DNL Analytics], even if it is populated in the [!UICONTROL onClick] event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

Im ersten Link zu [!DNL help.php] sehen Sie, dass die „events“-Variable den Wert behält, der festgelegt war, bevor auf den Link geklickt wurde. Dadurch kann „event1“ mit dem benutzerspezifischen Link gesendet werden. In the second example, the link to [!DNL test.php], event2 is not recorded because it is not listed in *`linkTrackEvents`*.

Um Verwirrung und potenzielle Probleme zu vermeiden, empfiehlt Adobe, einen Link, der zur Linkverfolgung verwendet wird, auszufüllen *`linkTrackVars`* und *`linkTrackEvents`* im [!UICONTROL onClick] -Ereignis einzutragen.

The *`linkTrackEvents`* variable contains the events that should be sent with [!UICONTROL custom], [!UICONTROL download], and [!UICONTROL exit] links. Diese Variable wird nur berücksichtigt, wenn sie "events" *`linkTrackVars`* enthält.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Konversion | „None“ |

## Syntax und mögliche Werte

Die Variable *`linkTrackEvents`* ist eine kommagetrennte Liste mit Ereignissen (ohne Leerzeichen).

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

In *`linkTrackEvents`*. These events are listed in [Events](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html). Wenn vor oder nach dem Ereignisnamen ein Leerzeichen steht, kann das Ereignis bei Bildanforderungen des Links nicht gesendet werden.

## Beispiele

```js
s.linkTrackEvents="purchase,event1"
```

```js
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Die JavaScript-Datei verwendet *`linkTrackEvents`* , wenn die Variable "events" *`linkTrackVars`* enthalten ist. "events"sollte *`linkTrackVars`* nur bei *`linkTrackEvents`* Definition enthalten sein.

* Vorsicht, wenn ein Ereignis auf einer Seite ausgelöst wird, das in *`linkTrackEvents`*. That event is recorded again with any [!UICONTROL exit], [!UICONTROL download], or [!UICONTROL custom] links unless the events variable is reset prior to that event (in the [!UICONTROL onClick] of a link or after the call to the *`t()`* function).

* If *`linkTrackEvents`* contains spaces between event names, the events are not recorded.
