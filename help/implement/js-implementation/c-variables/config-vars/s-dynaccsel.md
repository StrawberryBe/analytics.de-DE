---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.dynamicAccountSelection

Mithilfe der Variablen „“ können Sie die Report Suite anhand der URL der jeweiligen Seite dynamisch auswählen.

> [!NOTE] `dynamicAccountSelection` funktioniert beim benutzerspezifischen Linktracking nicht.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | False |

> [!NOTE]Sowohl `dynamicAccountList` als auch `dynamicAccountMatch` werden ignoriert, wenn die Variable `dynamicAccountSelection` nicht deklariert oder auf „False“ festgelegt ist.

## Syntax und mögliche Werte

```js
s.dynamicAccountSelection=[true|false]
```

Als Werte von *`dynamicAccountSelection`* sind nur „true“ und „false“ zulässig.

## Beispiele

```js
s.dynamicAccountSelection=true
```

```js
s.dynamicAccountSelection=false
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) nicht unterstützt.

* Verwenden Sie immer den [!DNL DigitalPulse Debugger], um zu bestimmen, welche Report Suite die Daten von den einzelnen Seiten erhält.
