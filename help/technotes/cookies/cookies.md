---
title: Adobe Analytics und Browser-Cookies
description: Erfahren Sie, wie sich Tracking-Präventionsmaßnahmen auf von Adobe Analytics gesetzte Third-Party- und First-Party-Cookies auswirken.
feature: Data Configuration and Collection
exl-id: c4a4751e-49fc-40c3-aa39-f0f0b20bda1b
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: ht
source-wordcount: '1985'
ht-degree: 100%

---

# Adobe Analytics und Browser-Cookies

In diesem Dokument wird erläutert, wie sich die Tracking-Präventionsmaßnahmen der wichtigsten Browser auf die von Adobe Analytics gesetzten Third-Party- und First-Party-Cookies auswirken. Es enthält Informationen zum Programm Intelligent Tracking Prevention (ITP) von Apple sowie zu den Einschränkungen von Chrome für Third-Party-Cookies über das SameSite-Attribut.

## Wie haben Browser die Verwendung von Cookies eingeschränkt?

>[!NOTE]
>[Geräteübergreifende Analysen](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=de#cda) und [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de#comparing-cja-to-traditional-adobe-analytics) können Cookies mithilfe einer Personen-ID (z. B. einer Hash-Anmelde-ID) zuordnen, sofern eine solche ID verfügbar ist.

### Einschränkungen bei Third-Party-Cookies

Cookies, die in einem Third-Party-Kontext verwendet werden, werden weithin nicht mehr unterstützt. Firefox und Safari haben 2019 bzw. 2020 standardmäßig begonnen, Third-Party-Cookies zu blockieren. Chrome hat Pläne angekündigt, die Unterstützung von Third-Party-Cookies im Jahr 2023 einzustellen. Third-Party-Cookies sind dann effektiv nicht mehr verwendbar.

Darüber hinaus lässt Chrome derzeit die Funktion von Cookies in einem Third-Party-Kontext nur zu, wenn das SameSite-Attribut auf „None“ gesetzt ist und sie als sicher gekennzeichnet sind, d. h., sie können nur über HTTPS verwendet werden. Weitere Informationen finden Sie im Abschnitt „[Was ist das SameSite-Cookie-Attribut und wie wirkt es sich auf Analytics aus?](#samesite-effect)“.

#### Welche Third-Party-Cookies von Adobe sind betroffen?

Der Besucher-ID-Dienst verwendet das Cookie „[demdex.net](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=de)“, um eine beständige ID für Besucher über verschiedene Kundendomänen hinweg bereitzustellen. Beim älteren Analytics-ID-Dienst wird das Cookie „s_vi“ als Third-Party-Cookie für Implementierungen festgelegt, die keine benutzerdefinierte CNAME-Erfassungsdomäne verwenden.

Bei Browsern, in denen Third-Party-Cookies blockiert werden, ist kein domänenübergreifendes Tracking verfügbar.

### Einschränkungen bei First-Party-Cookies {#limitations-first-party-cookies}

First-Party-Cookies sind in allen gängigen Browsern zulässig. Apple beschränkt jedoch über das Intelligent Tracking Program (ITP) die Lebensdauer von First-Party-Cookies, die von Adobe gesetzt werden. Dies betrifft Safari sowie alle Browser unter iOS und iPadOS.

Die First-Party-Cookies von Adobe laufen n ach 7 Tagen ab. Bei Clickthroughs, die Apple als von Trackern gesendet erkennt, sogar schon nach 24 Stunden. Bei einer Lebensdauer von sieben Tagen wird das Ablaufdatum des Cookies um weitere sieben Tage verlängert, wenn ein Besucher Ihrer Site innerhalb von sieben Tagen zurückkehrt Wenn ein Besucher jedoch erst nach acht Tagen zurückkehrt, wird er beim zweiten Besuch als neuer Benutzer behandelt.

Derzeit gelten ITP-Richtlinien für alle von Adobe gesetzten First-Party-Cookies, unabhängig davon, ob Sie den Besucher-ID-Dienst oder ältere Analytics-ID (Cookie „s_vi“) verwenden. Diese Richtlinien galten früher nur für Cookies, die Client-seitig gesetzt wurden, und nicht für Cookies, die Server-seitig über eine CNAME-Implementierung gesetzt wurden. Im November 2020 wurde ITP jedoch aktualisiert und gilt nun auch für CNAME-Implementierungen.

#### Zeitlicher Ablauf der wichtigsten Änderungen an der ITP-Richtlinie {#ITP-timeline}

* Februar 2019 mit [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/): Client-seitige Cookies wurden auf einen siebentägigen Ablauf beschränkt
* April 2019 mit [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/): Client-seitige Cookies wurden auf 24 Stunden für Anzeigenklicks beschränkt, wenn die Referrer-Domain a) an Site-übergreifendem Tracking beteiligt war und b) die endgültige URL eine Abfragezeichenfolge und/oder eine Fragmentkennung enthielt.
* November 2020 mit [CNAME Cloaking and Bounce Tracking Defense](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/): ITP-Einschränkungen wurden auf CNAME-Implementierungen erweitert.

