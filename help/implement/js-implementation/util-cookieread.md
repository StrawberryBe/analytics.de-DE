---
description: Ruft den Wert aus einem Cookie ab.
keywords: Analytics-Implementierung
seo-description: Ruft den Wert aus einem Cookie ab.
seo-title: Util.cookieRead
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.cookieRead
topic: Entwickler und Implementierung
uuid: 825 a 75 c 6-b 804-4 bfe-b 23 a -907113 b 8 bfa 6
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

