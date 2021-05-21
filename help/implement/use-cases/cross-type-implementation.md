---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
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
