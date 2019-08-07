---
description: Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.
keywords: Analytics-Implementierung; javascript; Javascript-Implementierung; appmeasurement; Appmeasurement herunterladen; Identitätsdienst; visitorapi. js; caching; Appmeasurement-Komprimierung
seo-description: Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.
seo-title: Übersicht über javascript-Implementierung
solution: Analytics
title: Übersicht über javascript-Implementierung
topic: Entwickler und Implementierung
uuid: bb 661 d 8 c-faf 9-4454-ac 3 c -0 c 1 a 4 c 0 a 9336
translation-type: tm+mt
source-git-commit: 883eb12c6c0f9b566dd485227d19cee16d9cfadc

---


# Übersicht über javascript-Implementierung

Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.

The easiest and recommended way to send data to [!DNL Analytics] is by using [Launch](/help/implement/implement-with-launch/create-analytics-property.md). In einigen Fällen bevorzugen Sie eventuell die ältere JavaScript-Methode zur Implementierung von Analytics.

>[!NOTE]
>
>In diesem Abschnitt wird die alte Methode zur Implementierung von Analytics beschrieben. All Analytics customers have access to [Launch](/help/implement/implement-with-launch/create-analytics-property.md), which is the standard method to deploy Experience Cloud tags.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

Um eine Seite mit Code zur Erfassung von Daten erfolgreich zu implementieren, müssen Sie über Zugriff auf Ihre Hostingserver verfügen, um neue Inhalte auf Ihre Website hochladen zu können. Außerdem ist es auch nützlich, wenn für die Implementierung von Code bereits eine Site vorhanden ist. 

Anhand der folgenden Schritte werden Sie durch eine grundlegende Analytics-Implementierung geführt.

| Aufgabe | Beschreibung |
|--- |--- |
| 1. Laden Sie appmeasurement für javascript und den ID-Dienst herunter. | Melden Sie sich über die Experience Cloud bei Analytics an. Die Downloaddatei ist unter Analytics &gt; Admin &gt; Code-Manager verfügbar. Die ZIP-Datei zum Download enthält mehrere Dateien. AppMeasurement.js und VisitorAPI.js sind zum Implementieren von Analytics relevant. |
| 2. Richten Sie den Identitätsdienst ein. (ehemals Besucher-ID-Service) | Siehe [Einrichten des Identitätsdiensts für Analytics](https://docs.adobe.com/content/help/en/id-service/using/home.html) |
| Aktualisieren `AppMeasurement.js`. | Copy the [example AppMeasurement.js code](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_4351543F2D6049218E18B48769D471E2) and paste it at the beginning of your `AppMeasurement.js` file. Aktualisieren Sie mindestens die folgenden Variablen:<ul><li>s.account="INSERT-RSID-HERE"</li><li>s.trackingServer="INSERT-TRACKING-SERVER-HERE"</li><li>s.visitorNamespace = "INSERT-NAMESPACE-HERE"</li><li>s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE")</li></ul><br>Siehe [Korrektes Füllen der Variablen trackingserver und trackingserversecure](https://helpx.adobe.com/analytics/kb/determining-data-center.html) oder wenden Sie sich an den Kundendienst, wenn Sie bezüglich eines dieser Werte nicht sicher sind. Wenn diese nicht korrekt eingestellt sind, werden Daten nicht von Ihrer Implementierung erfasst.</br> |
| 3. Host `AppMeasurement.js` und `VisitorAPI.js`. | Diese Core-JavaScript-Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Website zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien. |
| 4. Reference `AppMeasurement.js` and `VisitorAPI.js`  on all site pages. | <ul><li>Include the Visitor ID Service by adding the following line of code in the `head` or `body` tag on each page. `VisitorAPI.js` muss vor `AppMeasurement.js`:`script language="JavaScript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js"`</li><li>Include AppMeasurement for JavaScript by adding the following line of code in the `head` or `body` tag on each page: `script language="JavaScript" type="text/javascript"  src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"`</li></ul> |
| 5. Aktualisieren und Bereitstellen der Seiten-Code. | Copy the [Example Page Code](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7) and paste it just after the opening `body` tag on each page you want to track. Aktualisieren Sie mindestens die folgenden Variablen:<ul><li>var s=s_gi("INSERT-RSID-HERE")</li><li>s. pagename = "INSERT-NAME-HERE" (z. B. s. pagename = document. title)</li></ul> |
| 6. Überprüfen Sie mit dem Experience Cloud-Debugger, ob Daten gesendet werden. | Install the [Experience Cloud Debugger](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html#concept_B26FFE005EDD4E0FACB3117AE3E95AA2). Laden Sie anschließend eine Seite, auf der Sie den Seiten-Code bereitgestellt haben, und öffnen Sie den Debugger. Der Debugger zeigt Information darüber an, welche erfassten Daten gesendet wurden. |

## Zwischenspeicherung {#section_4E2D1D962DF046418134C43CFC49AD4A}

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript in diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden.

## Komprimierung bei JavaScript für AppMeasurement {#section_C10BBC84C81C414088F97363D29E021B}

Wenn Sie die Seitengröße mit H-Code reduzieren möchten(AppMeasurement für JavaScript 1.0 ist vorkomprimiert), empfiehlt Adobe, die Datei mittels GZIP zu komprimieren. GZIP wird in allen gängigen Browsern unterstützt und bietet beim Packen und Entpacken der JavaScript-Hauptdatei [!DNL s_code.js] eine höhere Performance als die JavaScript-Komprimierung.

Unter den folgenden Links wird erklärt, wie Sie die Komprimierung des [!DNL s_code.js]-JavaScript-Codes auf Ihrer Website per GZIP durchführen können:

[Apache Module mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html) (in englischer Sprache)

[Enabling gzip compression with Tomcat and Flex](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/) (in englischer Sprache)
