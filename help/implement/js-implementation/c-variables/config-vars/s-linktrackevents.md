---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.linkTrackEvents

Die Variable ist eine kommagetrennte Liste von Ereignissen, die mit einem [!UICONTROL benutzerspezifischen], [!UICONTROL Ausstiegs-] oder [!UICONTROL Download-Link] gesendet werden.

Wenn kein Ereignis in *`linkTrackEvents`* enthalten ist, wird es auch nicht zu [!DNL Analytics] gesendet, selbst wenn es im [!UICONTROL onClick]-Ereignis eines Links eingetragen ist (wie im nächsten Beispiel gezeigt):

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

Im ersten Link zu [!DNL help.php] sehen Sie, dass die „events“-Variable den Wert behält, der festgelegt war, bevor auf den Link geklickt wurde. Dadurch kann „event1“ mit dem benutzerspezifischen Link gesendet werden. Im zweiten Beispiel, dem Link zu [!DNL test.php], wird „event2“ nicht aufgezeichnet, da es in *`linkTrackEvents`* nicht aufgeführt ist.

Um Verwirrung und mögliche Probleme zu vermeiden, empfiehlt Adobe das Ausfüllen von *`linkTrackVars`* und *`linkTrackEvents`* in dem [!UICONTROL onClick]-Ereignis eines Links, der für das Linktracking verwendet wird.

Die Variable *`linkTrackEvents`* enthält die Ereignisse, die mit [!UICONTROL benutzerspezifischen], [!UICONTROL Download-] und [!UICONTROL Exitlinks] gesendet werden sollen. Diese Variable wird nur berücksichtigt, wenn *`linkTrackVars`* „Ereignisse“ enthält.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Konversion | "Keine" |

## Syntax und mögliche Werte

Die Variable *`linkTrackEvents`* ist eine kommagetrennte Liste mit Ereignissen (ohne Leerzeichen).

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

In *`linkTrackEvents`*. Eine Liste dieser Ereignisse finden Sie unter [Ereignisse](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html). Wenn vor oder nach dem Ereignisnamen ein Leerzeichen steht, kann das Ereignis bei Bildanforderungen des Links nicht gesendet werden.

## Beispiele

```js
s.linkTrackEvents="purchase,event1"
```

```js
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Die JavaScript-Datei verwendet nur *`linkTrackEvents`*, wenn *`linkTrackVars`* die Variable „Ereignisse“ enthält. „Ereignisse“ sollte nur in *`linkTrackVars`* enthalten sein, wenn *`linkTrackEvents`* definiert ist.

* Vorsicht, wenn ein Ereignis auf einer Seite ausgelöst wird, das in *`linkTrackEvents`*. Das Ereignis wird dann bei jedem [!UICONTROL Exit-], [!UICONTROL Download-] oder [!UICONTROL benutzerspezifischen] Link erneut aufgezeichnet, wenn die „events“-Variable nicht zuvor zurückgesetzt wird (im [!UICONTROL onClick]-Ereignis eines Links oder nach Aufruf der Funktion *`t()`*).

* Wenn bei *`linkTrackEvents`* zwischen Ereignisnamen Leerzeichen stehen, werden die Ereignisse nicht aufgezeichnet.
