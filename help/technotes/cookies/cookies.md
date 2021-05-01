---
title: Adobe Analytics und Browsercookies
description: Erfahren Sie, wie die von Adobe Analytics eingerichteten Drittanbieter- und Erstanbieter-Cookies durch Maßnahmen zur Rückverfolgung von Präventionsmaßnahmen beeinflusst werden.
translation-type: tm+mt
source-git-commit: 07c76cea1f6fd64957fd4fd20bc5187976f3c14c
workflow-type: tm+mt
source-wordcount: '1887'
ht-degree: 7%

---


# Adobe Analytics und Browsercookies

In diesem Dokument wird erläutert, wie die Präventionsmaßnahmen der wichtigsten Browser zur Verfolgung von Drittanbieter-Cookies und Erstanbieter-Cookies von Adobe Analytics beeinflussen. Es enthält Informationen zum Intelligent Tracking Prevention (ITP)-Programm von Apple sowie zu den Einschränkungen von Chrome für Drittanbieter-Cookies über das Attribut SameSite.

## Wie wurde die Verwendung von Cookies durch Browser eingeschränkt?

### Einschränkungen bei Drittanbieter-Cookies

Cookies, die in einem Drittanbieterkontext verwendet werden, werden weitgehend eingestellt. Firefox und Safari haben begonnen, Drittanbieter-Cookies standardmäßig ab 2019 bzw. 2020 zu blockieren. Chrome hat Pläne angekündigt, die Unterstützung von Drittanbieter-Cookies irgendwann im Jahr 2022 einzustellen. In diesem Fall sind Drittanbieter-Cookies praktisch unbrauchbar.

Außerdem erlaubt Chrome derzeit nur Cookies, die das Attribut &quot;SameSite&quot;auf &quot;Keine&quot;gesetzt haben und als sicher gekennzeichnet sind, d. h. sie können nur über HTTPS verwendet werden. Weitere Informationen finden Sie im Abschnitt &quot;[Was ist das Attribut &quot;SameSite-Cookie&quot;und wie wirkt es sich auf Analytics aus?](#samesite-effect)&quot;

#### Welche Adobe von Drittanbieter-Cookies sind betroffen?

Der Besucher-ID-Dienst verwendet das [`demdex.net`](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)-Cookie, um einen beständigen Bezeichner für Besucher über verschiedene Kundendomänen hinweg bereitzustellen. In Browsern, in denen Drittanbieter-Cookies blockiert sind, steht keine domänenübergreifende Verfolgung zur Verfügung.

### Erstanbieter-Cookie-Beschränkungen {#limitations-first-party-cookies}

Erstanbieter-Cookies sind in allen gängigen Browsern zulässig. Apple beschränkt jedoch die Lebensdauer von Erstanbieter-Cookies, die von der Adobe über ihr Intelligent Tracking Programm (ITP) eingestellt werden. Dazu gehören Safari unter MacOS und alle Browser unter iOS und iPadOS.

Die Erstanbieter-Cookies der Adobe sind auf einen Ablauf von 7 Tagen oder einen Ablauf von 24 Stunden für Clickthroughs beschränkt, von denen Apple feststellt, dass sie von Trackern stammen. Bei Ablauf von 7 Tagen verlängert sich das Ablaufdatum des Cookies um weitere sieben Tage, wenn ein Benutzer Ihre Site besucht und dann innerhalb dieser sieben Tage zurückkehrt. Wenn ein Benutzer jedoch Ihre Site besucht und dann innerhalb von acht Tagen zurückkehrt, wird er beim zweiten Besuch als neuer Benutzer behandelt.

Derzeit gelten ITP-Richtlinien für alle Erstanbieter-Cookies, die von der Adobe gesetzt werden, unabhängig davon, ob Sie den Besucher-ID-Dienst oder das Legacy-Analytics-ID-Cookie (&quot;s_vi&quot;-Cookie) verwenden. An einem Punkt galten diese Richtlinien nur für clientseitige Cookies und nicht für serverseitige Cookies, die über eine CNAME-Implementierung festgelegt wurden. Im November 2020 wurde ITP jedoch aktualisiert, um auch für CNAME-Implementierungen zu gelten.

#### Zeitablauf der wichtigsten Änderungen der ITP-Politik

* Februar 2019 mit [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/): Clientseitige Cookies waren auf einen siebentägigen Ablauf beschränkt
* April 2019 mit [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/): Clientseitige Cookies waren bei Anzeigenklicks auf 24 Stunden begrenzt, wenn die verweisende Domäne a) an der Site-übergreifenden Verfolgung beteiligt war und b) die endgültige URL eine Abfrage und/oder einen Fragmentbezeichner enthielt.
* November 2020 mit [CNAME Cloaking und Absprung-Tracking-Verteidigung](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/): ITP-Beschränkungen wurden auf CNAME-Implementierungen erweitert.

