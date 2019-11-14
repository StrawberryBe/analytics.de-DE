---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# propN

Mithilfe von Eigenschaftsvariablen ([!UICONTROL props]) werden benutzerdefinierte Berichte im [!UICONTROL Datenverkehrmodul] erstellt.

<!-- 

propN.xml

 -->

Eigenschaftsvariablen können als Zähler verwendet werden (um zu zählen, wie oft eine Seitenansicht gesendet wird), in Pfadsetzungsberichten oder in Korrelationsberichten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | c1 - c75 | Benutzerspezifischer Traffic | "" |

**Syntax und mögliche Werte** {#section_4D3013AF2979426B9589CA2BB9D254CD}

```js
s.propN="value"
```

Für [!UICONTROL Eigenschafts]variablen gelten die gleichen Einschränkungen wie für alle normalen Variablen.

**Beispiele** {#section_FFBB916DA9F44B668D5FAB7C511F6182}

```js
s.prop2="editorial" 
```

```js
s.prop15="toy category"
```

**Konfigurationseinstellungen** {#section_25FDEB6ECA8242A2A44EE540C083078A}

Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Fragen zu [!UICONTROL Besuchs]-, [!UICONTROL Besucher]- und [!UICONTROL Pfad]metriken bei [!UICONTROL Eigenschaft]svariablen haben.
