---
description: Beim Einsetzen von Werten in eine Variable sind einige Best Practices zu beachten.
keywords: Analytics-Implementierung
seo-description: Beim Einsetzen von Werten in eine Variable sind einige Best Practices zu beachten.
seo-title: Verwenden von Anführungszeichen
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Verwenden von Anführungszeichen
topic: Entwickler und Implementierung
uuid: 9 f 09 c 48 b -7 ae 5-441 e -8635-fd 6 bdc 2 e 94 c 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verwenden von Anführungszeichen

Beim Einsetzen von Werten in eine Variable sind einige Best Practices zu beachten.

Sie können einfache oder doppelte Anführungszeichen einsetzen. Achten Sie aber darauf, dann immer die gleiche Schreibweise zu verwenden. Wenn Sie einfache Anführungszeichen verwenden, verwenden Sie immer einfache Anführungszeichen. Wenn Sie doppelte Anführungszeichen verwenden, verwenden Sie immer doppelte Anführungszeichen. Beide folgenden Beispiele sind korrekt:

```js
s.prop2='test' (single quotes)
```

```js
s.prop2="test" (double quotes)
```

Achten Sie darauf, dass typografische Anführungszeichen deaktiviert sind. Wenn Sie einfache Anführungszeichen verwenden und im Wert der Variablen ein Apostroph steht, interpretiert JavaScript dieses als ein einfaches Anführungszeichen. JavaScript wird demnach damit das Ende einer Zeichenfolge signalisiert. Siehe folgendes Beispiel:

```js
s.pageName='John's Home Page'
```

In diesem Beispiel würde JavaScript den Apostroph in „John's“ (der auch ein einfaches Anführungszeichen ist) für das Ende der Zeichenfolge halten. Da der Rest der Zeichenfolge („'s Home Page“) für JavaScript unverständlich ist, würde dies zu einem Fehler führen, der die Bildanforderung verhindern würde. Beide der folgenden Beispiele würden funktionieren:

```js
s.pageName='John\'s Home Page'
```

```js
s.pageName="John's Home Page"
```

Im ersten Beispiel ist dem Apostroph ein umgekehrter Schrägstrich (\) vorangestellt (ein sogenanntes Escape-Zeichen). Daran erkennt JavaScript, dass der Apostroph nicht das Ende der Zeichenfolge angibt, sondern zu der Zeichenfolge gehört. Die Zeichenfolge selbst endet wie gewohnt bei dem einfachen Anführungszeichen. Im zweiten Beispiel ist die gesamte Zeichenfolge in doppelte Anführungszeichen gesetzt. In solchen Fällen kann ein einfaches Anführungszeichen nicht das Ende der Zeichenfolge bedeuten. Das gleiche gilt, wenn ein doppeltes Anführungszeichen Bestandteil der Zeichenfolge ist. So wäre zum Beispiel s.pageName="Team Says "We Win!"" falsch, da doppelte Anführungszeichen sowohl innerhalb der Zeichenfolge stehen als auch deren Anfang und Ende angeben sollen. Dies wäre nur bei s.pageName="Team Says \"We Win!\"" korrekt.
