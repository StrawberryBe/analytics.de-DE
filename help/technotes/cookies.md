---
title: Adobe Analytics und Browsercookies
description: Erfahren Sie, wie Adobe Analytics die Cookies von Browsern verarbeitet.
translation-type: ht
source-git-commit: 3566960f546d847ed4f6ca8ecbb9c759460f4fb0
workflow-type: ht
source-wordcount: '2286'
ht-degree: 100%

---


# Adobe Analytics und Browsercookies

Um eine dauerhafte Anwenderidentifizierung über Sites und Lösungen hinweg zu unterstützen, reagiert Adobe Analytics auf Änderungen bei der Verarbeitung von Cookies durch Browser. Die folgenden häufig gestellten Fragen enthalten Informationen darüber, wie die beständige Besucheridentifizierung trotz Änderungen des Browsercookies beibehalten wird.

## Inwiefern ändern Browser die Handhabung von Cookies?

Im Allgemeinen werden die meisten Browser bei der Speicherung von Drittanbieter-Cookies immer restriktiver. Dies kann sich auf das Tracking auswirken, wenn das Cookie vom Browser gelöscht oder abgelehnt wird. Der Safari-Browser legt außerdem verschiedene Einschränkungen für einige Erstanbieter-Cookies fest.

Die folgende Liste zeigt einige Änderungen, die je nach Browser vorgenommen wurden:

* Chrome: Ab Chrome 80 wird das `SameSite`-Attribut anders behandelt, um Drittanbieter-Cookies oder Site-übergreifende Anforderungen zu verwalten. Letztlich suchen Chrome-Entwickler nach Möglichkeiten, Drittanbieter-Cookies [komplett abzuschaffen](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html?m=1).

* Firefox und Edge: Produktankündigungen besagen, dass die anstehenden Versionen der Browser dieselben Änderungen wie in Chrome 80 enthalten werden.

