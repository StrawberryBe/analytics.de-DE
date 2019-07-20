---
description: Stellt fest, ob ein neuer Besuch beginnt.
keywords: Analytics-Implementierung
seo-description: Stellt fest, ob ein neuer Besuch beginnt.
seo-title: getVisitStart
solution: Analytics
title: getVisitStart
topic: Entwickler und Implementierung
uuid: 7 dd 3 e 51 f -2 f 73-4452-a 9 fb-cac 513 cd 28 eb
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getVisitStart

Stellt fest, ob ein neuer Besuch beginnt.

**Konfigurationsvariablen**

–

**Parameter**

c = (Zeichenfolgen-)Cookie-Name für die Verfolgung.

**Rückgabe**

(Ganzzahl) 1 auf der ersten besuchten Seite, sonst 0

**Beispielaufrufe**

```
s.eVar50 = s.getVisitStart("s_visit");
```

