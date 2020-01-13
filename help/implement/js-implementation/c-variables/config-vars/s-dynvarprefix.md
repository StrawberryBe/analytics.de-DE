---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.dynamicVariablePrefix {#concept_38C1F2452DDB47FCA8F458BE1398E276}

Mithilfe der Variablen „“ sind Implementierungen in Flag-Variablen möglich, die dynamisch aufgefüllt werden sollen.

Dynamisch aufgefüllt werden können Cookies, Anforderungsheader und Abfragezeichenfolgenparameter von Bildanforderungen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | D= | Alle | D= |

## Syntax und mögliche Werte

```js
s.prop1="D=User-Agent"
```

ODER BENUTZERDEFINIERTES FLAG FÜR DYNAMISCHE VARIABLEN VERWENDEN

```js
s.dynamicVariablePrefix=".."
```

## Beispiele

```js
s.prop1="D=User-Agent"
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
