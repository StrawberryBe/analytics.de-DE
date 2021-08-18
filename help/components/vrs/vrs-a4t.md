---
description: 'Besondere Hinweise bei der Verwendung von A4T- und Adobe Analytics-Virtual Report Suites '
title: Virtual Report Suites und Analytics for Target (A4T)
source-git-commit: 6a47ebc58cb36079940cfc4e5cdc80cf99c18a50
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Virtual Report Suites und Analytics for Target (A4T)

Beachten Sie diese Einschränkungen bei der Verwendung von Virtual Report Suites im Kontext von Adobe Target:

* Sie können keine Daten direkt aus Target an eine Virtual Report Suite senden, sondern nur an eine echte Report Suite.
* Sie können in einer Virtual Report Suite Berichte zu A4T-Aktivitäten erstellen. Die A4T-Daten sind jedoch auf die Zeilen beschränkt, die mit dem Virtual Report Suite-Segment (und allen anderen angewendeten Segmenten) übereinstimmen. Wenn Sie beispielsweise eine Virtual Report Suite für Ihre EMEA-Kunden erstellt haben, spiegeln die A4T-Daten in dieser Virtual Report Suite nur die Target-Daten für Ihre EMEA-Kunden wider.
* Sie können keine Segmente aus einer Virtual Report Suite zur Aktivierung wieder in Target veröffentlichen.