---
title: Häufig gestellte Fragen zur Implementierung von Analytics
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
keywords: Analytics Implementation;faq;frequently asked questions;evar expiration;custom event visibility;timestamp;visitor id grace period;visitor id;Experience Cloud visitor id;analytics visitor id;dtm;heartbeat;cookies;tracking server;performance;javascript;data collection;s_code version;s_code debug;track link types;track video;track mobile app;first party cookie;ssl certificate;certification expiration;certificate expiration;plugins;data insertion api;500 error;500;Manage user;manage group;users;groups
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

**Was ist der Unterschied zwischen Zuordnung und Gültigkeit von Variablen?**

Zuordnung und Gültigkeit sind beides Einstellungen, die Sie auf benutzerdefinierte Variablen anwenden können. Die *Zuordnung* kommt zum Tragen, wenn Sie einen beibehaltenen Variablenwert und einen neuen Variablenwert haben. Sie legt fest, ob der alte oder der neue Wert beibehalten wird. Die *Gültigkeit* kommt zum Tragen, wenn ein Variablenwert nicht beibehalten werden soll.

**Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID?**

Der Identitätsdienst weist eine eindeutige, beständige ID zu, die von den anderen Lösungen in Experience Cloud gemeinsam genutzt werden kann. Die Analytics-Besucher-ID wird nur von Analytics verwendet. Adobe empfiehlt, den Experience Cloud-Besucher-ID-Dienst in Ihrer Implementierung zu verwenden.

**Wie wird eine Besucher-ID eingestellt, wenn Cookies blockiert werden?**

Wenn das normale `s_vi`-Cookie nicht verfügbar ist, wird ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen `s_fid` wird mit einer Gültigkeit von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen.

**Wie wird Heartbeat-Video-Tracking implementiert?**

Weitere Informationen finden Sie unter [Messen von Audio und Video in Adobe Analytics](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html).

**Kann eine Dienstunterbrechung bei Adobe die Performance beeinträchtigen?**

Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf Ihre AppMeasurement-Bibliothek auswirkt. Wenn Sie Adobe Experience Platform Launch verwenden, wird die JavaScript-Datei von Akamai oder von einem von Ihrem Unternehmen bestimmten Server-Standort gehostet.

**Kann das Senden von Daten vom Browser an die Adobe-Dienste die Performance beeinträchtigen?**

AppMeasurement erstellt innerhalb der HTML-Seite ein Bildobjekt, das der Browser dann von den Adobe-Datenerfassungs-Servern anfordert. Falls der Datenerfassungs-Server sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Bildes verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Bildern durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten.

**Wie funktioniert das App-Tracking?**

Sie können das Adobe Experience Platform SDK verwenden. Weitere Informationen finden Sie unter [Übersicht über das Adobe Experience Platform SDK](https://aep-sdks.gitbook.io/docs/).

**Was sind Plug-ins?**

Plug-ins sind Codefragmente, die erweiterte Funktionen ausführen. Sie erweitern die Funktionen von AppMeasurement, um Ihnen mehr Funktionalität in Ihrer Implementierung zu bieten.
