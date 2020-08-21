---
title: dynamicAccountSelection
description: Die Variable „dynamicAccountSelection“ aktiviert oder deaktiviert die dynamische Kontoauswahl.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '85'
ht-degree: 100%

---


# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder in Adobe Experience Platform Launch nicht unterstützt.

Die `dynamicAccountSelection`-Variable ist ein boolescher Wert, der bestimmt, ob eine dynamische Kontoauswahl verwendet wird.

Wenn diese Einstellung auf `true` festgelegt ist, betrachtet die JavaScript-Datei `dynamicAccountMatch` und `dynamicAccountList`.

Wenn diese Variable auf `false` festgelegt oder nicht definiert ist, werden die Variablen `dynamicAccountMatch` und `dynamicAccountList` ignoriert.

Wenn diese Variable nicht definiert ist, lautet der Standardwert `false`.

## Syntax

```js
s.dynamicAccountSelection = [boolean];
```

## Beispiel

```js
s.dynamicAccountSelection = true;
```
