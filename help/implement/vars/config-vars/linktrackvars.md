---
title: linkTrackVars
description: Geben Sie an, welche Variablen in Bildanforderungen zum Linktracking einbezogen werden sollen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkTrackVars

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen `linkTrackVars` und [`linkTrackEvents`](linktrackevents.md), um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

This variable is not used for page view calls (`t()` method).

## Variablen in Linktracking-Aufrufen mit Adobe Experience Platform Launch

Launch füllt diese Variable automatisch im Backend basierend auf den in der Oberfläche festgelegten Variablen, sodass sie in Implementierungen mit Launch immer festgelegt wird.

>[!IMPORTANT] Wenn Sie Variablen in Launch mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie die Variable auch in `linkTrackVars` mit benutzerdefiniertem Code einbeziehen.

## s.linkTrackVars in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

The `s.linkTrackVars` variable is a string containing a comma-delimited list of variables that you want to include in link tracking image requests (`tl()` method). Die folgenden beiden Kriterien müssen erfüllt sein, um Dimensionen in Linktracking-Treffer einzubeziehen:

* Legen Sie den gewünschten Variablenwert fest. Beispiel: `s.eVar1 = "Example value";`.
* Legen Sie die gewünschte Variable in der `linkTrackVars`-Variablen fest. Beispiel: `s.linkTrackEvents = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Adobe hat jedoch AppMeasurement-Code im Code-Manager bereitgestellt, wobei diese Variable auf `"None"` gesetzt ist. Gültige Werte sind alle Variablen auf Seitenebene, die eine Dimension ausfüllen.

* Wenn diese Variable nicht definiert oder auf eine leere Zeichenfolge festgelegt ist, werden *alle* Variablen in Bildanforderungen zum Linktracking einbezogen.
* Wenn diese Variable auf `"None"` festgelegt ist, werden in Bildanforderungen zum Linktracking *keine* Variablen einbezogen.

>[!TIP] Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Variablen in dieser Variablen. Zum Beispiel ist `s.linkTrackVars = "eVar1";` korrekt, während `s.linkTrackVars = "s.eVar1";` nicht korrekt ist.

## Beispiel

Die folgende Linktracking-Funktion enthält nur `eVar1` (nicht `eVar2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
