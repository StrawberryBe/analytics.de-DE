---
description: Unter Verwendung von „adobe.com“ zu Beispielzwecken beziehen sich die hier beschriebenen Implementierungen auf das gleiche „visid“-Cookie.
keywords: Analytics Implementation
solution: Analytics
title: Implementierungsbeispiel
topic: Developer and implementation
uuid: 17d8d2b2-2303-495a-b0f9-d8d3c05f3893
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Implementierungsbeispiel

Unter Verwendung von „adobe.com“ zu Beispielzwecken beziehen sich die hier beschriebenen Implementierungen auf das gleiche „visid“-Cookie.

**Javascript:**

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

**Javascript:**

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

