---
description: Stellt fest, ob ein neuer Besuch beginnt.
keywords: Analytics Implementation
title: getVisitStart
topic: Developer and implementation
uuid: 7dd3e51f-2f73-4452-a9fb-cac513cd28eb
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getVisitStart

Stellt fest, ob ein neuer Besuch beginnt.

**Konfigurationsvariablen**

Keine

**Parameter**

c = (Zeichenfolgen-)Cookie-Name für die Verfolgung.

**Rückgabe**

(Ganzzahl) 1 auf der ersten besuchten Seite, sonst 0

**Beispielaufrufe**

```
s.eVar50 = s.getVisitStart("s_visit");
```

