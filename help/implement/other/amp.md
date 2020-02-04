---
title: Implementierung mit AMP
description: Implementieren Sie Adobe Analytics auf AMP-Seiten.
translation-type: tm+mt
source-git-commit: 9d2007bead6a4963022f8ea884169802b1c002ff

---


# Implementierung mit AMP

[AMP](https://amp.dev) ist ein Open-Source-HTML-Framework, das eine einfache Möglichkeit bietet, schnell und reibungslos ladende Webseiten zu erstellen.

Da Adobe Analytics zum Kompilieren und Senden einer Bildanforderung eine JavaScript-Bibliothek verwendet, sind Anpassungen in Ihrer Implementierung erforderlich, um Daten auf Seiten mit AMP an Adobe zu senden.

## Bestimmen der Methode zur Implementierung von Adobe Analytics auf Seiten mit AMP

Adobe hat zwei Methoden zur Implementierung von Adobe Analytics auf Seiten mit AMP erstellt. Beide verwenden das `<amp-analytics>` HTML-Tag. Weitere Informationen finden Sie unter [amp-analytics-Tag](https://github.com/ampproject/amphtml/tree/master/extensions/amp-analytics) im Ampproject GitHub.

* **Verwenden Sie die`"adobeanalytics"`Verfolgungsvorlage**: Analytics-Anforderung direkt auf der Seite erstellen
* **Verwenden Sie die`"analytics_nativeConfig"`Verfolgungsvorlage**: Verwenden Sie einen iframe, der denselben AppMeasurement-Code enthält, den Sie auf Ihrer normalen Site bereitstellen

In der folgenden Tabelle werden die beiden Methoden verglichen:

|  | **„adobeanalytics“-Vorlage** | **„adobeanalytics_nativeConfig“-Vorlage** |
|---|---|---|
| Besucher-/Besuchszahlen in der vorhandenen Report Suite | Hohe Inflation | Minimale Inflation |
| Verwenden einer separaten Report Suite | Empfohlen | Nicht erforderlich |
| Neue vs. wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Service | Nicht unterstützt | Unterstützt |
| Video- und Linktracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeitsgrad der Implementierung | Eher schwierig | Relativ einfach |
| Adobe Experience Cloud-Integrationen | Nicht unterstützt | Teilweise unterstützt |

Legen Sie anhand der Vor- und Nachteile in Ihrer Organisation fest, welche Methode Sie verwenden möchten. Beispielcode finden Sie unter [AMP-Beispiele](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web) im GitHub-Repository von Adobe.

> [!WARNING] Verwenden Sie nicht sowohl die `"adobeanalytics"` als auch die `"adobeanalytics_nativeConfig"` Vorlagen auf derselben Seite mit AMP. Wenn Sie dies versuchen, können Sie Fehler in der Browser-Konsole generieren und Besucher doppelt zählen.

## Methode 1: Verwenden Sie das amp-analytics-Tag mit der Vorlage &quot;adobeanalytics&quot;

The `"adobeanalytics"` tracking template uses the `<amp-analytics>` HTML tag to construct a tracking request directly. Sie können Trefferanforderungen angeben, die bei bestimmten Seitenereignissen ausgelöst werden, z. B. bei der Anzeige der Seite oder bei einem Klick. Klickereignisse können zum Anwenden bestimmter Element-IDs oder -Klassen angepasst werden, indem eine Auswahl festgelegt wird. Sie können die Vorlage laden, indem Sie `type="adobeanalytics"` zum amp-analytics-Tag hinzufügen.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der `pageLoad` Auslöser wird ausgelöst, wenn das Dokument sichtbar wird und die `pageName` Variable wie im `vars` Abschnitt definiert enthält. The second trigger `click` fires when a button is clicked. `eVar1` für dieses Ereignis mit dem Wert festgelegt `button clicked`.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.sc.omtrdc.net",
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

In the `click` trigger, you can specify a selector to ensure that whenever the specific DOM element is clicked (in this case, any button), the `buttonClick` request is fired and is automatically set to denote this hit as a link tracking call.

Zudem unterstützt `amp-analytics` eine Anzahl von Variablenersetzungen, sodass AMP bekannte Datenwerte bereitstellen kann. Weitere Informationen finden Sie unter [Variablen, die in amp-analytics](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) auf GitHub unterstützt werden.

> [!NOTE] Bildanforderungen, die mit dieser Methode an Adobe gesendet werden, enthalten keine Daten für viele Standardberichte (z. B. Browser, Bildschirmgröße oder verweisende Stelle). Wenn Sie diese Informationen in Treffer einschließen möchten, stellen Sie sicher, dass sie als Teil der Abfragezeichenfolge für die Bildanforderung enthalten sind. Weitere Informationen finden Sie unter Abfrageparameter [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md).

Adobe identifiziert Besucher mithilfe einer integrierten AMP-Funktion und setzt das Cookie `adobe_amp_id`. Diese Besucher-ID ist für jede andere von Adobe Analytics eingestellte ID eindeutig (z. B. das `s_vi` Cookie). Der Adobe Experience Cloud ID-Dienst wird bei dieser Implementierungsmethode nicht unterstützt.

> [!NOTE] AMP verwendet CDNs zur Bereitstellung von Inhalten. Es ist so strukturiert, dass für jedes CDN, aus dem ein Besucher Inhalte abruft, ein anderer individueller Besucher gezählt wird, was die Anzahl der individuellen Besucher erhöhen kann.

Die Verwendung einer separaten Report Suite für AMP-Seiten wird empfohlen, da AMP individuelle Besucher identifiziert.

This solution requires that the tracking server you specify in the `host` property matches the tracking server on your main site, so that your existing privacy policy controls are respected. Andernfalls erstellen Sie eine separate Datenschutzrichtlinie für Seiten, die AMP verwenden.

## Methode 2: Verwenden Sie das amp-analytics-Tag mit der Vorlage &quot;adobeanalytics_nativeConfig&quot;

The `"adobeanalytics_nativeConfig"` tag is easier to implement, as it uses the same tagging methodology you use on your normal web pages. Fügen Sie Folgendes zu Ihrem `amp-analytics` -Tag hinzu:

```html
<amp-analytics type="adobeanalytics_nativeConfig">
  <script type="application/json">
    {
      "requests": {
        "base": "https://${host}",
        "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}"
      },
      "vars": {
        "host": "example.sc.omtrdc.net"
      },
      "extraUrlParams": {
      "pageName": "Example AMP page",
      "v1": "eVar1 example value"
      }
    }
 </script>
</amp-analytics>
```

Eine auf Ihren Webservern gehostete HTML-Seite ist ebenfalls erforderlich:

```html
<html>
  <head>
    <title>Stats Example</title>
    <script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script>
    <script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script>
  </head>
  <body>
    <script>
      var v_orgId = "INSERT-ORG-ID-HERE";
      var s_account = "examplersid";
      var s_trackingServer = "example.sc.omtrdc.net";
      var visitor = Visitor.getInstance(v_orgId);
      visitor.trackingServer = s_trackingServer;
      var s = s_gi(s_account);
      s.account = s_account;
      s.trackingServer = s_trackingServer;
      s.visitorNamespace = s_visitorNamespace;
      s.visitor = visitor;
      s.pageName = s.Util.getQueryParam("pageName");
      s.eVar1 = s.Util.getQueryParam("v1");
      s.campaign = s.Util.getQueryParam("campaign");
      s.pageURL = s.Util.getQueryParam("pageURL");
      s.referrer = s.Util.getQueryParam("ref");
      s.t();
    </script>
  </body>
</html>
```

This approach sends data to a utility web page through query string parameters added to the `iframeMessage` request parameter. These query string parameters can be named whatever you like, as long as your `stats.html` page is configured to collect data from them.

Die `"adobeanalytics_nativeConfig"`-Vorlage kann zudem Abfragezeichenfolgenparameter hinzufügen, die auf den im `extraUrlParams`-Abschnitt des amp-analytics-Tags aufgeführten Variablen basieren. Im obigen Beispiel werden die Parameter `pageName` und `v1` einbezogen.

> [!IMPORTANT] Ihre `stats.html` Seite muss in einer separaten Subdomäne gehostet werden, die von der Domäne abweicht, auf der das AMP selbst gehostet wird. Das AMP-Framework lässt keine iframes aus derselben Subdomäne zu, in der sich die AMP-Seite selbst befindet. Wenn Ihr AMP beispielsweise auf gehostet wird, `amp.example.com`hosten Sie Ihre `stats.html` Seite in einer separaten Subdomäne wie `ampmetrics.example.com`.

Wenn ein Benutzer die Verfolgung auf Ihrer primären Site ablehnt, wird die Verfolgung bei allen AMPs ebenfalls eingestellt. Die Verwendung dieser Dienstprogrammseite bedeutet auch, dass AMP den Adobe Experience Cloud ID-Dienst unterstützen kann. Eine separate Report Suite ist nicht erforderlich.

Mit dieser Methode können die Linktracking und die Videoverfolgung nicht verwendet werden. Das `iframeMessage` -Tag in AMP kann nur einmal pro Seite geladen werden, sodass Sie keine anderen Bildanforderungen senden können, nachdem der Frame geladen wurde. Diese Methode erfordert auch mehr Verarbeitungsressourcen, was sich auf die Leistung des Bildlaufs auswirken kann. Diese Methode hat keine Auswirkungen auf die Seitenladezeit, da alle Ressourcen asynchron geladen werden.

## FAQs

**Ist die Videoverfolgung für beide Methoden verfügbar?**

Nein. Der AMP-Standard unterstützt nur Auslöser für &quot;visible&quot;, &quot;click&quot;und &quot;timer&quot;. Es werden noch keine expliziten Auslöser für die Videoverfolgung unterstützt, die vom `amp-analytics` Tag überwacht werden können. Außerdem kann die `"adobeanalytics_nativeConfig"` Vorlage nur einmal geladen werden, sodass nachfolgende Bildanforderungen nach dem Laden einer Seite nicht möglich sind.

**Wie kann ich AMP-Besucher von anderen in meinen Daten unterscheiden?**

Für alle AMP-Seiten erfasst die Dimension &quot; [!UICONTROL JavaScript-Version] &quot;einen Wert, der `AMP vX.X`dem ähnelt. Sie können auch eine benutzerdefinierte Dimension auf &quot;AMP&quot;festlegen, damit Sie diese Besucher segmentieren können.

**Wie sieht diese Implementierungsmethode im Vergleich zu Facebook Instant Articles aus?**

Facebook Instant Articles unterstützt eine ähnliche Lösung wie die `"adobeanalytics_nativeConfig"` Methode. Die `stats.html` Seite für diese Methode kann Ihren Analyseanforderungen für AMP und FIA gleichzeitig entsprechen. Weitere Informationen zur Implementierung der Verfolgung auf FIA finden Sie unter [Facebook Instant Articles](fb-instant-articles.md).
