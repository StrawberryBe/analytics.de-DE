---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicVariablePrefix {#concept_38C1F2452DDB47FCA8F458BE1398E276}

Mithilfe der Variablen „“ sind Implementierungen in Flag-Variablen möglich, die dynamisch aufgefüllt werden sollen.

Dynamisch aufgefüllt werden können Cookies, Anforderungsheader und Abfragezeichenfolgen-Parameter von Bildanforderungen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | D= | Alle | D= |

## Syntax und mögliche Werte

```js
s.prop1="D=User-Agent”
```

ODER BENUTZERDEFINIERTES FLAG FÜR DYNAMISCHE VARIABLEN VERWENDEN

```js
s.dynamicVariablePrefix=".."
```

## Beispiele

```js
s.prop1="D=User-Agent”
```

ODER BENUTZERDEFINIERTES FLAG FÜR DYNAMISCHE VARIABLEN VERWENDEN

```js
s.dynamicVariablePrefix=".."
```

```js
s.prop1="..User-Agent"
```

## Probleme, Fragen und Tipps

* Durch den Einsatz dynamischer Variablen lässt sich die Gesamtlänge der URL deutlich reduzieren, indem Werte in andere variablen kopiert werden.

* Dynamische Variablen können auch eingesetzt werden, um Daten aus Headern und Cookies zu erfassen, bei denen ein anderer Weg zur Datenerfassung nicht möglich ist.
