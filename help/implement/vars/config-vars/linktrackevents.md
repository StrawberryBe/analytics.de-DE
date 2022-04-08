---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignisse in Bildanforderungen zum Linktracking einbezogen werden sollen.
feature: Variables
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '258'
ht-degree: 100%

---

# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen [`linkTrackVars`](linktrackvars.md) und `linkTrackEvents`, um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Ereignisse in Linktracking-Aufrufen mit Tags in Adobe Experience Platform

Adobe Experience Platform schließt definierte Ereignisse automatisch in Linktracking-Treffern ein, wenn Sie keinen benutzerspezifischen Code verwenden.

>[!IMPORTANT]
>
>Wenn Sie Ereignisse in der Datenerfassungs-Benutzeroberfläche mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie das Ereignis auch in `linkTrackEvents` mit benutzerdefiniertem Code einbeziehen.

## s.linkTrackEvents in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.linkTrackEvents`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die Sie in Bildanforderungen zum Linktracking einbeziehen möchten (`tl()`-Methode). Die folgenden drei Kriterien müssen erfüllt sein, um Metriken in Linktracking-Treffer einzubeziehen:

* Legen Sie das gewünschte Ereignis in der [`events`](../page-vars/events/events-overview.md)-Variablen fest. Beispiel: `s.events = "event1";`.
* Setzen Sie die `events`-Variable in `linkTrackVars`. Beispiel: `s.linkTrackVars = "events";`.
* Legen Sie das gewünschte Ereignis in der `linkTrackEvents`-Variablen fest. Beispiel: `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Wenn diese Variable nicht definiert ist, werden alle Ereignisse in Bildanforderungen zum Linktracking einbezogen. Beachten Sie, dass die Datenerfassung diese Variable automatisch basierend auf den in der Benutzeroberfläche festgelegten Ereignissen füllt. Daher ist sie immer für Implementierungen eingerichtet, die Tags in Adobe Experience Platform verwenden.

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
