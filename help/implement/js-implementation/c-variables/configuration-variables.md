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
source-git-commit: 9212d70ab8fd7bc0ccfb7e781a92b1731f0a40bd

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

Um Hilfe zu bestimmten Konfigurationsvariablen zu erhalten, klicken Sie auf einen der folgenden Links:

* [s.account](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Geben Sie die Report Suite an, in der Daten gespeichert und berichtet werden.

* [s.dynamicAccountSelection](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Wählen Sie die Report Suite basierend auf der URL der einzelnen Seiten dynamisch aus.

* [s.dynamicAccountList: Specify the rules used for determining the destination report suite.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.dynamicAccountMatch](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Verwenden Sie das DOM-Objekt, um den Abschnitt der URL abzurufen, auf den alle Regeln angewendet werden.

* [s.dynamicVariablePrefix](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Stellen Sie die Kennzeichnung für dynamisch ausgefüllte Variablen bereit.

* [s.charSet](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Konvertieren Sie eingehende Daten zur Speicherung und Berichterstellung in UTF-8.

* [s.currencyCode: Determine the conversion rate to apply to revenue.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.cookieDomain](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Legt fest, welche Domäne die Cookies `s_cc` und `s_sq` Cookies eingestellt werden.

* [s.cookieDomainPeriods: Determine the domain for  and  cookies by specifying the number of periods in the domain of the page URL.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)`s_cc``s_sq`

* [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Geben Sie von JavaScript eingestellte Cookies (`s_sq`, `s_cc`Plug-Ins) an, bei denen es sich um Erstanbieter-Cookies handelt, auch mit Drittanbieter- `2o7.net` oder `omtrdc.net` -Domänen.

* [s.cookieLifetime: Determine lifespan of a cookie as processed by both JavaScript and data collection servers.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.doPlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Refer and allow the function to be called at the appropriate location within the JavaScript file.

* [s.registerPreTrackCallback: Function for taking as parameters both the callback (a function), and the parameters to that function.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.registerPostTrackCallback: Function for taking as parameters both the callback (a function), and the parameters to that function.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.trackDownLoadLinks: Track links to downloadable files on your site.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.trackExternalLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Determine whether any link clicked is an exit link.

* [s.trackInlineStats: Determine whether ClickMap data is gathered.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.linkDownloadFileTypes: Include a comma-separated list of file extensions.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)

* [s.linkInternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Enthält eine kommagetrennte Liste von Filtern, die die Links darstellen, die Teil der Site sind.

* [s.linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Stellen Sie fest, ob die Abfragezeichenfolge in die Berichte Exitlinks und Dateidownload aufgenommen werden soll.

* [s.linkTrackVars](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Include a comma-separated list of variables that are sent with custom, exit, and download links.

* [s.linkExternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Mit dieser Option können Sie Berichte zu einer bestimmten Untergruppe von Ausstiegslinks erstellen.

* [s.usePlugins: Call the  function prior to each image request.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)`s_doPlugins`

