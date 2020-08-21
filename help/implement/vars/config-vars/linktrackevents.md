---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignisse in Bildanforderungen zum Linktracking einbezogen werden sollen.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '246'
ht-degree: 100%

---


# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen [`linkTrackVars`](linktrackvars.md) und `linkTrackEvents`, um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Ereignisse in Linktracking-Aufrufen mit Adobe Experience Platform Launch

Launch erkennt automatisch in der Oberfläche definierte Ereignisse und schließt sie in Linktracking-Treffern ein.

>[!IMPORTANT]
>
>Wenn Sie Ereignisse in Launch mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie das Ereignis auch in `linkTrackEvents` mit benutzerdefiniertem Code einbeziehen.

## s.linkTrackEvents in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkTrackEvents`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die Sie in Bildanforderungen zum Linktracking einbeziehen möchten (`tl()`-Methode). Die folgenden drei Kriterien müssen erfüllt sein, um Metriken in Linktracking-Treffer einzubeziehen:

* Legen Sie das gewünschte Ereignis in der [`events`](../page-vars/events/events-overview.md)-Variablen fest. Beispiel: `s.events = "event1";`.
* Setzen Sie die `events`-Variable in `linkTrackVars`. Beispiel: `s.linkTrackVars = "events";`.
* Legen Sie das gewünschte Ereignis in der `linkTrackEvents`-Variablen fest. Beispiel: `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Wenn diese Variable nicht definiert ist, werden alle Ereignisse in Bildanforderungen zum Linktracking einbezogen. Beachten Sie, dass Launch diese Variable automatisch basierend auf Ereignissen füllt, die in der Benutzeroberfläche festgelegt sind. Daher wird sie immer in Implementierungen mit Launch festgelegt.

>[!TIP]
>
>Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Ereignissen in dieser Variablen. Zum Beispiel ist `s.linkTrackEvents = "event1";` korrekt, während `s.linkTrackEvents = "s.event1";` nicht korrekt ist.

## Beispiel

Die folgende Linktracking-Funktion enthält nur `event1` (nicht `event2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
