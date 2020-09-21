---
title: Implementieren mit AMP
description: Implementieren Sie Adobe Analytics auf AMP-Seiten.
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '1061'
ht-degree: 100%

---


# Implementieren mit AMP

[AMP](https://amp.dev) ist ein Open-Source-HTML-Framework, um auf einfache Weise schnell und problemlos ladende Webseiten zu erstellen.

Da Adobe Analytics zum Kompilieren und Senden einer Bildanforderung eine JavaScript-Bibliothek verwendet, sind Anpassungen in Ihrer Implementierung erforderlich, um Daten auf Seiten mit AMP an Adobe zu senden.

## Festlegen der Methode zum Implementieren von Adobe Analytics auf Seiten mit AMP

Adobe bietet zwei Methoden zum Implementieren von Adobe Analytics auf Seiten mit AMP. Beide verwenden das HTML-Tag `<amp-analytics>`. Weitere Informationen finden Sie unter [amp-analytics-Tag](https://github.com/ampproject/amphtml/tree/master/extensions/amp-analytics) im ampproject-GitHub.

* **Tracking-Vorlage`"adobeanalytics"`verwenden**: Erstellen Sie die Analytics-Anforderung direkt auf der Seite
* **`"analytics_nativeConfig"`Tracking-Vorlage verwenden**: Verwenden Sie einen iFrame, der denselben AppMeasurement-Code enthält, den Sie auf Ihrer normalen Website bereitstellen

In der folgenden Tabelle werden die beiden Methoden verglichen:

|  | **„adobeanalytics“-Vorlage** | **„adobeanalytics_nativeConfig“-Vorlage** |
|---|---|---|
| Besucher-/Besuchsanzahlen in bestehender Report Suite | Hohe Inflation | Minimale Inflation |
| Separate Report Suite verwenden | Empfohlen | Nicht erforderlich |
| Neue vs. wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Service | Nicht unterstützt | Unterstützt |
| Video- und Linktracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeitsgrad der Implementierung | Eher schwierig | Relativ einfach |
| Integrationen mit Adobe Experience Cloud | Nicht unterstützt | Teilweise unterstützt |

Legen Sie anhand der Vor- und Nachteile in Ihrer Organisation fest, welche Methode Sie verwenden möchten. Beispielcode finden Sie unter [AMP-Beispiele](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web) im GitHub-Repository von Adobe.

>[!WARNING]
>
>Verwenden Sie mit AMP nicht sowohl die `"adobeanalytics"`- als auch die `"adobeanalytics_nativeConfig"`-Vorlage auf derselben Seite. Wenn Sie dies versuchen, können Sie Fehler in der Browser-Konsole erzeugen und Besucher doppelt zählen.

## Methode 1: Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics“

Die Tracking-Vorlage `"adobeanalytics"` nutzt das `<amp-analytics>`-HTML-Tag, um direkt eine Tracking-Anforderung zu erstellen. Sie können Trefferanforderungen angeben, die bei bestimmten Seitenereignissen ausgelöst werden, z. B. bei der Anzeige der Seite oder bei einem Klick. Klickereignisse können angepasst werden, um sie auf bestimmte Element-IDs oder Klassen anzuwenden, indem eine Auswahl angegeben wird. Sie können die Vorlage laden, indem Sie `type="adobeanalytics"` zum amp-analytics-Tag hinzufügen.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der Auslöser `pageLoad` erfolgt, wenn das Dokument sichtbar wird und die `pageName`-Variable, wie im `vars`-Abschnitt definiert, enthält. Der zweite Auslöser `click` erfolgt beim Klick auf eine Schaltfläche. Für `eVar1` wird bei diesem Ereignis der Wert `button clicked` festgelegt.

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

Im `click`-Auslöser können Sie eine Auswahl festlegen, um sicherzustellen, dass bei jedem Klick auf das spezifische DOM-Element (in diesem Fall jede Schaltfläche) die `buttonClick`-Anforderung ausgelöst und automatisch zum Markieren dieses Vorgangs als Linktracking-Aufruf festgelegt wird.

Zudem unterstützt `amp-analytics` eine Anzahl von Variablenersetzungen, sodass AMP bekannte Datenwerte bereitstellen kann. Weitere Informationen finden Sie unter [In amp-analytics unterstützte Variablen](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) auf GitHub.

>[!NOTE]
>
>Bildanforderungen, die mit dieser Methode an Adobe gesendet werden, enthalten für viele Standardberichte (z. B. Browser, Bildschirmgröße oder Referrer) keine Daten. Wenn Sie diese Informationen in Treffer einschließen möchten, stellen Sie sicher, dass sie als Teil der Abfragezeichenfolge für die Bildanforderung enthalten sind. Weitere Informationen finden Sie unter [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md).

Adobe identifiziert Besucher mithilfe einer integrierten AMP-Funktion und setzt das `adobe_amp_id`-Cookie. Diese Besucher-ID ist für jede andere von Adobe Analytics festgelegte ID eindeutig (z. B. das `s_vi`-Cookie). Der Adobe Experience Cloud ID-Dienst wird bei dieser Implementierungsmethode nicht unterstützt.

>[!NOTE]
>
>AMP verwendet CDNs zur Bereitstellung von Inhalten. Dabei wird für jedes CDN, aus dem ein Besucher Inhalte abruft, ein anderer Unique Visitor gezählt wird, wodurch die Anzahl der Unique Visitors überhöht kann.

Aufgrund der Art und Weise, auf die AMP Unique Visitors identifiziert, wird die Verwendung einer separaten Report Suite für AMP-Seiten empfohlen.

Bei dieser Lösung muss der von Ihnen in der `host`-Eigenschaft festgelegte Trackingserver dem Trackingserver auf Ihrer Haupt-Website entsprechen, damit Ihre Datenschutzrichtlinien eingehalten werden. Andernfalls erstellen Sie eine separate Datenschutzrichtlinie für Seiten, die AMP verwenden.

## Methode 2: Verwenden des amp-analytics-Tags mit der Vorlage „adobeanalytics_nativeConfig“

Das `"adobeanalytics_nativeConfig"`-Tag ist einfacher zu implementieren, da es dieselbe Tagging-Methode wie auf Ihren normalen Websites nutzt. Fügen Sie Ihrem `amp-analytics`-Tag Folgendes hinzu:

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

Außerdem ist eine auf Ihren Webservern gehostete HTML-Seite erforderlich:

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

Bei diesem Ansatz werden Daten über Abfragezeichenfolgenparameter, die dem `iframeMessage`-Abfrageparameter hinzugefügt werden, an eine Dienstprogramm-Website gesendet. Diese Abfragezeichenfolgenparameter können beliebig benannt werden, solange Ihre `stats.html`-Seite so konfiguriert ist, dass sie die entsprechenden Daten daraus erfassen kann.

Die `"adobeanalytics_nativeConfig"`-Vorlage kann zudem Abfragezeichenfolgenparameter hinzufügen, die auf den im `extraUrlParams`-Abschnitt des amp-analytics-Tags aufgeführten Variablen basieren. Im obigen Beispiel werden die Parameter `pageName` und `v1` einbezogen.

>[!IMPORTANT]
>
>Ihre `stats.html`-Seite muss in einer anderen Unterdomäne als der Domäne gehostet werden, in der AMP selbst gehostet wird. Das AMP-Framework lässt keine iFrames aus derselben Unterdomäne zu, in der sich die AMP-Seite selbst befindet. Wenn Ihr AMP beispielsweise auf `amp.example.com` gehostet wird, hosten Sie Ihre `stats.html`-Seite in einer anderen Unterdomäne wie `ampmetrics.example.com`.

Wenn ein Benutzer bei dieser Methode das Tracking auf Ihrer primären Website deaktiviert, wird das Tracking auf all Ihren AMPs ebenfalls deaktiviert. Bei Verwendung dieser Dienstprogrammseite kann AMP auch den Adobe Experience Cloud ID-Dienst unterstützen. Eine separate Report Suite ist nicht erforderlich.

Mit dieser Methode können Linktracking und die Video-Tracking nicht verwendet werden. Das `iframeMessage`-Tag in AMP kann nur einmal pro Seite geladen werden, sodass Sie keine anderen Bildanforderungen senden können, nachdem der Frame geladen wurde. Diese Methode erfordert auch mehr Verarbeitungsressourcen, was sich auf die Bildlaufleistung auswirken kann. Diese Methode hat keine Auswirkungen auf die Seitenladezeit, da alle Ressourcen asynchron geladen werden.

## Häufig gestellte Fragen

**Ist Video-Tracking für beide Methoden verfügbar?**

Nein. Der AMP-Standard unterstützt nur Auslöser für „visible“ (sichtbar), „click“ (Klick) und „timer“ (Timer). Es werden noch keine expliziten Auslöser für das Video-Tracking unterstützt, die vom `amp-analytics`-Tag überwacht werden können. Außerdem kann die Vorlage `"adobeanalytics_nativeConfig"` nur einmal geladen werden, sodass nachfolgende Bildanforderungen nach dem Laden einer Seite nicht möglich sind.

**Wie können AMP-Besucher in den Daten von anderen unterschieden werden?**

Die Dimension [!UICONTROL JavaScript-Version] erfasst für alle AMP-Seiten einen Wert ähnlich `AMP vX.X`. Sie können auch eine benutzerdefinierte Dimension auf „AMP“ festlegen, damit Sie diese Besucher segmentieren können.

**Wie ist diese Implementierungsmethode mit Facebook Instant Articles zu vergleichen?**

Facebook Instant Articles unterstützt eine ähnliche Lösung wie die `"adobeanalytics_nativeConfig"`-Methode. Die `stats.html`-Seite für diese Methode kann Ihre Analyseanforderungen für AMP und FIA gleichzeitig erfüllen. Weitere Informationen zur Tracking-Implementierung auf FIA finden Sie unter [Facebook Instant Articles](fb-instant-articles.md).
