---
description: Implementieren Sie das AMP-Projekt (Accelerated Mobile Pages) in Adobe Analytics.
keywords: Analytics Implementation;amp;amp-analytics;adobeanalytics template;adobeanalytics_nativeConfig template;click tracking;visitor inflation;id service
title: Accelerated Mobile Pages
topic: Developer and implementation
uuid: c86e4a80-7191-4ee7-ab20-787730026c4b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Accelerated Mobile Pages

Implementieren Sie das AMP-Projekt (Accelerated Mobile Pages) in Adobe Analytics.

AMP ist ein [Open-Source-Projekt](https://www.ampproject.org/). Es ermöglicht Ihnen das Erstellen von Websites für statischen Inhalt, der schnell gerendert wird. Diese Funktion eignet sich hervorragend für Publisher, die für Mobilgeräte optimierte Inhalte einmal erstellen und dann sofort an jeden beliebigen Ort laden möchten. Abgedeckte Themen:

* [Funktionsweise](/help/implement/js-implementation/accelerated-mobile-pages.md#section_21C2836D63104794BCEBEECB6593AFBF)
* [Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics“](/help/implement/js-implementation/accelerated-mobile-pages.md#section_2E4EBF4EF623440D95DE98E78C47244E)
* [Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics_nativeConfig“](/help/implement/js-implementation/accelerated-mobile-pages.md#section_3556B68304A4492991F439885727E9FF)
* [Zusammenfassung](/help/implement/js-implementation/accelerated-mobile-pages.md#section_4D8ED26084F249738A5C2BC66B933A07)
* [Häufig gestellte Fragen](/help/implement/js-implementation/accelerated-mobile-pages.md#section_5F57AA2DE0C5452FB65241058A924C73)

**Zusätzliche Dokumentation und Beispiele**

* [Dokumentation](https://www.ampproject.org/docs/get_started/about-amp.html) zu externen Open-Source-AMP-Projekten
* [Beispiele](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web/amphtml) zur Einrichtung

## Funktionsweise {#section_21C2836D63104794BCEBEECB6593AFBF}

AMPs verfügen über speziell getaggte HTML-Seiten, die im Web auf verschiedenen Inhaltsbereitstellungsnetzwerken (Content Delivery Networks, CDNs) teilnehmender Technologiepartner und Herausgeber zwischengespeichert werden. So kann AMP-Inhalt aus der nächstmöglichen Quelle mit der geringstmöglichen Latenz bereitgestellt werden. Dadurch ergeben sich einige Herausforderungen an die Analyse, da Sie nie ganz sicher wissen, wo der Inhalt eines Herausgebers geladen wird, und externe Cookies die Besucheridentifikation erschweren.

Um eine deutlich reduzierte Seitenbreite und schnellere Seitenladezeit zu erzielen, beschränken AMPs die Nutzung von JavaScript und Cookies. Dies ist von Vorteil für Ihr Mobilgerät, da es deutlich weniger verarbeiten muss. Jedoch wird es immer schwieriger, einzelne Besucher korrekt zu messen und die Benutzerakquise und -bindung in Erfahrung zu bringen.

Um diese Probleme zu lösen, hat Adobe mit AMP-Partnern und -Herausgebern zwei Optionen entwickelt, zwischen denen Herausgeber je nach Geschäftsanforderungen wählen können. Beide verwenden das `amp-analytics`-Tag. Beim ersten Ansatz wird die Tracking-Vorlage `"adobeanalytics"` verwendet, um die Analytics-Anfrage direkt im AMP zu konstruieren. Beim zweiten Ansatz wird die Tracking-Vorlage `"analytics_nativeConfig"` verwendet, die einen iframe mit dem AppMeasurement-Code nutzt, den Sie auf Ihrer regulären Site bereitstellen. In der folgenden Tabelle sind die Vor- und Nachteile der beiden Ansätze aufgeführt.

|  | **„adobeanalytics“-Vorlage** | **„adobeanalytics_nativeConfig“-Vorlage**  |
|---|---|---|
| Besucher/Besucherzahl (in vorhandener Report Suite) | Hohe Inflation | Minimale Inflation |
| Verwenden einer separaten Report Suite | Empfohlen | Nicht erforderlich |
| Neue vs. wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Service | Nicht unterstützt | Unterstützt |
| Video- &amp; Link-Tracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeitsgrad der Implementierung | Eher schwierig | Relativ einfach |
| [!DNL Experience Cloud] Integrationen | Nicht unterstützt | Mit Einschränkungen unterstützt |

## Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics“ {#section_2E4EBF4EF623440D95DE98E78C47244E}

Die Tracking-Vorlage `"adobeanalytics"` nutzt das `amp-analytics`-Tag zur direkten Konstruktion einer Tracking-Anforderung. Wenn Sie die Vorlage `"adobeanalytics"` im `amp-analytics`-Tag verwenden, können Sie Anforderungen als Auslöser für bestimmte Seitenereignisse festlegen, z. B. dass die Seite durch einen Klick angezeigt wird (Videoanzeige etc. werden zukünftig folgen). Klickereignisse können zum Anwenden bestimmter Element-IDs oder -Klassen angepasst werden, indem eine Auswahl festgelegt wird. Adobe hat diese Einrichtung mit der Vorlage `"adobeanalytics"`, die speziell für [!DNL Adobe Analytics] entwickelt wurde, stark vereinfacht. Sie können die Vorlage laden, indem Sie `type="adobeanalytics"` zum amp-analytics-Tag hinzufügen.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der Auslöser `pageLoad` sorgt dafür, dass das Dokument angezeigt wird und dabei die Variable `pageName` wie in `vars section` definiert enthält. Der zweite Auslöser `click` erfolgt beim Klick auf eine Schaltfläche. Für `eVar 1` wird bei diesem Ereignis der Wert `button clicked` festgelegt.

```
  <amp-analytics type="adobeanalytics"> 
  <script type="application/json"> 
  { 
        "requests": { 
      "myClick": "${click}&v1=${eVar1}", 
  }, 
  "vars": { 
      "host": "metrics.example.com", 
      "reportSuites": "reportSuiteID", 
      "pageName": "Adobe Analytics Using amp-analytics tag" 
  }, 
    "triggers": { 
      "pageLoad": { 
        "on": "visible", 
        "request": "pageView" 
      }, 
      "click": { 
        "on": "click", 
        "selector": "button", 
        "request": "myClick", 
        "vars": { 
          "eVar1": "button clicked" 
        } 
      } 
    } 
  } 
  </script> 
  </amp-analytics> 
```

Im `click`-Auslöser können Sie eine Auswahl festlegen, um sicherzustellen, dass bei jedem Klick auf das spezifische DOM-Element (in diesem Fall jede Schaltfläche) die `buttonClick`-Anforderung ausgelöst und automatisch zum Markieren dieses Vorgangs als Nicht-Anzeige-Ereignis (d. h. `trackLink`-Aufruf) festgelegt wird.

Zudem unterstützt `amp-analytics` eine Anzahl von Variablenersetzungen, sodass AMP bekannte Datenwerte bereitstellen kann. Weitere Informationen zu diesem und weiteren Themen finden Sie in der [Dokumentation zur amp-analytics-Variablen](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md).

Hinweis: Wenn Sie Technologie- oder DOM-Variablen (z. B. Browser, Bildschirmgröße, Gerät, Referrer usw.) einbinden möchten, müssen Sie diese jeder Anforderung explizit hinzufügen, da sie nicht automatisch für Sie generiert werden. Die Dokumentation zu den einzelnen verfügbaren Abfragezeichenfolgeparametern, die zum Tracking verwendet werden, finden Sie [hier](https://marketing.adobe.com/resources/help/en_US/sc/implement/query_parameters.html).

Beim Prüfen der durch amp-analytics erzeugten Ergebnisse werden Sie feststellen, dass Adobe den `vid`-Abfrageparameter eingebunden hat. Wir setzen `vid` auf Basis einer integrierten AMP-Funktion fest, um eine benutzerdefinierte Analytics-Cookie-ID namens `adobe_amp_id` festzulegen. Diese ID hängt nicht mit anderen IDs zusammen, die an anderer Stelle von [!DNL Adobe Analytics] festgelegt wurden (z. B. `s_vi cookie`), und erstellt neue Besucher in jeder Report Suite, an die die Ergebnisse gesendet werden.

Sie müssen einige Einschränkungen beachten. Wenn der amp-analytics-Tag wie oben aufgeführt verwendet wird, sind Besucher von Ihrem normalen Tracking unabhängig, und da das AMP in jedem beliebigen Inhaltsbereitstellungsnetzwerk geladen werden kann, erhalten Sie einen einzelnen Besucher für jedes CDN, in dem dieses AMP einem Besucher angezeigt wird (die zuvor erwähnte Besucherinflation). Wenn Sie die `"adobeanalytics"`-Vorlage für `amp-analytics` verwenden, empfiehlt Adobe daher, Ihre Daten in einer separaten Report Suite speziell für das AMP abzulegen. Der [!DNL Experience Cloud] ID-Service (früher *`visitor ID service`*) wird bei dieser Methode nicht unterstützt, wenn Ihr Unternehmen also jetzt oder in Zukunft zusätzliche [!DNL Experience Cloud]-Integrationen benötigt, ist dies wahrscheinlich nicht die beste Option für Sie.

Der letzte und wohl wichtigste Punkt ist, dass bei dieser `amp-analytics`-Lösung der von Ihnen im Abschnitt `vars` festgelegte Tracking-Server dem Tracking-Server auf Ihrer Haupt-Site entsprechen muss, damit Ihre Datenschutzrichtlinien respektiert werden. Andernfalls müssen Sie separate Datenschutzrichtlinien für AMPs erstellen.

## Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics_nativeConfig“ {#section_3556B68304A4492991F439885727E9FF}

Das `"adobeanalytics_nativeConfig"`-Tag ist einfacher zu implementieren, da es dieselbe Tagging-Methode wie auf Ihren normalen Websites nutzt. Fügen Sie dazu Folgendes zu Ihrem `amp-analytics`-Tag hinzu:

```
<amp-analytics type="adobeanalytics_nativeConfig"> 
 <script type="application/json"> 
 { 
  "requests": { 
   "base": "https://${host}", 
   "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}" 
  }, 
  "vars": { 
   "host": "statshost.publishersite.com" 
  }, 
  "extraUrlParams": { 
   "pageName": "Adobe Analytics Using amp-analytics tag", 
   "v1": "eVar1 test value" 
  } 
 } 
 </script> 
</amp-analytics>  
```

Bei diesem Ansatz werden Daten über spezielle Abfragezeichenfolgeparameter, die dem `iframeMessage`-Abfrageparameter hinzugefügt werden, an eine Dienstprogramm-Website gesendet. Beachten Sie, dass wir in diesem Fall die Variable `ampdocUrl AMP` und den `documentReferrer` zur `pageURL` der Abfragezeichenfolgeparameter hinzugefügt haben und uns auf die oben erwähnte `iframeMessage`-Anforderung beziehen. Diese zusätzlichen Abfragezeichenfolgeparameter können beliebig benannt werden, wenn Ihre [!DNL stats.html]-Seite (unten angezeigt) so konfiguriert ist, dass sie die entsprechenden Daten daraus erfassen kann.

Die `"adobeanalytics_nativeConfig"`-Vorlage kann zudem Abfragezeichenfolgeparameter hinzufügen, die auf den im `extraUrlParams`-Abschnitt des amp-analytics-Tags aufgeführten Variablen basieren. In diesem Fall können Sie sehen, dass wir die Parameter `pageName` und `v1` festgelegt haben, die von unserer [!DNL stats.html]-Seite verwendet werden.

Beachten Sie, dass Sie nicht mehrere `amp-analytics`-Vorlagen gleichzeitig verwenden und die `"adobeanalytics"`-Vorlage sowie die `"adobeanalytics_nativeConfig"`-Vorlage nicht im selben AMP verwenden können. Wenn Sie das versuchen, tritt möglicherweise ein Fehler in der Browserkonsole auf, und Ihre Besucherzahl wird verfälscht.

```
<html> 
<head> 
<title>Stats Test</title> 
<script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script> 
<script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script> 
<html> 
<head> 
<title>Stats Test</title> 
<script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script> 
<script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script> 
</head> 
<body> 
<script> 
var v_orgId = "1234567@PublisherOrg"; 
var s_account = "reportSuite"; 
var s_trackingServer = "metrics.publisher.com"; 
var s_visitorNamespace = "publisherNamespace"; 
var visitor = Visitor.getInstance(v_orgId); 
visitor.trackingServer = s_trackingServer; 
var s = s_gi(s_account); 
s.account = s_account; 
s.trackingServer = s_trackingServer; 
s.visitorNamespace = s_visitorNamespace; 
s.visitor = visitor; 
s.pagename = s.Util.getQueryParam("pageName"); 
s.eVar1=s.Util.getQueryParam("v1"); 
s.campaign=s.Util.getQueryParam("campaign"); 
s.pageURL=s.Util.getQueryParam("pageURL"); 
s.referrer=s.Util.getQueryParam("ref"); 
s.t(); 
</script> 
</body> 
</html> 
```

Wie Sie oben sehen, können Sie Ihre vorhandene [!DNL VisitorAPI.js] und [!DNL AppMeasurement.js] (wie in unserem Beispiel) oder entsprechende Elemente Ihrer vorhandenen Implementierung verwenden bzw. verknüpfen und dann die korrekten Konfigurationsparameter hinzufügen. Um die korrekten Werte in den korrekten Variablen zu erfassen, können Sie die bereitgestellte `s.Util.getQueryParam`-Funktion verwenden, um die über die `iframeMessage`-URL abgerufenen Werte einzugeben und die entsprechenden Variablen wie auf einer regulären Seite festzulegen. If you use tag management software like Adobe's [ [!DNL Dynamic Tag Manager] ](https://www.adobe.com/solutions/digital-marketing/dynamic-tag-management.html), the query string parameters should be straightforward to capture. In diesem Fall wird für `s.pageName` der Wert festgelegt, den wir im Abfragezeichenfolgeparameter `pageName` eingegeben haben. Hier würde der Seitenname also *`Adobe Analytics Example 2`*.

>[!IMPORTANT]
>
>Aufgrund von Einschränkungen für iframes im AMP-Framework muss Ihre [!DNL stats.html]-Seite auf einer separaten Subdomäne der Domäne gehostet werden, auf der das AMP selbst gehostet wird. Das AMP-Framework lässt keine iframes aus derselben Subdomäne zu, in der sich die AMP-Seite selbst befindet. Wird Ihr AMP beispielsweise auf [!DNL amp.example.com] gehostet, sollten Sie Ihre [!DNL stats.html]-Seite in einer separaten Subdomäne wie [!DNL ampmetrics.example.com] oder einer ähnlichen Subdomäne hosten.

Da die Dienstprogrammseite auf Ihrer ursprünglichen Site gehostet wird, sind keine weiteren Schritte erforderlich, damit Ihre vorhandenen Datenschutzrichtlinien in allen AMPs unterstützt werden. Wenn sich ein Endbenutzer also vom Tracking auf Ihrer primären Site abmeldet, so wird das Tracking in all Ihren AMPs ohne weiteres Zutun beendet. Durch die Verwendung dieser Dienstprogrammseite kann das AMP den Adobe [!DNL Experience Cloud] ID-Dienst unterstützen. So können Sie die Messung aus Ihren AMPs in die restliche [!DNL Experience Cloud] integrieren (für gezielte Werbung, beispielsweise mit [!DNL Adobe Audience Manager]).

Wenn Ihr Unternehmen den [!DNL Experience Cloud] ID-Dienst noch nicht verwendet (oder eine Tag Management-Software wie den [!DNL Dynamic Tag Manager] von Adobe einsetzt), können Sie jedoch die [!DNL stats.html]-Seite auf eine beliebige Art mit Tags versehen. Verwenden Sie Ihre vorhandene Implementierung als Referenzpunkt. Der einzige Unterschied zu Ihrer Standardimplementierung besteht darin, dass Sie die entsprechenden Datenpunkte der amp-analytics `iframeMessage`-URL (oder der [!DNL document.URL] von der [!DNL stats.html]-Seite) für die einzelnen Variablen erhalten, die Sie festlegen möchten. Wenn Sie eine der [AMP-spezifischen Variablen](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) (wie oben gezeigt) wie den AMP-Referrer oder die AMP-Seiten-URL verwenden möchten, binden Sie diese wie im oben gezeigten iframeMessage-Objekt ein.

Diese Lösung ist zwar flexibel, jedoch hat sie auch Nachteile. Aufgrund von Einschränkungen in der `amp-analytics``iframeMessage` kann sie nur einmal in einer Seitenladung geladen werden. Somit ist das Link- oder Video-Tracking mit der `"adobeanalytics_nativeConfig"`-Vorlage leider nicht möglich. Zudem müssen einige in der Regel automatisch von unserem [!DNL AppMeasurement]-Code erfassten DOM-Werte wie `referrer` (betrifft die Berichte zu Suchmaschinen-Schlüsselwörtern, Referrern und Referrer-Typen oder enthält einen Tracking-Code einer Marketing-Kampagne) manuell an die `iframeMessage` weitergegeben werden. Dazu verwenden sie beliebige AMP-Variablen, die [verfügbar sind](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md). Daher empfiehlt Adobe, eine benutzerdefinierte Variable mit dem Wert-AMP festzulegen, wenn Sie AMP-Daten in eine vorhandene Report Suite eingeben, damit Sie den AMP-Traffic bei der Anzeige der zuvor erwähnten Berichte herausfiltern können. So sollten Standard-Technologieberichte wie Browser, Gerät, Bildschirmgröße oder Auflösung automatisch funktionieren.

Da der iframe als separate Seite geladen wird und das JavaScript auf dieser Seite vollständig ausführt, ist das AMP nicht so leicht wie vom AMP-Standard beabsichtigt. Dies wirkt sich nicht auf die Seitenladezeit aus (der iframe wird geladen, nachdem die Seite geladen wurde), aber CPU und Netzwerk werden stärker beansprucht als sonst. Dies könnte sich negativ auf das Scrollen auswirken. In der Praxis ist keine große Auswirkung festzustellen, aber wir arbeiten mit Google daran, die Auswirkungen dieses Ansatzes auf das Benutzererlebnis zu minimieren.

## Zusammenfassung {#section_4D8ED26084F249738A5C2BC66B933A07}

Wenn Sie Klick-Tracking benötigen und es Sie nicht stört, dass Besucher separat von Ihrer Site als vollständig neue Besucher gezählt werden, wenden Sie unsere Tracking-Vorlage `"adobeanalytics"` gemäß unserer Empfehlung an und nutzen Sie für die Daten eine *`separate report suite`*. Wenn Sie den [!DNL Experience Cloud] ID-Dienst benötigen, keine Besucher- oder Besuchsinflation wünschen und es Ihnen ausreicht, Analytics nur bei Seitenladung auszulösen, empfehlen wir Ihnen die `"adobeanalytics_nativeConfig"`-Lösung.

Adobe Analytics freut sich, in Zusammenarbeit mit Google und unseren Herausgebern branchenführende Analysefunktionen für Herausgeber im mobilen Web für ein deutlich schnelleres Benutzererlebnis bereitzustellen. Auch wenn diese beiden Lösungen derzeit ihre eigenen Kompromisse bieten, streben wir danach, die beste langfristige Lösung für die steigenden Analyseanforderungen unserer Kunden zu entwickeln.

Durch die schnelle Entwicklung des AMP-Projekts ergeben sich häufig Änderungen. Schauen Sie daher regelmäßig [hier](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web/amphtml) vorbei, um sich über Neuerungen an unseren Beispielen zu informieren. Das hier Gezeigte sollte für den Einstieg reichen, jedoch sollten Sie sich auf Änderungen einstellen, da wir unsere Integrationen weiter verbessern und weitere Herausgeber AMP anpassen werden.

Wenn Sie Fragen oder Probleme haben, wenden Sie sich an Ihren Adobe-Berater oder den Kundendienst.

## Häufig gestellte Fragen {#section_5F57AA2DE0C5452FB65241058A924C73}

<table id="table_9A2ED5E482E8423CB54F99613C04BEA0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Is video tracking available for either the <code> "adobeanalytics" </code> or <code> "adobeanalytics_nativeConfig" </code> template? </p> </td> 
   <td colname="col2"> <p> Leider noch nicht. Der AMP-Standard unterstützt lediglich Auslöser für „visible“, „click“ und „timer“. Spezifische Auslöser für das Video-Tracking, auf die der amp-analytics-Tag hört, werden noch nicht unterstützt. Also, because the <code> "adobeanalytics_nativeConfig" </code> tag can only be loaded once, it is not compatible with video viewing which occurs after the AMP has loaded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sie haben erwähnt, dass die Besucherinflation mit der „<code> adobeanalytics_nativeConfig </code>“-Vorlage in Ihrem Vergleich geringer ausfällt. Was bedeutet das? What would cause visitor inflation in either the <code> "adobeanalytics" </code> or the <code> "adobeanalytics_nativeConfig" </code> solution? </p> </td> 
   <td colname="col2"> <p>The <code> "adobeanalytics" </code> template does not allow Adobe Analytics to set a visitor identification cookie; this means all visits and visitors to your AMP page will be treated as a new and independent visit and visitor in your report suite. </p> <p>The <code> "adobeanalytics_nativeConfig" </code> template, however, allows the Adobe Analytics visitor identification cookie to be set in nearly all cases, except for new visitors using the Safari browser. Das bedeutet, dass Besucher aus Safari, die zuvor noch keine Site eines Herausgebers besucht haben, in den Adobe Analytics-Berichten zu hoch angesetzt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sollte ich eine separate Report Suite für AMPs verwenden? </p> </td> 
   <td colname="col2"> <p>Wenn Sie die adobeanalytics-Vorlage verwenden, empfehlen wir Ihnen aufgrund des Problems mit der Besucher-/Besuchsinflation, eine separate Report Suite für AMPs zu verwenden. Wir werden jedoch auch die JavaScript-Version auf „AMP vX.X“ aus der amp-analytics-Tag-Vorlage festlegen, sodass Sie diesen Traffic bei Bedarf aus einer kombinierten Report Suite herausfiltern können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ist der <span class="keyword">Experience Cloud ID</span>-Dienst? Brauche ich ihn? </p> </td> 
   <td colname="col2"> <p>Der <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/"  >Identitätsdienst</a> (früher <span class="term">Besucher-ID-Dienst</span>) aktiviert die <span class="keyword"> Experience Cloud</span>-Core Services und ermöglicht Integrationen zwischen verschiedenen Adobe <span class="keyword"> Experience Cloud</span>-Lösungen. Wenn Sie über Integrationen mit <span class="keyword">Adobe Audience Manager</span> oder <span class="keyword">Adobe Target</span> verfügen, nutzen Sie diesen Dienst vermutlich. Dieser Dienst ist zudem die Grundlage für viele geplante Funktionen von <span class="keyword">Adobe Analytics</span>. Wenn Sie Unterstützung beim ID-Dienst benötigen oder später benötigen werden, empfehlen wir Ihnen die <code> iframeMessage </code>-Lösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>For the <code> "adobeanalytics_nativeConfig" </code> template, where should I host my utility page? </p> </td> 
   <td colname="col2"> <p>Der AMP-Standard lässt das Laden von iframes aus der exakten Domäne und Subdomäne des AMP nicht zu. Daher empfehlen wir, die Dienstprogrammseite in einer von Ihrer Haupt-Site separaten Subdomäne zu hosten, insbesondere wenn Ihr Unternehmen über ein eigenes CDN verfügt, das auf das Zwischenspeichern von AMPs abzielt. Wählen Sie für maximale Kompatibilität eine Subdomäne wie <span class="filepath">ampmetrics.publisher.com</span>, die vom Speicherort des tatsächlichen AMP-Inhalts getrennt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Besteht hier nicht eine große Ähnlichkeit zu <span class="keyword">Facebook Instant Articles </span>? Wie richte ich <span class="keyword">Adobe Analytics</span> mit Facebook Instant Articles ein? </p> </td> 
   <td colname="col2"> <p> Facebook Instant Articles unterstützt eine ähnliche Lösung wie die oben aufgeführte nativeConfig-Lösung. Die oben erstellte stats.html-Seite kann Ihre Analyseanforderungen für sowohl AMP als auch FIA zugleich erfüllen. Weitere Informationen zur Implementierung des Trackings in FIA finden Sie unter <a href="/help/implement/js-implementation/analytics-facebook-instant-articles.md"  > Facebook Instant Articles </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

