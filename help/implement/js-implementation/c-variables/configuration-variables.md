---
description: Konfigurationsvariablen, die in AppMeasurement.js festgelegt sind.
keywords: Analytics-Implementierung
seo-description: Konfigurationsvariablen in AppMeasurement.js für Adobe Analytics eingestellt
seo-title: Konfigurationsvariablen
solution: Analytics
subtopic: Variablen
title: Konfigurationsvariablen
topic: Entwickler und Implementierung
uuid: a19484b6-e350-4c12-b4d6-a31c79a42db0
translation-type: tm+mt
source-git-commit: edc1ecb471aadb9399664c0985a3aa3ecde328bf

---


# Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Die am häufigsten verwendeten Konfigurationsvariablen, die normalerweise in der globalen JavaScript-Datei AppMeasurement.js festgelegt werden. Diese Variablen können gegebenenfalls im Code und in Links auf Seitenebene von Analytics festgelegt werden.

Not all of these variables appear in the code by default when you generate code through the **[!UICONTROL Admin Tool]** &gt; **[!UICONTROL Code Manager]**. Einige dieser Konfigurationsvariablen sind möglicherweise nicht für die Implementierungsanforderungen Ihrer Site geeignet.

Zu den Zielen der Verwendung dieser Konfigurationsvariablen zählen u. a.:

* Tracking mehrerer Sites/Domänen
* Verwenden von Währung für Einkäufe
* Erfassen von Daten in verschiedenen Sprachen
* Link-Tracking (Anzahl heruntergeladener Dateien, Links zu externen Sites)
* Tracking einzigartiger Links für einzigartige Zwecke

>[!NOTE]
>
>[!DNL AppMeasurement] erfordert, dass alle Konfigurationsvariablen vor dem anfänglichen Aufruf der track-Funktion festgelegt werden, `t()`. Wenn Konfigurationsvariablen nach dem Aufruf von festgelegt werden, `t()`können unerwartete Ergebnisse auftreten. To ensure proper data collection, all configuration variables must be above the `doPlugins` function.

## s.account {#concept_685A5C832A6C40619ACB5920925785DC}

Die Variable „“ gibt an, in welcher Report Suite Daten gespeichert und angezeigt werden.

If sending to multiple report suites (multi-suite tagging), `s.account` may be a comma-separated list of values. Die Report Suite-ID wird von Adobe bestimmt.

**Parameter**

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| 40 Byte | Im URL-Pfad | Keine | Keine |

Jede Report Suite-ID muss mit dem Wert übereinstimmen, der in der [!DNL Admin Console] erstellt wurde. Report Suite-IDs dürfen maximal 40 Byte lang sein. Alle Report Suites zusammengenommen (die gesamte kommagetrennte Liste) unterliegen jedoch keinen Beschränkungen.

Die Report Suite stellt bei Berichten die grundlegendste Segmentierungsebene dar. Sie können so viele Report Suites festlegen, wie Ihr Vertrag zulässt. Jede Report Suite bezieht sich auf eine bestimmte Reihe von Tabellen, die in den Datenerfassungsservern von Adobe gefüllt werden. Eine Report Suite wird durch die Variable `s_account`in Ihrem JavaScript-Code identifiziert. 

Die aktuelle Report Suite wird in [!DNL Analytics] oben links in den Berichten im Site-Dropdownfeld angezeigt. Jede Report Suite besitzt eine eindeutige ID, die als Report Suite-ID bezeichnet wird. Die Variable `s_account`enthält eine oder mehrere Report Suite-IDs, an die Daten gesendet werden. Der Wert für die Report Suite-ID, der [!DNL Analytics]-Benutzern nicht angezeigt wird, muss von Adobe bereitgestellt oder genehmigt werden, bevor Sie ihn verwenden können. Zu jeder Report Suite-ID gibt es einen leicht verständlichen Anzeigenamen, der in der [!DNL Admin Console] im Abschnitt „Report Suites“ geändert werden kann.

The `s_account` variable is normally declared inside the JavaScript file (s_code.js). Sie können die `s_account` Variable auf der HTML-Seite deklarieren. Dies ist eine gängige Praxis, wenn sich der Wert von `s_account` Seite zu Seite ändern kann. Because the `s_account` variable has a global scope, it should be declared immediately before including Adobe's JavaScript file. If `s_account` does not have a value when the JavaScript file is loaded, no data is sent to [!DNL Analytics].

Adobe's [!DNL DigitalPulse Debugger] displays the value of `s_account` in the path of the URL that appears just below the word "Image," just after /b/ss/. In einigen Fällen wird der Wert von `s_account` auch in der Domäne vor 112.2o7.net angezeigt. Der Wert im Pfad ist der einzige Wert, der die Ziel-Report Suite vorgibt. Im folgenden Beispiel ist die Stelle im Debugger, die die Report Suites angibt, fett markiert dargestellt. Siehe   [DigitalPulse-Debugger prüfen](../../../implement/impl-testing/debugger.md#concept_B26FFE005EDD4E0FACB3117AE3E95AA2).

```js
https://mycompany.112.207.net/b/ss/ 
<b>mycompanycom,mycompanysection</b>/1/H.1-pdv-2/s21553246810948?[AQB]
```

