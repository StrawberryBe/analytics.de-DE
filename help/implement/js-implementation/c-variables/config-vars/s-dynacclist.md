---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountList

[!DNL AppMeasurement] für JavaScript kann dynamisch eine Report Suite auswählen, an die die Daten gesendet werden. Die Variable „“ enthält die Regeln, mit denen die Ziel-Report Suite ermittelt wird.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | "" |

Diese Variable wird gemeinsam mit den Variablen *`dynamicAccountSelection`* and *`dynamicAccountMatch`* variables. Die Regeln in *`dynamicAccountList`* werden angewendet, wenn "true" *`dynamicAccountSelection`* festgelegt ist, und sie gelten für den Abschnitt der URL, der in *`dynamicAccountMatch`* angegeben ist.

Wenn keine der Regeln in *`dynamicAccountList`* Übereinstimmung mit der URL der Seite steht, wird die in identifizierte Report Suite verwendet `s_account` . Die in dieser Variablen aufgeführten Regeln werden von links nach rechts angewendet. Wenn mehrere Regeln auf eine Seiten-URL zutreffen, wird die Report Suite anhand der Regel ermittelt, die am weitesten links steht. Aus diesem Grund sollten Sie allgemeinere Regeln in der Liste weiter rechts platzieren.

In den folgenden Beispielen ist die Seiten-URL `www.mycompany.com/path1/?prod_id=12345` und `dynamicAccountSelection` auf *true* eingestellt `s_account``mysuitecom.`

| DynamicAccountList-Wert | DynamicAccountMatch-Wert | Report Suite, die die Daten erhält |
|---|---|---|
| `mysuite2=www2.mycompany.com;mysuite1=mycompany.com` | window.location.host | mysuite1 |
| "mysuite1=path4,path1;mysuite2=path2" | window.location.pathname | mysuite1, mysuite2 |
| "mysuite1=path5" | window.location.pathname | mysuitecom, mysuite1 |
| "myprodsuite=prod_id" | window.location.search?window.location.search:"?") | myprodsuite |

## Syntax und mögliche Werte

Die Variable `dynamicAccountList` ist eine durch Semikolons getrennte Liste mit Einträgen der Form „Name=Wert“ (Regeln). Jeder Eintrag der Liste muss die folgenden Elemente enthalten:

* Eine oder mehrere Report Suite-IDs (mit Kommas getrennt)
* Ein Gleichheitszeichen
* Einen oder mehrere URL-Filter (mit Kommas getrennt)

```js
s.dynamicAccountList=rs1[,rs2]=domain1.com[,domain2.com/path][;...]
```

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden (keine Leerzeichen).

## Beispiele

```js
s.dynamicAccountList="mysuite2=www2.mycompany.com;mysuite1=mycompany.com"
```

```js
s.dynamicAccountList="ms1,ms2=site1.com;ms1,ms3=site3.com"
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Die dynamische Kontoauswahl wird nicht von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* Wenn die Seiten-URL mit mehreren Regeln übereinstimmt, wird die Regel ausgewählt, die am weitesten links steht.
* Wenn keine der Regeln zutrifft, wird die standardmäßige Report Suite verwendet.
* Bei Seiten, die auf einer lokalen Festplatte gespeichert oder über ein webbasiertes Übersetzungsmodul übersetzt werden (wie z. B. die übersetzten Seiten in Google), funktioniert die dynamische Kontoauswahl möglicherweise nicht mehr. Für eine präzisere Nachverfolgung müssen Sie die Variable `s_account` serverseitig auffüllen.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.

* Achten Sie bei Verwendung der dynamischen Kontoauswahl darauf, jedes Mal, wenn Sie eine neue Domäne abrufen, eine Aktualisierung durchzuführen *`dynamicAccountList`* .
* Die Ziel-Report Suite können Sie mit dem [!DNL DigitalPulse Debugger] ermitteln. The `dynamicAccountSelection` variable always overrides the value of `s_account`.
