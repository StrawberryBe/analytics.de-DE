---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 5d6ff87bd49140a974fcaaeed714d0f0b7d1e58b

---


# s.dynamicAccountList

> [!NOTE] Die `s.dynamicAccountList` Variable wird in den [aktuellen AppMeasurement-Bibliotheken](../../c-appmeasurement-js/appmeasure-mjs.md)nicht unterstützt. Es wird nur in älteren AppMeasurement-Versionen wie H-Code verwendet.

Die `s.dynamicAccountList` Variable wird verwendet, um dynamisch eine Report Suite zu bestimmen, an die Daten gesendet werden sollen. Es wird zusammen mit den `dynamicAccountSelection` Variablen und `dynamicAccountMatch` Variablen verwendet. Die in `dynamicAccountList` aufgeführten Regeln werden angewendet, wenn `dynamicAccountSelection` sie auf `true`festgelegt sind, und sie gelten für den Abschnitt der in `dynamicAccountMatch`.

## Syntax und mögliche Werte

```JavaScript
s.dynamicAccountList="rs1[,rs2]=domain1.com[,domain2.com/path][;...]";
```

Valid input is a semicolon-separated list of name=value pairs (rules). Jede Liste enthält die folgenden Elemente:

* One or more report suite ID's (separated by commas)
* An equals sign
* One or more URL filters (comma-separated)

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden (keine Leerzeichen).

## Beispiele

Bei allen folgenden Beispielen lautet die Seiten-URL `https://example.com/path2/?prod_id=12345`, die `dynamicAccountSelection` Variable ist auf `true`und die `s_account` Variable auf `examplersid`.

```js
// In this example, the report suite that receives data is examplersid1.
s.dynamicAccountMatch = "window.location.hostname";
s.dynamicAccountList = "examplersid2=www2.example.com;examplersid1=example.com";

// In this example, the report suite that receives data is examplersid2.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid2=path2;examplersid3=path3";

// In this example, no rules match so it resorts to the default rsid in s_account, examplersid.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid4=path4;examplersid5=path5";
```

## Probleme, Fragen und Tipps

* Die in dieser Variablen aufgeführten Regeln werden von links nach rechts angewendet. If the `dynamicAccountMatch` variable matches more than one rule, the left-most rule is used to determine the report suite. As a result, place more generic rules to the right of the list.
* If no rules match, the default report suite in `s_account` is used.
* Wenn Ihre Seite auf der Festplatte eines Benutzers gespeichert oder über eine webbasierte Übersetzungs-Engine übersetzt wird (z. B. die übersetzten Seiten von Google), funktioniert die dynamische Kontoauswahl wahrscheinlich nicht.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.
* Testen Sie die Ziel-Report Suite [!DNL Adobe Experience Cloud Debugger] mit dem .
