---
description: Konfigurationsvariablen, die in AppMeasurement.js festgelegt sind.
keywords: Analytics-Implementierung
seo-description: Konfigurationsvariablen in AppMeasurement.js für Adobe Analytics eingestellt
seo-title: Konfigurationsvariablen
solution: Analytics
subtopic: Variablen
title: Konfigurationsvariablen
topic: Entwickler und Implementierung
uuid: a19484b6-e350-4c12-b4d6-a31c79a42db0
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Die am häufigsten verwendeten Konfigurationsvariablen, die normalerweise in der globalen JavaScript-Datei AppMeasurement.js festgelegt werden. Diese Variablen können gegebenenfalls im Code und in Links auf Seitenebene von Analytics festgelegt werden.

Not all of these variables appear in the code by default when you generate code through the **[!UICONTROL Admin Tool]** &gt; **[!UICONTROL Code Manager]**. Einige dieser Konfigurationsvariablen sind möglicherweise nicht für die Implementierungsanforderungen Ihrer Site geeignet.

Zu den Zielen der Verwendung dieser Konfigurationsvariablen zählen u. a.:

* Tracking mehrerer Sites/Domänen
* Verwenden von Währung für Einkäufe
* Erfassen von Daten in verschiedenen Sprachen
* Link-Tracking (Anzahl heruntergeladener Dateien, Links zu externen Sites)
* Tracking einzigartiger Links für einzigartige Zwecke

>[!NOTE]
>
>[!DNL AppMeasurement] erfordert, dass alle Konfigurationsvariablen vor dem anfänglichen Aufruf der track-Funktion festgelegt werden, `t()`. Wenn Konfigurationsvariablen nach dem Aufruf von festgelegt werden, `t()`können unerwartete Ergebnisse auftreten. To ensure proper data collection, all configuration variables must be above the `doPlugins` function.

Hilfe zu bestimmten Konfigurationsvariablen finden Sie unter den folgenden Links:

* [s_account](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Geben Sie die Report Suite an, in der Daten gespeichert und berichtet werden.

* [s.dynamicAccountSelection](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Dynamically select the report suite based on the URL of each page.

* [s.dynamicAccountList](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Geben Sie die Regeln an, die zur Bestimmung der Ziel-Report Suite verwendet werden.

* [s.dynamicAccountMatch](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Verwenden Sie das DOM-Objekt, um den Abschnitt der URL abzurufen, auf den alle Regeln angewendet werden.

* [s.dynamicVariablePrefix](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Stellen Sie die Kennzeichnung für dynamisch ausgefüllte Variablen bereit.

* [s.charSet](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Konvertieren Sie eingehende Daten zur Speicherung und Berichterstellung in UTF-8.

* [s.currencyCode](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Legen Sie die Konversionsrate fest, die auf den Umsatz angewendet werden soll.

* [s.cookieDomain: Determines which domain the  and  cookies are set.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)`s_cc``s_sq`

* [s.cookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Bestimmen Sie die Domäne für `s_cc` und `s_sq` Cookies, indem Sie die Anzahl der Punkte in der Domäne der Seiten-URL angeben.

* [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Geben Sie von JavaScript eingestellte Cookies (`s_sq`, `s_cc`Plug-Ins) an, bei denen es sich um Erstanbieter-Cookies handelt, auch mit Drittanbieter- `2o7.net` oder `omtrdc.net` -Domänen.

* [s.cookieLifetime: Determine lifespan of a cookie as processed by both JavaScript and data collection servers.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.doPlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Rufen Sie die Funktion auf und lassen Sie sie am entsprechenden Speicherort in der JavaScript-Datei aufrufen.

* [s.registerPreTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Funktion zur Verwendung sowohl des Callbacks (einer Funktion) als auch der Parameter dieser Funktion als Parameter.

* [s.registerPostTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Funktion zur Verwendung sowohl des Callbacks (einer Funktion) als auch der Parameter dieser Funktion als Parameter.

* [s.trackDownLoadLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Verfolgen Sie Links zu herunterladbaren Dateien auf Ihrer Site.

* [s.trackExternalLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Stellen Sie fest, ob ein angeklickter Link ein Exitlink ist.

* [strackInlineStats](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Bestimmen Sie, ob ClickMap-Daten gesammelt werden.

* [s.linkDownloadFileTypes](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Fügen Sie eine kommagetrennte Liste der Dateierweiterungen ein.

* [s.linkInternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Enthält eine kommagetrennte Liste von Filtern, die die Links darstellen, die Teil der Site sind.

* [s.linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Stellen Sie fest, ob die Abfragezeichenfolge in die Berichte Exitlinks und Dateidownload aufgenommen werden soll.

* [s.linkTrackVars](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Fügen Sie eine kommagetrennte Liste von Variablen hinzu, die mit benutzerspezifischen, Ausstiegs- und Downloadlinks gesendet werden.

* [s.linkExternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Mit dieser Option können Sie Berichte zu einer bestimmten Untergruppe von Ausstiegslinks erstellen.

* [s.usePlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Rufen Sie die `s_doPlugins` Funktion vor jeder Bildanforderung auf.