**Syntax und mögliche Werte** {#section_3BE913DF26D848AEB4CB5B0A6CE7F0CA}

Die Report Suite-ID ist eine alphanumerische Zeichenfolge mit ASCII-Zeichen und einer maximalen Länge von 40 Byte. Der Bindestrich ist das einzige nicht alphanumerische Zeichen, das zulässig ist. Leerzeichen, Punkte, Kommas und sonstige Satzzeichen sind nicht zulässig. Die Variable `s_account` kann mehrere Report Suites enthalten, die alle Daten von der jeweiligen Seite erhalten.

```js
var s_account="reportsuitecom[,reportsuite2[,reportsuite3]]"
```

Alle Werte von `s_account` müssen von Adobe bereitgestellt oder genehmigt werden.

**Beispiele** {#section_16580A9101B64560A58C7745397FB42F}

```js
var s_account="mycompanycom"
```

```js
var s_account="mycompanycom,mycompanysection"
```

**Konfiguration der Variablen in Analytics** {#section_7DFB2CCF02F045AFB1AD4F376638393B}

Der zu einer Report Suite-ID zugehörige Anzeigename kann von Adobe [!DNL Customer Care] geändert werden. Der Anzeigename wird in [!DNL Analytics] links oben im Site-Dropdownfeld angezeigt.

**Probleme, Fragen und Tipps** {#section_BFFDA5C0AF31442494B0E02F0925CF93}

* If `s_account` is empty, not declared, or contains an unexpected value, no data is collected.
* When the `s_account` variable is a comma-separated list (multi-suite tagging), do not put spaces between report suite IDs.
* If [!UICONTROL s.dynamicAccountSelection] is set to *True* the URL is used to determine the destination report suite. Use the [!DNL DigitalPulse Debugger] to determine the destination report suite(s).

* In manchen Fällen kann [!DNL VISTA] eingesetzt werden, um die Ziel-Report Suite zu ändern. Wenn Erstanbietercookies eingesetzt werden oder die Site mehr als 20 aktive Report Suites besitzt, wird empfohlen, Daten mit [!DNL VISTA] in andere Report Suites umzuleiten oder zu kopieren.

* Always declare `s_account` inside the JS file or just before it is included.

## s.dynamicAccountSelection {#concept_FAD499DB357148DB8BD74F08093D3E35}

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

**Syntax und mögliche Werte** {#section_36E5D0E2170345F5A652B44CE85DFED1}

```js
s.dynamicAccountSelection=[true|false]
```

Als Werte von *`dynamicAccountSelection`*.

**Beispiele** {#section_E8CE8BA62C7545889531495E2521663D}

```js
s.dynamicAccountSelection=true
```

```js
s.dynamicAccountSelection=false
```

**Konfigurationseinstellungen** {#section_F052FA38144B4F84B015A263A8E711CF}

Keine

**Probleme, Fragen und Tipps** {#section_62F0B0895BC84A05840AEEED0643DE60}

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8)nicht unterstützt.
* Always use the [!DNL DigitalPulse Debugger] to determine which report suite is receiving data from each page.

## s.dynamicAccountList {#concept_19715BA0AD4D41748E0C4A4A6B71AB51}

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

**Syntax und mögliche Werte** {#section_7360E4354ED345E8BAAE210DBD58A7EC}

The `dynamicAccountList` variable is a semicolon-separated list of name=value pairs (rules). Jeder Eintrag der Liste muss die folgenden Elemente enthalten:

* Eine oder mehrere Report Suite-IDs (mit Kommas getrennt)
* Ein Gleichheitszeichen
* Einen oder mehrere URL-Filter (mit Kommas getrennt)

```js
s.dynamicAccountList=rs1[,rs2]=domain1.com[,domain2.com/path][;...]
```

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden (keine Leerzeichen).

**Beispiele** {#section_49936D14EF6D45859B666C9E7A4CBA9E}

```js
s.dynamicAccountList="mysuite2=www2.mycompany.com;mysuite1=mycompany.com"
```

```js
s.dynamicAccountList="ms1,ms2=site1.com;ms1,ms3=site3.com"
```

**Konfigurationseinstellungen** {#section_9F99CD741BC7449B8CCC108094B2EB85}

Keine

**Probleme, Fragen und Tipps** {#section_3E10534FCC05457AB67147BB480C8BB3}

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8)nicht unterstützt.
* Wenn die Seiten-URL mit mehreren Regeln übereinstimmt, wird die Regel ausgewählt, die am weitesten links steht.
* Wenn keine der Regeln zutrifft, wird die standardmäßige Report Suite verwendet.
* Bei Seiten, die auf einer lokalen Festplatte gespeichert oder über ein webbasiertes Übersetzungsmodul übersetzt werden (wie z. B. die übersetzten Seiten in Google), funktioniert die dynamische Kontoauswahl möglicherweise nicht mehr. Für eine präzisere Nachverfolgung müssen Sie die Variable `s_account` serverseitig auffüllen.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.

* Achten Sie bei Verwendung der dynamischen Kontoauswahl darauf, jedes Mal, wenn Sie eine neue Domäne abrufen, eine Aktualisierung durchzuführen *`dynamicAccountList`* .
* Die Ziel-Report Suite können Sie mit dem [!DNL DigitalPulse Debugger] ermitteln. The `dynamicAccountSelection` variable always overrides the value of `s_account`.

## s.dynamicAccountMatch {#concept_718171E602214CCC9905C749708BBE52}

Die Variable „“ ruft mithilfe des DOM-Objekts den Abschnitt der URL ab, auf den alle in „“ aufgeführten Regeln angewendet werden.

This variable is only valid when *`dynamicAccountSelection`* is set to 'True.' Da der Standardwert [!DNL window.location.host] lautet, ist diese Variable nicht erforderlich, damit die [!UICONTROL dynamische Kontoauswahl] ordnungsgemäß funktioniert. For additional information, see [dynamicAccountList](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_19715BA0AD4D41748E0C4A4A6B71AB51).

Die Regeln in `dynamicAccountList` werden auf den Wert von angewendet `dynamicAccountMatch`. Wenn `dynamicAccountMatch` nur [!DNL window.location.host] (Standard) enthalten ist, `dynamicAccountList` gelten die Regeln nur für die Domäne der Seite.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | window.location.host |

**Syntax und mögliche Werte** {#section_95CD81972C22419B80A921CA137D3841}

The `dynamicAccountMatch` variable is usually populated by the Adobe consultant who provides the AppMeasurement for JavaScript file. Jedoch können die nachfolgend aufgeführten Werte jederzeit übernommen werden.

```js
s.dynamicAccountMatch=[DOM object]
```

| Beschreibung | Wert |
|---|---|
| Domäne (Standard) | window.location.host |
| Pfad | window.location.pathname |
| Abfragezeichenfolge | (window.location.search?window.location.search:"?") |
| Domäne und Pfad | window.location.host+window.location.pathname |
| Pfad und Abfragezeichenfolge | window.location.pathname+(window.location.search?window.location.search:"?") |
| Vollständige URL | window.location.href |

**Beispiele** {#section_924687CCE255421AA2223A3D4B8B6A30}

```js
s.dynamicAccountMatch=window.location.pathname
```

```js
s.dynamicAccountMatch=window.location.host+window.location.pathname
```

**Konfigurationseinstellungen** {#**section_43BCE13B1ADD4D418DF7CBB9DD7A6472}

Keine

**Probleme, Fragen und Tipps** {#section_EF9B2977BC21497D8C5EEB9BAD731E17}

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8)nicht unterstützt.
* Bei auf einer Festplatte gespeicherten Seiten ist [!DNL window.location.host] leer, wodurch deren Seitenansichten an die standardmäßige Report Suite (in `s_account`).

* Bei über ein webbasiertes Tool übersetzten Seiten (wie z. B. Google) funktioniert die [!UICONTROL Dynamische Kontoauswahl] nicht richtig. Für eine präzisere Nachverfolgung müssen Sie die Variable [!UICONTROL s_account] serverseitig auffüllen.

## s.dynamicVariablePrefix {#concept_38C1F2452DDB47FCA8F458BE1398E276}

Mithilfe der Variablen „“ sind Implementierungen in Flag-Variablen möglich, die dynamisch aufgefüllt werden sollen.

Dynamisch aufgefüllt werden können Cookies, Anforderungsheader und Abfragezeichenfolgen-Parameter von Bildanforderungen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | D= | Alle | D= |

**Syntax und mögliche Werte** {#section_D0669899567F46B6A081C7661362BA81}

```js
s.prop1="D=User-Agent”
```

ODER BENUTZERDEFINIERTES FLAG FÜR DYNAMISCHE VARIABLEN VERWENDEN

```js
s.dynamicVariablePrefix=".."
```

**Beispiele** {#section_DD148560F9E8416EBCF159194FA427AC}

```js
s.prop1="D=User-Agent”
```

ODER BENUTZERDEFINIERTES FLAG FÜR DYNAMISCHE VARIABLEN VERWENDEN

```js
s.dynamicVariablePrefix=".."
```

```js
s.prop1="..User-Agent"
```

**Probleme, Fragen und Tipps** {#section_6889908FBD78488D955F67DDB17617B1}

* Durch den Einsatz dynamischer Variablen lässt sich die Gesamtlänge der URL deutlich reduzieren, indem Werte in andere variablen kopiert werden.
* Dynamische Variablen können auch eingesetzt werden, um Daten aus Headern und Cookies zu erfassen, bei denen ein anderer Weg zur Datenerfassung nicht möglich ist.

## s.charSet {#concept_E65B9A8F75C3482C87D0D455805F89BD}

Die Eigenschaft "charSet", die normalerweise in der JavaScript-Datei festgelegt wird, wird von Analytics verwendet, um eingehende Daten für die Speicherung und Berichterstellung in UTF-8 zu konvertieren.

>[!N] Hinweis: Die Eigenschaft charSet ist beim Senden von Daten an eine Multibyte-Report Suite erforderlich und sollte niemals mit einer Standard-Report Suite verwendet werden. Die Platzierung von charSet in Verbindung mit einer Standard-ISO-Report Suite kann zum Abschneiden von Variablen oder unerwarteten Zeichenkonvertierungen führen.

Der Wert der Eigenschaft charSet sollte mit der Webseitenkodierung im META-Tag oder in der HTTP-Kopfzeile übereinstimmen, auch wenn die Syntax etwas unterschiedlich aussehen kann. Das META-Tag kann zwar einen Alias für die Kodierung verwenden, doch sollte der Wert von charSet den bevorzugten (oder offiziellen) Namen der Kodierung benutzen.

Einige der gängigeren Kodierungen und die zugehörigen bevorzugten Namen und Aliase sind in der folgenden Tabelle aufgeführt.

| Bevorzugter Name | Aliase |
|--- |--- |
| ISO-8859-1 | ISO_8859-1,CP819,latin1 |
| ISO-8859-2 | ISO_8859-2,latin2 |
| ISO-8859-5 | ISO_8859-5,cyrillic |
| Big5 | Big-5 |
| Shift_JIS | SJIS |

Da zahlreiche Kodierungen und Aliase vorhanden sind, wenden Sie sich an Ihren Implementierungsberater oder den Adobe-Kundendienst, um den korrekten Wert für charSet zu bestätigen, wenn er nicht in der oben stehenden Tabelle aufgeführt ist.

If a site has different web encodings on different pages, or a single JavaScript file is used for multiple sites, the charSet property can be set to a default value in the JavaScript file and then reset on specific pages as needed to override the default; for example, `s.charSet="UTF-8"` or `s.charSet="SJIS"`.

Jeder nicht leere Wert des Parameters „charSet“ führt dazu, dass Daten zum Speichern in UTF-8 konvertiert werden. Alle Zeichen im Bereich 128-255 werden in die entsprechende UTF-8-Doublebyte-Sequenz konvertiert und gespeichert. Diese Zeichen werden in einer Standard-Report Suite nicht richtig angezeigt. Daher sollte die Eigenschaft charSet niemals in Verbindung mit einer Standard-Report Suite verwendet werden.

Genauso umgeht ein leerer Wert des Parameters charSet den Datenkonvertierungsprozess, und alle Zeichen im Bereich 128-255 werden als Singlebyte-Sequenz gespeichert. Diese Zeichen werden in einer Multibyte-Report Suite nicht richtig angezeigt, da die Singlebyte-Codes für diese Zeichen kein gültiger UTF-8 sind. Daher sollte der Parameter charSet grundsätzlich in Verbindung mit einer Multibyte-Report Suite verwendet werden. Außerdem sollte in Bezug auf die Webseitenkodierung der richtige Wert verwendet werden.

If the *`charSet`* variable contains an incorrect value, the data in all other variables are translated incorrectly. If JavaScript variables on your pages (e.g. *`pageName`*, [!UICONTROL prop1], or *`channel`*) contain only ASCII characters, *`charSet`* does not need to be defined. Wenn die Variablen auf Ihren Seiten jedoch Nicht-ASCII-Zeichen enthalten, muss die *`charSet`* Variable gefüllt werden.

**Parameter**

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | CE | Keine | "" |

**Syntax und mögliche Werte** {#section_EBC2176067A04D9E814CF78A86DC80FA}

```js
s.charSet="character_set"
```

**Beispiele** {#section_406DE0A2B58441DB8512F5B3BE5D9CB5}

```js
s.charSet="ISO-8859-1"
```

```js
s.charSet="SJIS"
```

## s.currencyCode {#concept_CE216F1610E2499D8178DB9A8EB97C63}

Die Variable bestimmt die Konversionsrate, die auf den Umsatz angewendet werden soll.

Alle Geldbeträge werden in einer Währung Ihrer Wahl gespeichert. Wenn dies die gleiche Währung ist, wie in *`currencyCode`*, or *`currencyCode`* is empty, no conversion is applied.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | cc | Konversion &gt; Einkäufe &gt; Umsatz Alle Konversionsberichte, die Umsätze oder Geldbeträge anzeigen | „USD“ |

Wenn Besucher auf Ihrer Website Einkäufe in verschiedenen Währungen tätigen können, sollten Sie mithilfe der Variablen *`currencyCode`* sicherstellen, dass Umsätze in der entsprechenden Währung gespeichert werden. For example, if the base currency for your report suite is USD, and you sell an item for 40 Euros, you should populate the *`currencyCode`* with "EUR" on the HTML page. Nach Eingang der Daten bei der Datenerfassung werden diese 40 Euro dann unter Verwendung des aktuellen Konversionskurses in USD umgerechnet.

Wenn Sie Verkäufe in mehreren Währungen tätigen, empfiehlt es sich, die Variable *`currencyCode`* auf der HTML-Seite anstatt in der JavaScript-Datei aufzufüllen. Wenn Sie anstelle der von Adobe verwendeten Konversionsraten Ihre eigenen Konversionsraten verwenden möchten, stellen Sie die *`currencyCode`* auf die Basiswährung Ihrer Report Suite ein. Dann rechnen Sie alle Umsätze um, bevor diese nach [!DNL Analytics] gesendet werden.

Wechselkurskonversionen werden sowohl bei Umsatz- als auch bei Währungs-Ereignissen vorgenommen. Das sind Ereignisse, mit denen Werte zu Umsätzen summiert werden, wie Steuern und Versandkosten. Die Umsatz- und Währungs-Ereignisse werden in den Produktzeichenfolgen angegeben. Weitere Informationen zu Produkten finden Sie unter [events](../../../implement/js-implementation/c-variables/page-variables.md#concept_FFD115543D54401B98FE683BD7D5B3FE).

**Syntax und mögliche Werte** {#section_7CD68F08AB4848EE9B0D19DCC3F1BECE}

```js
s.currencyCode="currency_code"
```

**Beispiele** {#section_D55ED45369544C8AAA02B3193752636C}

```js
s.currencyCode="GBP"
```

```js
s.currencyCode="EUR"
```

**Konfigurationseinstellungen** {#section_D05E29F545A04958B1C0A82248BCA1B0}

Adobe [!DNL Customer Care] kann die für Ihre Report Suite standardmäßig eingestellte Währung ändern. Wenn die Basiswährung für eine Report Suite geändert wird, werden die im System vorhandenen Umsätze nicht umgerechnet. Alle neuen Umsatzwerte werden entsprechend umgerechnet.

**Probleme, Fragen und Tipps** {#section_08A80A87B54A4861905953A6FA61FF8F}

* Wenn Sie überraschend hohe Umsätze in Berichten feststellen, stellen Sie sicher, dass die *`currencyCode`* Variable und die Basiswährung der Report Suite korrekt eingestellt sind.
* The *`currencyCode`* variable is not persistent, meaning that the variable must be passed in the same image request as any revenue or other currency-related metrics.
* Währungs-Ereignisse dürfen nicht für Zwecke eingesetzt werden, bei denen es nicht um Währungen geht. Wenn Sie beliebige oder dynamische Werte zählen möchten, die keine Währungen sind, verwenden Sie den Ereignistyp [!UICONTROL numeric].
* Wenn die Variable *`currencyCode`* leer ist, wird keine Konversion vorgenommen.

Weitere Informationen finden Sie unter [Währungscodes](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/currency.html).

## s.cookieDomain {#concept_6164C39CF8BE4737A7EF1DE5A8376C1B}

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set.

Commonly, `s.cookieDomainPeriods` is used to generate `s.cookieDomain` from `window.location.hostnam`e. Instead of using `s.cookieDomainPeriods`, you can explicitly set `s.cookieDomain` to what you want to use in your implementation. Beispielsweise können Sie Cookies bei einem vollständig qualifizierten Seitennamen ablegen, indem Sie Folgendes verwenden:

`s.cookieDomain = window.location.hostname;`

## s.cookieDomainPeriods {#concept_F17A59C7D8F54F5897AD40980B6725EB}

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set by determining the number of periods in the domain of the page URL. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen.

Der Standardwert für *`cookieDomainPeriods`* ist "2". This is the value that is used if *`cookieDomainPeriods`* is omitted. Bei Verwendung der Domäne `www.mysite.com`sollte *`cookieDomainPeriods`* beispielsweise "2"verwendet werden. Zum `www.mysite.co.jp`Beispiel *`cookieDomainPeriods`* sollte "3".

If *`cookieDomainPeriods`* is set to "2" but the domain contains three periods, the JavaScript file attempts to set cookies on the domain suffix.

Wenn Sie beispielsweise *`cookieDomainPeriods`* auf "2"für die Domäne einstellen `www.mysite.co.jp`, werden die `s_cc` und die `s_sq` Cookies für die Domäne erstellt `co.jp`. Da `co.jp` eine ungültige Domäne ist, werden diese Cookies von fast allen Browsern zurückgewiesen. Dadurch gehen Daten zur Zuordnung von Besucherklicks verloren, und im Bericht [!UICONTROL Besucherprofil] &gt; [!UICONTROL Technologie] &gt; [!UICONTROL Cookies] steht dann, dass fast 100 % der Besucher Cookies abgelehnt haben.

Wenn *`cookieDomainPeriods`* auf 3 eingestellt ist, die Domäne jedoch nur zwei Punkte enthält, setzt die JavaScript-Datei Cookies in der Subdomäne der Site. Wenn Sie beispielsweise *`cookieDomainPeriods`* auf "3"in der Domäne einstellen `www2.mysite.com`, werden die `s_cc` und die `s_sq` Cookies in der Domäne erstellt `www2.mysite.com`. When a visitor goes to another subdomain of your site (such as `www4.mysite.com`), all cookies set with `www2.mysite.com` cannot be read.

>[!NOTE]
>
>Do not include additional subdomains as part of *`cookieDomainPeriods`*. Zum Beispiel `store.toys.mysite.com` hätte es immer noch *`cookieDomainPeriods`* auf "2"gesetzt. Bei dieser Variablendefinition werden die Cookies korrekt in der Stammdomäne [!DNL mysite.com] gesetzt. Setting *`cookieDomainPeriods`* to "3" in this example would set cookies on the domain [!DNL toys.mysite.com], which has the same implications as the prior example.

Siehe auch [s.fpCookieDomainPeriods](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_0A25BD152B0744989E7C662A95448274).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | CDP | Betrifft mehrere Berichte und steuert, wie die Besucherkennung gespeichert und verarbeitet wird. | 2 |

>[!NOTE]
>
>Einige Cloud-Computing-Dienste werden als Domänen der obersten Ebene betrachtet, die das Schreiben von Cookies nicht zulassen. (Beispiel: `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com`usw.) Bei einer Implementierung mithilfe dieser Dienste können Sie von der Analytics-Datenschutzeinstellung betroffen sein, die Benutzer entfernt, die alle Cookies blockiert haben, wenn Sie keine eigene Domäne eingerichtet haben (z. B. beim Testen Ihrer Implementierung). In diesem Fall wird jeder Treffer, bei dem das System feststellt, dass Cookies deaktiviert, nicht funktionsfähig oder nicht für den Zugriff verfügbar sind, deaktiviert und somit vom Reporting ausgeschlossen.

**Beispiele** {#section_4218BE29FA5E49F58975A2094329B268}

Manuelles Festlegen der Variablen:

```js
s.cookieDomainPeriods = "3";
```

Verschiedene Beispiele zum dynamischen Festlegen der Variablen, wenn eine JavaScript-Hauptdatei beide Typen hostet:

```js
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```

```js
s.cookieDomainPeriods = "2"; 
var d=window.location.hostname; 
if(d.indexOf(".co.uk") > 0 || d.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

```js
s.cookieDomainPeriods = "2"; 
if(window.location.indexOf(".co.jp") > 0 || window.location.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

**Probleme, Fragen und Tipps** {#section_F3BE3F039E5C4359B694DBB61369822C}

* If you notice that visitor click map data is absent, or that the [!UICONTROL Traffic] &gt; [!UICONTROL Technology] &gt; [!UICONTROL Cookies] report shows a large percentage of visitors who reject cookies, check that the value of *`cookieDomainPeriods`* is correct.

* If *`cookieDomainPeriods`* is higher than the number of sections in the domain, cookies will be set with the full domain. Dies kann zu Datenverlusten führen, wenn Besucher zwischen Subdomänen wechseln.
* Die Variable wurde bei nicht mehr unterstützten Implementierungen verwendet, bevor der Besucher-ID-Cookie festgelegt *`cookieDomainPeriods`* *`trackingServer`* wurde. Obwohl diese Implementierung nur im veralteten Code vorkommt, besteht bei fehlender korrekter Definition *`cookieDomainPeriods`* in diesem Fall die Gefahr eines Datenverlusts.

## s.fpCookieDomainPeriods {#concept_0A25BD152B0744989E7C662A95448274}

Die Variable „“ dient für Cookies, die von JavaScript gesetzt werden (s_sq, s_cc, Plug-ins) und von Erstanbietern stammen, selbst wenn Ihre Implementierung die Domänen 2o7.net oder omtrdc.net von Drittanbietern verwendet.

The *`fpCookieDomainPeriods`* variable should never be dynamically set . Bei Verwendung *`cookieDomainPeriods`* empfiehlt es sich, einen Wert *`fpCookieDomainPeriods`* auch anzugeben. *`fpCookieDomainPeriods`* erbt den *`cookieDomainPeriods`* Wert. Note that *`fpCookieDomainPeriods`* does not affect the domain on which the visitor ID cookie is set, even if your implementation treats this as a first-party cookie.

The name " *`fpCookieDomainPeriods`*" refers to the number of periods (".") in der Domäne, wenn diese mit „www“. beginnt. For example, `www.mysite.com` contains two periods, while `www.mysite.co.jp` contains three periods. Another way to describe the variable is the number of sections in the main domain of the site (two for `mysite.com` and three for `mysite.co.jp`).

Die [!DNL AppMeasurement] für JavaScript-Datei verwendet die *`fpCookieDomainPeriods`* Variable, um die Domäne zu bestimmen, mit der Erstanbieter-Cookies außer dem [!UICONTROL Besucher-ID] -Cookie (s_vi) gesetzt werden. Diese Variable wirkt sich auf mindestens zwei andere Cookies aus, inklusive „s_sq“ und „s_cc“ (mit denen Besucherklicks zugeordnet bzw. Cookies geprüft werden). Außerdem hat es auch Auswirkungen auf Cookies, die von Plug-ins verwendet werden (wie z. B. [!UICONTROL getValOnce]).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | cookieDomainPeriods |

**Codebeispiel für das Festlegen von Cookiedomänenvariablen** {#section_5200A92D40384C82998606E800B69E13}

```js
s.fpCookieDomainPeriods="2" 
var d=window.location.hostname 
if(d.indexOf('.co.uk')>-1||d.indexOf('.com.au')>-1) 
  s.fpCookieDomainPeriods="3" 
```

**Syntax und mögliche Werte** {#section_87923F4C12E74AF99CC9AFC0FFD77D49}

The *`cookieDomainPeriods`* variable is expected to be a string, as shown below.

```js
s.fpCookieDomainPeriods="3"
```

**Beispiele** {#section_EF7355718AD849BF963EE9F6F9F79891}

```js
s.fpCookieDomainPeriods="3"
```

```js
s.fpCookieDomainPeriods="2"
```

**Konfigurationseinstellungen** {#section_DB65D9BC4F3048C8AD08F9A7CD8FCFC0}

Keine

## s.cookieLifetime {#concept_8347C6648B0E4D4996E2F223C34B9A3D}

Die Variable „“ wird sowohl von JavaScript als auch von Datenerfassungsservern verwendet, um die Lebensdauer eines Cookies zu bestimmen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | cl | „Datenverkehr“ &gt; „Technologie“ &gt; „Cookies“ &gt; Alle Berichte, die mit Besuchern in Verbindung stehen | "" |

Wenn *`cookieLifetime`* festgelegt ist, überschreibt sie alle anderen Cookie-Ablauffristen sowohl für JavaScript als auch für Datenerfassungsserver (mit einer Ausnahme, die unten beschrieben wird). The *`cookieLifetime`* variable can have one of three values:

* [!DNL Analytics] Cookies
* Cookies
* JavaScript-Einstellungen und -Plug-ins

**Syntax und mögliche Werte** {#section_09D4D122451B45FAB2C9398600EC66F1}

```js
s.cookieLifetime="value"
```

Die folgenden Werte sind möglich:

* ""
* „NONE“
* „SESSION“
* Eine Ganzzahl, die für die Anzahl der Sekunden bis zum Ablaufen steht

**Beispiele** {#section_91499F70C8B14D3292FCF1B60F04E30A}

```js
s.cookieLifetime="SESSION"
```

```js
s.cookieLifetime="86400" // one day in seconds
```

**Konfigurationseinstellungen** {#section_7BDAD4CFE8414C9BA5717A8C8B1BDD34}

Keine

**Probleme, Fragen und Tipps** {#section_23E24877F6554E0D9F8C8B7A9C2994B2}

*`cookieLifetime`* betrifft die [!DNL Analytics] Verfolgung. If, for example, *`cookieLifetime`* is two days, then monthly, quarterly, and yearly unique visitor reports will be incorrect. Seien Sie daher vorsichtig, wenn Sie in *`cookieLifetime`*.

## s.doPlugins {#concept_676EAE4FAFCF4B018876390FC874EFDA}

Die Variable „“ ist ein Verweis auf die Funktion „“ und soll dafür sorgen, dass die Funktion „“ in der JavaScript-Datei an der richtigen Stelle aufgerufen wird.

The *`s_doPlugins`* function is called each time any of the following occurs:

* Die *`t()`* Funktion
* Die *`tl()`* Funktion
* auf einen Exit- oder Downloadlink geklickt wird.
* auf ein Seitenelement geklickt wird, das mittels Besucherklickzuordnung nachverfolgt wird.

Die Variable *`doPlugins`* dient zum Ausführen angepasster Routinen für die Sammlung oder Änderungen von Daten. If you are using an object name other than "s," make sure that the *`s_doPlugins`* is renamed appropriately. Wenn Ihr Objektname beispielsweise s_mc lautet, sollte die *`s_doPlugins`* Funktion s_mc_doPlugins heißen.

**Syntax und mögliche Werte** {#section_5CFB94598521455E80947964A306EA89}

Die *`s_doPlugins`* Funktion sollte nicht in Anführungszeichen gesetzt werden und *`doPlugins`* immer dem genauen Namen der *`s_doPlugins`* Funktion zugeordnet werden (wenn diese Funktion umbenannt wird).

```js
s.doPlugins=s_doPlugins;
```

**Beispiele** {#section_A5CF0054C56745268A1313CCC7730022}

```js
s.doPlugins=s_doPlugins;
```

```js
s_mc.doPlugins=s_mc_doPlugins;
```

**Konfigurationseinstellungen** {#section_641F0EC55E3349E5A3F8671446797074}

Keine

**Probleme, Fragen und Tipps** {#section_0C7FB61CF0C946EF8A7D1B686D36E6ED}

* Der einzige Grund, den Objektnamen zu ändern (z. B. von „s“ zu „s_mc“), wäre, wenn Sie Inhalt mit anderen Benutzern teilen oder von anderen Benutzern beziehen möchten. Beim Umbenennen der  *`s_doPlugins`* function to [!UICONTROL s_mc_doPlugins] ensures that another client's JavaScript file does not overwrite your *`doPlugins`* function.

* Wenn Sie unerwartet damit beginnen, Inhalte von einem anderen Adobe-Kunden abzurufen, und Ihre *`s_doPlugins`* *`s_doPlugins`* Funktion überschrieben wird, können Sie die Funktion einfach umbenennen, ohne den Objektnamen zu ändern. Wählen Sie einfach einen anderen Objektnamen, als andere JavaScript-Dateien auf der gleichen Seite verwenden würden – das ist zwar nicht erforderlich, stellt jedoch die beste Lösung dar.

## s.registerPreTrackCallback und s.registerPostTrackCallback

Diese Funktionen verwenden als Parameter: den Rückruf (eine Funktion) und die Parameter für diese Funktion. Beispiel:

```
s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
    console.log("pre track callback"); 
    console.dir(requestUrl); // Request URL 
    console.dir(a); // param1 
    console.dir(b); // param2 
    console.dir(c); // param3 
}, "param1", "param2", "param3");
```

Der Rückruf wird über die `requestUrl` und sämtliche Parameter aufgerufen, die weitergegeben werden, wenn der Rückruf registriert wird. Das geschieht entweder vor oder nach dem Tracking-Anruf, abhängig davon, welche Methode bei der Registrierung des Rückrufs verwendet wird.

Die Reihenfolge, in der diese Rückrufe aufgerufen werden, steht nicht fest. Rückrufe, die in der Funktion „Pre“ registriert sind, werden aufgerufen, nachdem die finale Tracking-URL erstellt wurde. Die „Post“-Rückrufe werden auf einen erfolgreichen Tracking-Anruf hin aufgerufen (wenn der Tracking-Anruf fehlschlägt, werden diese Funktionen nicht aufgerufen). Mit `registerPreTrackCallback` registrierte Rückrufe beeinträchtigen den Tracking-Anruf nicht. Außerdem wird das Aufrufen jeglicher Tracking-Methoden in jeglichen registrierten Rückrufen nicht empfohlen, da es zu einer Endlosschleife führen könnte.

## s.trackDownLoadLinks {#concept_0A7AEAB3172A4BEA8B2E8B1A3A8F596C}

Legen Sie „“ auf „true“ fest, wenn Sie Links für herunterladbare Dateien auf Ihrer Site verfolgen möchten.

Wenn "true" *`trackDownloadLinks`* angegeben ist, wird *`linkDownloadFileTypes`* bestimmt, welche Links herunterladbare Dateien sind.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackDownloadLinks`* ist nur dann auf „false“ zu setzen, wenn die Site keine herunterladbaren Dateien enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf herunterladbare Dateien verfolgt wird. If *`trackDownloadLinks`* is 'true,' when a file download link is clicked, data is immediately sent to [!DNL Analytics]. Zu den gesendeten Daten gehören die Download-URL des Links sowie Daten zur Besucherklickzuordnung für diesen Link. Wenn *`trackDownloadLinks`* is 'false,' then visitor click map data for links to downloadable files on your site is likely to be under reported.

**Syntax und mögliche Werte** {#section_828492CC2A144BC68D18C30CF397EEFC}

Die Variable *`trackDownloadLinks`kann entweder „true“ oder „false“ sein.*

**Beispiele** {#section_BE2FA1873EBD4C5CA95E98B922B10280}

```
js
s.trackDownloadLinks=true 
```

```
js
s.trackDownloadLinks=false
```

**Konfigurationseinstellungen** {#section_9A5F69966BAF433A8DA2BCF655A652D1}

Keine

**Probleme, Fragen und Tipps** {#section_B3764520D81143968F96CB69AADD457F}

* When *`trackDownloadLinks`* is 'false,' links that people use to download files on your site are likely to be under reported in visitor click map.
* When *`trackDownloadLinks`* is 'true,' data is sent each time a visitor clicks a file download link.

## s.trackExternalLinks {#concept_E1321318696841648A54CF77F6C4A7AF}

Wenn "true"ist, wird ermittelt, ob ein angeklickter Link ein Exitlink ist.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackExternalLinks`* ist nur dann auf „false“ zu setzen, wenn Ihre Site keine Exitlinks enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf Exitlinks verfolgt wird. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Wenn *`trackExternalLinks`* is 'true,' then when you click an exit link, tracking data is immediately sent. Dazu gehören die URL des Exitlinks, der Linkname und Daten zur Benutzerklickzuordnung für den Link. Wenn *`trackExternalLinks`* is 'false,' then visitor click map data for exit links on your site is likely to be under reported.

**Syntax und mögliche Werte** {#section_267748949A7544658E1D838AAEF964B2}

Die Variable *`trackExternalLinks`kann entweder „true“ oder „false“ sein.*

```
js
s.trackExternalLinks=true|false
```

**Beispiele** {#section_EF18DB05884240F5B5062631E68E10A7}

```
js
s.trackExternalLinks=true 
```

```
js
s.trackExternalLinks=false
```

**Konfigurationseinstellungen** {#section_C8748CFE36324FAFB14C23E3E1FB5082}

Keine

**Probleme, Fragen und Tipps** {#section_FE2C3AF17DA24EA8A944BF1D394FB5BC}

* When *`trackExternalLinks`* is 'false,' links that take people away from your site are likely to be under reported in visitor click map.
* When *`trackExternalLinks`* is 'true,' data is sent each time a visitor clicks on an exit link (before link target loads).

## s.trackInlineStats {#concept_E3A811D9761E4917935F6CD9059C7FCC}

Die Variable bestimmt, ob ClickMap-Daten gesammelt werden.

If *`trackInlineStats`* is 'true,' data about the page and link clicked are stored in a cookie called s_sq. If 'false,' s_sq will have a value of "[[B]]," which is considered null.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | ClickMap | False |

**Syntax und mögliche Werte** {#section_46B2C1DD0D104A01A9C239929420CD90}

```
js
s.trackInlineStats=true|false
```

Die Variable *`trackInlineStats`kann entweder „true“ oder „false“ sein.*

**Beispiele** {#section_F146770917A3493AB8007626913CD6AB}

```js
s.trackInlineStats=true
```

```js
s.trackInlineStats=false
```

**Konfigurationseinstellungen** {#section_FB2CDB07CDCE454786D96A66E4D8EDCD}

Keine

## s.linkDownloadFileTypes {#concept_06CC14C69DFD4887A5E6967A157A9E05}

Die Variable „“ ist eine kommagetrennte Liste mit Dateierweiterungen.

Wenn die Site Links zu Dateien mit diesen Dateierweiterungen enthält, werden die URLs dieser Links im Bericht [!UICONTROL Dateidownloads] angezeigt.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | Keine | Traffic &gt; Sitetraffic &gt; Dateidownloads | "exe, zip, wav, mp3, mov, mpg, avi, wmv, doc, pdf, xls" |

Die Variable ist *`linkDownloadFileTypes`* nur relevant, wenn auf "True"festgelegt *`trackDownloadLinks`* ist.

Im Bericht [!UICONTROL Dateidownloads] werden nur Klicks auf Links gezählt, die mit der linken Maustaste erfolgten. Dateidownloads, die beim Laden einer Seite automatisch gestartet wurden oder die nur nach einer Weiterleitung erfolgten, werden im Bericht [!UICONTROL Dateidownloads] nicht gezählt. Auch Downloads, die über die Kontextmenüoption „Speichern unter“ erfolgen, werden im Bericht [!UICONTROL Dateidownloads] nicht gezählt.

Die Variable *`linkDownloadFileTypes`* kann auch eingesetzt werden, um Klicks zu RSS-Feeds nachzuverfolgen. Wenn Sie Links zu RSS-Feeds mit der Erweiterung .xml oder einer anderen Erweiterung haben, können Sie durch Anhängen von ",xml"an die *`linkDownloadFileTypes`* Liste sehen, wie oft auf jeden RSS-Link geklickt wird.

**Syntax und mögliche Werte** {#section_E0B3F3817BBF4B11AFAABEF8BB951E5A}

Nehmen Sie nur Dateierweiterungen (ohne Leerzeichen) auf.

```js
s.linkDownloadFileTypes="type1[,type2[,type3[...]]]"
```

Jede beliebige Dateierweiterung kann in die Liste eingetragen werden. Achten Sie darauf, keine gängigen Dateierweiterungen (wie HTM oder ASPX) in *`linkDownloadFileTypes`*. Andernfalls wird bei jedem Klick eine weitere Bildanforderung gesendet und als primärer Server-Aufruf gezählt.

**Beispiele** {#section_C53F1AF768434CEBA65F3D255BC470AD}

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls"
```

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls,xml"
```

**Konfigurationseinstellungen** {#section_CE24D5852E4D441A958A4EDDB82382A7}

Keine

**Probleme, Fragen und Tipps** {#section_786CF22D5553429EB6524B13774793BC}

* Nur Klicks mit der linken Maustaste oder Dateidownloads führen dazu, dass die URL im Bericht [!UICONTROL Dateidownloads] aufgeführt wird.
* Wenn eine allgemeine Dateierweiterung in *`linkDownloadFileTypes`* aufgenommen wird, kann sich die Gesamtzahl der Server-Aufrufe erheblich erhöhen, die an Server von Adobe gesendet werden.
* Links zu serverseitigen Umleitungen oder HTML-Seiten, die automatisch mit dem Download einer Datei beginnen, werden nur gezählt, wenn die Dateierweiterung in *`linkDownloadFileTypes`*.
* Links, die JavaScript verwenden (wie z. B. „javascript:openLink“), werden bei Dateidownloads nicht gezählt.

## s.linkInternalFilters {#concept_D53C1186762E4AAE82451712B0801CAD}

Mithilfe der „“-Variablen wird bestimmt, welche Links auf der Site Exitlinks sind.

Die Variable enthält eine kommagetrennte Liste mit Filtern, die die Links darstellen, die zu Ihrer Site gehören.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks |  |

>[!NOTE]
>
>Wir hatten zuvor vorgeschlagen, linkInternalFilters auf javascript zu setzen:. Dies führte jedoch dazu, dass alle Domänen als extern betrachtet wurden, einschließlich der aktuellen Domäne, in der sich das Tag befindet. Wenn mehrere Domänen als intern betrachtet werden sollen, können Sie sie wie in den folgenden Beispielen hinzufügen.

Die Variable *`linkInternalFilters`* wird bestimmt, ob ein Link ein Exitlink ist. Zu Exitlinks gehören alle Links, über die Besucher von Ihrer Site weg geleitet werden. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* den Wert `"true"`. (Informationen zur Verarbeitung von Exitlinks durch DTM finden Sie unter [Linktracking](https://marketing.adobe.com/resources/help/en_US/dtm/link_tracking.html) in der Dokumentation für Dynamic Tag Management.) Bei den Filtern *`linkInternalFilters`* wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Die Liste der Filter in *`linkInternalFilters`* gilt standardmäßig für die Domäne und den Pfad jedes Links. If *`linkLeaveQueryString`* is set to `"true"`, then the filters apply to the entire URL (domain, path, and query string). Die Filter werden immer auf den absoluten Pfad der URL angewendet, auch wenn ein relativer Pfad als href-Wert verwendet wird.

Stellen Sie sicher, dass alle Domänen Ihrer Site (und aller Partnersites, die Ihre JavaScript-Datei verwenden) in *`linkInternalFilters`*. Wenn nicht sämtliche Domänen in der Liste enthalten sind, werden Links auf und zu diesen Domänen als Exitlinks betrachtet, wodurch die Zahl der gesendeten Server-Aufrufe zunimmt. Wenn Sie möchten, dass mehrere Domänen oder Unternehmen eine einzelne [!DNL AppMeasurement] *`linkInternalFilters`* für JavaScript-Dateien verwenden, sollten Sie erwägen, die Seite zu füllen und dabei den in der JavaScript-Datei angegebenen Wert außer Kraft zu setzen. Wenn Vanitydomänen vorhanden sind, die sofort zu Ihrer Hauptdomäne umgeleitet werden, müssen diese nicht in die Liste aufgenommen werden.

Das folgende Beispiel zeigt, wie diese Variable verwendet wird. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="mysite.com" 
s.linkExternalFilters="" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Exit Link</a> 
<a href="https://www2.site1.com/partners/">Exit Link</a> 
```

**Syntax und mögliche Werte** {#section_810966F09912415B96EA9C2EDAE0CEA0}

The *`linkInternalFilters`* variable is a comma-separated list of ASCII characters. Leerzeichen sind nicht erlaubt.

```js
s.linkInternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

**Beispiele** {#section_491F48556DC247889D54C66FC431B4EC}

```js
s.linkInternalFilters="mysite.com"
```

```js
s.linkInternalFilters="mysite.com,mysite.net,vanity1.com"
```

**Konfigurationseinstellungen** {#section_546AC1FACB664ABFBCF312990097C987}

Keine

**Probleme, Fragen und Tipps** {#section_E83A6F8B6EE44D51A2800D83F8BB264F}

* Include all domains that the [!DNL AppMeasurement] for JavaScript file may be served under in the filter list.
* Überprüfen Sie in regelmäßigen Abständen, ob der Bericht [!UICONTROL Pfade] &gt; [!UICONTROL Einstiege und Ausstiege] &gt; [!UICONTROL Exitlinks] nur korrekte Einträge enthält.

* Überprüfen Sie in regelmäßigen Abständen Ihre Partnerverträge auf Einschränkungen bei der Linktracking. So kann es Ihnen zum Beispiel untersagt sein, Links nachzuverfolgen, die in Display-Anzeigen des Partners stehen. Filtern Sie Partnerlinks, indem Sie deren Domäne zu *`linkInternalFilters`*:

```js
s.linkInternalFilters="mysite.com,mysite.net,mypartner.net/adclick"
```

## s.linkLeaveQueryString {#concept_118C280E29394DB5A16DBBF41EB4D742}

Standardmäßig sind Abfragezeichenfolgen in allen Berichten ausgeschlossen. 

Bei einigen Exitlinks und Downloadlinks befindet sich der wichtige Teil der URL möglicherweise in der Abfragezeichenfolge (wie in der folgenden Beispiel-URL):

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

Der Name der Download-Datei kann in der Abfragezeichenfolge festgelegt sein, sodass die Abfragezeichenfolge erforderlich ist, damit der Bericht [!UICONTROL Dateidownloads] genauer ist.

Die Variable *`linkLeaveQueryString`* bestimmt, ob die Abfragezeichenfolge in den Berichten [!UICONTROL Exitlinks] und [!UICONTROL Dateidownload] enthalten sein soll.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | Keine | Dateidownloads für Exitlinks | false |

>[!NOTE]
>
>Setting `linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.

**Syntax** {#section_C40CF036B71A496D92574C6E46DE8302}

```js
s.linkLeaveQueryString=[false/true]
```

**Beispiele** {#section_E42CEC8DDE624A4B979F4F6C8094A7F9}

```js
s.linkLeaveQueryString=false
```

**Mögliche Werte** {#section_E13211451B664B909B1BFDD050472F18}

```js
s.linkLeaveQueryString=false
```

```js
s.linkLeaveQueryString=true
```

**Konfigurationseinstellungen** {#section_835FD74D3CA9425A9D091CACF88A6F1F}

Bei dieser Variablen sind keine Konfigurationen erforderlich.

**Probleme, Fragen und Tipps** {#section_085E79D1A7F74F5D95F82D34FB82AEC4}

* Setting `s.linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.
* The `linkLeaveQueryString` variable does not affect recorded page URLs, visitor click map, or [!UICONTROL Path] reports.

## s.linkTrackVars {#concept_A6B117826C15402EBD0781A94C8065B9}

Die Variable „“ ist eine kommagetrennte Liste von Variablen, die bei benutzerspezifischen, Download- und Ausstiegslinks gesendet werden.

If *`linkTrackVars`* is set to "", all variables that have values are sent with link data. Um zu vermeiden, dass Instanzen oder Seitenansichten, die mit anderen Variablen verbunden sind, zu hoch ansteigen, empfiehlt Adobe, einen Link, der zur Linkverfolgung verwendet wird, mit dem *onClick`linkTrackVars`-Ereignis zu füllen**`linkTrackEvents`und im onClick* -Ereignis einzugehen.

Alle Variablen, die mit Linkdaten gesendet werden sollen (benutzerspezifische, Download- und Ausstiegslinks) sind in *`linkTrackVars`*. Wenn *`linkTrackEvents`* dies verwendet wird, sollte *`linkTrackVars`* "events"enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Alle | „None“ |

Verwenden Sie beim Eintragen von Werten in *`linkTrackVars`*, do not use the 's.' prefix for variables. Anstatt beispielsweise *`linkTrackVars`* "s.prop1"einzugeben, sollten Sie "prop1"eingeben. Das folgende Beispiel zeigt, wie *`linkTrackVars`* es zu verwenden ist.

```js
s.linkTrackVars="eVar1,events" 
s.linkTrackEvents="event1" 
s.events="event1" 
s.eVar1="value A" 
s.eVar2="value B" 
s.t() // eVar1, event1 and event2 are recorded 
<a href="https://google.com">event1 and eVar1 are recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.eVar1='value C';s.events='';s.tl(this,'o')">eVar1 is recorded</a> 
```

Da der Link zu „google.com“ ein Exitlink ist (es sei denn, Sie sind Google), werden mit den Ausstieglinkdaten „event1“ und „eVar1“ gesendet. Dadurch nehmen die Instanzen zu, die mit „eVar1“ verknüpft sind, sowie die Anzahl, wie oft „event1“ ausgelöst wurde. In the link to [!DNL test.php], [!UICONTROL eVar1] is sent with a value of 'value C' because that is the current value of [!UICONTROL eVar1] at the time that *`tl()`* is called.

**Syntax und mögliche Werte** {#section_DCC239F5CFE74959856764DAB1862BA7}

The *`linkTrackVars`* variable is a case-sensitive, comma-separated list of variable names, without the object name prefix. Anstelle von „s.eVar1“ müssen Sie also „eVar1“ verwenden.

```js
s.linkTrackVars="variable_name[,variable_name[...]]"
```

Die Variable darf *`linkTrackVars`* nur Variablen enthalten, die an [!DNL Analytics]Folgendes gesendet werden: *`events`*, *`campaign`*, *`purchaseID`*, *`products`*, [!UICONTROL eVar1-75], [!UICONTROL prop1-75], [!UICONTROL hier1-5]*`channel`**`server`**`state`**`zip`**`pageType`*,,,,,, und.

**Beispiele** {#section_546BAAC7373A41BF8583B280EAAB607C}

```js
s.linkTrackVars="events,prop1,eVar49"
```

```js
s.linkTrackVars="products"
```

**Konfigurationseinstellungen** {#section_E387604B8A434A7F89A82A886649A89D}

Keine

**Probleme, Fragen und Tipps** {#section_99E0783A608C4462945F35D21AB4AC2B}

* If *`linkTrackVars`* is blank, all variables that have values are tracked with all server calls.
* Any variable listed in *`linkTrackVars`* that has a value at the time of any download, exit, or custom link, are tracked.
* Bei Verwendung *`linkTrackEvents`* muss "events" *`linkTrackVars`* enthalten sein.

* Lassen Sie bei Variablen das Präfix „s.“ oder „s_objektname“. weg.

## s.linkTrackEvents {#concept_34D029097A674D0A97690C9569590EF5}

The  variable is a comma-separated list of events that are sent with a [!UICONTROL custom], [!UICONTROL exit], or [!UICONTROL download] link.

If an event is not in *`linkTrackEvents`*, it is not sent to [!DNL Analytics], even if it is populated in the [!UICONTROL onClick] event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

Im ersten Link zu [!DNL help.php] sehen Sie, dass die „events“-Variable den Wert behält, der festgelegt war, bevor auf den Link geklickt wurde. Dadurch kann „event1“ mit dem benutzerspezifischen Link gesendet werden. In the second example, the link to [!DNL test.php], event2 is not recorded because it is not listed in *`linkTrackEvents`*.

Um Verwirrung und potenzielle Probleme zu vermeiden, empfiehlt Adobe, einen Link, der zur Linkverfolgung verwendet wird, auszufüllen *`linkTrackVars`* und *`linkTrackEvents`* im [!UICONTROL onClick] -Ereignis einzutragen.

The *`linkTrackEvents`* variable contains the events that should be sent with [!UICONTROL custom], [!UICONTROL download], and [!UICONTROL exit] links. Diese Variable wird nur berücksichtigt, wenn sie "events" *`linkTrackVars`* enthält.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Konversion | „None“ |

**Syntax und mögliche Werte** {#section_89BA2425FBDC400A8C8B7FCDE7D67D63}

The *`linkTrackEvents`* variable is a comma-separated list of events (no spaces).

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

In *`linkTrackEvents`*. These events are listed in [Events](../../../implement/js-implementation/c-variables/page-variables.md#concept_FFD115543D54401B98FE683BD7D5B3FE). Wenn vor oder nach dem Ereignisnamen ein Leerzeichen steht, kann das Ereignis bei Bildanforderungen des Links nicht gesendet werden.

**Beispiele** {#section_AB7F952E522A4DCC92944EBF74C26BDD}

```js
s.linkTrackEvents="purchase,event1"
```

```js
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

**Konfigurationseinstellungen** {#section_D938A47346D94A0C9E98FB327F2EF349}

Keine

**Probleme, Fragen und Tipps** {#section_DBB68BECC9D44380816113DB2566C38C}

* Die JavaScript-Datei verwendet sie nur, *`linkTrackEvents`* wenn sie die Variable "events" *`linkTrackVars`* enthält. "events"sollte *`linkTrackVars`* nur bei *`linkTrackEvents`* Definition enthalten sein.

* Vorsicht, wenn ein Ereignis auf einer Seite ausgelöst wird, das in *`linkTrackEvents`*. That event is recorded again with any [!UICONTROL exit], [!UICONTROL download], or [!UICONTROL custom] links unless the events variable is reset prior to that event (in the [!UICONTROL onClick] of a link or after the call to the *`t()`* function).

* If *`linkTrackEvents`* contains spaces between event names, the events are not recorded.

## s.linkExternalFilters {#concept_92A59169DCE443EBAE81A373B27BB6DD}

Wenn Ihre Site viele Links zu externen Sites enthält und Sie nicht sämtliche Exitlinks verfolgen möchten, setzen Sie „“ so ein, dass nur eine bestimmte Untermenge der Ausstiegs-Links im Bericht aufgeführt wird.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Pfade &gt; Einstiege und Ausstiege &gt; Exitlinks | "" |

Die Variable Bei *`linkExternalFilters`* einer Variablen handelt es sich um eine optionale Variable, mit der *`linkInternalFilters`* ermittelt wird, ob ein Link ein Exitlink ist. Jeder Link, der einen Besucher weg von Ihrer Site führt, gilt als Exitlink. Ob ein Exitlink in ein Popupfenster oder in das vorhandene Fenster führt, spielt keine Rolle, damit ein Link in Berichten als Exitlink aufgeführt wird. Exitlinks werden nur verfolgt, wenn *`trackExternalLinks`* is set to 'true.' Bei den Filtern in *`linkExternalFilters`* und *`linkInternalFilters`* sind die Groß- und Kleinschreibung nicht zu beachten.

>[!NOTE]
>
>Wenn Sie diese nicht verwenden möchten, löschen Sie sie *`linkExternalFilters`* oder setzen Sie sie auf "".

Die Filter werden standardmäßig in der Liste angezeigt *`linkExternalFilters`* und *`linkInternalFilters`* gelten für die Domäne und den Pfad jedes Links. Wenn "true"festgelegt *`linkLeaveQueryString`* ist, gelten die Filter für die gesamte URL (Domäne, Pfad und Abfragezeichenfolge). Diese Filter werden immer auf den absoluten Pfad der URL angewendet, auch wenn ein relativer Pfad als href-Wert verwendet wird.

Mit *`linkInternalFilters`* haben die meisten Firmen genug Kontrolle über Exitlinks, sodass sie *`linkExternalFilters`*. Using *`linkExternalFilters`* simply decreases the likelihood that an exit link is considered external. If *`linkExternalFilters`* has a value, then a link is considered only external if it does not match *`linkInternalFilters`* and does match *`linkExternalFilters`*.

Das folgende Beispiel zeigt, wie diese Variable verwendet wird. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="javascript:,mysite.com" 
s.linkExternalFilters="site1.com,site2.com,site3.com/partners" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Not an Exit Link</a> 
<a href="https://www.site1.com">Exit Link</a> 
<a href="https://www2.site3.com/partners/offer.asp">Exit Link</a> 
```

**Syntax und mögliche Werte** {#section_E35DAAAE8BDE44CEB8F6763EF1344693}

The *`linkExternalFilters`* variable is a comma-separated list of ASCII characters. Leerzeichen sind nicht erlaubt.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

Jeder beliebige Teil einer URL kann in *`linkExternalFilters`*, separated by commas.

**Beispiele** {#section_1D2F13EEC28942868C2F4207ADF2DDE0}

```js
s.linkExternalFilters="partnersite.com,partnertwo.net/path/"
```

```js
s.linkExternalFilters=""
```

**Konfigurationseinstellungen** {#section_2D0CA911855B4B3698145FC18D5021C3}

Keine

**Probleme, Fragen und Tipps** {#section_8B40E6F539E3473B934A8DB7C5086D73}

* Using *`linkExternalFilters`* can result in fewer links on your site being exit links. Verwenden Sie diese Variable nicht anstelle von, *`linkInternalFilters`* um zu erzwingen, dass interne Links zu Ausstiegslinks werden.

* Wenn Sie auf die Abfragezeichenfolge eines Links angewendet werden *`linkExternalFilters`* sollten, stellen Sie sicher, dass auf "true"festgelegt *`linkLeaveQueryString`* ist. See [linkLeaveQueryString](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_118C280E29394DB5A16DBBF41EB4D742) before setting to `"true"`.

* To disable exit link tracking, set *`trackExternalLinks`* to `"false"`.

## s.usePlugins {#concept_81836470A25C41228CE04084565F667D}

If the  function is available and contains useful code, [!UICONTROL s_usePlugins] should be set to 'true.'

Wenn [!UICONTROL usePlugins] auf "true"gesetzt ist, wird die *`s_doPlugins`* Funktion vor jeder Bildanforderung aufgerufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

**Syntax und mögliche Werte** {#section_BAD0F150047A4B7FB1214491B939A1FC}

```js
s.usePlugins=true|false
```

Die Variable [!UICONTROL usePlugins] kann entweder „true“ oder „false“ sein.

**Beispiele** {#section_1423CC3026384B1A9F78B272166B1DF5}

```js
s.usePlugins=true
```

```js
s.usePlugins=false
```

Die Variable [!UICONTROL usePlugins] sollte nur dann auf "false"gesetzt (oder nicht deklariert) werden, wenn die *`s_doPlugins`* Funktion nicht in Ihrer JavaScript-Datei deklariert ist.

**Konfigurationseinstellungen** {#section_DFD41717134147E988B6AFC7DE5BB9E3}

Keine