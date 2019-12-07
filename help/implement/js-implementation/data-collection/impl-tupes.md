---
description: Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.
keywords: Analytics Implementation
title: Rückverfolgung über verschiedene Implementierungstypen hinweg
topic: Developer and implementation
uuid: a0a3229a-79a2-4dc2-b0be-4b8fac2efa3a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Rückverfolgung über verschiedene Implementierungstypen hinweg

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

Beim Einsatz mehrerer Typen von Implementierungen (wie JavaScript und fest kodierte Bildanfragen) müssen Sie sicherstellen, dass die folgenden Variablen angegeben sind und miteinander übereinstimmen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (bei Einsatz von SSL)

Wenn diese nicht in sämtlichen Implementierungen übereinstimmen, werden Benutzer bei der Verfolgung möglicherweise als separate Besucher erfasst.
