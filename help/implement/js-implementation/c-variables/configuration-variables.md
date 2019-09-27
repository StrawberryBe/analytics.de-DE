---
description: Configuration variables set in AppMeasurement.js.
keywords: Analytics-Implementierung
seo-description: Konfigurationsvariablen in AppMeasurement.js für Adobe Analytics eingestellt
seo-title: Konfigurationsvariablen
solution: Analytics
subtopic: Variablen
title: Konfigurationsvariablen
topic: Entwickler und Implementierung
uuid: a19484b6-e350-4c12-b4d6-a31c79a42db0
translation-type: tm+mt
source-git-commit: a340bb50ec437db64dafaddc0b20aec740aee299

---


# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. The most-common configuration variables that are typically set in the main global JavaScript AppMeasurement.js). These variables can be set within the Analytics page-level code and links when appropriate.

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

* [s.dynamicAccountSelection](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-dynaccsel.html): Wählen Sie die Report Suite basierend auf der URL der einzelnen Seiten dynamisch aus.

* [s.dynamicAccountList](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-dynacclist.html): Geben Sie die Regeln an, die zur Bestimmung der Ziel-Report Suite verwendet werden.

* [s.dynamicAccountMatch](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-dynaccmatch.html): Verwenden Sie das DOM-Objekt, um den Abschnitt der URL abzurufen, auf den alle Regeln angewendet werden.

* [s.dynamicVariablePrefix](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-dynvarprefix.html): Stellen Sie die Kennzeichnung für dynamisch ausgefüllte Variablen bereit.

* [s.charSet](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-charset.html): Konvertieren Sie eingehende Daten zur Speicherung und Berichterstellung in UTF-8.

* [s.currencyCode](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-currcode.html): Legen Sie die Konversionsrate fest, die auf den Umsatz angewendet werden soll.

* [s.cookieDomain](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-cookdom.html): Legt fest, welche Domäne die Cookies `s_cc` und `s_sq` Cookies eingestellt werden.

* [s.cookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-cookdomperiods.html): Bestimmen Sie die Domäne für `s_cc` und `s_sq` Cookies, indem Sie die Anzahl der Punkte in der Domäne der Seiten-URL angeben.

* [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-fpcookdomperiods.html): Geben Sie von JavaScript eingestellte Cookies (`s_sq`, `s_cc`Plug-Ins) an, bei denen es sich um Erstanbieter-Cookies handelt, auch mit Drittanbieter- `2o7.net` oder `omtrdc.net` -Domänen.

* [s.cookieLifetime: Determine lifespan of a cookie as processed by both JavaScript and data collection servers.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-cooklifetime.html)

* [s.doPlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-doplugins.html): Rufen Sie die Funktion auf und lassen Sie sie am entsprechenden Speicherort in der JavaScript-Datei aufrufen.

* [s.registerPreTrackCallback: Function for taking as parameters both the callback (a function), and the parameters to that function.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-regpretrackcback.html)

* [s.registerPostTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-regpretrackcback.html): Funktion zur Verwendung sowohl des Callbacks (einer Funktion) als auch der Parameter dieser Funktion als Parameter.

* [s.trackDownLoadLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackdnloadlinks.html): Verfolgen Sie Links zu herunterladbaren Dateien auf Ihrer Site.

* [s.trackExternalLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackextlinks.html): Determine whether any link clicked is an exit link.

* [s.trackInlineStats: Determine whether ClickMap data is gathered.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackinlinestats.html)

* [s.linkDownloadFileTypes: Include a comma-separated list of file extensions.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkdownldftype.html)

* [s.linkInternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkintfilters.html): Enthält eine kommagetrennte Liste von Filtern, die die Links darstellen, die Teil der Site sind.

* [s.linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linklvqrystring.html): Stellen Sie fest, ob die Abfragezeichenfolge in die Berichte Exitlinks und Dateidownload aufgenommen werden soll.

* [s.linkTrackVars](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html): Fügen Sie eine kommagetrennte Liste von Variablen hinzu, die mit benutzerspezifischen, Ausstiegs- und Downloadlinks gesendet werden.

* [s.linkExternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkextfilters.html): Mit dieser Option können Sie Berichte zu einer bestimmten Untergruppe von Ausstiegslinks erstellen.

* [s.usePlugins: Call the  function prior to each image request.](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-useplugins.html)`s_doPlugins`

