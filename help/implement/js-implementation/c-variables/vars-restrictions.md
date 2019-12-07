---
description: Zeichen und Zeichenfolgen, die in JavaScript-Variablen nicht erlaubt sind
keywords: Analytics Implementation
subtopic: Variables
title: Unzulässige JavaScript-Zeichen
topic: Developer and implementation
uuid: 04e3b4b4-7ff5-4673-8060-34302b6ee545
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Unzulässige JavaScript-Zeichen

Zeichen und Zeichenfolgen, die in JavaScript-Variablen nicht erlaubt sind

* Tabulator (0x09)
* Wagenrücklauf (0x0D)
* Zeilenvorschub (0x0A)
* ASCII-Zeichen mit einem Wert größer 127 (es sei denn, dass Multi-Byte-Zeichen aktiviert sind und *`charSet`* entsprechend aufgefüllt werden)
* HTML-Tags (z. B. <b></b> oder &amp;#153)

Bei vielen Variablen (vor allem „products, „hierarchy“ und „events“) gibt es noch weitere Einschränkungen oder Syntaxanforderungen. Angaben zu den jeweiligen Einschränkungen und Syntaxanforderungen der einzelnen Variablen finden Sie im entsprechenden Abschnitt zu den Parametern der Variablen *`s_account`*.
