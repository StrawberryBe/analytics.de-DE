---
description: Cookies in Analytics
title: Häufig gestellte Fragen zu Browser- und Analytics-Cookies
uuid: null
translation-type: tm+mt
source-git-commit: 38de617d3c77195d2308e14783962f6690b4b3fc

---


# Häufig gestellte Fragen zu Browsern und Analytics-Cookies

Um eine dauerhafte Benutzeridentifizierung über Eigenschaften und Lösungen hinweg zu unterstützen, reagiert Adobe Analytics auf Änderungen bei der Behandlung von Cookies in Browsern. Die folgenden häufig gestellten Fragen enthalten Informationen darüber, wie die beständige Besucheridentifizierung bei Änderungen am Browser-Cookie beibehalten wird.

## Wie ändern Browser die Art und Weise, wie sie Cookies handhaben?

Im Allgemeinen werden die meisten Browser bei der Speicherung von Drittanbieter-Cookies immer restriktiver. Dies kann sich auf die Verfolgung auswirken, wenn das Cookie vom Browser gelöscht oder abgelehnt wird. Der Safari-Browser legt außerdem einige Einschränkungen für einige Erstanbieter-Cookies fest.

Die folgende Liste zeigt einige Änderungen, die je nach Browser vorgenommen wurden:

* Chrome: Ab Chrome 80 wird das `SameSite` Attribut anders behandelt, um Drittanbieter-Cookies oder Site-übergreifende Anforderungen zu verwalten. Letztlich suchen Chrome-Entwickler nach Möglichkeiten, Drittanbieter-Cookies [komplett zu veraltet](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html?m=1) .

* Firefox und Edge: Produktankündigungen besagen, dass die verschiedenen Versionen der Browser dieselben Änderungen wie in Chrome 80 vornehmen müssen.

