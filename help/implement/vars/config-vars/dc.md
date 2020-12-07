---
title: dc
description: Eine eingestellte Variable, mit der Sie bestimmen können, welches Rechenzentrum verwendet werden soll.
translation-type: tm+mt
source-git-commit: dfe2b09b2ee287219d18099c51b6fbd7c86bab21
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 100%

---


# dc

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie stattdessen [`trackingServer`](trackingserver.md).

In früheren Versionen von Adobe Analytics mussten Sie bei Adobe angeben, an welches Rechenzentrum Sie Daten senden möchten. Das Senden von Treffern an das falsche Rechenzentrum führte zu Datenverlust.

Adobe hat diese Erfahrung verbessert, indem es jeder Implementierung erlaubt, Treffer an `sc.adobedc.net` zu senden. Die Angabe des Rechenzentrums ist nicht mehr erforderlich.
