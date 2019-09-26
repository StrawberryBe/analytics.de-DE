---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.account

Die Variable „“ gibt an, in welcher Report Suite Daten gespeichert und angezeigt werden.

If sending to multiple report suites (multi-suite tagging), `s.account` may be a comma-separated list of values. Die Report Suite-ID wird von Adobe bestimmt.

## Parameter

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| 40 Byte | Im URL-Pfad | Keine | Keine |

Jede Report Suite-ID muss mit dem Wert übereinstimmen, der in der [!DNL Admin Console] erstellt wurde. Report Suite-IDs dürfen maximal 40 Byte lang sein. Alle Report Suites zusammengenommen (die gesamte kommagetrennte Liste) unterliegen jedoch keinen Beschränkungen.

Die Report Suite stellt bei Berichten die grundlegendste Segmentierungsebene dar. Sie können so viele Report Suites festlegen, wie Ihr Vertrag zulässt. Jede Report Suite bezieht sich auf eine bestimmte Reihe von Tabellen, die in den Datenerfassungsservern von Adobe gefüllt werden. Eine Report Suite wird durch die Variable `s_account`in Ihrem JavaScript-Code identifiziert. 

Die aktuelle Report Suite wird in [!DNL Analytics] oben links in den Berichten im Site-Dropdownfeld angezeigt. Jede Report Suite besitzt eine eindeutige ID, die als Report Suite-ID bezeichnet wird. Die Variable `s_account`enthält eine oder mehrere Report Suite-IDs, an die Daten gesendet werden. Der Wert für die Report Suite-ID, der [!DNL Analytics]-Benutzern nicht angezeigt wird, muss von Adobe bereitgestellt oder genehmigt werden, bevor Sie ihn verwenden können. Zu jeder Report Suite-ID gibt es einen leicht verständlichen Anzeigenamen, der in der [!DNL Admin Console] im Abschnitt „Report Suites“ geändert werden kann.

The `s_account` variable is normally declared inside the JavaScript file (s_code.js). Sie können die `s_account` Variable auf der HTML-Seite deklarieren. Dies ist eine gängige Praxis, wenn sich der Wert von `s_account` Seite zu Seite ändern kann. Because the `s_account` variable has a global scope, it should be declared immediately before including Adobe's JavaScript file. If `s_account` does not have a value when the JavaScript file is loaded, no data is sent to [!DNL Analytics].

Adobe's [!DNL DigitalPulse Debugger] displays the value of `s_account` in the path of the URL that appears just below the word "Image," just after /b/ss/. In einigen Fällen wird der Wert von `s_account` auch in der Domäne vor 112.2o7.net angezeigt. Der Wert im Pfad ist der einzige Wert, der die Ziel-Report Suite vorgibt. Im folgenden Beispiel ist die Stelle im Debugger, die die Report Suites angibt, fett markiert dargestellt. Siehe   [DigitalPulse-Debugger prüfen](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html).

```js
https://mycompany.112.207.net/b/ss/ 
<b>mycompanycom,mycompanysection</b>/1/H.1-pdv-2/s21553246810948?[AQB]
```

## Syntax und mögliche Werte

Die Report Suite-ID ist eine alphanumerische Zeichenfolge mit ASCII-Zeichen und einer maximalen Länge von 40 Byte. Der Bindestrich ist das einzige nicht alphanumerische Zeichen, das zulässig ist. Leerzeichen, Punkte, Kommas und sonstige Satzzeichen sind nicht zulässig. Die Variable `s_account` kann mehrere Report Suites enthalten, die alle Daten von der jeweiligen Seite erhalten.

```js
var s_account="reportsuitecom[,reportsuite2[,reportsuite3]]"
```

Alle Werte von `s_account` müssen von Adobe bereitgestellt oder genehmigt werden.

## Beispiele

```js
var s_account="mycompanycom"
```

```js
var s_account="mycompanycom,mycompanysection"
```

## Konfiguration der Variablen in Analytics

Der zu einer Report Suite-ID zugehörige Anzeigename kann von Adobe [!DNL Customer Care] geändert werden. Der Anzeigename wird in [!DNL Analytics] links oben im Site-Dropdownfeld angezeigt.

## Probleme, Fragen und Tipps

* If `s_account` is empty, not declared, or contains an unexpected value, no data is collected.
* When the `s_account` variable is a comma-separated list (multi-suite tagging), do not put spaces between report suite IDs.
* If [!UICONTROL s.dynamicAccountSelection] is set to *True* the URL is used to determine the destination report suite. Use the [!DNL DigitalPulse Debugger] to determine the destination report suite(s).

* In manchen Fällen kann [!DNL VISTA] eingesetzt werden, um die Ziel-Report Suite zu ändern. Wenn Erstanbietercookies eingesetzt werden oder die Site mehr als 20 aktive Report Suites besitzt, wird empfohlen, Daten mit [!DNL VISTA] in andere Report Suites umzuleiten oder zu kopieren.

* Always declare `s_account` inside the JS file or just before it is included.
