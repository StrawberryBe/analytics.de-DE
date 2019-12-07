---
description: Schreibt einen Wert in ein Cookie.
keywords: Analytics Implementation
subtopic: JavaScript AppMeasurement
title: Util.cookieWrite
topic: Developer and implementation
uuid: 8d526e4c-6d7a-4119-9434-d7ce4fbb7577
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Util.cookieWrite

Schreibt einen Wert in ein Cookie.

**Syntax:**

```
s.Util.cookieWrite(key, value [,expire])
```

**Parameter:**

| Parameter | Beschreibung |
|---|---|
| key | (erforderlich) Der Schlüssel zum Schreiben von Werten in Cookies. |
| value | (optional) Der Wert, der in Cookies geschrieben werden soll. |
| expire | (optional) Ein Date-Objekt mit dem Ablaufdatum für das Cookie. In der Standardeinstellung wird ein Sitzungscookie verwendet. |

**Rückgabe:**

**Beispiel:**

```js
//set a cookie with an expiration 6 months from now 
var date = new Date(); 
date.setMonth(date.getMonth() + 6); 
var success = s.Util.cookieWrite("my_cookie", "my_value", date);
```

