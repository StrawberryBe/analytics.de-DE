---
description: Besondere Hinweise bei der Verwendung von Virtual Report Suites in A4T und Adobe Analytics
title: Virtual Report Suites und Analytics for Target (A4T)
feature: VRS
exl-id: b81e5100-f512-4219-a8ab-5d7f6219d206
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 100%

---

# Virtual Report Suites und Analytics for Target (A4T)

Beachten Sie diese Einschränkungen bei der Verwendung von Virtual Report Suites im Kontext von Adobe Target:

* Sie können direkt aus Target keine Daten an eine Virtual Report Suite senden, sondern nur an eine echte Report Suite.
* Sie können in einer Virtual Report Suite Berichte zu A4T-Aktivitäten erstellen. Die A4T-Daten sind jedoch auf die Zeilen beschränkt, die mit dem Virtual Report Suite-Segment (und allen anderen angewendeten Segmenten) übereinstimmen. Wenn Sie beispielsweise eine Virtual Report Suite für Ihre EMEA-Kunden erstellt haben, spiegeln die A4T-Daten in dieser Virtual Report Suite nur die Target-Daten für Ihre EMEA-Kunden wider.
* Sie können keine Segmente aus einer Virtual Report Suite wieder in Target zur Aktivierung veröffentlichen.
