---
description: Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.
keywords: Analytics Implementation;javascript;javascript implementation;appmeasurement;download appmeasurement;Identity Service;visitorapi.js;caching;appmeasurement compression
title: Übersicht über die JavaScript-Implementierung
topic: Developer and implementation
uuid: bb661d8c-faf9-4454-ac3c-0c1a4c0a9336
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Übersicht über die JavaScript-Implementierung

Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.

Die einfachste und empfohlene Methode zum Senden von Daten an [!DNL Analytics] ist die Verwendung von [Launch](/help/implement/implement-with-launch/create-analytics-property.md). In einigen Fällen bevorzugen Sie eventuell die ältere JavaScript-Methode zur Implementierung von Analytics.

> [!NOTE] In diesem Abschnitt wird die alte Methode zur Implementierung von Analytics beschrieben. Alle Analytics-Kunden haben Zugriff auf [Launch](/help/implement/implement-with-launch/create-analytics-property.md), wobei es sich um die Standardmethode für das Bereitstellen von Experience Cloud-Tags handelt.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

Um eine Seite mit Code zur Erfassung von Daten erfolgreich zu implementieren, müssen Sie über Zugriff auf Ihre Hostingserver verfügen, um neue Inhalte auf Ihre Website hochladen zu können. Außerdem ist es auch nützlich, wenn für die Implementierung von Code bereits eine Site vorhanden ist.

Anhand der folgenden Schritte werden Sie durch eine grundlegende Analytics-Implementierung geführt.

| Aufgabe | Beschreibung |
|--- |--- |
| 1. Laden Sie AppMeasurement für JavaScript und den ID-Service herunter. | Melden Sie sich bei Analytics über Experience Cloud an. Die Download-Datei ist unter „Analytics“ &gt; „Admin“ &gt; „Code-Manager“ verfügbar.  Die ZIP-Datei zum Download enthält mehrere Dateien.  AppMeasurement.js und VisitorAPI.js sind zum Implementieren von Analytics relevant. |
| 2. Richten Sie den Identitätsdienst ein. (Zuvor Besucher-ID-Dienst) | See [Set up the Identity Service for Analytics](https://docs.adobe.com/content/help/en/id-service/using/home.html) |
| 3. Aktualisieren Sie `AppMeasurement.js` | Copy the [example AppMeasurement.js code](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_4351543F2D6049218E18B48769D471E2) and paste it at the beginning of your `AppMeasurement.js` file. Aktualisieren Sie mindestens die folgenden Variablen:<ul><li>s.account="INSERT-RSID-HERE"</li><li>s.trackingServer="INSERT-TRACKING-SERVER-HERE"</li><li>s.visitorNamespace = "INSERT-NAMESPACE-HERE"</li><li>s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE")</li></ul><br>Siehe [Korrektes Füllen der Variablen](https://helpx.adobe.com/analytics/kb/determining-data-center.html) trackingServer und trackingServerSecure oder wenden Sie sich an ClientCare, wenn Sie sich bezüglich eines dieser Werte nicht sicher sind. Wenn diese nicht korrekt eingestellt sind, werden Daten nicht von Ihrer Implementierung erfasst.</br> |
| 4. Hosten Sie `AppMeasurement.js` und `VisitorAPI.js`. | Diese Core-JavaScript-Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Website zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien. |
| 5. Verweisen Sie auf allen Seiten der Website auf `AppMeasurement.js` und `VisitorAPI.js`. | <ul><li>Integrieren Sie den Besucher-ID-Service, indem Sie dem Tag `head` oder `body` auf jeder Seite die folgende Codezeile hinzufügen. (`VisitorAPI.js` muss vor `AppMeasurement.js` integriert werden).<br>`script language="JavaScript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js"`</br></li><li>Integrieren Sie den AppMeasurement für JavaScript, in dem Sie dem Tag `head` oder `body` auf jeder Seite die folgende Codezeile hinzufügen:<br>`script language="JavaScript" type="text/javascript"  src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"`</br></li></ul> |
| 6. Aktualisieren Sie den Seiten-Code und stellen Sie ihn bereit. | Copy the [Example Page Code](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7) and paste it just after the opening `body` tag on each page you want to track. Aktualisieren Sie mindestens die folgenden Variablen:<ul><li>var s=s_gi("INSERT-RSID-HERE")</li><li>s.pageName="INSERT-NAME-HERE" (for example, s.pageName=document.title)</li></ul> |
| 7. Prüfen Sie mit dem Experience Cloud-Debugger, ob Daten gesendet werden. | Installieren Sie den [Experience Cloud-Debugger](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html#concept_B26FFE005EDD4E0FACB3117AE3E95AA2). Laden Sie anschließend eine Seite, auf der Sie den Seiten-Code bereitgestellt haben, und öffnen Sie den Debugger. Der Debugger zeigt Information darüber an, welche erfassten Daten gesendet wurden. |

## Zwischenspeicherung {#section_4E2D1D962DF046418134C43CFC49AD4A}

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript in diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden.

## Komprimierung bei JavaScript für AppMeasurement {#section_C10BBC84C81C414088F97363D29E021B}

Wenn Sie die Seitengröße mit H-Code reduzieren möchten (AppMeasurement für JavaScript 1.0 ist vorkomprimiert), empfiehlt Adobe, die Datei mittels GZIP zu komprimieren. GZIP wird in allen gängigen Browsern unterstützt und bietet beim Packen und Entpacken der JavaScript-Hauptdatei [!DNL s_code.js] eine höhere Performance als die JavaScript-Komprimierung.

Unter den folgenden Links wird erklärt, wie Sie die Komprimierung des [!DNL s_code.js]-JavaScript-Codes auf Ihrer Website per GZIP durchführen können:

[Apache Module mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html) (in englischer Sprache)

[Enabling gzip compression with Tomcat and Flex](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/) (in englischer Sprache)
