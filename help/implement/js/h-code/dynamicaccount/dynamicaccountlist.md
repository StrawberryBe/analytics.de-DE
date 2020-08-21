---
title: dynamicAccountList
description: Legen Sie eine Logik fest, wie Ihre Implementierung die Report Suite bestimmt.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '258'
ht-degree: 100%

---


# s.dynamicAccountList

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder in Adobe Experience Platform Launch nicht unterstützt.

Die `s.dynamicAccountList`-Variable bestimmt dynamisch den Wert von `s_account`. Ist `dynamicAccountSelection` gleich `true`, wird die `dynamicAccountMatch`-Variable mit `dynamicAccountList` verglichen. Wenn eine Übereinstimmung gefunden wird, wird die entsprechende Report Suite-ID verwendet.

## Syntax

Diese Variable ist eine Zeichenfolge, die automatisch von der JavaScript-Datei analysiert wird.

```JavaScript
s.dynamicAccountList = "[rsid]=[valuetomatch],[rsid2]=[valuetomatch]";
```

Gültige Eingabe ist eine durch Semikolon getrennte Liste von rsid- und value-Paaren. Jede Liste enthält die folgenden Elemente:

* Eine oder mehrere Report Suite-IDs (durch Kommas getrennt)
* Ein Gleichheitszeichen
* Eine oder mehrere übereinstimmende Zeichenfolgen (durch Kommas getrennt)

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden. Fügen Sie keine Leerzeichen ein.

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
* Bei Seiten, die auf einer lokalen Festplatte gespeichert oder über ein Web-basiertes Übersetzungsmodul übersetzt werden (wie z. B. die übersetzten Seiten in Google), funktioniert die dynamische Kontoauswahl wahrscheinlich nicht mehr.
* Die `dynamicAccountSelection`-Regeln gelten nur für den in `dynamicAccountMatch` festgelegten Abschnitt der URL.
* Verwenden Sie den [!DNL Adobe Experience Cloud Debugger], um die Ziel-Report Suites zu testen.
