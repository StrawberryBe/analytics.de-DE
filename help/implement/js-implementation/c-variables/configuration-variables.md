---
description: Konfigurationsvariablen, die in AppMeasurement.js festgelegt sind.
keywords: Analytics-Implementierung
seo-description: Konfigurationsvariablen, die in AppMeasurement.js für Adobe Analytics eingestellt sind
seo-title: Konfigurationsvariablen
solution: Analytics
subtopic: Variablen
title: Konfigurationsvariablen
topic: Entwickler und Implementierung
uuid: a19484b6-e350-4c12-b4d6-a31c79a42db0
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Konfigurationsvariablen Überblick

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Die häufigsten Konfigurationsvariablen, die in der Regel im globalen JavaScript (AppMeasurement.js) festgelegt werden. Diese Variablen können bei Bedarf in Code und Links auf Ebene der Analytics-Seite festgelegt werden.

Nicht alle dieser Variablen werden standardmäßig im Code angezeigt, wenn Sie Code über **[!UICONTROL Admin Tool]** &gt; **[!UICONTROL Code-Manager]** generieren. Einige dieser Konfigurationsvariablen sind möglicherweise nicht für die Implementierungsanforderungen Ihrer Site geeignet.

Zu den Zielen der Verwendung dieser Konfigurationsvariablen zählen u. a.:

* Tracking mehrerer Sites/Domänen
* Verwenden von Währung für Einkäufe
* Erfassen von Daten in verschiedenen Sprachen
* Link-Tracking (Anzahl heruntergeladener Dateien, Links zu externen Sites)
* Tracking einzigartiger Links für einzigartige Zwecke

> [!NOTE][!DNL AppMeasurement]Für  müssen alle Konfigurationsvariablen vor dem ersten Aufruf der Tracking-Funktion (`t()`) eingestellt werden. Wenn Konfigurationsvariablen nach dem Aufruf von `t()` festgelegt werden, können unerwartete Ergebnisse auftreten. Um eine korrekte Datenerfassung sicherzustellen, müssen alle Konfigurationsvariablen über der Funktion `doPlugins` liegen:

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

* [s.cookieLifetime](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-cooklifetime.html): Legen Sie die Lebensdauer eines Cookies fest, die sowohl von JavaScript- als auch von Datenerfassungsservern verarbeitet wird.

* [s.doPlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-doplugins.html): Rufen Sie die Funktion auf und lassen Sie sie am entsprechenden Speicherort in der JavaScript-Datei aufrufen.

* [s.registerPreTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-regpretrackcback.html): Funktion zur Verwendung als Parameter sowohl den Rückruf (eine Funktion) als auch die Parameter dieser Funktion.

* [s.registerPostTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-regpretrackcback.html): Funktion zur Verwendung als Parameter sowohl den Rückruf (eine Funktion) als auch die Parameter dieser Funktion.

* [s.trackDownLoadLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackdnloadlinks.html): Verfolgen Sie Links zu herunterladbaren Dateien auf Ihrer Site.

* [s.trackExternalLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackextlinks.html): Stellen Sie fest, ob ein angeklickter Link ein Exitlink ist.

* [s.trackInlineStats](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-trackinlinestats.html): Bestimmen Sie, ob ClickMap-Daten gesammelt werden.

* [s.linkDownloadFileTypes](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkdownldftype.html): Fügen Sie eine kommagetrennte Liste der Dateierweiterungen ein.

* [s.linkInternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkintfilters.html): Enthält eine kommagetrennte Liste von Filtern, die die Links darstellen, die Teil der Site sind.

* [s.linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linklvqrystring.html): Stellen Sie fest, ob die Abfragezeichenfolge in die Berichte Exitlinks und Dateidownload aufgenommen werden soll.

* [s.linkTrackVars](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html): Fügen Sie eine kommagetrennte Liste von Variablen hinzu, die mit benutzerspezifischen, Ausstiegs- und Downloadlinks gesendet werden.

* [s.linkExternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkextfilters.html): Mit dieser Option können Sie Berichte zu einer bestimmten Untergruppe von Ausstiegslinks erstellen.

* [s.usePlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-useplugins.html): Rufen Sie die `s_doPlugins` Funktion vor jeder Bildanforderung auf.

