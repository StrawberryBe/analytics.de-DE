---
title: dc
description: Eine zurückgestellte Variable, mit der Sie bestimmen können, welches Rechenzentrum verwendet werden soll.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# dc

> [!IMPORTANT] Diese Variable wird eingestellt. Verwenden Sie [`trackingServer`](trackingserver.md) stattdessen.

In früheren Versionen von Adobe Analytics mussten Sie von Adobe angeben, an welches Rechenzentrum Sie Daten senden möchten. Das Senden von Treffern an das falsche Rechenzentrum führte zu Datenverlust.

Adobe hat diese Erfahrung verbessert, da jede Implementierung Treffer an senden kann `sc.omtrdc.net`. Die Angabe des Rechenzentrums ist nicht mehr erforderlich.
