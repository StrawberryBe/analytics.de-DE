---
title: Häufig gestellte Fragen zur Implementierung von Analytics
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
keywords: Analytics Implementation;faq;frequently asked questions;evar expiration;custom event visibility;timestamp;visitor id grace period;visitor id;Experience Cloud visitor id;analytics visitor id;dtm;heartbeat;cookies;tracking server;performance;javascript;data collection;s_code version;s_code debug;track link types;track video;track mobile app;first party cookie;ssl certificate;certification expiration;certificate expiration;plugins;data insertion api;500 error;500;Manage user;manage group;users;groups
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

**Was ist der Unterschied zwischen der Variablenzuordnung und dem Ablauf?**

Zuordnung und Ablauf sind beide Einstellungen, die Sie auf benutzerdefinierte Variablen anwenden können. *Die Zuordnung* kommt zum Tragen, wenn Sie einen beständigen Variablenwert und einen neuen Variablenwert haben. Er bestimmt, ob der alte oder der neue Wert beibehalten wird. *Das Ablaufdatum* kommt zum Tragen, wenn ein Variablenwert nicht beibehalten werden soll.

**Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID?**

Der Identitätsdienst weist eine eindeutige, beständige ID zu, die in der Experience Cloud für andere Lösungen freigegeben werden kann. Die Analytics-Besucher-ID wird nur von Analytics verwendet. Adobe empfiehlt die Verwendung des Experience Cloud-Besucher-ID-Service in Ihrer Implementierung.

**Wie wird eine Besucher-ID eingestellt, wenn Cookies blockiert werden?**

If the standard `s_vi` cookie is unavailable, a fallback cookie is created on the domain of the website with a randomly generated unique ID. This cookie, named `s_fid`, is set with a 2-year expiration and is used as the fallback identification method going forward.

**Wie implementiere ich die Heartbeat-Videoverfolgung?**

Weitere Informationen finden Sie unter [Messen von Audio und Video in Adobe Analytics](https://docs.adobe.com/content/help/en/media-analytics/using/media-overview.html).

**Kann eine Serviceunterbrechung bei Adobe die Leistung beeinträchtigen?**

Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass ein Adobe-Ausfall Ihre AppMeasurement-Bibliothek nicht beeinträchtigt. Wenn Sie Adobe Experience Platform Launch verwenden, wird die JavaScript-Datei von Akamai oder einem von Ihrem Unternehmen bestimmten Serverstandort gehostet.

**Kann das Senden von Daten vom Browser an Adobe-Dienste die Leistung reduzieren?**

AppMeasurement erstellt ein Bildobjekt auf der HTML-Seite und der Browser fordert dann das Bildobjekt von den Adobe-Datenerfassungsservern an. Wenn die Datenerfassungsserver langsam oder nicht reagieren, wird die Thread-Verarbeitung dieser Anforderung verzögert, bis das Bild zurückgegeben wird oder ein Timeout auftritt. Da in Browsern die Verarbeitung von Images durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten.

**Wie kann ich eine mobile App verfolgen?**

Sie können das Adobe Experience Platform SDK verwenden. Weitere Informationen finden Sie unter Übersicht über das [Adobe Experience Platform SDK](https://aep-sdks.gitbook.io/docs/) .

**Was sind Plug-ins?**

Plug-ins sind Codefragmente, die erweiterte Funktionen ausführen. Sie erweitern die Funktionen von AppMeasurement, um Ihnen mehr Funktionalität in Ihrer Implementierung zu bieten.
