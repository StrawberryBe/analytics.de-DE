---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# referrer

Mithilfe der Variablen „“ können verlorene Referrer-Informationen wiederhergestellt werden.


<!-- 

referrer.xml

 -->

Häufig werden serverseitige und JavaScript-Umleitungen eingesetzt, um Besucher an die richtigen Stellen weiterzuleiten. Beim Umleiten eines Browsers geht jedoch die ursprüngliche Verweis-URL verloren.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | R | Datenverkehr &gt; Suchmethoden Konversion &gt; Suchmethoden | document.referrer |

Viele Firmen setzen Umleitungen an zahlreichen Stellen auf ihren Websites ein. So kann zum Beispiel ein Besucher aus einem gebührenpflichtigen Suchergebnis einer Suchmaschine umgeleitet werden. Beim Umleiten eines Browsers geht die verweisende URL häufig verloren. Die Variable *`referrer`* kann verwendet werden, um den ursprünglichen *`referrer`*-Wert auf der ersten Seite nach einer Umleitung wiederherzustellen. *`referrer`* kann Server-seitig oder über JavaScript aus der Abfragezeichenfolge gefüllt werden.

Damit Analytics einen Referrer aufzeichnet, muss dieser korrekt formatiert sein, d. h., er muss im normalen URL-Format mit Angabe eines Protokolls und geeigneten Speicherorts formuliert sein.

**Syntax und mögliche Werte** {#section_A0365D76789C4F4A959E81FE5A9D491D}

```js
s.referrer="URL"
```

Im *`referrer`*. Stellen Sie sicher, dass die Zeichenfolge URL-kodiert ist (keine Leerzeichen).

**Beispiele** {#section_86FB1577670C4AA18BF3718F0832FCD4}

```js
s.referrer="https://www.google.com/search?q=search+string" 
s.referrer=<%=referrerVar%> // populated server-side  
if(s.getQueryParam('ref') 
s.referrer=s.getQueryParam('ref') 
```

**Konfigurationseinstellungen** {#section_7AAEF28A7CBC446984F32C0659EFBF8D}

Keine

**Probleme, Fragen und Tipps** {#section_B42BF7FBA1094FF9805707FEA810CFE1}

*`referrer`* muss wie eine normale URL aussehen und eine Angabe zum Protokoll enthalten.
