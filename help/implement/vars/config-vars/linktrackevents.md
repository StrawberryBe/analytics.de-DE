---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignisse in Bildanforderungen zur Linktracking einbezogen werden sollen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zur Linktracking einbeziehen. Verwenden Sie die Variablen `linkTrackVars` und `linkTrackEvents` , um Dimensionen und Metriken selektiv in `tl()` Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe (`t()` Funktion) verwendet.

## Ereignisse bei Linktracking-Aufrufen mit Adobe Experience Platform Launch

Launch erkennt automatisch in der Oberfläche definierte Ereignisse und schließt sie in Linktracking-Treffern ein.

> [!IMPORTANT] Wenn Sie Ereignisse in Launch mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie das Ereignis auch bei der `linkTrackEvents` Verwendung von benutzerspezifischem Code einbeziehen.

## s.linkTrackEvents in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkTrackEvents` Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die Sie in Bildanforderungen zur Linktracking einbeziehen möchten (`tl()` Funktion). Die folgenden drei Kriterien müssen erfüllt sein, um Metriken in Linktracking-Treffer einzubeziehen:

* Legen Sie das gewünschte Ereignis in der `events` Variablen fest. Beispiel: `s.events = "event1";`.
* Set the `events` variable in `linkTrackVars`. Beispiel: `s.linkTrackVars = "events";`.
* Legen Sie das gewünschte Ereignis in der `linkTrackEvents` Variablen fest. Beispiel: `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Wenn diese Variable nicht definiert ist, werden alle Ereignisse in Bildanforderungen zur Linktracking einbezogen. Beachten Sie, dass Launch diese Variable automatisch basierend auf Ereignissen füllt, die in der Benutzeroberfläche festgelegt sind. Daher wird sie immer in Implementierungen mit Launch eingestellt.

> [!TIP] Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Ereignissen in dieser Variablen. Zum Beispiel `s.linkTrackEvents = "event1";` ist richtig, während `s.linkTrackEvents = "s.event1";` falsch.

## Beispiel

Die folgende Linkverfolgungsfunktion enthält nur `event1` (nicht `event2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
