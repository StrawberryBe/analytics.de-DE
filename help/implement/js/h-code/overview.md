---
title: H-Code - JavaScript-Implementierung - Übersicht
description: Erfahren Sie mehr über den Arbeitsablauf zur Implementierung von H-Code auf Ihrer Site.
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# H-Code - JavaScript-Implementierung - Übersicht

> [!IMPORTANT] Diese Version der Datenerfassung wird nicht mehr unterstützt. Aktualisieren Sie auf [Adobe Experience Platform Launch](../../launch/overview.md) oder [AppMeasurement for JavaScript](../overview.md).

Sie müssen Zugriff auf Ihre Hostingserver haben, um eine Seite mit Code zur Datenerfassung erfolgreich implementieren zu können. Die folgenden Schritte führen Sie durch eine grundlegende Analytics H-Code-Implementierung.

> [!NOTE] Sie müssen bereits über eine vorhandene Kopie von verfügen, um diese Anweisungen `s_code.js` zu befolgen. Adobe bietet keine Möglichkeit mehr, H-Code im Code-Manager herunterzuladen.

1. **JS-Hauptdateivariablen** aktualisieren: Bearbeiten Sie die `s_code.js` Datei und stellen Sie sicher, dass die folgenden Variablen aktualisiert werden:
   * `s_account` enthält die Report Suite-ID, an die Sie Daten senden möchten. Siehe
   * `s.trackingServer` enthält die Cookies zum Speicherort. Siehe [trackingServer](../../vars/config-vars/trackingserver.md).
2. **Hosten Sie die`s_code.js`Datei auf Ihrer Site**: Diese Datei befindet sich normalerweise zusammen mit anderen Skripten auf Ihrem Webserver.
3. **Referenz`s_code.js`auf allen Seiten**: Stellen Sie sicher, dass alle einzelnen Seiten die JavaScript-Hauptdatei aufrufen, und zwar im HTML- `<body>` Tag (nicht im `<head>` -Tag).
   > [!TIP] H-Code erfordert, dass das `s_code.js` Skript innerhalb des `<body>` -Tags aufgerufen wird. Dies unterscheidet sich von anderen Implementierungsmethoden, von denen die meisten Skriptverweise im Tag `<head>` enthalten sein müssen.
4. **Definieren Sie seitenspezifische Variablen auf jeder Seite**: Für jede Seite sollten einzelne Variablen definiert sein, z. B. Seitenname oder eVars. Einzelne Variablen werden normalerweise mit einem Inline- `<script>` Tag auf jeder Seite definiert.
5. **Verwenden Sie den Debugger, um die Datenerfassung** zu überprüfen: Laden Sie den [Experience Cloud-Debugger](../../validate/debugger.md) herunter und installieren Sie ihn, um sicherzustellen, dass Daten an Adobe gesendet werden und dass Seitenvariablen korrekt definiert sind.

## Zwischenspeicherung

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript in diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden.

## H-Code-Komprimierung

Wenn Sie sich wegen der Downloadgröße der `s_code.js` Datei Sorgen machen, empfiehlt Adobe, die `s_code.js` Datei mit GZIP zu komprimieren. GZIP wird von allen gängigen Browsern unterstützt und bietet eine bessere Leistung als die JavaScript-Komprimierung. Siehe [Apache Module mod_deflate](http://httpd.apache.org/docs/current/mod/mod_deflate.html) in der Apache-Dokumentation.
