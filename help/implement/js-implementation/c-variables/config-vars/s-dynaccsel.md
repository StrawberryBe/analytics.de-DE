---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.dynamicAccountSelection

Mithilfe der Variablen „“ können Sie die Report Suite anhand der URL der jeweiligen Seite dynamisch auswählen.

> [!NOTE] `dynamicAccountSelection` funktioniert bei der benutzerspezifischen Linktracking nicht.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | False |

> [!NOTE]Sowohl `dynamicAccountList` als auch `dynamicAccountMatch` werden ignoriert, wenn die Variable `dynamicAccountSelection` nicht deklariert oder auf „False“ festgelegt ist.

## Syntax und mögliche Werte

```js
s.dynamicAccountSelection=[true|false]
```

Als Werte von *`dynamicAccountSelection`*.

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

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) nicht unterstützt.

* Verwenden Sie immer den [!DNL DigitalPulse Debugger], um zu bestimmen, welche Report Suite die Daten von den einzelnen Seiten erhält.
