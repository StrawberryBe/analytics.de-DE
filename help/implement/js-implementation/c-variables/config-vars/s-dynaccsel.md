---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountSelection

Mithilfe der Variablen „“ können Sie die Report Suite anhand der URL der jeweiligen Seite dynamisch auswählen.

>[!NOTE]
>
>`dynamicAccountSelection` funktioniert bei der benutzerspezifischen Linktracking nicht.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | False |

>[!NOTE]
>
>Both `dynamicAccountList` and `dynamicAccountMatch` are ignored if the `dynamicAccountSelection` variable is not declared or set to 'false.'

## Syntax und mögliche Werte

```js
s.dynamicAccountSelection=[true|false]
```

Als Werte von *`dynamicAccountSelection`* zu trennen.

## Beispiele

```js
s.dynamicAccountSelection=true
```

```js
s.dynamicAccountSelection=false
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Die dynamische Kontoauswahl wird nicht von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* Always use the [!DNL DigitalPulse Debugger] to determine which report suite is receiving data from each page.
