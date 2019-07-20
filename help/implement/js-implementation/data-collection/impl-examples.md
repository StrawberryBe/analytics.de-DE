---
description: Unter Verwendung von „adobe.com“ zu Beispielzwecken beziehen sich die hier beschriebenen Implementierungen auf das gleiche „visid“-Cookie.
keywords: Analytics-Implementierung
seo-description: Unter Verwendung von „adobe.com“ zu Beispielzwecken beziehen sich die hier beschriebenen Implementierungen auf das gleiche „visid“-Cookie.
seo-title: Implementierungsbeispiel
solution: Analytics
title: Implementierungsbeispiel
topic: Entwickler und Implementierung
uuid: 17 d 8 d 2 b 2-2303-495 a-b 0 f 9-d 8 d 3 c 05 f 3893
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Implementierungsbeispiel

Unter Verwendung von „adobe.com“ zu Beispielzwecken beziehen sich die hier beschriebenen Implementierungen auf das gleiche „visid“-Cookie.

**JavaScript:**

```js
var s_account="omniturecom" 
s.visitorNamespace="omniture" 
s.trackingServer="omniture.112.2o7.net"
```

**Fest programmierte Bildanforderung:**

```
<img border="0" alt="" src="https://omniture.112.2o7.net/b/ss/omniturecom/5?ns=omniture" width="1" height="1" /> 
```

**AppMeasurement:**

```js
s.account="omniturecom"; 
s.visitorNamespace="omniture"; 
s.trackingServer="omniture.112.2o7.net";
```

Und, wenn Erstanbieter-Cookies eingesetzt werden:

**JavaScript:**

```js
var s_account="omniturecom" 
s.visitorNamespace"omniture" 
s.trackingServer="metrics.omniture.com"
```

**Fest programmierte Bildanforderung:**

```
<img border="0" alt="" src="https://metrics.omniture.com/b/ss/omniturecom/5" width="1" height="1" />
```

**AppMeasurement:**

```js
s.account="omniturecom"; 
s.visitorNamespace="omniture"; 
s.trackingServer="metrics.omniture.com";
```

