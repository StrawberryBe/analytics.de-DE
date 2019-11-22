---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# propN

Mithilfe von (`prop`)-Eigenschaftsvariablen werden benutzerdefinierte Berichte im Traffic-Modul erstellt.


<!-- 

propN.xml

 -->

Eigenschaftsvariablen können als Zähler verwendet werden (um zu zählen, wie oft eine Seitenansicht gesendet wird), in Pfadsetzungsberichten oder in Korrelationsberichten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | c1 - c75 | Benutzerspezifischer Traffic | "" |

**Syntax und mögliche Werte**

```js
s.propN="value"
```

Für [!UICONTROL Eigenschafts]variablen gelten die gleichen Einschränkungen wie für alle normalen Variablen.

**Beispiele**

```js
s.prop2="editorial" 
```

```js
s.prop15="toy category"
```

**Konfigurationseinstellungen**

Contact Adobe Customer Care about showing Visit, Visitor, and Path metrics for `prop` variables.
