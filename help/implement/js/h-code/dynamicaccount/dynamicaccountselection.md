---
title: dynamicAccountSelection
description: Die Variable "dynamicAccountSelection"aktiviert oder deaktiviert die dynamische Kontoauswahl.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# dynamicAccountSelection

> [!IMPORTANT] Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder beim Starten der Adobe Experience Platform nicht unterstützt.

Die `dynamicAccountSelection` Variable ist ein boolescher Wert, der bestimmt, ob eine dynamische Kontoauswahl verwendet wird.

Wenn diese Einstellung auf `true`festgelegt ist, wird die JavaScript-Datei angezeigt `dynamicAccountMatch` und `dynamicAccountList`.

Wenn diese Variable auf `false`festgelegt ist oder nicht definiert ist, werden die Variablen `dynamicAccountMatch` und `dynamicAccountList` ignoriert.

Wenn diese Variable nicht definiert ist, lautet der Standardwert `false`.

## Syntax

```js
s.dynamicAccountSelection = [boolean];
```

## Beispiel

```js
s.dynamicAccountSelection = true;
```
