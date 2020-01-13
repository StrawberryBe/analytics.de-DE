---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.charSet

Anhand der Eigenschaft „charSet“, die normalerweise in der JavaScript-Datei platziert wird, konvertiert Analytics eingehende Daten für die Speicherung und Berichterstellung in UTF-8.

>[!NHinweis:] Die Eigenschaft charSet ist beim Senden von Daten an eine Multibyte-Report Suite erforderlich und sollte niemals mit einer Standard-Report Suite verwendet werden. Die Platzierung von charSet in Verbindung mit einer Standard-ISO-Report Suite kann zum Abschneiden von Variablen oder unerwarteten Zeichenkonvertierungen führen.

Der Wert der Eigenschaft charSet sollte mit der Webseitenkodierung im META-Tag oder in der HTTP-Kopfzeile übereinstimmen, auch wenn die Syntax etwas unterschiedlich aussehen kann. Das META-Tag kann zwar einen Alias für die Kodierung verwenden, doch sollte der Wert von charSet den bevorzugten (oder offiziellen) Namen der Kodierung benutzen.

Einige der gängigeren Kodierungen und die zugehörigen bevorzugten Namen und Aliase sind in der folgenden Tabelle aufgeführt.

| Bevorzugter Name | Aliase |
|--- |--- |
| ISO-8859-1 | ISO_8859-1,CP819,latin1 |
| ISO-8859-2 | ISO_8859-2,latin2 |
| ISO-8859-5 | ISO_8859-5,cyrillic |
| Big5 | Big-5 |
| Shift_JIS | SJIS |

Da es zahlreiche Codierungen und Aliase gibt, lassen Sie sich den geeigneten Wert für „charSet“ von Ihrem Implementierungsberater oder von der Adobe-Kundenunterstützung bestätigen, sofern er nicht in der oben stehenden Tabelle aufgeführt ist.

Falls die Seiten einer Site verschiedene Webcodierungen aufweisen oder dieselbe JavaScript-Datei für mehrere Sites verwendet wird, kann die Eigenschaft „charSet“ in der JavaScript-Datei je nach Bedarf auf einen Standardwert gesetzt und dann auf bestimmten Seiten zurückgesetzt werden, um den Standard zu überschreiben. Beispiel: `s.charSet="UTF-8"` oder `s.charSet="SJIS"`.

Jeder nicht leere Wert des Parameters „charSet“ führt dazu, dass Daten zum Speichern in UTF-8 konvertiert werden. Alle Zeichen im Bereich 128-255 werden in die entsprechende UTF-8-Doublebyte-Sequenz konvertiert und gespeichert. Diese Zeichen werden in einer Standard-Report Suite nicht richtig angezeigt. Daher sollte die Eigenschaft charSet niemals in Verbindung mit einer Standard-Report Suite verwendet werden.

Genauso umgeht ein leerer Wert des Parameters charSet den Datenkonvertierungsprozess, und alle Zeichen im Bereich 128-255 werden als Singlebyte-Sequenz gespeichert. Diese Zeichen werden in einer Multibyte-Report Suite nicht richtig angezeigt, da die Singlebyte-Codes für diese Zeichen kein gültiger UTF-8 sind. Daher sollte der Parameter charSet grundsätzlich in Verbindung mit einer Multibyte-Report Suite verwendet werden. Außerdem sollte in Bezug auf die Webseitenkodierung der richtige Wert verwendet werden.

Wenn die Variable *`charSet`* einen fehlerhaften Wert enthält, werden die Daten in allen anderen Variablen falsch umgewandelt. Wenn JavaScript-Variablen auf Ihren Seiten (z. B. *`pageName`*, [!UICONTROL prop1] oder *`channel`*) nur ASCII-Zeichen enthalten, muss *`charSet`* nicht definiert werden. Wenn die Variablen auf Ihren Seiten jedoch Nicht-ASCII-Zeichen enthalten, muss die Variable *`charSet`* gefüllt werden.

## Parameter

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| nicht angegeben | CE | nicht angegeben | "" |

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
