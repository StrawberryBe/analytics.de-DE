---
title: Implementieren mit AMP
description: Implementieren Sie Adobe Analytics auf AMP-Seiten.
feature: Implementation Basics
exl-id: 51a2662e-2a24-48f1-b17a-d1e1a57a394b
source-git-commit: 4c75275f9abbff6b9a5a25be370eabc2801eb7fb
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 71%

---

# Implementieren mit AMP

[AMP](https://amp.dev) ist ein Open-Source-HTML-Framework, um auf einfache Weise schnell und problemlos ladende Webseiten zu erstellen.

Da Adobe Analytics zum Kompilieren und Senden einer Bildanforderung eine JavaScript-Bibliothek verwendet, sind Anpassungen in Ihrer Implementierung erforderlich, um Daten auf Seiten mit AMP an Adobe zu senden.

## Festlegen der Methode zum Implementieren von Adobe Analytics auf Seiten mit AMP

Adobe bietet zwei Methoden zum Implementieren von Adobe Analytics auf Seiten mit AMP. Beide verwenden das HTML-Tag `<amp-analytics>`. Siehe [amp-analytics](https://amp.dev/de/documentation/components/amp-analytics) Weitere Informationen finden Sie in der AMP-Dokumentation .

* **Verwenden Sie die `"adobeanalytics"` template**: Erstellen Sie die Analytics-Anforderung direkt auf der Seite
* **Verwenden Sie die `"analytics_nativeConfig"` template**: Verwenden Sie einen iframe, der denselben AppMeasurement-Code enthält, den Sie auf Ihrer normalen Site bereitstellen.

In der folgenden Tabelle werden die beiden Methoden verglichen:

|   | **`"adobeanalytics"`bearbeiten** | **`"adobeanalytics_nativeConfig"`bearbeiten** |
|---|---|---|
| Besucher-/Besuchsanzahlen in bestehender Report Suite | Hohe Inflation | Minimale Inflation |
| Separate Report Suite verwenden | Empfohlen | Nicht erforderlich |
| Neue vs. wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Service | Nicht unterstützt | Unterstützt |
| Video- und Linktracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeitsgrad der Implementierung | Schwierigkeit | Relativ einfach |
| Integrationen mit Adobe Experience Cloud | Nicht unterstützt | Teilweise unterstützt |

Legen Sie die Vor- und Nachteile ab, sodass Sie die beste Implementierungsmethode für Ihr Unternehmen auswählen können.

>[!WARNING]
>
>Verwenden Sie mit AMP nicht sowohl die `"adobeanalytics"`- als auch die `"adobeanalytics_nativeConfig"`-Vorlage auf derselben Seite. Wenn Sie dies versuchen, können Sie Fehler in der Browser-Konsole erzeugen und Besucher doppelt zählen.

## Methode 1: Verwenden Sie die `<amp-analytics>` Tag mit dem `"adobeanalytics"` template

Die Tracking-Vorlage `"adobeanalytics"` nutzt das `<amp-analytics>`-HTML-Tag, um direkt eine Tracking-Anforderung zu erstellen. Sie können Trefferanforderungen angeben, die bei bestimmten Seitenereignissen ausgelöst werden, z. B. bei der Anzeige der Seite oder bei einem Klick. Klickereignisse können angepasst werden, um sie auf bestimmte Element-IDs oder Klassen anzuwenden, indem eine Auswahl angegeben wird. Sie können die Vorlage laden, indem Sie `type="adobeanalytics"` zum amp-analytics-Tag hinzufügen.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der Auslöser `pageLoad` erfolgt, wenn das Dokument sichtbar wird und die `pageName`-Variable, wie im `vars`-Abschnitt definiert, enthält. Der zweite Auslöser `click` erfolgt beim Klick auf eine Schaltfläche. Die `eVar1` für dieses Ereignis mit dem Wert festgelegt ist `button clicked`.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.data.adobedc.net",
        "reportSuites": "reportSuiteID1,reportSuiteID2",
        "pageName": "Adobe Analytics Using amp-analytics tag"
      },
      "triggers": {
        "pageLoad": {
          "on": "visible",
          "request": "pageview"
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

Die `<amp-analytics>` Tag unterstützt Variablenersetzungen, sodass AMP bekannte Datenwerte bereitstellen kann. Weitere Informationen finden Sie unter [In unterstützte Variablen`amp-analytics` auf GitHub.](https://github.com/ampproject/amphtml/blob/main/extensions/amp-analytics/analytics-vars.md)

>[!NOTE]
>
>Bildanforderungen, die mit dieser Methode an Adobe gesendet werden, enthalten für viele Standardberichte (z. B. Browser, Bildschirmgröße oder Referrer) keine Daten. Wenn Sie diese Informationen in Treffer einbeziehen möchten, stellen Sie sicher, dass sie als Teil der Abfragezeichenfolge für Bildanforderungen enthalten sind. Siehe [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md) für eine vollständige Liste der Abfrageparameter für Bildanforderungen und der zugehörigen Variablen.

Adobe identifiziert Besucher mithilfe einer integrierten AMP-Funktion und setzt das `adobe_amp_id`-Cookie. Diese Besucher-ID ist für jede andere von Adobe Analytics festgelegte ID eindeutig. Für jedes CDN, aus dem ein Besucher Inhalte abruft, wird ein anderer Unique Visitor gezählt, was die Anzahl der Unique Visitors erhöhen kann. Die Verwendung einer separaten Report Suite für AMP-Seiten wird dringend empfohlen, da AMP Unique Visitors identifiziert. Der Adobe Experience Cloud ID-Dienst wird nicht unterstützt.

Bei dieser Lösung muss der von Ihnen in der `host`-Eigenschaft festgelegte Trackingserver dem Trackingserver auf Ihrer Haupt-Website entsprechen, damit Ihre Datenschutzrichtlinien eingehalten werden. Andernfalls erstellen Sie eine separate Datenschutzrichtlinie für Seiten, die AMP verwenden.

## Methode 2: Verwenden Sie die `<amp-analytics>` Tag mit dem `"adobeanalytics_nativeConfig"` template

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
        "host": "example.data.adobedc.net"
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
      var s_account = "examplersid1,examplersid2";
      var s_trackingServer = "example.data.adobedc.net";
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

Die `"adobeanalytics_nativeConfig"` -Vorlage fügt zudem Abfragezeichenfolgenparameter hinzu, die auf den Variablen basieren, die im `extraUrlParams` Abschnitt `<amp-analytics>` -Tag. Im obigen Beispiel werden die Parameter `pageName` und `v1` einbezogen.

>[!IMPORTANT]
>
>Ihre `stats.html`-Seite muss in einer anderen Unterdomäne als der Domain gehostet werden, in der AMP selbst gehostet wird. Das AMP-Framework lässt keine iFrames aus derselben Unterdomäne zu, in der sich die AMP-Seite selbst befindet. Wenn Ihr AMP beispielsweise auf `amp.example.com` gehostet wird, hosten Sie Ihre `stats.html`-Seite in einer anderen Unterdomäne wie `ampmetrics.example.com`.

Wenn ein Benutzer bei dieser Methode das Tracking auf Ihrer primären Website deaktiviert, wird das Tracking auf all Ihren AMPs ebenfalls deaktiviert. Bei Verwendung dieser Dienstprogrammseite kann AMP auch den Adobe Experience Cloud ID-Dienst unterstützen. Eine separate Report Suite ist nicht erforderlich.

Mit dieser Methode können Linktracking und die Video-Tracking nicht verwendet werden. Das `iframeMessage`-Tag in AMP kann nur einmal pro Seite geladen werden, sodass Sie keine anderen Bildanforderungen senden können, nachdem der Frame geladen wurde. Diese Methode erfordert auch mehr Verarbeitungsressourcen, was sich auf die Bildlaufleistung auswirken kann. Diese Methode hat keine Auswirkungen auf die Seitenladezeit, da alle Ressourcen asynchron geladen werden.

## Häufig gestellte Fragen

**Wie können AMP-Besucher in den Daten von anderen unterschieden werden?**

Die Dimension [!UICONTROL JavaScript-Version] erfasst für alle AMP-Seiten einen Wert ähnlich `AMP vX.X`. Sie können auch eine benutzerdefinierte Dimension auf &quot;AMP&quot;festlegen, damit Sie diese Besucher segmentieren können.

**Wie ist diese Implementierungsmethode mit Facebook Instant Articles zu vergleichen?**

Facebook Instant Articles unterstützt eine ähnliche Lösung wie die `"adobeanalytics_nativeConfig"`-Methode. Die `stats.html`-Seite für diese Methode kann Ihre Analyseanforderungen für AMP und FIA gleichzeitig erfüllen. Weitere Informationen zur Tracking-Implementierung auf FIA finden Sie unter [Facebook Instant Articles](fb-instant-articles.md).
