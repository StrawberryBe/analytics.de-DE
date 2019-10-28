---
description: Stellt fest, ob ein neuer Besuch beginnt.
keywords: Analytics-Implementierung
seo-description: Stellt fest, ob ein neuer Besuch beginnt.
seo-title: getVisitStart
solution: Analytics
title: getVisitStart
topic: Entwickler und Implementierung
uuid: 7dd3e51f-2f73-4452-a9fb-cac513cd28eb
translation-type: ht
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

