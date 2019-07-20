---
description: Implementieren von Analytics in Facebook Instant Articles.
keywords: Analytics-Implementierung; embed; benutzerdefinierte Variable; benutzerdefiniertes Ereignis; Besucherverfolgung; tracking; Einschränkungen
seo-description: Implementieren von Analytics in Facebook Instant Articles.
seo-title: Facebook Instant Articles
solution: Analytics
title: Facebook Instant Articles
topic: Entwickler und Implementierung
uuid: 04 b 6366 b -7 c 52-4 dae-b 2 dd-bb 6 b 78 fd 409 c
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Facebook Instant Articles

Implementieren von Analytics in Facebook Instant Articles.

Facebook Instant Articles dient Herausgebern als neue Methode zur Erstellung von schnellen, interaktiven Artikeln auf Facebook. Mit Instant Articles wird Inhalt bis zu 10-mal schneller geladen als mobile Websites.

Adobe Analytics kann mit Facebook Instant Articles integriert werden und so das Besucherverhalten bei der Interaktion mit dem Inhalt verfolgen. Da sich der Inhalt des Herausgebers in der Facebook-App und nicht auf den Websites des Herausgebers befindet, unterscheidet sich der Tagging-Ansatz von der Analytics-Standardimplementierung.

## Schritt 1. Einbetten einer Analytics HTML-Seite {#section_0DF847F8BA624CF8A239C10003A39E59}

Beim Erstellen Ihres Facebook Instant Article-Inhalts können Sie den HTML-Inhalt von Analytics in ein iFrame einbetten. Beispiel:

```
<iframe class="no-margin" src="https://[your-domain-here]/analytics.html" height="0"></iframe>
```

## Schritt 2: Bearbeiten Ihrer Analytics-HTML {#section_76707B51D63A47FF833C2D3FFF8412B4}

Mit dem folgenden HTML-Muster können Sie Statistiken aus den Instant Articles verwenden. Diese Datei wird in der Regel auf einem der Webserver Ihres Unternehmens gehostet. Beim Laden eines Instant Articles wird die Datei wie im ersten Schritt erklärt in einen iframe geladen, der das Senden der Analysedaten an Adobe auslöst.

```
<html> 
    <head> 
        <title>Facebook Stats</title> 
        <script language="javaScript" type="text/javascript" src="https://[your-domain-here]/js/VisitorAPI.js"></script> 
        <script language="javaScript" type="text/javascript" src="https://[your-domain-here]/js/AppMeasurement.js"></script> 
    </head> 
    <body> 
        <script> 
            //Standard Variable Configuration 
   var v_orgId = "[your-marketing-cloud-org-id]@AdobeOrg"; 
   var s_account = "[your-report-suite-id]"; 
   var s_trackingServer = "[your-tracking-server]"; 
   var s_visitorNamespace = "[your-namespace]"; 
     
   //Instantiation 
   var visitor = Visitor.getInstance(v_orgId); 
   visitor.trackingServer = s_trackingServer; 
     
   var s = s_gi(s_account); 
   s.account = s_account; 
   s.trackingServer = s_trackingServer; 
   s.visitorNamespace = s_visitorNamespace; 
   s.visitor = visitor; 
     
   //Custom Variables 
   s.pageName = s.Util.getQueryParam("pageName"); 
   s.prop10 = "Facebook Instant Article"; 
       
   //Page View Image Request Call 
   s.t(); 
        </script> 
    </body> 
</html> 
```

**Bearbeiten dieses HTML-Musters für Ihre spezifische Implementierung**

1. Wir empfehlen Ihnen, die neuesten Versionen der unbearbeiteten VisitorAPI.js und AppMeasurement.js auf einem gemeinsamen Verzeichnis auf den Web-Servern Ihres Unternehmens zu hosten.

   Diese Dateien können bei Bedarf auch aus dem Code-Manager in der Analytics-Benutzeroberfläche heruntergeladen werden.

1. Binden Sie Ihre Standardkonfigurationsvariablen Ihrer Analytics-Implementierung ein:

   1. Ihre Experience Cloud-Organisations-ID
   1. die Report Suite-ID, in der der Facebook Instant Article-Traffic erfasst wird
   1. die Domäne des Tracking-Servers Ihres Unternehmens
   1. Ihre Besucher-Namespace-Variable. **Hinweis:** Viele dieser Werte finden Sie in Ihrer Analytics-Standardimplementierung. Der Kundendienst oder Adobe Consulting unterstützen Sie bei Bedarf beim Bereitstellen der entsprechenden Werte.

