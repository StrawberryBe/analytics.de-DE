---
title: linkTrackVars
description: Geben Sie an, welche Variablen in Bildanforderungen zur Linktracking einbezogen werden sollen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkTrackVars

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zur Linktracking einbeziehen. Verwenden Sie die Variablen `linkTrackVars` und `linkTrackEvents` , um Dimensionen und Metriken selektiv in `tl()` Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe (`t()` Funktion) verwendet.

## Variablen bei Linktracking-Aufrufen mit Adobe Experience Platform Launch

Launch füllt diese Variable automatisch auf dem Backend basierend auf Variablen, die in der Oberfläche festgelegt sind, sodass sie immer in Implementierungen mit Launch eingestellt wird.

> [!IMPORTANT] Wenn Sie Variablen in Launch mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie die Variable auch bei der `linkTrackVars` Verwendung von benutzerspezifischem Code einbeziehen.

## s.linkTrackVars in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkTrackVars` Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Variablen enthält, die Sie in Bildanforderungen zur Linktracking einbeziehen möchten (`tl()` Funktion). Beide der folgenden Kriterien müssen erfüllt sein, um Dimensionen in Linktracking-Treffern einzubeziehen:

* Legen Sie den gewünschten Variablenwert fest. Beispiel: `s.eVar1 = "Example value";`.
* Legen Sie die gewünschte Variable in der `linkTrackVars` Variablen fest. Beispiel: `s.linkTrackEvents = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Adobe hat jedoch AppMeasurement-Code im Code-Manager bereitgestellt, wobei diese Variable auf `"None"`. Gültige Werte sind alle Variablen auf Seitenebene, die eine Dimension ausfüllen.

* Wenn diese Variable nicht definiert oder auf eine leere Zeichenfolge festgelegt ist, werden *alle* Variablen in Bildanforderungen zur Linktracking einbezogen.
* Wenn diese Variable auf `"None"`festgelegt ist, werden in Bildanforderungen zur Linktracking *keine* Variablen einbezogen.

> [!TIP] Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Variablen in dieser Variablen. Zum Beispiel `s.linkTrackVars = "eVar1";` ist richtig, während `s.linkTrackVars = "s.eVar1";` falsch.

## Beispiel

Die folgende Linkverfolgungsfunktion enthält nur `eVar1` (nicht `eVar2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
