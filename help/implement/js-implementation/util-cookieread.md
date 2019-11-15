---
description: Ruft den Wert aus einem Cookie ab.
keywords: Analytics Implementation
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.cookieRead
topic: Developer and implementation
uuid: 825a75c6-b804-4bfe-b23a-907113b8bfa6
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Util.cookieRead

Ruft den Wert aus einem Cookie ab.

**Syntax:**

```
s.Util.cookieRead(key)
```

**Parameter:**

| Parameter | Beschreibung |
|---|---|
| key | (erforderlich) Der Schlüssel zum Schreiben von Werten in Cookies. |

**Rückgabe:**

Der Wert des Cookies oder eine leere Zeichenfolge, wenn das Cookie nicht gefunden wurde.

**Beispiel:**

```js
var myCookie = s.Util.cookieRead("my_cookie");
```

