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


# visitorID

Besucher können anhand der Variablen „“ oder mittels IP-Adresse/Benutzeragent identifiziert werden.


<!-- 

visitorID.xml

 -->

*`visitorID`* kann bis zu 100 alphanumerische Zeichen lang sein und darf keine Bindestriche enthalten.

Wenn Sie ausdrücklich eine benutzerdefinierte ID einstellen, wird diese immer vor anderen ID-Methoden verwendet.

Die Reihenfolge der Verwendung lautet: s.visitorID &gt; s_vi &gt; s_fid &gt; IP/UA.

| ** Maximale Größe** | ** Debug-Parameter** | ** Ausgefüllte Berichte** | ** Standardwert** |
|---|---|---|---|
| 100 Byte | vid | Keine | "" |

**Syntax und mögliche Werte** {#section_5F768C7AE6824557997E92B295C09280}

```js
s.visitorID="visitor_id"
```

> [!NOTE] Die Variable *`visitorID`* darf keinen Bindestrich enthalten.

**Beispiele** {#section_F7F07FEFAC3644A5A084D166ACE1315E}

```js
s.visitorID="abc123"
```

**Konfigurationseinstellungen** {#section_582B376FE55C4BCA8F978E0F62B5DB54}

Keine
