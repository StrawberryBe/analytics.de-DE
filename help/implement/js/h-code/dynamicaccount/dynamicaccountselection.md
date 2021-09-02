---
title: dynamicAccountSelection
description: Die Variable „dynamicAccountSelection“ aktiviert oder deaktiviert die dynamische Kontoauswahl.
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: ht
source-wordcount: '85'
ht-degree: 100%

---

# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder der Datenerfassungs-Benutzeroberfläche nicht unterstützt.

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