* Safari: With [Safari 12.1](https://webkit.org/blog/category/privacy/), first party persistent cookies set through the document.cookie API, often known as “client-side” cookies, have their expiration capped at seven days.

## Was ist der Unterschied zwischen Drittanbieter-Cookies und Erstanbieter-Cookies?

### Erstanbieter-Cookies

Erstanbieter-Cookies werden von Kunden-Websites (domänenspezifisch) erstellt und in Clientbrowsern gespeichert, wenn Benutzer Kunden-Websites besuchen. Alle Browser akzeptieren in der Regel Erstanbieter-Cookies. Bei einer Analytics-Implementierung von Erstanbieter-Cookies wird das Besucher-ID-Cookie an einem Adobe-Knoten erstellt, wenn der Hostname mithilfe eines [CNAME](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html)mit der Domäne abgeglichen wird. Das Cookie wird dann vom Browser in einem Erstanbieterkontext akzeptiert. Weitere Informationen finden Sie unter [Informationen zu Erstanbieter-Cookies](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html).

### Drittanbieter-Cookies

Drittanbieter-Cookies werden nicht von Websites erstellt, die Benutzer besuchen. Obwohl Browser derzeit alle Drittanbieter-Cookies gleich behandeln und entsprechend speichern, können sich Drittanbieter-Cookies selbst auf unterschiedliche, wichtige Weise verhalten. Bei der Analytics-Drittanbieter-Cookie-Implementierung eines Kunden ruft der Client nur Adobe an und nicht unbekannte oder verdächtige Drittanbieterdomänen. Dies ist die aktuelle Methode zur Implementierung von Analytics für sichere (HTTPS) und zuverlässige Verfolgung mit beständigen Bezeichnern. Diese Methode wird durch Konfiguration der Datei AppMeasurement.js implementiert. Weitere Informationen finden Sie unter [Cookies und Experience Platform Identity Service](https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html).

![Cookie-Unterschiede](assets/cookieimage.PNG)

## Wie speichern und verwalten Browser derzeit Analytics-Cookies?

Je nach Implementierung werden Analytics-Cookies wie folgt gespeichert:

### Drittanbieter-Cookie-Implementierungen

Browser speichern die Adobe [demdex.net](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/demdex-calls.html) -ID derzeit als Drittanbieter-Cookie. Dieses Cookie stellt domänenübergreifende IDs bereit und ermöglicht sicheren (https) Inhalt.

### Erstanbieter-Cookie-Implementierungen

Durch die Konfiguration eines CNAME können Ihre Benutzer Adobe-Cookies in einem Erstanbieter-Cookie-Kontext für ihre Browser empfangen. Dies kann eine praktikable Option sein, wenn eine Drittanbieter-Cookie-Implementierung für Ihre Benutzer nicht optimal ist.

## Welches ist das SameSite-Cookie-Attribut und wie wirkt es sich auf Analytics aus?

Mit der Veröffentlichung des Chrome 80-Browsers - und den anschließenden Versionen von Firefox und Edge-Browsern - erzwingt das Attribut SameSite-Cookie die Spezifikation für drei verschiedene Werte zur Steuerung des Verhaltens von Site-übergreifender Anforderung, wie folgt:

* `None`: Diese Einstellung ermöglicht den Site-übergreifenden Zugriff und ermöglicht die Weitergabe von Cookies in einem Drittanbieterkontext. Um dieses Attribut anzugeben, müssen Sie auch angeben `Secure` und alle Browseranforderungen müssen HTTPS folgen. Wenn Sie beispielsweise das Cookie setzen, verbinden Sie die Werte des Attributs wie folgt: `Set-Cookie: example_session=test12; SameSite=None; Secure`. Wenn die Cookies nicht richtig beschriftet sind, sind sie für die neueren Browser nicht verwendbar und werden abgelehnt.

* `Lax`: Ermöglicht das Senden von Site-übergreifenden Anforderungen mit Cookies derselben Site nur für Navigation auf oberster Ebene mit *sicheren* (schreibgeschützten, wie `GET`) HTTP-Methoden.

* `Strict`: Das gleiche Site-Cookie wird nicht für Website-Anfragen von Drittanbietern gesendet. Das Cookie wird nur gesendet, wenn die Site für das Cookie mit der Site in der URL-Leiste übereinstimmt.

Das Standardverhalten in diesen Browserversionen besteht darin, Cookies zu behandeln, die kein bestimmtes `SameSite` Attribut haben, das gleiche wie `SameSite=Lax`.

## Wie reagiert Adobe Analytics auf diese Änderungen?

Alle Adobe-Cookie-Updates werden über Adobe-Server verarbeitet und Adobe hat seine Edge-Server aktualisiert, um die entsprechenden Cookie-Attribute festzulegen. Adobe hat serverseitige Updates veröffentlicht, um Cookies von Drittanbietern mit den entsprechenden Attributen festzulegen. Für Ihre Sites sind keine JavaScript-Aktualisierungen erforderlich.

Diese Aktualisierung durch Adobe Edge-Server erfolgt automatisch, wenn Benutzer eine Website besuchen, auf der das Cookie verwendet wird. Bei den meisten Adobe-Produkten verfügen Cookies über die entsprechenden Flags, da Chrome 80 veröffentlicht wird. Eine Ausnahme bilden Adobe Analytics-Implementierungen, bei denen die Datenerfassung von Drittanbietern und nicht der Experience Cloud-Identitätsdienst (ECID) verwendet werden. Bei diesen Kunden kann es zu einem geringfügigen vorübergehenden Anstieg neuer Besucher kommen, die sonst als wiederkehrende Besucher gekennzeichnet wären.

Bei Browsern, die Google als falsch gehandhabt hat, wenn sie auf `SameSite`eingestellt `None` sind, bleibt `SameSite` die Einstellung deaktiviert.

Die folgende Tabelle fasst Analytics-Cookies zusammen:


![Analytics-Cookie-Tabelle](assets/cookie_table.png)


## Wie kann ich meine Site am besten auf Chrome-, Firefox- und Edge-Änderungen vorbereiten?

Analytics-Kunden sollten bestätigen, dass ihre JavaScript-Konfiguration HTTPS für ihre Aufrufe an Adobe-Dienste verwendet. ECID leitet HTTP-Aufrufe von Drittanbietern an den HTTPS-Endpunkt weiter, was die Latenz erhöhen kann, was bedeutet, dass Sie Ihre Konfiguration nicht ändern müssen.

Adobe empfiehlt, sicherzustellen, dass alle Seiten Ihrer Site mit HTTPS versorgt werden.

### Ein CNAME für mehrere Domänen

Wenn Sie über eine CNAME-Implementierung verfügen, die in derselben Domäne wie Ihre Website festgelegt ist, handelt es sich um einen Erstanbieter-Cookie-Kontext, an dem Sie keine Änderungen vornehmen müssen.

Wenn Sie jedoch über mehrere Domänen verfügen und denselben CNAME für die Datenerfassung in allen Ihren Domänen verwenden, wird er in diesen anderen Domänen als Drittanbieter-Cookie behandelt. Mit Chrome 80 ist es auf diesen anderen Domänen nicht mehr sichtbar. Damit das Verhalten in allen Browsern ähnlicher wird, setzt Analytics den `SameSite` Wert dieses Cookies explizit auf `Lax`. Wenn Sie dieses Cookie in einem benutzerfreundlichen Drittanbieterkontext verwenden, müssen Sie das Cookie mit dem `SameSite=None` Wert setzen, was bedeutet, dass Sie immer HTTPS verwenden müssen. Wenden Sie sich an den Adobe-Kundendienst, um den Wert von SameSite für Ihre sicheren CNAMEs zu ändern. Beachten Sie, dass diese Aktion NICHT für Analytics-Kunden erforderlich ist, die ECID verwenden.

## Welche Auswirkungen haben Safari-Änderungen (ITP 2.1) auf Analytics?

Trotz Änderungen in Safari 12.1 werden weiterhin Datensätze aus Adobe Experience Cloud-Cookies erfasst. Obwohl Cookies auf sieben Tage begrenzt sind, verlängern Besucher, die innerhalb dieser Zeit zu Ihrer Eigenschaft zurückkehren, das Cookie und verhindern, dass es für weitere sieben Tage abläuft. Die Anzahl der Lookback-Fenster und rückkehrenden Besucher kann für Safari-Traffic reduziert werden, bis ein Adobe-Update verfügbar ist.

Aufgrund des verkürzten Ablauffensters von sieben Tagen kann es bei Kunden zu einem Anstieg der Unique Visitors kommen. Besuchs- und Seitenansichtszahlen sollten nicht betroffen sein. Wenn Sie eine Immobilie mit saisonalem Traffic haben, z. B. Steuerdienstleistungen oder Urlaubsvertrieb, sehen Sie möglicherweise eine höhere Auswirkung, da dieser Besucher nicht zwischen den Jahreszeiten verbunden ist.

Wenn Sie einen CNAME verwenden, speichert der Besucher-ID-Service die ECID in einem serverseitigen Erstanbieter-Cookie. Auf diese Weise kann das Cookie für die gesamte Dauer beibehalten werden.

**Hinweis: ITP 2.1 gilt nicht für eingebettete Browser in mobilen Apps.**

### Betroffene Erstanbieter-Cookies

Erstanbieter-Cookies, die durch erstellt `document.cookie` werden, sind betroffen. Wenn Sie diese Cookies über HTTP-Antwort (serverseitig) oder CNAME-Zertifizierung setzen, sind Sie von den Änderungen in ITP 2.1 nicht betroffen. Die folgenden Erstanbieter-Cookies und zugehörige Adobe JavaScript-Bibliotheken sind betroffen:

* AMCV-Cookies, die von der ECID-Dienstbibliothek (Experience Cloud ID) eingestellt werden
* Analytics-Legacy-Ausweichcookie `s_fid`

Analytics-Legacy- `s_vi` -Cookies als Drittanbieter-Cookie, einschließlich Erfassungszielgruppen von 2o7.net oder omtrdc.net, werden weiterhin basierend auf früheren Versionen von ITP blockiert.

Zusammenfassung:

* Wenn Sie einen CNAME haben und den Besucher-ID-Service verwenden — Ihre Implementierung wird davon nicht betroffen sein.

* Wenn Sie im Erstanbieterkontext einen Erstanbieter-CNAME verwenden und nicht den Besucher-ID-Service verwenden — Ihre Implementierung wird davon nicht betroffen sein.

* Wenn Sie eine Erstanbieter-Cookie-Domäne im Drittanbieterkontext oder mit den standardmäßigen Drittanbieter-Domänennamen (z. B. 2o7.net, omtrdc.net usw.) verwenden, blockiert Safari sie weiterhin wie bisher.

* Wenn Sie eine benutzerdefinierte Besucher-ID verwenden — Dies hängt davon ab, wie Ihre Besucher-ID gespeichert wird. Wenn Sie Ihre ID in einem &quot;clientseitigen&quot; Erstanbieter-Cookie speichern, gilt der Ablauf von sieben Tagen. Wenn Sie Ihre benutzerdefinierte ID auf andere Weise speichern, müssen Sie prüfen, ob Sie davon betroffen sind.

### Am wenigsten betroffene Datensätze

Datensätze mit aktiven Besuchern, die häufig zurückkehren, sind am wenigsten von den Änderungen betroffen. Wenn der Inhalt Ihrer Site so gestaltet ist, dass Kunden täglich oder mindestens mehrmals in der Woche zurückkehren, werden die Cookies für diese aktiven Benutzer vor Ablauf erneuert. Soziale Netzwerke, Nachrichten- und andere Medien-Sites haben wahrscheinlich große Gruppen von Benutzern, die häufig zurückkehren.

Kunden, die `s_vi` als primäre Besucher-ID verwenden und bei der Datenerfassung durch Erstanbieter mit einem CNAME konfiguriert sind, werden von ITP 2.1 nicht beeinträchtigt. Beachten Sie, dass in Fällen, in denen `s_vi` kein Ausweichcookie gesetzt werden kann, das Ausweichcookie verwendet werden `s_fid` kann und einen Ablauf von sieben Tagen hat.

Am wenigsten betroffen sind auch Datensätze, die den Besucher-ID-Service verwenden und eine Erstanbieterdomäne haben.

## Haben Safari-Änderungen Auswirkungen auf mein Geschäft?

Adobe empfiehlt Kunden, die Auswirkungen in ihrem eigenen Unternehmen zu messen, bevor sie Änderungen an der Datenerfassung vornehmen. Dies kann mit den unten in diesem Abschnitt beschriebenen Methoden erfolgen.

Um die Auswirkungen auf die Berichterstellung und das Testen zu messen, müssen Sie wissen, welche Art von Besucher- und Cookie-Verfolgung Sie implementiert haben und wie viel Traffic Sie von Benutzern mit Safari haben. Berücksichtigen Sie die folgenden Punkte, um die Auswirkungen auf Ihr Geschäft zu messen:

* Überprüfen Sie, welche Cookie-Typen von Ihren Adobe-Bibliotheken eingestellt werden.

* Öffnen Sie Ihre Entwicklerkonsole in Ihrem neuesten Safari-Browser. Wenn eines der oben aufgeführten Cookies in Ihrer Erstanbieterdomäne eingestellt ist, können diese Änderungen Sie betreffen.

* Wenn ein `s_vi` Cookie, aber kein im Kontext eines CNAME eingestelltes `AMCV` Cookie angezeigt wird, verwenden Sie einen CNAME zur Besucheridentifizierung, und Ihre Analytics-Nutzung wird von diesen Änderungen nicht beeinflusst. Wenn sowohl ein `s_vi` Cookie als auch ein `AMCV` Cookie im Kontext eines CNAME gesetzt werden, verwenden Sie in letzter Zeit oder derzeit eine Übergangsphase, und ein Teil Ihres Analytics-Traffics kann betroffen sein.

* Verwenden Sie Analytics, um den Prozentsatz der Besucher zu messen, die nicht innerhalb von sieben Tagen zurückkehren. Wenn Ihre Besucher innerhalb von sieben Tagen wiederholt zurückkehren, wird Ihr Traffic möglicherweise nicht wesentlich beeinträchtigt. Anleitungen zur Verwendung von Analytics, um dies herauszufinden, finden Sie unter Auswirkungen von [Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

* Messen Sie Ihren Traffic-Prozentsatz von Safari-Browsern, um festzustellen, ob Änderungen ausreichend gerechtfertigt sind. Anweisungen zur Verwendung von Analytics, um den Prozentsatz des Safari-Traffics auf Ihren Sites zu ermitteln, finden Sie unter Auswirkungen von [Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Welche Browser verwenden meine Besucher am häufigsten?

Wenn Sie mehr über die von Ihren Besuchern verwendeten Browser erfahren möchten, können Sie mithilfe der Analytics- [Browserdimension](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-browsers.html) ermitteln, welche Browser für Ihre Sites am häufigsten verwendet werden. Sie können Analytics-Dimensionen auch verwenden, um zu sehen, welche Browser je nach geografischen Regionen am häufigsten verwendet werden. For more information, see [GeoSegmentation](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-geosegmentation.html).

Laut [Statistik](https://gs.statcounter.com/browser-market-share/all)betrug der weltweite Marktanteil der einzelnen Browser Ende 2019 für jeden Browser:

* Chrome: ~64 %
* Safari: ~17 %
* Firefox: ~4 %
* Kante: ~2 %

Wenn sich der Marktanteil ändert, können Sie Ihre Implementierungsstrategie anhand solcher [Statistiken](https://gs.statcounter.com/browser-market-share/all) überprüfen.

## Wie kann ich am besten kurzfristig mit Änderungen von ITP 2.1 in Safari arbeiten?

Das Adobe-Programm für CNAME und verwaltetes Zertifikat wird verwendet, um mit ITP-Änderungen umzugehen. Mit dem Adobe Managed Certificate-Programm können Sie ohne zusätzliche Kosten ein neues Erstanbieter-Zertifikat für Erstanbieter-Cookies implementieren. Adobe bietet heute lösungsorientierte CNAME-Dienste an und versucht, das Analytics-Zertifizierungsprogramm kurzfristig zu nutzen.

Jeder aktuelle Analytics-Kunde mit einem CNAME-Setup, der auch Experience Cloud ID-Services zur Besucheridentifizierung verwendet, kann eine zukünftige ECID-Bibliotheksaktualisierung nutzen. Durch diese Änderung können CNAME-zertifizierte Tracking-Server die ECID verwalten und als Referenz für die Besucheridentifizierung verwendet werden. Weitere Informationen finden Sie in aufeinander folgenden Versionen der ECID-Bibliothek.

Adobe ist bekannt, dass nicht alle Kunden von ECID-Bibliotheken CNAMES oder Analytics verwenden. Allen ECID-Kunden wird ein CNAME-Setup angeboten, um die gleiche Funktionalität zu nutzen.

Wenn Sie derzeit keinen CNAME für Ihre Implementierung verwenden, können Sie den Prozess mit dem Kundendienst starten.

## Welche Pläne verfolgt Adobe in Zukunft für eine dauerhafte Besucheridentifizierung?

Zu den neuen Funktionen und Implementierungen gehören:

* Selbstbedienungsoptionen für die CNAME-Zertifizierung in allen Adobe-Lösungen

* Flexible Datenerfassungsmethoden für Besucher-IDs, BYOI (mit eigener Identität) und API-erste Datenerfassung

* Identitätsdiagramme für Adobe Experience Platform

* Einheitlicher Ansatz bei der Adobe-Datenerfassung

Adobe setzt sich für eine präzisere Personalisierung von Kunden ein, die ein personalisiertes Erlebnis wünschen. Adobe bemüht sich, unseren Kunden eine Online-Identitätsfunktionalität anzubieten, die ihnen hilft, sich an die Datenschutzentscheidungen ihrer Kunden anzupassen.

## Weitere Informationen

Weitere Informationen:

* [Adobe Experience Cloud: Cookie-Aktualisierungen für Google Chrome](https://medium.com/adobetech/adobe-experience-cloud-cookie-updates-for-google-chrome-19ad67cf1598)

* [Auswirkungen von Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac)

