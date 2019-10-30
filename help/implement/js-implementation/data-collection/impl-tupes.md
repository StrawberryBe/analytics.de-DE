---
description: Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.
keywords: Analytics-Implementierung
seo-description: Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.
seo-title: Rückverfolgung über verschiedene Implementierungstypen hinweg
solution: Analytics
title: Rückverfolgung über verschiedene Implementierungstypen hinweg
topic: Entwickler und Implementierung
uuid: a0a3229a-79a2-4dc2-b0be-4b8fac2efa3a
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Rückverfolgung über verschiedene Implementierungstypen hinweg

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

Beim Einsatz mehrerer Typen von Implementierungen (wie JavaScript und fest kodierte Bildanfragen) müssen Sie sicherstellen, dass die folgenden Variablen angegeben sind und miteinander übereinstimmen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (bei Einsatz von SSL)

Wenn diese nicht in sämtlichen Implementierungen übereinstimmen, werden Benutzer bei der Verfolgung möglicherweise als separate Besucher erfasst.