1. [Legen Sie die benutzerdefinierte Variablen- und Ereignisverfolgung fest](../../implement/js-implementation/analytics-facebook-instant-articles.md#section_932C41BD21154C25B99389299BDF3E0B).
1. Binden Sie die Anforderungssyntax für das Seitenanzeigebild ein `( s.t())`.

## Schritt 3. Festlegen der benutzerdefinierten Variablen- und Ereignisverfolgung {#section_932C41BD21154C25B99389299BDF3E0B}

Benutzerdefinierte Variablen und Ereignisse können über verschiedene Ansätze in Ihrer Analytics-HTML verfolgt werden. Der erste Ansatz sieht vor, die JavaScript-Logik in Ihre benutzerdefinierte Konfiguration einzubinden (ähnlich wie bei der Analytics-Standardimplementierung). Um den Wert einer Eigenschaft festzulegen, verwenden Sie einfach dieselbe Syntax, die Sie in einer normalen Implementierung verwenden würden:

```
s.prop10 = "Facebook Instant Article";
```

Sie können zudem Variablen dynamisch an den iframe senden, indem Sie Abfragezeichenfolgenparameter im iframe `src`-Attribut nutzen. Beispiel:

```
<iframe class="no-margin" src="https://[your-domain-here]/analytics.html?prop1=dynamic%20article%20title&eVar1=facebook%20page%20name&pageName=your%20page%20name%20here&cmpId=your%20campaignID%20here" height="0"></iframe>
```

Those query string parameters can subsequently be set in the custom variables section of your analytics HTML JavaScript by using the `Util.getQueryParam` function within the default [!DNL AppMeasurement] library, as follows:

```
s.pageName = s.Util.getQueryParam("pageName"); 
s.campaign = s.Util.getQueryParam("cmpId"); 
s.eVar1 = s.Util.getQueryParam("eVar1"); 
s.prop1 = s.Util.getQueryParam("prop1"); 
```

## Besucher-Tracking {#section_60F0C77659534949831E85B5FD9AE81E}

Wenn die Analytics HTML-Seite auf Ihrem Web-Server gehostet wird, unterstützt Adobe Ihre vorhandenen Datenschutzrichtlinien in allen Facebook Instant Articles. Wenn sich ein Endbenutzer also vom Tracking auf Ihrer primären Site abmeldet, so wird das Tracking in all Ihren Facebook Instant Articles ohne weiteres Zutun beendet. Auf dieser Dienstprogrammseite wird auch der Identitätsdienst (Besucher-ID) unterstützt, damit Sie die in Ihren Facebook Instant Articles erfassten Metriken und Variablen mit dem Rest der Experience Cloud integrieren können. (An example is for targeted advertising using [!DNL Adobe Audience Manager]).

## Tracking-Einschränkungen {#section_1EE1BB069A3148DB9446371AFE196567}

Bei diesem Ansatz müssen einige Aspekte beachtet werden. Sämtliche DOM-Werte, die in der Regel nur über JavaScript im Facebook Instant Article (z. B. Referrer) verfügbar sind, können im iframe nicht zum Tracking abgerufen werden. Jedoch sollten Standardtechnologieberichte wie Browser, Gerät, Bildschirmgröße oder Auflösung normal funktionieren. Zudem können Sie die pageURL abrufen, indem Sie auf Ihrer Dienstprogrammseite auf [!DNL document.referrer] verweisen.

## Wie geht es weiter? {#section_A170A10E2A3642A784DF720195DA8B38}

[!DNL Adobe Analytics] freut sich, in Zusammenarbeit mit Facebook und unseren Herausgebern branchenführende Analysefunktionen für Herausgeber im mobilen Web für ein deutlich schnelleres Benutzererlebnis bereitzustellen. Wir streben danach, die beste langfristige Lösung für die steigenden Analyseanforderungen unserer Kunden zu entwickeln.

Durch die schnelle Entwicklung des Facebook Instant Article-Projekts ergeben sich häufig Änderungen. Schauen Sie daher regelmäßig vorbei, um sich über Neuerungen zu informieren. Stellen Sie sich auf Änderungen ein, da wir unsere Integrationen weiter verbessern und weitere Herausgeber Facebook Instant Articles anpassen werden. 

Wenn Sie Fragen oder Probleme haben, wenden Sie sich an Ihren Adobe-Berater oder den Kundendienst.
