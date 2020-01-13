---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.usePlugins

Wenn die Funktion verfügbar ist und brauchbaren Code enthält, muss [!UICONTROL s_usePlugins] auf „True“ gesetzt werden.

Wenn [!UICONTROL usePlugins] auf „true“ gesetzt ist, wird die Funktion *`s_doPlugins`* vor jeder Bildanforderung aufgerufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | True |

## Syntax und mögliche Werte

```js
s.usePlugins=true|false
```

Die Variable [!UICONTROL usePlugins] kann entweder „true“ oder „false“ sein.

## Beispiele

```js
s.usePlugins=true
```

```js
s.usePlugins=false
```

Die Variable [!UICONTROL usePlugins] sollte nur dann auf „false“ gesetzt (oder nicht deklariert) werden, wenn die Funktion *`s_doPlugins`* nicht in Ihrer JavaScript-Datei deklariert ist.

## Konfigurationseinstellungen

Keine