* Safari: In [Safari 12.1](https://webkit.org/blog/category/privacy/) ist die Gültigkeit aller persistenten Cookies von Erstanbietern, die über die document.cookie-API gesetzt werden (auch „Client-seitige Cookies“ genannt), auf sieben Tage begrenzt.

## Was ist der Unterschied zwischen Drittanbieter- und Erstanbieter-Cookies?

### Erstanbieter-Cookies

Erstanbieter-Cookies werden von Kunden-Websites (domänenspezifisch) erstellt und in Clientbrowsern gespeichert, wenn Anwender Kunden-Websites besuchen. Alle Browser akzeptieren in der Regel Erstanbieter-Cookies. Bei einer Analytics-Implementierung von Erstanbieter-Cookies wird das Besucher-ID-Cookie an einem Adobe-Knoten erstellt, wenn der Host-Name mithilfe eines [CNAME](https://docs.adobe.com/content/help/de-DE/id-service/using/reference/analytics-reference/cname.html) mit der Domäne abgeglichen wird. Das Cookie wird dann vom Browser in einem Erstanbieterkontext akzeptiert. Weitere Informationen finden Sie unter [Informationen zu Erstanbieter-Cookies](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.html).

### Drittanbieter-Cookies

Drittanbieter-Cookies werden nicht von den Websites erstellt, die Anwender besuchen. Obwohl Browser derzeit alle Drittanbieter-Cookies gleich behandeln und entsprechend speichern, können sich die Drittanbieter-Cookies selbst auf unterschiedliche Weise verhalten. Bei der Analytics-Implementierung von Drittanbieter-Cookies eines Kunden sendet der Client Aufrufe nur an Adobe und nicht an unbekannte oder verdächtige Drittanbieterdomänen. Dies ist die aktuelle Methode zur Implementierung von Analytics für sicheres (HTTPS) und zuverlässiges Tracking mit beständigen Kennungen. Diese Methode wird durch Konfiguration der Datei „AppMeasurement.js“ implementiert. Weitere Informationen finden Sie unter [Cookies und Experience Platform Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/intro/cookies.html).

![Cookie-Vergleich](assets/cookies2.png)

## Wie speichern und verwalten Browser derzeit Analytics-Cookies?

Je nach Implementierung werden Analytics-Cookies wie folgt gespeichert:

### Drittanbieter-Cookie-Implementierungen

Browser speichern die Adobe-ID [demdex.net](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/reference/demdex-calls.html) derzeit als Drittanbieter-Cookie. Dieses Cookie stellt domänenübergreifende IDs bereit und ermöglicht sicheren Inhalt (HTTPS).

### Erstanbieter-Cookie-Implementierungen

Durch die Konfiguration eines CNAME können Ihre Anwender Adobe-Cookies in einem Erstanbieter-Cookie-Kontext für ihre Browser empfangen. Dies kann eine praktikable Option sein, wenn eine Drittanbieter-Cookie-Implementierung für Ihre Anwender nicht optimal ist.

## Was ist das SameSite-Cookie-Attribut und wie wirkt es sich auf Analytics aus?

Mit der Veröffentlichung des Chrome 80-Browsers – und der anstehenden Versionen von Firefox und Edge – erzwingt das SameSite-Cookie-Attribut die Spezifikation für die drei folgenden Werte, um das Verhalten Site-übergreifender Anfragen zu steuern:

* `None`: Diese Einstellung ermöglicht den Site-übergreifenden Zugriff und die Weitergabe von Cookies in einem Drittanbieterkontext. Um dieses Attribut anzugeben, müssen Sie auch `Secure` angeben und alle Browser-Anfragen müssen HTTPS nutzen. Beim Einstellen des Cookies verbinden Sie beispielsweise die Werte des Attributs wie folgt: `Set-Cookie: example_session=test12; SameSite=None; Secure`. Wenn die Cookies nicht richtig beschriftet sind, sind sie für die neueren Browser nicht verwendbar und werden abgelehnt.

* `Lax`: Ermöglicht das Senden von Site-übergreifenden Anfragen mit Cookies derselben Site nur für Navigation auf oberster Ebene mit *sicheren* (schreibgeschützt, wie z. B. `GET`) HTTP-Methoden.

* `Strict`: Das SameSite-Cookie wird nicht für Website-Anfragen von Drittanbietern gesendet. Das Cookie wird nur gesendet, wenn die Site für das Cookie mit der Site in der URL-Leiste übereinstimmt.

Das Standardverhalten in diesen Browser-Versionen besteht darin, Cookies, die kein bestimmtes `SameSite`-Attribut aufweisen, wie `SameSite=Lax` zu behandeln.

## Wie reagiert Adobe Analytics auf diese Änderungen?

Alle Adobe-Cookie-Updates werden über Adobe-Server verarbeitet und Adobe hat seine Edge-Server aktualisiert, um die entsprechenden Cookie-Attribute festzulegen. Adobe hat Server-seitige Updates veröffentlicht, um Cookies von Drittanbietern mit den entsprechenden Attributen festzulegen. Für Ihre Sites sind keine JavaScript-Updates erforderlich.

Diese Aktualisierung durch die Adobe Edge-Server erfolgt automatisch, wenn Anwender eine Website besuchen, auf der das Cookie verwendet wird. Bei den meisten Adobe-Produkten verfügen Cookies über die entsprechenden Flags, wenn Chrome 80 veröffentlicht wird. Eine Ausnahme bilden Adobe Analytics-Implementierungen, bei denen statt Experience Cloud Identity Service (ECID) die Datenerfassung von Drittanbietern verwendet wird. Bei diesen Kunden kann es zu einem geringfügigen vorübergehenden Anstieg neuer Besucher kommen, die sonst als wiederkehrende Besucher gekennzeichnet wären.

Bei Browsern, die laut Google Cookies falsch verarbeiten, wenn `SameSite` auf `None` eingestellt ist, wird `SameSite` nicht festgelegt.

Die folgende Tabelle fasst Analytics-Cookies zusammen:

![Cookie-Tabelle](assets/cookies1.png)

## Wie kann ich meine Site am besten auf Chrome-, Firefox- und Edge-Änderungen vorbereiten?

Analytics-Kunden sollten sicherstellen, dass ihre JavaScript-Konfiguration HTTPS für ihre Aufrufe an Adobe-Dienste verwendet. ECID leitet HTTP-Aufrufe von Drittanbietern an den HTTPS-Endpunkt weiter, was zwar die Latenz erhöhen kann, aber auch bedeutet, dass Sie Ihre Konfiguration nicht ändern müssen.

Adobe empfiehlt, sicherzustellen, dass alle Seiten Ihrer Site mit HTTPS bereitgestellt werden.

### Ein CNAME für mehrere Domänen

Wenn Sie über eine CNAME-Implementierung verfügen, die in derselben Domäne wie Ihre Website festgelegt ist, handelt es sich um einen Erstanbieter-Cookie-Kontext, an dem Sie keine Änderungen vornehmen müssen.

Wenn Sie jedoch über mehrere Domänen verfügen und denselben CNAME für die Datenerfassung in all Ihren Domänen verwenden, wird er in diesen anderen Domänen als Drittanbieter-Cookie behandelt. Mit Chrome 80 ist es auf diesen anderen Domänen nicht mehr sichtbar. Damit das Verhalten in allen Browsern ähnlicher wird, setzt Analytics den `SameSite`-Wert dieses Cookies explizit auf `Lax`. Wenn Sie dieses Cookie in einem benutzerfreundlichen Drittanbieterkontext verwenden, muss das Cookie mit dem Wert `SameSite=None` eingestellt sein, was bedeutet, dass Sie immer HTTPS verwenden müssen. Wenden Sie sich an die Adobe-Kundenunterstützung, um den SameSite-Wert für Ihre sicheren CNAMEs zu ändern. Beachten Sie, dass diese Aktion NICHT für Analytics-Kunden erforderlich ist, die ECID verwenden.

## Welche Auswirkungen haben Safari-Änderungen (ITP 2.1) auf Analytics?

Trotz Änderungen in Safari 12.1 werden weiterhin Datensätze aus Adobe Experience Cloud-Cookies erfasst. Cookies sind zwar auf sieben Tage begrenzt, doch Besucher, die innerhalb dieser Zeit zu Ihrer Site zurückkehren, verlängern das Cookie und sorgen so dafür, dass es weitere sieben Tage gültig bleibt. Die Anzahl der Lookback-Fenster und wiederkehrenden Besucher wird möglicherweise für Safari-Traffic reduziert, bis ein Adobe-Update verfügbar ist.

Aufgrund des verkürzten Gültigkeitszeitraums von sieben Tagen kann es bei Kunden zu einem Anstieg der Unique Visitors kommen. Besuchs- und Seitenansichtszahlen sollten nicht betroffen sein. Wenn Sie über eine Site mit saisonalem Traffic verfügen, z. B. Steuerdienstleistungen oder Feiertagssaison im Einzelhandel, erleben Sie möglicherweise eine höhere Auswirkung, da entsprechende Besucher nicht zwischen den Jahreszeiten verbunden sind.

Wenn Sie einen CNAME verwenden, speichert der Besucher-ID-Dienst die ECID in einem Server-seitigen Erstanbieter-Cookie. Auf diese Weise kann das Cookie für die gesamte Dauer beibehalten werden.

**Hinweis: ITP 2.1 gilt nicht für eingebettete Browser in Apps.**

### Betroffene Erstanbieter-Cookies

Erstanbieter-Cookies, die durch `document.cookie` erstellt werden, sind betroffen. Wenn Sie diese Cookies über HTTP-Antworten (Server-seitig) oder CNAME-Zertifizierung setzen, sind Sie von den Änderungen in ITP 2.1 nicht betroffen. Die folgenden Erstanbieter-Cookies und zugehörige Adobe-JavaScript-Bibliotheken sind betroffen:

* AMCV-Cookies, die von der ECID-Dienstbibliothek (Experience Cloud ID) festgelegt werden
* Altes Analytics-Ausweich-Cookie `s_fid`

Das alte Analytics-Cookie `s_vi` wird als Drittanbieter-Cookie, einschließlich Erfassungszielen von 2o7.net oder omtrdc.net, basierend auf früheren Versionen von ITP weiterhin blockiert.

Zusammenfassung:

* Wenn Sie einen CNAME verwenden und den Besucher-ID-Dienst verwenden, ist Ihre Implementierung nicht betroffen.

* Wenn Sie im Erstanbieterkontext einen Erstanbieter-CNAME, aber nicht den Besucher-ID-Dienst verwenden, ist Ihre Implementierung nicht betroffen.

* Wenn Sie eine Erstanbieter-Cookie-Domäne im Drittanbieterkontext oder mit den standardmäßigen Drittanbieter-Domänennamen (z. B. 2o7.net, omtrdc.net usw.) verwenden, blockiert Safari sie weiterhin wie bisher.

* Wenn Sie eine benutzerspezifische Besucher-ID verwenden, ist es entscheidend, wie Ihre Besucher-ID gespeichert wird. Wenn Sie Ihre ID in einem Client-seitigen Erstanbieter-Cookie speichern, gilt die Gültigkeit von sieben Tagen. Wenn Sie Ihre benutzerspezifische ID auf andere Weise speichern, müssen Sie überprüfen, ob Sie betroffen sind.

### Am wenigsten betroffene Datensätze

Datensätze mit aktiven Besuchern, die häufig zurückkehren, sind am wenigsten von den Änderungen betroffen. Wenn der Inhalt Ihrer Site so gestaltet ist, dass Kunden täglich oder mindestens mehrmals in der Woche zurückkehren, werden die Cookies für diese aktiven Anwender vor Ablauf der Gültigkeit verlängert. Soziale Netzwerke, Nachrichten- und andere Medien-Sites haben wahrscheinlich große Gruppen von Anwendern, die häufig zurückkehren.

Kunden, die `s_vi` als primäre Besucher-ID verwenden und die mit Erstanbieter-Datenerfassung unter Verwendung eines CNAME konfiguriert sind, werden von ITP 2.1 nicht beeinträchtigt. Beachten Sie, dass in Fällen, in denen `s_vi` nicht festgelegt werden kann, möglicherweise das Ausweich-Cookie `s_fid` mit einer Gültigkeit von sieben Tagen verwendet wird.

Am wenigsten betroffen sind auch Datensätze, die den Besucher-ID-Dienst verwenden und eine Erstanbieterdomäne aufweisen.

## Haben Safari-Änderungen Auswirkungen auf mein Geschäft?

Adobe empfiehlt Kunden, die Auswirkungen in ihrem eigenen Unternehmen zu messen, bevor sie Änderungen an der Datenerfassung vornehmen. Dies kann mit den unten in diesem Abschnitt beschriebenen Methoden erfolgen.

Um die Auswirkungen auf Reporting und Tests zu messen, müssen Sie wissen, welche Art von Besucher- und Cookietracking Sie implementiert haben und wie viel Traffic von Anwendern mit Safari stammt. Berücksichtigen Sie die folgenden Punkte, um die Auswirkungen auf Ihr Geschäft zu messen:

* Überprüfen Sie, welche Cookie-Typen von Ihren Adobe-Bibliotheken festgelegt werden.

* Öffnen Sie Ihre Entwicklerkonsole im neuesten Safari-Browser. Wenn eines der oben aufgeführten Cookies in Ihrer Erstanbieterdomäne eingestellt ist, können die Änderungen Sie betreffen.

* Wenn ein `s_vi`-Cookie, aber kein im Kontext eines CNAME eingestelltes `AMCV`-Cookie angezeigt wird, verwenden Sie einen CNAME zur Besucheridentifizierung und Ihre Analytics-Nutzung ist von diesen Änderungen nicht betroffen. Wenn sowohl ein `s_vi`- als auch ein `AMCV`-Cookie im Kontext eines CNAME gesetzt werden, verwenden Sie in letzter Zeit oder derzeit eine Übergangsphase und ein Teil Ihres Analytics-Traffics ist möglicherweise betroffen.

* Verwenden Sie Analytics, um den Prozentsatz der Besucher zu messen, die nicht innerhalb von sieben Tagen zurückkehren. Wenn Ihre Besucher innerhalb von sieben Tagen wiederholt zurückkehren, wird Ihr Traffic möglicherweise nicht wesentlich beeinträchtigt. Anleitungen zur Verwendung von Analytics, um dies herauszufinden, finden Sie unter [Auswirkungen von Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

* Messen Sie Ihren Traffic-Prozentsatz von Safari-Browsern, um festzustellen, ob Änderungen ausreichend gerechtfertigt sind. Anweisungen zur Verwendung von Analytics, um den Prozentsatz des Safari-Traffics auf Ihren Sites zu ermitteln, finden Sie unter [Auswirkungen von Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Welche Browser verwenden meine Besucher am häufigsten?

Wenn Sie mehr über die von Besuchern verwendeten Browser erfahren möchten, können Sie mithilfe der Analytics-Dimension [Browser](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/browser.html) ermitteln, welche Browser für Ihre Sites am häufigsten verwendet werden. Sie können Analytics-Dimensionen auch verwenden, um zu sehen, welche Browser je nach geografischen Regionen am häufigsten verwendet werden. Weitere Informationen finden Sie unter [GeoSegmentation](https://docs.adobe.com/content/help/de-DE/analytics/components/dimensions/countries.html).

Laut [Statcounter](https://gs.statcounter.com/browser-market-share/all) erreichten die einzelnen Browser Ende 2019 folgende Marktanteile:

* Chrome: ca. 64 %
* Safari: ca. 17 %
* Firefox: ca. 4 %
* Edge: ca. 2 %

Wenn sich der Marktanteil ändert, können Sie Ihre Implementierungsstrategie anhand solcher [Statistiken](https://gs.statcounter.com/browser-market-share/all) überprüfen.

## Wie kann ich am besten kurzfristig mit den Änderungen von ITP 2.1 in Safari umgehen?

Das Adobe-Programm für CNAME und verwaltete Zertifikate wird verwendet, um mit ITP-Änderungen umzugehen. Mit diesem Programm können Sie ohne zusätzliche Kosten ein neues Erstanbieterzertifikat für Erstanbieter-Cookies implementieren. Heute bietet Adobe verschiedene lösungsbasierte CNAME-Dienste an und versucht kurzfristig, das Analytics-Zertifizierungsprogramm zu nutzen.

Jeder aktuelle Analytics-Kunde mit einem CNAME-Setup, der auch Experience Cloud ID Services zur Besucheridentifizierung verwendet, kann ein künftiges Update der ECID-Bibliothek nutzen. Durch diese Änderung können CNAME-zertifizierte Trackingserver die ECID verwalten und als Referenz für die Besucheridentifizierung verwendet werden. Weitere Informationen sind in aufeinanderfolgenden Versionen der ECID-Bibliothek verfügbar.

Adobe ist bekannt, dass nicht alle Kunden der ECID-Bibliothek CNAMEs oder Analytics verwenden. Allen ECID-Kunden wird ein CNAME-Setup angeboten, um die gleiche Funktionalität zu erreichen.

Wenn Sie derzeit keinen CNAME für Ihre Implementierung verwenden, können Sie den Prozess durch ein Gespräch mit der Kundenunterstützung einleiten.

## Welche Pläne verfolgt Adobe in Zukunft für eine beständige Besucheridentifizierung?

Zu den neuen Funktionen und Implementierungen gehören:

* Self-Service-Optionen zur CNAME-Zertifizierung in allen Adobe-Lösungen

* Flexible Datenerfassungsmethoden für Besucher-IDs, BYOI (Bring Your Own Identity) und API-basierter Datenerfassung

* Identitätsdiagramme von Adobe Experience Platform

* Einheitlicher Ansatz bei der Adobe-Datenerfassung

Adobe setzt sich für eine präzisere Personalisierung für Kunden ein, die individuelle Erlebnisse anbieten möchten. Adobe bemüht sich, unseren Kunden eine Online-Identitätsfunktion anzubieten, mit der sie sich an die Datenschutzentscheidungen ihrer Kunden anpassen können.

## Weitere Informationen

Weitere Informationen finden Sie unter:

* [Adobe Experience Cloud: Cookie-Updates für Google Chrome](https://medium.com/adobetech/adobe-experience-cloud-cookie-updates-for-google-chrome-19ad67cf1598)

* [Auswirkungen von Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac)
