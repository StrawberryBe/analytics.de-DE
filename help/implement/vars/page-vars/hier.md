---
title: hier
description: Implementieren Sie Hierarchievariablen in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# hier

Hierarchievariablen sind benutzerdefinierte Variablen, mit denen Sie die Struktur einer Site sehen können.

> [!TIP] Diese Variable wurde in früheren Versionen von Adobe Analytics häufiger verwendet. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Classifications.

Diese Variable ist nützlich für Sites mit mehr als drei Ebenen in ihrer Site-Struktur. Eine Medien-Site kann beispielsweise vier Ebenen zum Abschnitt &quot;Sport&quot;haben: `Sports`, `Local Sports`, `Baseball`und `Team name`. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ widergegeben.

Adobe unterstützt bis zu 5 Hierarchievariablen in Ihrer Implementierung. Wenn die Hierarchie aktiviert ist, entscheiden Sie über ein Trennzeichen für die Variable und die maximale Anzahl von Ebenen für die Hierarchie. Wenn das Trennzeichen beispielsweise ein Komma ist, würde die Hierarchie wie folgt aussehen:

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn beispielsweise einer Ihrer Abschnitte aufgerufen wird, wählen Sie `Coach Griffin, Jim`ein anderes Trennzeichen als ein Komma. Die maximale Variablenanzahl beträgt insgesamt 255 Byte. Trennzeichen können aus mehreren Zeichen bestehen, z. B. `||` oder `/|\`, die in Variablenwerten mit geringerer Wahrscheinlichkeit auftreten.

## Beispiele

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
