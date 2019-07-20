---
description: Implementieren Sie das AMP-Projekt (Accelerated Mobile Pages) in Adobe Analytics.
keywords: Analytics-Implementierung; amp; amp-analytics; adobeanalytics template; adobeanalytics_ nativeconfig template; Klick-Tracking; Besucherinflation; ID-Dienst
seo-description: Implementieren Sie das AMP-Projekt (Accelerated Mobile Pages) in Adobe Analytics.
seo-title: Accelerated Mobile Pages
solution: Analytics
title: Accelerated Mobile Pages
topic: Entwickler und Implementierung
uuid: c 86 e 4 a 80-7191-4 ee 7-ab 20-787730026 c 4 b
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Accelerated Mobile Pages

Implementieren Sie das AMP-Projekt (Accelerated Mobile Pages) in Adobe Analytics.

AMP ist ein [Open-Source-Projekt](https://www.ampproject.org/). Es ermöglicht Ihnen das Erstellen von Websites für statischen Inhalt, der schnell gerendert wird. Diese Funktion eignet sich hervorragend für Publisher, die für Mobilgeräte optimierte Inhalte einmal erstellen und dann sofort an jeden beliebigen Ort laden möchten. Abgedeckte Themen:

* [Funktionsweise](../../implement/js-implementation/accelerated-mobile-pages.md#section_21C2836D63104794BCEBEECB6593AFBF)
* [Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics“](../../implement/js-implementation/accelerated-mobile-pages.md#section_2E4EBF4EF623440D95DE98E78C47244E)
* [Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics_nativeConfig“](../../implement/js-implementation/accelerated-mobile-pages.md#section_3556B68304A4492991F439885727E9FF)
* [Zusammenfassung](../../implement/js-implementation/accelerated-mobile-pages.md#section_4D8ED26084F249738A5C2BC66B933A07)
* [Häufig gestellte Fragen](../../implement/js-implementation/accelerated-mobile-pages.md#section_5F57AA2DE0C5452FB65241058A924C73)

**Zusätzliche Dokumentation und Beispiele**

* [Dokumentation](https://www.ampproject.org/docs/get_started/about-amp.html) zu externen Open-Source-AMP-Projekten
* [Beispiele](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web/amphtml) zur Einrichtung

## Funktionsweise {#section_21C2836D63104794BCEBEECB6593AFBF}

AMPs verfügen über speziell getaggte HTML-Seiten, die im Web auf verschiedenen Inhaltsbereitstellungsnetzwerken (Content Delivery Networks, CDNs) teilnehmender Technologiepartner und Herausgeber zwischengespeichert werden. So kann AMP-Inhalt aus der nächstmöglichen Quelle mit der geringstmöglichen Latenz bereitgestellt werden. Dadurch ergeben sich einige Herausforderungen an die Analyse, da Sie nie ganz sicher wissen, wo der Inhalt eines Herausgebers geladen wird, und externe Cookies die Besucheridentifikation erschweren. 

Um eine deutlich reduzierte Seitenbreite und schnellere Seitenladezeit zu erzielen, beschränken AMPs die Nutzung von JavaScript und Cookies. Dies ist von Vorteil für Ihr Mobilgerät, da es deutlich weniger verarbeiten muss. Jedoch wird es immer schwieriger, einzelne Besucher korrekt zu messen und die Benutzerakquise und -bindung in Erfahrung zu bringen.

Um diese Probleme zu lösen, hat Adobe mit AMP-Partnern und -Herausgebern zwei Optionen entwickelt, zwischen denen Herausgeber je nach Geschäftsanforderungen wählen können. Beide verwenden das `amp-analytics`-Tag. The first approach uses the `"adobeanalytics"` tracking template to construct the Analytics request directly from within the AMP. The second approach uses the `"analytics_nativeConfig"` tracking template, which uses an iframe containing the AppMeasurement code you deploy on your normal site. In der folgenden Tabelle sind die Vor- und Nachteile der beiden Ansätze aufgeführt.

|  | **„adobeanalytics“-Vorlage** | ** "adobeanalytics_ nativeconfig" template** |
|---|---|---|
| Besucher/Besucherzahl (in vorhandener Report Suite) | Hohe Inflation | Minimale Inflation |
| Verwenden einer separaten Report Suite | Empfohlen | Nicht erforderlich |
| Neue vs. wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Service | Nicht unterstützt | Unterstützt |
| Video- &amp; Link-Tracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeitsgrad der Implementierung | Eher schwierig | Relativ einfach |
| [!DNL Experience Cloud] Integrationen | Nicht unterstützt | Mit Einschränkungen unterstützt |

## Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics“ {#section_2E4EBF4EF623440D95DE98E78C47244E}

The `"adobeanalytics"`tracking template utilizes the `amp-analytics` tag to construct a tracking request directly. Using the `"adobeanalytics"` template in the `amp-analytics` tag, you can specify hit requests that fire on specific page events, like the page becoming visible or on a click (and in the future, video views and more). Klickereignisse können zum Anwenden bestimmter Element-IDs oder -Klassen angepasst werden, indem eine Auswahl festgelegt wird. Adobe has made this easy to set up using the `"adobeanalytics"` template specifically designed for [!DNL Adobe Analytics]. You can load the template by adding `type="adobeanalytics"` to the amp-analytics tag.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der Auslöser `pageLoad` sorgt dafür, dass das Dokument angezeigt wird und dabei die Variable `pageName` wie in `vars section` definiert enthält. Der zweite Auslöser `click` erfolgt beim Klick auf eine Schaltfläche. `eVar 1` für dieses Ereignis mit dem Wert `button clicked`festgelegt.

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

Hinweis: Wenn Sie Technologie- oder DOM-Variablen (z. B. Browser, Bildschirmgröße, Gerät, Referrer usw.) einbinden möchten, müssen Sie diese jeder Anforderung explizit hinzufügen, da sie nicht automatisch für Sie generiert werden. Die Dokumentation zu den einzelnen verfügbaren Abfragezeichenfolgeparametern, die zum Tracking verwendet werden, finden Sie [hier](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=query_parameters).

Beim Prüfen der durch amp-analytics erzeugten Ergebnisse werden Sie feststellen, dass Adobe den `vid`-Abfrageparameter eingebunden hat. Wir setzen `vid` auf Basis einer integrierten AMP-Funktion fest, um eine benutzerdefinierte Analytics-Cookie-ID namens `adobe_amp_id` festzulegen. This ID is independent of any other ID being set by [!DNL Adobe Analytics] elsewhere (e.g. `s_vi cookie`) and creates new visitors in any report suite the hits are sent to.

Sie müssen einige Einschränkungen beachten. Wenn der amp-analytics-Tag wie oben aufgeführt verwendet wird, sind Besucher von Ihrem normalen Tracking unabhängig, und da das AMP in jedem beliebigen Inhaltsbereitstellungsnetzwerk geladen werden kann, erhalten Sie einen einzelnen Besucher für jedes CDN, in dem dieses AMP einem Besucher angezeigt wird (die zuvor erwähnte Besucherinflation). For this reason, Adobe recommends that if you use the `"adobeanalytics"` template for `amp-analytics`, you put your data into a separate report suite specific to AMP. Also, the [!DNL Experience Cloud] ID service (formerly, *`visitor ID service`*) is not supported using this method, so if your business requires additional [!DNL Experience Cloud] integrations, or will in the future, this is probably not the option for you.

Der letzte und wohl wichtigste Punkt ist, dass bei dieser `amp-analytics`-Lösung der von Ihnen im Abschnitt `vars` festgelegte Tracking-Server dem Tracking-Server auf Ihrer Haupt-Site entsprechen muss, damit Ihre Datenschutzrichtlinien respektiert werden. Andernfalls müssen Sie separate Datenschutzrichtlinien für AMPs erstellen.

## Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics_nativeConfig“ {#section_3556B68304A4492991F439885727E9FF}

The `"adobeanalytics_nativeConfig"` tag is easier to implement, as it will use the same tagging methodology you use on your normal web pages. Fügen Sie dazu Folgendes zu Ihrem `amp-analytics`-Tag hinzu:

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

The `"adobeanalytics_nativeConfig"` template also adds query string parameters based on the variables listed in the `extraUrlParams` section of the amp-analytics tag. In diesem Fall können Sie sehen, dass wir die Parameter `pageName` und `v1` festgelegt haben, die von unserer [!DNL stats.html]-Seite verwendet werden.

Be aware that you can only use a single `amp-analytics` template at a time and can not use the `"adobeanalytics"` template as well as the `"adobeanalytics_nativeConfig"` template on the same AMP. Wenn Sie das versuchen, tritt möglicherweise ein Fehler in der Browserkonsole auf, und Ihre Besucherzahl wird verfälscht.

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
s.referrer=s.Util.getQueryParam(“ref”); 
s.t(); 
</script> 
</body> 
</html> 
```

Wie Sie oben sehen, können Sie Ihre vorhandene [!DNL VisitorAPI.js] und [!DNL AppMeasurement.js] (wie in unserem Beispiel) oder entsprechende Elemente Ihrer vorhandenen Implementierung verwenden bzw. verknüpfen und dann die korrekten Konfigurationsparameter hinzufügen. Um die korrekten Werte in den korrekten Variablen zu erfassen, können Sie die bereitgestellte `s.Util.getQueryParam`-Funktion verwenden, um die über die `iframeMessage`-URL abgerufenen Werte einzugeben und die entsprechenden Variablen wie auf einer regulären Seite festzulegen. If you use tag management software like Adobe's [ [!DNL Dynamic Tag Manager] ](https://www.adobe.com/solutions/digital-marketing/dynamic-tag-management.html), the query string parameters should be straightforward to capture. In diesem Fall wird für `s.pageName` der Wert festgelegt, den wir im Abfragezeichenfolgeparameter `pageName` eingegeben haben. Hier würde der Seitenname also *`Adobe Analytics Example 2`*.

>[!IMPORTANT]
>
>Due to restrictions on iframes in the AMP framework, your [!DNL stats.html] page must be hosted on a separate subdomain from the domain the AMP itself is hosted on. Das AMP-Framework lässt keine iframes aus derselben Subdomäne zu, in der sich die AMP-Seite selbst befindet. Wird Ihr AMP beispielsweise auf [!DNL amp.example.com] gehostet, sollten Sie Ihre [!DNL stats.html]-Seite in einer separaten Subdomäne wie [!DNL ampmetrics.example.com] oder einer ähnlichen Subdomäne hosten.

Da die Dienstprogrammseite auf Ihrer ursprünglichen Site gehostet wird, sind keine weiteren Schritte erforderlich, damit Ihre vorhandenen Datenschutzrichtlinien in allen AMPs unterstützt werden. Wenn sich ein Endbenutzer also vom Tracking auf Ihrer primären Site abmeldet, so wird das Tracking in all Ihren AMPs ohne weiteres Zutun beendet. Durch die Verwendung dieser Dienstprogrammseite kann das AMP den Adobe [!DNL Experience Cloud] ID-Dienst unterstützen. So können Sie die Messung aus Ihren AMPs in die restliche [!DNL Experience Cloud] integrieren (für gezielte Werbung, beispielsweise mit [!DNL Adobe Audience Manager]).

Wenn Ihr Unternehmen den [!DNL Experience Cloud] ID-Dienst noch nicht verwendet (oder eine Tag Management-Software wie den [!DNL Dynamic Tag Manager] von Adobe einsetzt), können Sie jedoch die [!DNL stats.html]-Seite auf eine beliebige Art mit Tags versehen. Verwenden Sie Ihre vorhandene Implementierung als Referenzpunkt. Der einzige Unterschied zu Ihrer Standardimplementierung besteht darin, dass Sie die entsprechenden Datenpunkte der amp-analytics `iframeMessage`-URL (oder der [!DNL document.URL] von der [!DNL stats.html]-Seite) für die einzelnen Variablen erhalten, die Sie festlegen möchten. Wenn Sie eine der [AMP-spezifischen Variablen](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) (wie oben gezeigt) wie den AMP-Referrer oder die AMP-Seiten-URL verwenden möchten, binden Sie diese wie im oben gezeigten iframeMessage-Objekt ein.

Diese Lösung ist zwar flexibel, jedoch hat sie auch Nachteile. Aufgrund von Einschränkungen in der `amp-analytics``iframeMessage`   kann sie nur einmal in einer Seitenladung geladen werden. This means you will not be able to do link tracking or video tracking with the `"adobeanalytics_nativeConfig"` template. Moreover, some DOM values that are typically captured automatically by our [!DNL AppMeasurement] code, such as `referrer` (which impacts the Search Engine Keyword reports, Referrer, and Referrer Type reports, or may include a marketing campaign tracking code) will have to be passed manually to the `iframeMessage` using whatever AMP variables [are available](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md). Daher empfiehlt Adobe, eine benutzerdefinierte Variable mit dem Wert-AMP festzulegen, wenn Sie AMP-Daten in eine vorhandene Report Suite eingeben, damit Sie den AMP-Traffic bei der Anzeige der zuvor erwähnten Berichte herausfiltern können. So sollten Standard-Technologieberichte wie Browser, Gerät, Bildschirmgröße oder Auflösung automatisch funktionieren.

Da der iframe als separate Seite geladen wird und das JavaScript auf dieser Seite vollständig ausführt, ist das AMP nicht so leicht wie vom AMP-Standard beabsichtigt. Dies wirkt sich nicht auf die Seitenladezeit aus (der iframe wird geladen, nachdem die Seite geladen wurde), aber CPU und Netzwerk werden stärker beansprucht als sonst. Dies könnte sich negativ auf das Scrollen auswirken. In der Praxis ist keine große Auswirkung festzustellen, aber wir arbeiten mit Google daran, die Auswirkungen dieses Ansatzes auf das Benutzererlebnis zu minimieren.

## Zusammenfassung {#section_4D8ED26084F249738A5C2BC66B933A07}

If you need click tracking and don't mind visitors being counted as entirely new visitors separate from your site, use the `"adobeanalytics"` tracking template, with our recommendation that you put the data into a *`separate report suite`*. If you need the [!DNL Experience Cloud] ID service, do not want visitor or visit inflation, and are okay with only firing Analytics on page load, we recommend using the `"adobeanalytics_nativeConfig"` solution.

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
   <td colname="col1"> <p> Ist das Video-Tracking für die Vorlage „<code>adobeanalytics</code>“ oder „<code>adobeanalytics_nativeConfig</code>“ verfügbar? </p> </td> 
   <td colname="col2"> <p> Leider noch nicht. Der AMP-Standard unterstützt lediglich Auslöser für „visible“, „click“ und „timer“. Spezifische Auslöser für das Video-Tracking, auf die der amp-analytics-Tag hört, werden noch nicht unterstützt. Da das „<code>adobeanalytics_nativeConfig</code>“-Tag nur einmal geladen werden kann, ist es nicht mit der Videoanzeige kompatibel, die nach dem Laden des AMP erfolgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sie haben erwähnt, dass die Besucherinflation mit der „<code>adobeanalytics_nativeConfig</code>“-Vorlage in Ihrem Vergleich geringer ausfällt. Was bedeutet das? Wodurch wird eine Besucherinflation in der „<code>adobeanalytics</code>“- oder „<code>adobeanalytics_nativeConfig</code>“-Lösung verursacht? </p> </td> 
   <td colname="col2"> <p>Die „<code>adobeanalytics</code>“-Vorlage erlaubt es Adobe Analytics nicht, ein Cookie zur Identifizierung von Besuchern abzulegen. Dies bedeutet, dass alle Besuche und Besucher Ihrer AMP-Seite in Ihrer Report Suite als neue und unabhängige Besuche und Besucher behandelt werden. </p> <p>Mit der „<code>adobeanalytics_nativeConfig</code>“-Vorlage kann jedoch in fast allen Fällen das Adobe Analytics-Cookie zur Identifizierung von Besuchern abgelegt werden, mit Ausnahme von neuen Besuchern, die den Safari-Browser verwenden. Dies bedeutet, dass alle Besucher, die Safari verwenden und die Website eines Publishers noch nicht besucht haben, in Adobe Analytics-Reporting überhöht angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sollte ich eine separate Report Suite für AMPs verwenden? </p> </td> 
   <td colname="col2"> <p>Wenn Sie die adobeanalytics-Vorlage verwenden, empfehlen wir Ihnen aufgrund des Problems mit der Besucher-/Besuchsinflation, eine separate Report Suite für AMPs zu verwenden. Wir werden jedoch auch die JavaScript-Version auf „AMP vX.X“ aus der amp-analytics-Tag-Vorlage festlegen, sodass Sie diesen Traffic bei Bedarf aus einer kombinierten Report Suite herausfiltern können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ist der <span class="keyword">Experience Cloud ID</span>-Dienst? Brauche ich ihn? </p> </td> 
   <td colname="col2"> <p>The <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/" format="https" scope="external"> Identity Service </a> (formerly <span class="term"> visitor ID service </span>) enables <span class="keyword"> Experience Cloud </span> core services and allows integrations between different Adobe <span class="keyword"> Experience Cloud </span> solutions. Wenn Sie über Integrationen mit <span class="keyword">Adobe Audience Manager</span> oder <span class="keyword">Adobe Target</span> verfügen, nutzen Sie diesen Dienst vermutlich. Dieser Dienst ist zudem die Grundlage für viele geplante Funktionen von <span class="keyword">Adobe Analytics.</span> Wenn Sie Unterstützung beim ID-Dienst benötigen oder später benötigen werden, empfehlen wir Ihnen die <code>iframeMessage</code>-Lösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wo soll ich meine Dienstprogrammseite hosten, wenn ich die Vorlage „<code>adobeanalytics_nativeConfig</code>“ verwende? </p> </td> 
   <td colname="col2"> <p>Der AMP-Standard lässt das Laden von iframes aus der exakten Domäne und Subdomäne des AMP nicht zu. Daher empfehlen wir, die Dienstprogrammseite in einer von Ihrer Haupt-Site separaten Subdomäne zu hosten, insbesondere wenn Ihr Unternehmen über ein eigenes CDN verfügt, das auf das Zwischenspeichern von AMPs abzielt. Wählen Sie für maximale Kompatibilität eine Subdomäne wie <span class="filepath">ampmetrics.publisher.com</span>, die vom Speicherort des tatsächlichen AMP-Inhalts getrennt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Besteht hier nicht eine große Ähnlichkeit zu <span class="keyword">Facebook Instant Articles </span>? Wie richte ich <span class="keyword">Adobe Analytics</span> mit Facebook Instant Articles ein? </p> </td> 
   <td colname="col2"> <p> Facebook Instant Articles unterstützt eine ähnliche Lösung wie die oben aufgeführte nativeConfig-Lösung. Die oben erstellte stats.html-Seite kann Ihre Analyseanforderungen für sowohl AMP als auch FIA zugleich erfüllen. Weitere Informationen zur Implementierung des Trackings in FIA finden Sie unter <a href="../../implement/js-implementation/analytics-facebook-instant-articles.md#concept_AC9AD1431CD14F919E329A161A80AA08" format="dita" scope="local"> Facebook Instant Articles </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

