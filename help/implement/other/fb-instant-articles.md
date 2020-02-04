---
title: Implementieren mit Facebook Instant Articles
description: Implementieren Sie Adobe Analytics auf Facebook Instant Article-Seiten.
translation-type: tm+mt
source-git-commit: 9d2007bead6a4963022f8ea884169802b1c002ff

---


# Implementieren mit Facebook Instant Articles

Mit Facebook Instant Articles können Herausgeber schnelle, interaktive Artikel auf Facebook erstellen. Mit Instant Articles wird Inhalt bis zu 10-mal schneller geladen als mobile Websites.

Sie können Adobe Analytics in Facebook Instant Articles einbetten, um das Besucherverhalten zu verfolgen. Da sich der Inhalt des Herausgebers in der Facebook-App und nicht auf den Websites des Herausgebers befindet, unterscheidet sich der Tagging-Ansatz geringfügig von der Analytics-Standardimplementierung.

## Arbeitsablauf

Der übergreifende Arbeitsablauf zur Implementierung von Adobe Analytics lautet wie folgt:

1. Erstellen Sie eine `stats.html` Seite. Code auf dieser Seite, um Abfragezeichenfolgenparameter aus der URL abzurufen und jeden Parameter einer Analytics-Variablen zuzuweisen
1.  Hosten Sie die `stats.html` Seite auf Ihrem Webserver
1. Implementieren von Analytics im Facebook Instant Article durch Verweis auf die `stats.html` Datei in einem iframe
1. Abfragezeichenfolgenparameter in das iFrame- `src` Attribut einschließen

### Schritt 1: Erstellen einer `stats.html` Seite

Mit dem folgenden HTML-Muster können Sie Statistiken aus den Instant Articles verwenden. Diese Datei wird in der Regel auf einem der Webserver Ihres Unternehmens gehostet. Jedes Mal, wenn ein Instant Article geladen wird, wird die Datei in einen iframe geladen, wodurch Daten an Adobe gesendet werden.

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
      var s_trackingServer = "example.sc.omtrdc.net";
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

### Schritt 2: Hosten Sie die `stats.html` Seite auf Ihrem Webserver

Adobe empfiehlt das Hosten Ihrer `stats.html` Seite zusammen mit der neuesten Version von `AppMeasurement.js` und `VisitorAPI.js`. Arbeiten Sie mit den entsprechenden Engineering-Teams in Ihrer Organisation zusammen, um diese Datei am richtigen Ort zu hosten.

### Schritt 3: Verweis `stats.html` auf jeder Facebook Instant Article-Seite

Betten Sie beim Erstellen von Facebook Instant Article-Inhalten den HTML-Inhalt der Analyse in einen iframe ein. Beispiel:

```html
<iframe class="no-margin" src="https://example.com/stats.html" height="0"></iframe>
```

### Schritt 4: Festlegen der Verfolgung benutzerspezifischer Variablen und Ereignisse

Benutzerspezifische Variablen und Ereignisse können in Ihrer Analytics-HTML auf zwei verschiedene Arten verfolgt werden:

* Fügen Sie Variablenwerte und -ereignisse direkt in die `stats.html` Seite ein. Die hier definierten Variablen eignen sich am besten für Werte, die normalerweise für alle Facebook Instant Articles gleich sind.
* Fügen Sie Variablenwerte als Teil einer Abfragezeichenfolge ein, die auf den iframe verweist. Mit dieser Methode können Sie Variablenwerte aus dem Facebook Instant Article an den iframe senden, der Analytics-Code hostet.

Das folgende Beispiel zeigt mehrere benutzerdefinierte Variablen, die in einer Abfragezeichenfolge enthalten sind. Das darin enthaltene JavaScript `stats.html` prüft dann die Abfragezeichenfolge mit `s.Util.getQueryParam()`.

```html
<iframe class="no-margin" src="https://example.com/stats.html?eVar2=Dynamic%20article%20title&pageName=Example%20article%20name&cmpId=exampleID123" height="0"></iframe>
```

> [!NOTE] Die Dimension &quot;Verweisende Stelle&quot;wird aufgrund der Art von iframes nicht automatisch verfolgt. Stellen Sie sicher, dass Sie diese Dimension als Teil Ihrer Abfragezeichenfolge einbeziehen, wenn Sie sie verfolgen möchten.

## Facebook Instant Articles und privacy

Solange die Analytics-HTML-Seite auf Ihrem Webserver gehostet wird, unterstützt Adobe Ihre bestehenden Datenschutzrichtlinien für alle Facebook Instant Articles. Wenn ein Benutzer sich gegen die Verfolgung auf Ihrer primären Site entscheidet, wird er auch die Verfolgung in allen Ihren Facebook Instant Articles abwählen. Die Dienstprogrammseite unterstützt auch den Adobe Experience Cloud-Identitätsdienst, damit Sie Facebook Instant Article-Daten in den Rest der Experience Cloud integrieren können.
