---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.useForcedLinkTracking


Die Variable „“ gibt an, in welcher Report Suite Daten gespeichert und angezeigt werden.

Wenn Daten an mehrere Report Suites gesendet werden (Multi-Suite-Tagging), kann `s.account` aus einer durch Kommas getrennten Liste von Werten bestehen. Die Report Suite-ID wird von Adobe bestimmt.

## Parameter

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| 40 Byte | Im URL-Pfad | nicht angegeben | nicht angegeben |

Jede Report Suite-ID muss mit dem Wert übereinstimmen, der in der [!DNL Admin Console] erstellt wurde. Report Suite-IDs dürfen maximal 40 Byte lang sein. Alle Report Suites zusammengenommen (die gesamte kommagetrennte Liste) unterliegen jedoch keinen Beschränkungen.

Die Report Suite stellt bei Berichten die grundlegendste Segmentierungsebene dar. Sie können so viele Report Suites festlegen, wie Ihr Vertrag zulässt. Jede Report Suite bezieht sich auf eine bestimmte Reihe von Tabellen, die in den Datenerfassungsservern von Adobe gefüllt werden. Eine Report Suite wird durch die Variable `s_account` in Ihrem JavaScript-Code identifiziert.

Die aktuelle Report Suite wird in [!DNL Analytics] oben links in den Berichten im Site-Dropdownfeld angezeigt. Jede Report Suite besitzt eine eindeutige ID, die als Report Suite-ID bezeichnet wird. Die Variable `s_account` enthält eine oder mehrere Report Suite-IDs, an die Daten gesendet werden. Der Wert für die Report Suite-ID, der [!DNL Analytics]-Benutzern nicht angezeigt wird, muss von Adobe bereitgestellt oder genehmigt werden, bevor Sie ihn verwenden können. Zu jeder Report Suite-ID gibt es einen leicht verständlichen Anzeigenamen, der in der [!DNL Admin Console] im Abschnitt „Report Suites“ geändert werden kann.

Die Variable `s_account` wird normalerweise in der JavaScript-Datei (s_code.js) deklariert. Sie können die Variable `s_account` auf der HTML-Seite deklarieren. Dies ist eine gängige Praxis, wenn sich der Wert von `s_account` von Seite zu Seite ändern kann. Da die Variable `s_account` einen globalen Gültigkeitsbereich besitzt, sollte sie sofort deklariert werden, bevor die JavaScript-Datei von Adobe aufgenommen wird. Wenn `s_account` beim Laden der JavaScript-Datei keinen Wert enthält, werden auch keine Daten an [!DNL Analytics] gesendet.

[!DNL DigitalPulse Debugger]von Adobe zeigt den Wert von `s_account` im Pfad der URL an, die direkt unter dem Wort „Bild“ direkt nach /b/ss/ angezeigt wird. In einigen Fällen wird der Wert von `s_account` auch in der Domäne vor 112.2o7.net angezeigt. Der Wert im Pfad ist der einzige Wert, der die Ziel-Report Suite vorgibt. Im folgenden Beispiel ist die Stelle im Debugger, die die Report Suites angibt, fett markiert dargestellt. Siehe [DigitalPulse-Debugger prüfen](https://docs.adobe.com/content/help/de-DE/analytics/implementation/testing-and-validation/debugger.html).

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

* Wenn `s_account` leer oder nicht deklariert ist oder einen unerwarteten Wert enthält, werden keine Daten erfasst.
* Wenn `s_account` eine kommagetrennte Liste ist (Multi-Suite-Tagging), dürfen Sie zwischen den einzelnen Report Suite-IDs keine Leerzeichen setzen.
* Wenn [!UICONTROL s.dynamicAccountSelection] auf *True* eingestellt ist, wird die Ziel-Report Suite anhand der URL bestimmt. Verwenden Sie den [!DNL DigitalPulse Debugger], um die Ziel-Report Suites zu bestimmen.

* In manchen Fällen kann [!DNL VISTA] eingesetzt werden, um die Ziel-Report Suite zu ändern. Wenn Erstanbietercookies eingesetzt werden oder die Site mehr als 20 aktive Report Suites besitzt, wird empfohlen, Daten mit [!DNL VISTA] in andere Report Suites umzuleiten oder zu kopieren.

* Deklarieren Sie `s_account` immer innerhalb der JS-Datei oder direkt vor der Stelle mit der Include-Anweisung.