ITP-Richtlinien werden häufig weiterentwickelt. Die neuesten Richtlinien finden Sie unter [Tracking Prevention in Webkit](https://webkit.org/tracking-prevention) von Apple.

#### Welche First-Party-Cookies von Adobe sind betroffen?

Alle von Adobe gesetzten First-Party-Cookies und die zugehörigen JavaScript-Bibliotheken sind von ITP-Richtlinien betroffen:

* [AMCV-Cookies](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=de), die von der Bibliothek des Besucher-ID-Diensts von Adobe Experience Cloud (ECID) festgelegt werden
* Das veraltete Analytics-Cookie [„s_vi“](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de), wenn es für die First-Party-Datenerfassung mit CNAME konfiguriert ist
* Das veraltete Analytics-Cookie [„s_fid“](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de), das als Ausweich-Cookie verwendet wird, wenn „s_vi“ nicht gesetzt werden kann

#### Wie wirkt sich ITP auf Safari auf Analytics aus?

Die Auswirkungen der ITP-Einschränkungen können je nach dem Verhalten Ihrer Benutzer erheblich variieren. Dies betrifft nur Besucher, die einen von ITP betroffenen Browser verwenden (z. B. Safari) und nach einer Abwesenheit von sieben Tagen zurückkehren. Wenn Besucher keinen ITP-Browser verwenden oder innerhalb von sieben Tagen zurückkehren, sind sie davon nicht betroffen. Es ist wichtig, Ihre eigenen Daten in Analytics zu überprüfen, um das Ausmaß der Auswirkungen dieser Beschränkung zu verstehen. Tipps zum Messen der Auswirkungen auf Ihre Sites finden Sie unter „[Wie kann ich feststellen, ob Safari-Änderungen mein Unternehmen beeinträchtigen?](#measure-itp-effect)“.

Wenn sich diese Einschränkungen auf Ihre Daten auswirken, sehen Sie Folgendes:

1. Erhöhte Besucherzahlen, da wiederkehrende Besucher als neue Besucher gezählt werden, weil ihre Cookies abgelaufen sind. Alle Metriken, die auf der Besuchermetrik basieren (z. B. Umsatz pro Besucher), sind ebenfalls betroffen.
2. Änderungen an der Attribution. Die Attribution beruht auf der Verknüpfung von Konversionsereignissen mit vorherigen Aktivitäten desselben Besuchers. Sobald ein Cookie abläuft, werden nachfolgende Ereignisse einem neuen Besucher zugeordnet. Die Aktivitäten des neuen Besuchers können nicht mit den Aktivitäten des vorherigen Besuchers verknüpft werden.

>[!NOTE]
>
>ITP-Technologien gelten derzeit nicht für eingebettete Browser in Apps.

## Was ist der Unterschied zwischen Drittanbieter- und Erstanbieter-Cookies?

### Drittanbieter-Cookies

Third-Party-Cookies werden nicht von den Websites erstellt, die Anwender besuchen.

Obwohl Browser derzeit alle Third-Party-Cookies gleich behandeln und entsprechend speichern, können sich Third-Party-Cookies unterschiedlich verhalten. Bei der Implementierung von Analytics-Third-Party-Cookies eines Kunden speichern Browser die Adobe-ID [demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de) als Third-Party-Cookie, der Client führt jedoch Aufrufe nur zu Adobe und nicht zu unbekannten oder verdächtigen Third-Party-Domains durch. Dieses Cookie stellt Domain-übergreifende persistente IDs bereit und ermöglicht sicheren Content (HTTPS). Weitere Informationen finden Sie unter [Cookies und Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=de).

In Analytics-Implementierungen werden Third-Party-Cookies für Domain-übergreifendes Tracking und für Werbeanwendungen wie Retargeting-Anzeigen verwendet. Mit Third-Party-Cookies können Sie Besucher identifizieren, die verschiedene Domains besuchen, deren Inhaber Sie sind, oder denen Anzeigen auf Sites präsentiert werden, deren Inhaber Sie nicht sind.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### Erstanbieter-Cookies

First-Party-Cookies sind Domain-spezifisch und werden von Kunden-Websites erstellt und in Client-Browsern gespeichert, wenn Benutzer die Websites besuchen. Alle Browser akzeptieren im Allgemeinen First-Party-Cookies, obwohl [Safari das Ablaufen einiger First-Party-Cookie-Typen](#limitations-first-party-cookies) begrenzt.

In Analytics-Implementierungen werden First-Party-Cookies verwendet, um Benutzer zu identifizieren, wenn sie sich auf Ihrer Site befinden. Daher werden sämtliche Analysen von Benutzeraktivitäten unterstützt. Sie benötigen keine Third-Party-Cookies, um die Aktivitäten auf der Site zu verstehen.

Weitere Informationen finden Sie unter [Informationen zu Erstanbieter-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de).

![Cookie-Vergleich](/help/technotes/assets/cookies2.png)

## Was ist das SameSite-Cookie-Attribut und wie wirkt es sich auf Analytics-Cookies aus? {#samesite-effect}

Seit der Veröffentlichung des Chrome 80-Browsers im Februar 2020 – und der darauf folgenden Versionen der Browser Firefox und Edge – erzwingt das SameSite-Cookie-Attribut die Spezifikation für drei verschiedene Werte, die steuern, ob Cookies in einem Third-Party-Kontext verwendet werden können:

* `None`: Diese Einstellung ermöglicht den Site-übergreifenden Zugriff und die Weitergabe von Cookies in einem Drittanbieterkontext. Um dieses Attribut anzugeben, müssen Sie auch `Secure` angeben und alle Browser-Anfragen müssen HTTPS nutzen. Beim Einstellen des Cookies verbinden Sie beispielsweise die Werte des Attributs wie folgt: `Set-Cookie: example_session=test12; SameSite=None; Secure`. Wenn Cookies nicht richtig beschriftet sind, sind sie für die neueren Browser nicht verwendbar und werden abgelehnt.

* `Lax`: Ermöglicht das Senden von Site-übergreifenden Anfragen mit Cookies derselben Site nur für die Navigation auf oberster Ebene mit *sicheren* (schreibgeschützt, wie z. B. `GET`) HTTP-Methoden.

* `Strict`: Das SameSite-Cookie wird nicht für Website-Anfragen von Drittanbietern gesendet. Das Cookie wird nur gesendet, wenn die Site für das Cookie mit der Site in der URL-Leiste übereinstimmt.

Das Standardverhalten in diesen Browser-Versionen besteht darin, Cookies, die kein bestimmtes `SameSite`-Attribut aufweisen, wie `SameSite=Lax` zu behandeln.

### Wie verwaltet Analytics SameSite-Cookie-Attribute?

Für Kunden, die den Besucher-ID-Dienst verwenden, sind die Eigenschaften `SameSite=None` und `secure` standardmäßig festgelegt, sodass diese Cookies Third-Party-Anwendungen unterstützen können.

Bei Kunden, die ältere Analytics-IDs (Cookies „s_vi“ und „s_fid“) verwenden, werden Cookies ebenfalls gesetzt, um Third-Party-Anwendungen mit Standarderfassungs-Domains zu ermöglichen: adobedc.net, 2o7.net und omtrdc.net. Für Kunden, die eine CNAME-Implementierung verwenden, setzt Analytics `SameSite=Lax`.

>[!NOTE]
>
>Wenn Sie mehrere Domains besitzen und denselben CNAME für die Datenerfassung in all Ihren Domains verwenden, wird das Cookie in diesen anderen Domains als Third-Party-Cookie behandelt. Wenn Sie ältere Analytics-IDs verwenden, sollten Sie Ihre Einstellung zu `SameSite=None` aktualisieren, damit diese Cookies für alle Ihre Sites gemeinsam genutzt werden können. Weitere Informationen finden Sie unter „[Ändern des SameSite-Werts bei Verwendung eines CNAME für mehrere Domains](#samesite-one-cname)“ im nächsten Abschnitt.

Bei Browsern, die laut Google Cookies falsch verarbeiten, wenn `SameSite` auf `None` eingestellt ist, wird `SameSite` nicht festgelegt.

Die folgende Tabelle fasst die SameSite-Attribute für Analytics-Cookies zusammen:

![Cookie-Tabelle](/help/technotes/assets/cookies1.png)

### Wie können die Anforderungen für das SameSite-Attribut auf meiner Site erfüllt werden?

#### Bereitstellen aller Seiten Ihrer Site mit HTTPS

Vergewissern Sie sich, dass Ihre JavaScript-Konfiguration HTTPS für alle Aufrufe an Adobe-Dienste verwendet.

Wenn Ihre Site den Besucher-ID-Dienst von Experience Cloud verwendet, leitet der Service HTTP-Aufrufe von Drittanbietern an den HTTPS-Endpunkt weiter, was die Latenz erhöhen kann, aber auch bedeutet, dass Sie Ihre Konfiguration nicht ändern müssen.

#### Ändern des SameSite-Werts bei Verwendung eines CNAME für mehrere Domains {#samesite-one-cname}

>[!NOTE]
>
>Die folgenden Informationen beziehen sich nur auf Sites, die nicht den Besucher-ID-Dienst von Experience Cloud verwenden.

Wenn Sie über eine CNAME-Implementierung in derselben Domain wie Ihre Website verfügen, wird das Cookie in einem First-Party-Kontext erzeugt und Sie müssen keine Änderungen vornehmen.

Wenn Sie aber mehrere Domains besitzen und denselben CNAME für die Datenerfassung in all Ihren Domains verwenden, wird das Cookie in diesen anderen Domains als Third-Party-Cookie behandelt. Mit Chrome 80 und höher ist es in diesen anderen Domains nicht mehr sichtbar. Um das Verhalten in allen Browsern zu vereinheitlichen, setzt Analytics den `SameSite`-Wert dieses Cookies explizit auf `Lax`. Wenn Sie dieses Cookie im Kontext eines vertrauenswürdigen Drittanbieters verwenden, muss das Cookie auf den Wert `SameSite=None` eingestellt sein, was bedeutet, dass Sie immer HTTPS verwenden müssen. Wenn Sie dies noch nicht getan haben, wenden Sie sich an die Kundenunterstützung von Adobe, um den SameSite-Wert für Ihre sicheren CNAME-Elemente zu ändern.

## Wie kann ich feststellen, ob Safari-Änderungen mein Unternehmen beeinträchtigen? {#measure-itp-effect}

Adobe empfiehlt Kunden, die Auswirkungen innerhalb ihres eigenen Unternehmens zu messen, bevor sie die Datenerfassung ändern. Sie können Analysis Workspace verwenden, um die Auswirkungen der ITP-Tracking-Prävention auf Ihr Unternehmen zu messen:

* Messen Sie den Prozentsatz Ihres Traffics von ITP-verwalteten Browsern:

   1. Erstellen Sie ein Segment, um zu sehen, wie viele Besucher eine ITP-Plattform verwenden.

      >[!NOTE]
      >
      >Welche spezifischen Browser von ITP betroffen sind, hängt davon ab, ob Sie eine CNAME-Implementierung verwendet haben. Weitere Informationen finden Sie unter „[Zeitlicher Ablauf der wichtigsten Änderungen an der ITP-Richtlinie](#ITP-timeline)“.

      ![Segment für ITP-Besucher](/help/technotes/assets/itp-visitor-segment.png)

   2. Wenden Sie das Segment auf die Anzahl der Besuche an, um die relative Nutzung von Safari in Ihrer Benutzerbasis zu verstehen. Auf diese Weise können Sie eine Tabelle wie die folgende erstellen:

      ![Prozentsatz der Besuche durch ITP-Besucher](/help/technotes/assets/visits-vs-safari-visits.png)

* Messen Sie den Prozentsatz der Besucher, die Nicht-Safari-Browser verwenden und nicht innerhalb von sieben Tagen zurückkehren. Wenn Besucher, die einen anderen Browser als Safari verwenden, innerhalb von sieben Tagen wiederholt zurückkehren, wird Ihr Safari-Traffic möglicherweise nicht wesentlich beeinträchtigt.

   1. Erstellen Sie ein Segment wie das folgende für Nicht-Safari-Traffic.

      ![Segment für Besucher, die nach sieben Tagen zurückkehren](/help/technotes/assets/visits-after-seven-days.png)

   2. Wenden Sie das Segment auf die Anzahl der Besuche an, um die relative Nutzung von Safari in Ihrer Benutzerbasis zu verstehen. Auf diese Weise können Sie eine Tabelle wie die folgende erstellen:

      ![Prozentsatz der Besucher, die nach sieben Tagen zurückkehren](/help/technotes/assets/percent-visits-after-seven-days.png)

### Möglichkeiten zur Datenanpassung beim Reporting

Wenn Ihr Unternehmen von der ITP-Tracking-Prävention betroffen ist, können Sie die folgenden Maßnahmen in Erwägung ziehen, um Ihre Daten beim Reporting anzupassen.

* Erstellen Sie ein Segment, um ITP-Benutzer herauszufiltern.

   ![Segment für Nicht-ITP-Besucher](/help/technotes/assets/non-itp-visitor-segment.png)

* Erstellen Sie eine berechnete Metrik, um eine Anpassung anhand der bekannten Besucherinflation vorzunehmen.

   ![Berechnete Metrik zur Anpassung anhand der Besucherinflation](/help/technotes/assets/estimated-itp-visitors-metric.png)

>[!MORELIKETHIS]
>
>[Optionen zum Abmildern der Auswirkungen von Beschränkungen für Browser-Cookies](cookieless.md)
>[Auswirkungen des neuen App Tracking Transparency Framework von Apple auf Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833?profile.language=de)
