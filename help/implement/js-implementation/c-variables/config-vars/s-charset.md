---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.charSet

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

If the *`charSet`* variable contains an incorrect value, the data in all other variables are translated incorrectly. If JavaScript variables on your pages (e.g. *`pageName`*, [!UICONTROL prop1], or *`channel`*) contain only ASCII characters, *`charSet`* does not need to be defined. However, if the variables on your pages contain non-ASCII characters, the  variable must be populated.*`charSet`*

## Parameter

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | CE | Keine | "" |

## Syntax und mögliche Werte

```js
s.charSet="character_set"
```

## Beispiele

```js
s.charSet="ISO-8859-1"
```

```js
s.charSet="SJIS"
```
