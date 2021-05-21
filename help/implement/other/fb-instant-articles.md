---
title: Implementieren mit Facebook Instant Articles
description: Implementieren Sie Adobe Analytics auf Facebook Instant Article-Seiten.
exl-id: 2189f70d-32f0-4137-9d53-7acab0f15e6c
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '466'
ht-degree: 100%

---

# Implementieren mit Facebook Instant Articles

Mit Facebook Instant Articles können Vermarkter schnelle, interaktive Artikel auf Facebook erstellen. Mit Instant Articles wird Inhalt bis zu 10-mal schneller geladen als mobile Websites.

Sie können Adobe Analytics in Facebook Instant Articles einbetten, um das Besucherverhalten zu verfolgen. Da sich der Inhalt des Vermarkters in der Facebook-App und nicht auf den Websites des Vermarkters befindet, unterscheidet sich der Tagging-Ansatz von der Analytics-Standardimplementierung.

## Workflow

Der übergreifende Workflow zur Implementierung von Adobe Analytics lautet wie folgt:

1. Erstellen Sie eine `stats.html`-Seite. Codieren Sie diese Seite, um Abfragezeichenfolgenparameter aus der URL abzurufen und jeden Parameter einer Analytics-Variablen zuzuweisen.
1. Hosten Sie die `stats.html`-Seite auf Ihrem Webserver.
1. Implementieren Sie Analytics für Facebook Instant Article, indem Sie die `stats.html`-Datei in einem iFrame referenzieren.
1. Schließen Sie die Abfragezeichenfolgenparameter in das iFrame-Attribut `src` ein.

### Schritt 1: Erstellen einer `stats.html`-Seite

Mit dem folgenden HTML-Muster können Sie Statistiken aus den Instant Articles verwenden. Diese Datei wird in der Regel auf einem der Webserver Ihres Unternehmens gehostet. Jedes Mal, wenn ein Instant Article geladen wird, wird die Datei in einen iFrame geladen, wodurch Daten an Adobe gesendet werden.

```html
<html>
  <head>
    <title>Facebook Stats</title>
      <script language="javaScript" type="text/javascript" src="VisitorAPI.js"></script>
      <script language="javaScript" type="text/javascript" src="AppMeasurement.js"></script>
  </head>
  <body>
    <script>
      var v_orgId = "INSERT-ORG-ID-HERE";
      var s_account = "examplersid";
      var s_trackingServer = "example.data.adobedc.net";
      var visitor = Visitor.getInstance(v_orgId);
      visitor.trackingServer = s_trackingServer;

      var s = s_gi(s_account);
      s.account = s_account;
      s.trackingServer = s_trackingServer;
      s.visitor = visitor;

      s.pageName = s.Util.getQueryParam("pageName");
      s.pageURL = document.referrer; // The referrer to the utility page is the parent frame
      s.campaign = s.Util.getQueryParam("cmpId");
      s.eVar1 = "Facebook Instant Article";
      s.eVar2 = s.Util.getQueryParam("eVar2");

      s.t();
    </script>
  </body>
</html>
```

### Schritt 2: Hosten der `stats.html`-Seite auf Ihrem Webserver

Adobe empfiehlt das Hosten Ihrer `stats.html`-Seite zusammen mit den neuesten Versionen von `AppMeasurement.js` und `VisitorAPI.js`. Arbeiten Sie mit den entsprechenden Technik-Teams in Ihrer Organisation zusammen, um diese Datei am richtigen Speicherort zu hosten.

### Schritt 3: Referenzieren von `stats.html` auf jeder Facebook Instant Article-Seite

Betten Sie beim Erstellen von Facebook Instant Article-Inhalten den HTML-Inhalt von Analytics in einen iFrame ein. Beispiel:

```html
<iframe class="no-margin" src="https://example.com/stats.html" height="0"></iframe>
```

### Schritt 4: Festlegen des benutzerdefinierten Variablen- und Ereignis-Trackings

Benutzerdefinierte Variablen und Ereignisse können über zwei verschiedene Ansätze in Ihrer Analytics-HTML verfolgt werden:

* Fügen Sie Variablenwerte und -ereignisse direkt in die `stats.html`-Seite ein. Die hier definierten Variablen eignen sich am besten für Werte, die normalerweise für alle Facebook Instant Articles gleich sind.
* Fügen Sie Variablenwerte als Teil einer Abfragezeichenfolge ein, die auf den iFrame verweist. Mit dieser Methode können Sie Variablenwerte aus dem Facebook Instant Article an den iFrame senden, der den Analytics-Code hostet.

Das folgende Beispiel zeigt mehrere benutzerdefinierte Variablen, die in einer Abfragezeichenfolge enthalten sind. Das in `stats.html` enthaltene JavaScript prüft dann die Abfragezeichenfolge mit `s.Util.getQueryParam()`.

```html
<iframe class="no-margin" src="https://example.com/stats.html?eVar2=Dynamic%20article%20title&pageName=Example%20article%20name&cmpId=exampleID123" height="0"></iframe>
```

>[!NOTE]
>
>Die Dimension „Referrer“ wird aufgrund der Art der iFrames nicht automatisch verfolgt. Stellen Sie sicher, dass Sie diese Dimension als Teil Ihrer Abfragezeichenfolge einbeziehen, wenn Sie sie verfolgen möchten.

## Facebook Instant Articles und Datenschutz

Wenn die Analytics HTML-Seite auf Ihrem Webserver gehostet wird, unterstützt Adobe Ihre vorhandenen Datenschutzrichtlinien in allen Facebook Instant Articles. Wenn ein Benutzer das Tracking auf Ihrer primären Website deaktiviert, wird das Tracking auf all Ihren Facebook Instant Articles ebenfalls deaktiviert. Die Dienstprogrammseite unterstützt auch den Adobe Experience Cloud-Identitätsdienst, damit Sie Facebook Instant Article-Daten in den Rest von Experience Cloud integrieren können.
