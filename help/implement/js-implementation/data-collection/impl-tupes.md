---
description: Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.
keywords: Analytics-Implementierung
seo-description: Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.
seo-title: Verfolgen Sie die verschiedenen Implementierungstypen.
solution: Analytics
title: Verfolgen Sie die verschiedenen Implementierungstypen.
topic: Entwickler und Implementierung
uuid: a 0 a 3229 a -79 a 2-4 dc 2-b 0 be -4 b 8 fac 2 efa 3 a
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verfolgen Sie die verschiedenen Implementierungstypen.

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

Beim Einsatz mehrerer Typen von Implementierungen (wie JavaScript und fest kodierte Bildanfragen) müssen Sie sicherstellen, dass die folgenden Variablen angegeben sind und miteinander übereinstimmen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (bei Einsatz von SSL)

Wenn diese nicht in sämtlichen Implementierungen übereinstimmen, werden Benutzer bei der Verfolgung möglicherweise als separate Besucher erfasst.