ITP-Richtlinien entwickeln sich häufig. Die neuesten Richtlinien finden Sie unter [Tracking Prevention in Webkit](https://webkit.org/tracking-prevention).

#### Welche Erstanbieter-Cookies von Adoben sind betroffen?

Alle von der Adobe eingestellten Erstanbieter-Cookies und die zugehörigen JavaScript-Bibliotheken sind von den ITP-Richtlinien betroffen:

* [`AMCV` von der Adobe Experience Cloud Besucher ID (ECID)-Dienstbibliothek ](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html) eingestellte Cookies
* Das Analytics-Legacy [`s_vi`-Cookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html), wenn es mit der Erstanbieter-Datenerfassung mithilfe eines CNAME konfiguriert wird
* Das Analytics-Legacy [`s_fid`-Cookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html), das das Ausweichcookie ist, das verwendet wird, wenn `s_vi` nicht eingestellt werden kann

#### Welche Auswirkungen hat ITP auf Safari für Analytics?

Die Auswirkungen der ITP-Beschränkungen variieren je nach Verhalten der Benutzer erheblich. Davon sind nur Besucher betroffen, die einen von ITP betroffenen Browser (d. h. Safari) verwenden und nach einer Abwesenheit von sieben Tagen zurückkehren. Wenn Besucher keinen ITP-Browser verwenden oder innerhalb von sieben Tagen zurückkehren, sind sie davon nicht betroffen. Es ist wichtig, dass Sie Ihre eigenen Daten in Analytics überprüfen, um zu verstehen, wie stark diese Einschränkung wirkt. Tipps zum Messen der Auswirkungen auf Ihre Sites finden Sie unter &quot;[Wie kann ich feststellen, ob Safari-Änderungen mein Geschäft betreffen?](#measure-itp-effect)&quot;

Wenn sich diese Einschränkungen auf Ihre Daten auswirken, sehen Sie Folgendes:

1. Erhöhte Besucher zählt, da wiederkehrende Besucher als neue Besucher behandelt werden, da ihre Cookies abgelaufen sind. Alle Metriken, die auf der Metrik &quot;Besucher&quot;basieren (z. B. &quot;Umsatz pro Besucher&quot;), sind ebenfalls betroffen.
2. Änderungen an der Zuordnung. Konversionselemente sind an vorhergehende Aktivitäten desselben Besuchers gebunden. Sobald ein Cookie abläuft, werden zukünftige Ereignis mit einem neuen Besucher verknüpft, und Konversionen können nicht mehr an den ursprünglichen Besucher gebunden werden.

>[!NOTE]
>
>ITP-Technologien gelten derzeit nicht für eingebettete Browser in mobilen Apps.

## Was ist der Unterschied zwischen Drittanbieter- und Erstanbieter-Cookies?

### Drittanbieter-Cookies

Drittanbieter-Cookies werden nicht von den Websites erstellt, die Benutzer besuchen.

Obwohl Browser derzeit alle Drittanbieter-Cookies gleich behandeln und entsprechend speichern, können sich Drittanbieter-Cookies unterschiedlich verhalten. Bei der Analytics-Drittanbieter-Cookie-Implementierung eines Kunden speichern Browser die Adobe [demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)-ID als Drittanbieter-Cookie. Der Client ruft jedoch nur die Adobe und nicht zu unbekannte oder verdächtige Drittanbieter-Domänen auf. Dieses Cookie stellt domänenübergreifende IDs bereit und ermöglicht sicheren (HTTPS-)Inhalt. Weitere Informationen finden Sie unter [Cookies und Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html).

In Analytics-Implementierungen werden Drittanbieter-Cookies zur domänenübergreifenden Verfolgung und für Werbezwecke verwendet, einschließlich Targeting-Anzeigen. Mit Drittanbieter-Cookies können Sie Besucher identifizieren, wenn Sie verschiedene Domänen besuchen, deren Inhaber Sie sind, oder wenn Anzeigen auf Sites angezeigt werden, die Ihnen nicht gehören.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### Erstanbieter-Cookies

Erstanbieter-Cookies sind domänenspezifisch und werden von Kunden-Websites erstellt und in Clientbrowsern gespeichert, während Benutzer die Websites besuchen. Alle Browser akzeptieren in der Regel Erstanbieter-Cookies, obwohl [Safari den Ablauf bestimmter Erstanbieter-Cookie-Typen einschränkt.](#limitations-first-party-cookies)

In Analytics-Implementierungen werden Erstanbieter-Cookies verwendet, um Benutzer zu identifizieren, wenn sie sich auf Ihrer Site befinden, und unterstützen daher die gesamte Analyse der Aktivität von Benutzern. Sie benötigen keine Drittanbieter-Cookies, um die Aktivität vor Ort zu verstehen.

Weitere Informationen finden Sie unter [Informationen zu Erstanbieter-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html).

![Cookie-Vergleich](/help/technotes/assets/cookies2.png)

## Welches ist das SameSite-Cookie-Attribut und wie wirkt es sich auf Analytics-Cookies aus? {#samesite-effect}

Mit der Veröffentlichung des Chrome 80-Browsers im Februar 2020 — und aufeinander folgenden Versionen von Firefox und Edge-Browsern — Das SameSite-Cookie-Attribut erzwingt die Angabe für drei verschiedene Werte, um das Verhalten von Site-übergreifenden Anforderungen zu steuern:

* `None`: Diese Einstellung ermöglicht den Site-übergreifenden Zugriff und die Weitergabe von Cookies in einem Drittanbieterkontext. Um dieses Attribut anzugeben, müssen Sie auch `Secure` angeben und alle Browser-Anfragen müssen HTTPS nutzen. Beim Einstellen des Cookies verbinden Sie beispielsweise die Werte des Attributs wie folgt: `Set-Cookie: example_session=test12; SameSite=None; Secure`. Wenn die Cookies nicht richtig beschriftet sind, sind sie für die neueren Browser nicht verwendbar und werden abgelehnt.

* `Lax`: Ermöglicht das Senden von Site-übergreifenden Anforderungen mit Cookies derselben Site nur für die Navigation auf der obersten Navigationsebene mit  *sicheren*  (schreibgeschützten) HTTP-Methoden, z. B.  `GET`).

* `Strict`: Das SameSite-Cookie wird nicht für Website-Anfragen von Drittanbietern gesendet. Das Cookie wird nur gesendet, wenn die Site für das Cookie mit der Site in der URL-Leiste übereinstimmt.

Das Standardverhalten in diesen Browser-Versionen besteht darin, Cookies, die kein bestimmtes `SameSite`-Attribut aufweisen, wie `SameSite=Lax` zu behandeln.

### Wie verwaltet Analytics SameSite-Cookie-Attribute?

Alle Cookie-Updates für Adoben werden über Adoben-Server verarbeitet, und die Adobe Edge-Server legen die entsprechenden Cookie-Attribute fest. Alle Drittanbieter-Cookies wurden serverseitig mit den entsprechenden Attributen aktualisiert. Für Ihre Sites sind keine JavaScript-Updates erforderlich.

Diese Aktualisierung durch die Edge-Server der Adobe erfolgte automatisch, wenn die Benutzer jede Website besuchten, auf der das Cookie verwendet wurde. Bei den meisten Adoben hatten Cookies die entsprechenden Flags, als Chrome 80 im Jahr 2020 veröffentlicht wurde. Die Ausnahme bildeten Adobe Analytics-Implementierungen, die die Datenerfassung von Drittanbietern verwenden und nicht den Experience Cloud-Besucher-ID-Dienst verwenden. Bei dieser Implementierung müssen Sie die Kundenunterstützung bitten, die Flags zu ändern. Weitere Informationen finden Sie unter &quot;[Ändern Sie den Wert von &quot;SameSite&quot;, wenn Sie einen CNAME für mehrere Domänen](#samesite-one-cname) verwenden. Bis die Kennzeichnung geändert wird, kann es bei diesen Kunden zu einer geringfügigen vorübergehenden Zunahme neuer Besucher kommen, die sonst als wiederkehrende Besucher gekennzeichnet würden.

Bei Browsern, die Google als falsch gehandhabt hat, wenn `SameSite` auf `None` eingestellt ist, bleibt `SameSite` stattdessen deaktiviert.

In der folgenden Tabelle sind die Attribute von SameSite für Analytics-Cookies zusammengefasst:

![Cookie-Tabelle](/help/technotes/assets/cookies1.png)

### Wie können die Anforderungen an die Adresse meiner Site für das SameSite-Attribut lauten?

#### Alle Seiten Ihrer Site mit HTTPS bereitstellen

Vergewissern Sie sich, dass Ihre JavaScript-Konfiguration HTTPS für alle Aufrufe von Adobe Services verwendet.

Wenn Ihre Site den Experience Cloud-Besucher-ID-Dienst verwendet, leitet der Dienst HTTP-Aufrufe von Drittanbietern an seinen HTTPS-Endpunkt weiter, was die Latenz erhöhen kann, was bedeutet, dass Sie Ihre Konfiguration nicht ändern müssen.

#### Ändern Sie den Wert &quot;GleichSite&quot;, wenn Sie einen CNAME für mehrere Domänen {#samesite-one-cname} verwenden

>[!NOTE]
>
>Die folgenden Informationen beziehen sich nur auf Sites, die den Experience Cloud-Besucher-ID-Dienst nicht verwenden.

Wenn Sie über eine CNAME-Implementierung verfügen, die in derselben Domäne wie Ihre Website festgelegt ist, wird das Cookie in einem Erstanbieterkontext erstellt und Sie müssen keine Änderungen vornehmen.

Wenn Sie jedoch über mehrere Domänen verfügen und denselben CNAME für die Datenerfassung in allen Ihren Domänen verwenden, wird das Cookie in diesen anderen Domänen als Drittanbieter-Cookie behandelt. Mit Chrome 80 und höher ist es auf diesen anderen Domänen nicht mehr sichtbar. Um das Verhalten in allen Browsern ähnlicher zu gestalten, hat Analytics den Wert `SameSite` dieses Cookies explizit auf `Lax` gesetzt. Wenn Sie dieses Cookie in einem benutzerfreundlichen Drittanbieterkontext verwenden, muss das Cookie mit dem Wert `SameSite=None` gesetzt werden. Dies bedeutet auch, dass Sie immer HTTPS verwenden müssen. Falls noch nicht geschehen, wenden Sie sich an den Kundendienst der Adobe, um den SameSite-Wert für Ihre sicheren CNAMEs zu ändern.

## Wie kann ich feststellen, ob Safari-Änderungen mein Geschäft beeinträchtigen? {#measure-itp-effect}

Adobe empfiehlt Kunden, die Auswirkungen innerhalb ihrer eigenen Firma zu messen, bevor sie die Datenerfassung ändern. Sie können Analysis Workspace verwenden, um die Auswirkungen der ITP-Verfolgungsverhütung auf Ihr Unternehmen zu messen:

* Messen Sie den Prozentsatz Ihres Traffics von ITP-basierten Browsern:

   1. Erstellen Sie ein Segment, um zu sehen, wie viele Besucher eine ITP-Plattform verwenden.

      ![Segment für ITP-Besucher](/help/technotes/assets/itp-visitor-segment.png)

   2. Wenden Sie das Segment auf die Anzahl der Besuche an, um die relative Nutzung von Safari in Ihrer Benutzerbasis zu verstehen. Auf diese Weise können Sie eine Tabelle wie die folgende erstellen:

      ![Prozentsatz der Besuche durch ITP-Besucher](/help/technotes/assets/visits-vs-safari-visits.png)

* Messen Sie den Prozentsatz der Besucher, die Nicht-Safari-Browser verwenden und die nicht innerhalb von sieben Tagen zurückkehren. Wenn Ihre Besucher ohne Safari innerhalb von sieben Tagen wiederholt zurückkehren, wird Ihr Safari-Traffic möglicherweise nicht wesentlich beeinträchtigt.

   1. Erstellen Sie ein Segment wie das folgende für Nicht-Safari-Traffic.

      ![Segment für Besucher, die nach sieben Tagen zurückkehren](/help/technotes/assets/visits-after-seven-days.png)

   2. Wenden Sie das Segment auf die Anzahl der Besuche an, um die relative Nutzung von Safari in Ihrer Benutzerbasis zu verstehen. Auf diese Weise können Sie eine Tabelle wie die folgende erstellen:

      ![Prozentsatz der Besucher, die nach sieben Tagen zurückkehren](/help/technotes/assets/percent-visits-after-seven-days.png)

### Möglichkeiten zur Datenanpassung während des Berichte

Wenn Ihr Unternehmen von der ITP-Verfolgungsvermeidung betroffen ist, sollten Sie die folgenden Maßnahmen in Erwägung ziehen, um Ihre Daten während des Berichte anzupassen.

* Erstellen Sie ein Segment, um ITP-Benutzer auszufiltern.

   ![Segment für Nicht-ITP-Besucher](/help/technotes/assets/non-itp-visitor-segment.png)

* Erstellen Sie eine errechnete Metrik, um die Besucher-Inflation zu berücksichtigen.

   ![Berechnete Metrik zur Anpassung an die Besucher-Inflation](/help/technotes/assets/estimated-itp-visitors-metric.png)

>[!MORELIKETHIS]
>
>[Optionen zur Abschwächung der Auswirkungen von Browser-Cookie-Einschränkungen](cookieless.md)
>[Auswirkungen des neuen Apple App Tracking Transparency Framework auf Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833)
