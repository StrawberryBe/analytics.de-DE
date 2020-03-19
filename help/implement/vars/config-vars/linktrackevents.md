---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignis in Bildanforderungen zur Linktracking einbezogen werden sollen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zur Linktracking einbeziehen. Verwenden Sie die Variablen [`linkTrackVars`](linktrackvars.md) und `linkTrackEvents` , um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md) Aufrufe einzubeziehen.

Diese Variable wird nicht für Aufrufe der Ansicht von Seiten verwendet ([`t()`](../functions/t-method.md) Methode).

## Ereignis bei Linktracking-Aufrufen mit Adobe Experience Platform Launch

Launch erkennt automatisch in der Oberfläche definierte Ereignis und schließt sie in Linktracking-Treffern ein.

> [!IMPORTANT] Wenn Sie Ereignis in Launch mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie das Ereignis auch bei der `linkTrackEvents` Verwendung von benutzerspezifischem Code einbeziehen.

## s.linkTrackEvents in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkTrackEvents` Variable ist eine Zeichenfolge mit einer kommagetrennten Liste von Ereignissen, die Sie in Bildanforderungen zur Linktracking einbeziehen möchten (`tl()` Methode). Die folgenden drei Kriterien müssen erfüllt sein, um Metriken in Linktracking-Treffer einzubeziehen:

* Legen Sie das gewünschte Ereignis in der [`events`](../page-vars/events/events-overview.md) Variablen fest. Beispiel: `s.events = "event1";`.
* Set the `events` variable in `linkTrackVars`. Beispiel: `s.linkTrackVars = "events";`.
* Legen Sie das gewünschte Ereignis in der `linkTrackEvents` Variablen fest. Beispiel: `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Wenn diese Variable nicht definiert ist, werden alle Ereignis in Bildanforderungen zur Linktracking einbezogen. Beachten Sie, dass Launch diese Variable automatisch auf Grundlage der in der Benutzeroberfläche festgelegten Ereignis füllt. Daher wird sie immer in Implementierungen mit Launch eingestellt.

> [!TIP] Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`), wenn Sie Ereignis in dieser Variablen angeben. Zum Beispiel `s.linkTrackEvents = "event1";` ist richtig, während `s.linkTrackEvents = "s.event1";` falsch.

## Beispiel

Die folgende Linkverfolgungsfunktion enthält nur `event1` (nicht `event2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
