---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.dynamicAccountList

> [!NOTE] Die `s.dynamicAccountList`-Variable wird in den [aktuellen AppMeasurement-Bibliotheken](../../c-appmeasurement-js/appmeasure-mjs.md) nicht unterstützt. Sie wird nur in älteren AppMeasurement-Versionen wie H-Code verwendet.

Die `s.dynamicAccountList`-Variable wird verwendet, um dynamisch eine Report Suite zu bestimmen, an die Daten gesendet werden sollen. Sie wird zusammen mit den Variablen `dynamicAccountSelection` und `dynamicAccountMatch` verwendet. Die Regeln in `dynamicAccountList` werden angewendet, wenn `dynamicAccountSelection` als `true` festgelegt ist, und sie gelten für den Abschnitt der URL, der in `dynamicAccountMatch` angegeben ist.

## Syntax und mögliche Werte

```JavaScript
s.dynamicAccountList="rs1[,rs2]=domain1.com[,domain2.com/path][;...]";
```

Eine gültige Eingabe ist eine durch Semikolons getrennte Liste mit Einträgen der Form „Name=Wert“ (Regeln). Jede Liste enthält die folgenden Elemente:

* Eine oder mehrere Report Suite-IDs (durch Kommas getrennt)
* Ein Gleichheitszeichen
* Einen oder mehrere URL-Filter (durch Kommas getrennt)

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden (keine Leerzeichen).

## Beispiele

Bei allen folgenden Beispielen lautet die Seiten-URL `https://example.com/path2/?prod_id=12345`, und die `dynamicAccountSelection`-Variable ist auf `true` und die `s_account`-Variable auf `examplersid` festgelegt.

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

* Die in dieser Variablen aufgeführten Regeln werden von links nach rechts angewendet. Wenn mehrere Regeln auf eine `dynamicAccountMatch`-Variable zutreffen, wird die Report Suite anhand der Regel ermittelt, die am weitesten links steht. Aus diesem Grund sollten Sie allgemeinere Regeln in der Liste weiter rechts platzieren.
* Wenn keine der Regeln zutrifft, wird die standardmäßige Report Suite in `s_account` verwendet.
* Bei Seiten, die auf einer lokalen Festplatte gespeichert oder über ein webbasiertes Übersetzungsmodul übersetzt werden (wie z. B. die übersetzten Seiten in Google), funktioniert die dynamische Kontoauswahl wahrscheinlich nicht mehr.
* Die `dynamicAccountSelection`-Regeln gelten nur für den in `dynamicAccountMatch` festgelegten Abschnitt der URL.
* Verwenden Sie den [!DNL Adobe Experience Cloud Debugger], um die Ziel-Report Suites zu testen.
