---
description: Zeichen und Zeichenfolgen, die in JavaScript-Variablen nicht erlaubt sind
keywords: Analytics-Implementierung
seo-description: Zeichen und Zeichenfolgen, die in JavaScript-Variablen nicht erlaubt sind
seo-title: Unzulässige javascript-Zeichen
solution: Analytics
subtopic: Variablen
title: Unzulässige javascript-Zeichen
topic: Entwickler und Implementierung
uuid: 04 e 3 b 4 b 4-7 ff 5-4673-8060-34302 b 6 ee 545
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Unzulässige javascript-Zeichen

Zeichen und Zeichenfolgen, die in JavaScript-Variablen nicht erlaubt sind

* Tabulator (0x09)
* Wagenrücklauf (0x0D)
* Zeilenvorschub (0x0A)
* ASCII-Zeichen mit einem Wert größer 127 (es sei denn, dass Multi-Byte-Zeichen aktiviert sind und *`charSet`* entsprechend aufgefüllt werden)
* HTML tags (e.g. <b></b> or &amp;#153)

Bei vielen Variablen (vor allem „products, „hierarchy“ und „events“) gibt es noch weitere Einschränkungen oder Syntaxanforderungen. Angaben zu den jeweiligen Einschränkungen und Syntaxanforderungen der einzelnen Variablen finden Sie im entsprechenden Abschnitt zu den Parametern der Variablen *`s_account`*.
