---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
translation-type: ht
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651
workflow-type: ht
source-wordcount: '102'
ht-degree: 100%

---


# Tracking über verschiedene Implementierungstypen hinweg

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Versuchen Sie nicht, Ihre Implementierung zu verändern, wenn Sie nicht genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

Beim Einsatz mehrerer Typen von Implementierungen (wie JavaScript und fest kodierte Bildanfragen) müssen Sie sicherstellen, dass die folgenden Variablen angegeben sind und miteinander übereinstimmen:

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`* (bei Einsatz von SSL)

Wenn diese nicht in sämtlichen Implementierungen übereinstimmen, werden Benutzer bei der Verfolgung möglicherweise als separate Besucher erfasst.
