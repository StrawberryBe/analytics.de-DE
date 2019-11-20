---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: d5804b411c28270ef910eec5a815532c067a4642

---


# media.trackVars

Die variable „“ gibt an, welche Variablen bei einem Medientreffer gesendet werden sollen.

<!-- 

media_trackVars.xml

 -->

Dies gilt nur bei JavaScript und [!UICONTROL ActionSource].

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | s.Media.trackVars="None" |

**Syntax und mögliche Werte** {#section_7374684A7EB34AE685E8C40A66CFD289}

Variablennamen wie [!UICONTROL propN], *`eVarN`*, *`events`*, *`channel`* usw.

**Beispiele** {#section_48653222ABA14AB0A3C4471659971FAA}

```js
s.Media.trackVars="prop2,events,eVar3"
```

**Probleme, Fragen und Tipps** {#section_615AE1B696124B00B78F651B03813EAB}

* Selbst wenn „eVar3“ in [!UICONTROL trackVars] angegeben ist, wird es mit dem Medientreffer gesendet.

## mobile {#concept_0CEE045F57B444138C0EAA015FC7EA70}

Die Variable „“ steuert, in welcher Reihenfolge Cookies und Abonnenten-IDs zum Identifizieren von Besuchern eingesetzt werden.

<!-- 

mobile.xml

 -->

Siehe [Mobilfunkprotokolle](/help/implement/js-implementation/c-additional-libraries/network-protocols.md).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | /5/ oder /1/ im Pfad der Bild-URL | Keine | Keine |

**Syntax und mögliche Werte** {#section_7F1C58090C454882BA9D3D66C9263A76}

```js
s.mobile="any_string" //subscriber id used first, produces /5/ in path of image url 
s.mobile=""  // if set to an empty string or not set at all, cookies used first, produces /1/ in path of image url 
```

**Probleme, Fragen und Tipps** {#section_06CD5CB4EF1E4B9FBE3B9D1F18AAFA30}

Verwenden Sie besucherübergreifende Identifikation, um mögliche Spitzen im Besucher-Traffic bei der Verwendung der Variable *`s.mobile`* mit der JavaScript-Cookie-Implementierung zu vermeiden.
