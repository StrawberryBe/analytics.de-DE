---
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
keywords: Analytics-Implementierung;FAQ;häufig gestellte Fragen;eVar-Gültigkeit;Sichtbarkeit benutzerspezifischer Ereignisse;Zeitstempel;Besucher-ID-Übergangsphase;Besucher-ID;Experience Cloud-Besucher-ID;Analytics-Besucher-ID;DTM;Heartbeat;Cookies;Tracking-Server;Leistung;JavaScript;Datenerfassung;s_code-Version;s_code debuggen;Link-Typen verfolgen;Video verfolgen;mobile App verfolgen;Erstanbieter-Cookies;SSL-Zertifikat;Zertifizierungsgültigkeit;Zertifikatgültigkeit;Plug-ins;Dateneinfüge-API;500-Fehler;500;Benutzer verwalten;Gruppe verwalten;Benutzer;Gruppen
seo-description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
seo-title: Häufig gestellte Fragen zur Implementierung von Analytics
solution: Analytics
title: Häufig gestellte Fragen zur Implementierung von Analytics
topic: Entwickler und Implementierung
uuid: 983d759a-c4f2-4021-84c8-0486dbb951b8
translation-type: ht
source-git-commit: 0143edbcbab3450f6932367f51e9e4c79bc1ae63

---


# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

<table id="table_91790388C2DE4C5E8AEF0B9981AFFE27"> 
 <tbody> 
  <tr> 
   <td> <b>Frage</b> </td> 
   <td> <b>Antwort</b> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Wie verwalte ich Analytics-Benutzer und -Gruppen? </p> </td> 
   <td colname="col3"> <p>Informationen zur Verwaltung von Benutzern und Gruppen finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/reference/user_management.html" format="html" scope="external">Benutzer und Produkte verwalten</a> in der Adobe Experience Cloud-Hilfe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>eVar-Gültigkeit – Warum wird den eVars in den Berichten „Keine“ zugeordnet? </p> </td> 
   <td colname="col3"> <p> <span class="uicontrol"> Läuft ab nach</span> Hier wird ein Zeitraum bzw. ein Ereignis angegeben, nach dem der eVar-Wert abläuft (d. h. er keine Zuweisung von Erfolgsereignissen mehr erhält). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Tritt das Ereignis nicht ein, läuft die Variable auch nicht ab. <a href="https://marketing.adobe.com/resources/help/de_DE/reference/conversion_var_admin.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Sichtbarkeit benutzerdefinierter Ereignisse – Warum werden benutzerdefinierte Ereignisse nicht im Berichtemenü angezeigt? </p> </td> 
   <td colname="col3"> <p>In der Spalte „Sichtbarkeit“ können Sie Standardmetriken (integrierte Metriken), benutzerspezifische Ereignisse und die im Menü, in der Metrikauswahl, im Generator für berechnete Metriken und im Segmentaufbau integrierten Ereignisse ausblenden. Diese Einstellung wirkt sich nicht auf die Datenerfassung für diese Metrik oder das Ereignis aus, sondern nur auf die Sichtbarkeit auf der Benutzeroberfläche. <a href="https://marketing.adobe.com/resources/help/de_DE/reference/metric-visibility.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Zeitstempel – Was muss ich beachten, bevor ich die Einstellungen zum Zeitstempel ändere? </p> </td> 
   <td colname="col3"> <p>Mit der Funktion „Zeitstempel optional“ können Sie Daten mit und ohne Zeitstempel ohne Datenverlust kombinieren. Offline-Daten mit Zeitstempel von einem mobilen Gerät können – mittels eines clientseitigen Zeitstempelaufrufs – mit Daten ohne Zeitstempel einer Live-Webseite kombiniert oder in die Daten jeder Plattform integriert werden. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/timestamps-overview.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Besucher-ID – Wie funktioniert die Übergangsphase, und wie wird sie ermöglicht? </p> </td> 
   <td colname="col3"> <p>Wir empfehlen, eine Übergangsphase zu konfigurieren, wenn mehrere JavaScript-Dateien vorhanden sind, die Daten an dieselbe Report Suite senden, oder wenn Sie für die Site weitere Technologien wie Flash-Videomessung verwenden. <a href="https://marketing.adobe.com/resources/help/de_DE/mcvid/mcvid_grace_period.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Besucher-ID – Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID? </p> </td> 
   <td colname="col3"> <p>Der Identitätsdienst dient der Zuweisung eines eindeutigen, beständigen Identifikators zu sämtlichen Besuchern Ihrer Site. Mit dieser ID können Besucher und deren Daten für andere Lösungen in der Experience Cloud freigegeben werden. Zudem kann diese ID lösungsspezifische IDs wie die Analytics Besucher-ID ersetzen oder verwenden. <a href="https://marketing.adobe.com/resources/help/de_DE/mcvid/mcvid-overview.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Besucher-ID – Wie wird die Besucher-ID festgelegt, wenn Cookies blockiert werden? </p> </td> 
   <td colname="col3"> <p>Wenn das normale s_vi-Cookie nicht verfügbar ist, wird ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen s_fid wird mit einem Ablaufzeitraum von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/visid_fallback.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Dynamic Tag Management – Warum wird meine DTM-Regel nicht ausgelöst? </p> </td> 
   <td colname="col3"> <p>Wenn Ihre ereignisbasierte Regel nicht ausgelöst wird, liegt vermutlich bei der Auswahl oder der Bedingung der Regel ein Fehler vor. Suchen Sie das Element auf Ihrer Website, bei dem die gewünschte Ereignisaktion auftritt, klicken Sie mit der rechten Maustaste und wählen Sie „Element überprüfen“ aus. Überprüfen Sie das markierte Skript im sich öffnenden Feld und stellen Sie sicher, dass das Targeting für das richtige Element erfolgt. <a href="https://marketing.adobe.com/resources/help/de_DE/dtm/c_Troubleshooting.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Wie implementiere ich Heartbeat-Video-Tracking? </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/sc/appmeasurement/hbvideo/" format="https" scope="external"> Dieser Abschnitt</a> enthält Anweisungen zum Herunterladen der Video-Heartbeat-SDKs und Entwickerleitfäden für Ihre Plattform. Laden Sie auch den Entwicklerleitfaden herunter, der beim Herunterladen des SDK im docs-Ordner enthalten ist. Darin finden Sie genaue Anweisungen für Video-Heartbeat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Wie kann ich Cookies der richtigen Subdomäne hinzufügen? </p> </td> 
   <td colname="col3"> Die Variable <span class="varname">cookieDomainPeriods</span> bestimmt, in welcher Domäne die Analytics-Cookies „s_cc“ und „s_sq“ gesetzt werden, indem sie bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen. Siehe [Configuration Variables](/help/implement/js-implementation/c-variables/configuration-variables.md) </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Tracking-Server – Wie fülle ich meinen Tracking-Server korrekt aus? </p> </td> 
   <td colname="col3"> <p>Wenn Sie eine Implementierung konfigurieren, um Daten an Adobe Analytics-Server zu senden, müssen Sie sie an das korrekte Verzeichnis senden. Ansonsten riskieren Sie verfälschte Besucherzahlen oder Datenverlust. <a href="https://helpx.adobe.com/de/analytics/kb/determining-data-center.html" format="https" scope="external"> [Mehr...] </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Leistung: Kann sich ein Fehler beim Laden des externen Adobe JavaScript auf die Leistung auswirken (ob aufgrund der Internetverbindung, des Proxy, der Firewall oder einer Serviceunterbrechung bei Adobe)? </p> </td> 
   <td colname="col3"> <p>Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf die Ausführung von JavaScript auswirkt. Bei Verwendung des Dynamic Tag Managements wird die JavaScript-Datei von Akamai oder einem vom Kunden festgelegten Server bereitgestellt. </p> <p>Informationen hierzu finden Sie auch unter der Frage <i>Reduziert sich durch das Dynamic Tag Management die Leistung meiner Website?</i> im Abschnitt <a href="https://marketing.adobe.com/resources/help/en_US/dtm/faq.html" format="https" scope="external">Häufig gestellte Fragen (FAQ) zum Dynamic Tag Management </a>. </p> <p>Wenn Sie sich nicht auf die CDN von Akamai verlassen möchten, können Sie zusätzlich auch Ihre eigene zentrale Datei zum dynamisches Tag-Management hosten. Lesen Sie hierzu auch <a href="https://marketing.adobe.com/resources/help/de_DE/dtm/deployment.html" format="https" scope="external">Embed Code and Hosting Options</a> (in englischer Sprache). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Leistung: Kann sich durch das Laden des externen Adobe JavaScript die Leistung reduzieren? </p> </td> 
   <td colname="col3"> <p> Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript auf diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden. </p> <p> JavaScript for [!DNL AppMeasurement]-Komprimierung: Falls Sie Bedenken hinsichtlich der Seitengröße des Adobe JavaScript-Clients haben, empfiehlt Adobe die Komprimierung der Datei mit GZIP. GZIP wird in allen gängigen Browsern unterstützt und bietet beim Packen und Entpacken der JavaScript-Hauptdatei <span class="filepath">s_code.js</span> eine höhere Performance als die JavaScript-Komprimierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Leistung: Kann sich durch das Senden von Daten über den Browser an Adobe-Dienste die Leistung reduzieren? </p> </td> 
   <td colname="col3"> <p> Die Adobe JavaScript-Datei erstellt innerhalb der HTML-Seite ein Imageobjekt, das der Browser dann von Adobe-Servern anfordert. Falls der Adobe-Server nun sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Image verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Images durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Leistung: Kann sich ein von Adobe ausgehendes JavaScript-Ereignis auf das Verhalten oder die Funktionalität des Systems auswirken? </p> </td> 
   <td colname="col3"> <p>Nein. Lesen Sie hierzu auch die Antworten zu den vorangegangenen Fragen zur Leistung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> Wie kann ich erfasste Daten basierend auf von mir selbst festgelegten Bedingungen ändern? </td> 
   <td colname="col3"> Die Verwendung von Verarbeitungsregeln erleichtert die Datenerfassung und ermöglicht die Verwaltung der Inhalte, die an die Berichterstellung gesendet werden. <a href="https://marketing.adobe.com/resources/help/de_DE/reference/processing_rules.html" format="https" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Welche ist die aktuelle Version der s_code-Datei? </td> 
   <td> Dieser Abschnitt enthält den Versionsverlauf für [!DNL AppMeasurement]-Bibliotheken von Web- und mobilen Plattformen. Die aktuelle Version jeder Bibliothek kann unter „Reports &amp; Analytics“ &gt; „Admin Tools“ &gt; „Code-Manager“ heruntergeladen werden. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/appmeasurement/release/c_release_notes_javascript.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie kann ich eine s_code-Datei debuggen? </td> 
   <td> Der Adobe Debugger (zuvor DigitalPulse-Debugger) ist ein kostenloses Tool von Adobe, mit dem Sie die auf einer beliebigen Seite Ihrer Site erfassten Daten anzeigen können. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/debugger.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie kann ich unterschiedliche Link-Typen verfolgen? </td> 
   <td> Dateidownloads und Exitlinks können automatisch anhand von Parametern verfolgt werden, die in der AppMeasurement für JavaScript-Datei festgelegt sind. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/function_tl.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie kann ich Videos tracken? </td> 
   <td> JavaScript kann verwendet werden, um eine große Bandbreite an Playern zu verfolgen. Für die Verfolgung mit JavaScript fügen Sie den Code zu der Webseite hinzu, die Ihren Player enthält, und verfolgen den Player mithilfe von Ereignis-Handlern. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/appmeasurement/video/video_js.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie kann ich eine mobile App tracken? </td> 
   <td> In Adobe Mobile Services können Akquise-Links mit eindeutigen Trackingcodes generiert werden. Wenn ein Benutzer eine App aus dem Apple App Store herunterlädt und ausführt, nachdem er auf den generierten Link geklickt hat, sammelt der SDK die Akquise-Daten automatisch und sendet sie an Adobe Mobile Services. <a href="https://marketing.adobe.com/resources/help/de_DE/mobile/ios/acquisition.html" format="http" scope="external"> iOS</a> <a href="https://marketing.adobe.com/resources/help/de_DE/mobile/android/acquisition.html" format="http" scope="external">Android </a> </td> 
  </tr> 
  <tr> 
   <td> Wie implementiere ich Video-Tracking? </td> 
   <td> Sie können Media-Player tracken, indem Sie Funktionen erstellen, die an die Ereignis-Handler von Video-Playern angehängt werden. Damit können Sie zur gegebenen Zeit Media.open, Media.play, Media.stop und Media.close aufrufen. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/appmeasurement/video/video_js_events.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie richte ich Erstanbieter-Cookies ein? </td> 
   <td> Analytics verwendet Cookies, um Informationen zu Variablen und Komponenten zu liefern, die nicht zwischen Bildanfragen und Browsersitzungen bestehen bleiben. Diese harmlosen Cookies stammen aus einer von Adobe gehosteten Domain und werden als Drittanbieter-Cookies bezeichnet. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cert.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wie erhalte ich ein SSL-Zertifikat? </td> 
   <td> Bestimmen Sie, ob an Ihrem Standort https://-Protokolle verwendet werden. Ist dies der Fall, ist die Anforderung eines CSR- und der Erwerb eines SSL-Zertifikats erforderlich. Hinweis: Ein SSL-Zertifikat ist nicht erforderlich, wenn Sie keine sicheren Seiten oder Inhalte haben. Dieser gesamte Schritt kann übersprungen werden, wenn Sie auf Ihrer Seite lediglich das Protokoll „https://“ verwenden. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cert.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Wo finde ich Informationen über die Gültigkeit eines Zertifikats? </td> 
   <td> SSL-Zertifikate laufen jedes Jahr ab, d. h. Adobe fordert in diesem Fall ein aktualisiertes Zertifikat an. Der FPC-Spezialist warnt in diesem Fall ausreichend, dennoch wird eine proaktive Überwachung des Auslaufens empfohlen, sodass Adobe dieses aktualisierte Zertifikat erhält. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_renewals.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Was sind Plug-ins? </td> 
   <td> AppMeasurement für JavaScript-Plug-ins sind Programme oder Funktionen, die verschiedene erweiterte Funktionen durchführen. Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an. Wenn Sie mit JavaScript Daten erfassen möchten, aber nicht genau wissen, wie Sie dabei vorgehen sollen, wenden Sie sich an Ihren Kundenbetreuer. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/impl_plugins.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Informationen zur Dateneinfüge-API? </td> 
   <td> Für das Senden von Daten zu Analytics stellt Adobe mehrere Methoden zur Verfügung. <a href="https://marketing.adobe.com/resources/help/de_DE/reference/usecase_sending_data_to_sc.html" format="http" scope="external"> [Mehr...] </a> </td> 
  </tr> 
  <tr> 
   <td> Was ist ein 500-Fehler? </td> 
   <td> Informationen über den internen Server-Fehler, der den Status „500 Query Error“ verursacht hat. <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/pageType.html" format="http" scope="external">Siehe pageType-Variable </a> </td> 
  </tr> 
 </tbody> 
</table>

| Frage | Antwort |
|---|---|
| Wie verwalte ich Analytics-Benutzer und -Gruppen? | Informationen zum Verwalten von Benutzern und Gruppen finden Sie im Abschnitt zum [Verwalten von Benutzern und Produkten in Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html) in der Hilfe zu den Core Services in Adobe Experience Cloud. |
| eVar-Gültigkeit – Warum wird den eVars in den Berichten „Keine“ zugeordnet? | `Expire After` gibt einen Zeitraum bzw. ein Ereignis an, nach dem der eVar-Wert abgelaufen ist (d. h. er keine Zuweisung von Erfolgsereignissen mehr erhält). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Tritt das Ereignis nicht ein, läuft die Variable auch nicht ab. [[Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| Sichtbarkeit benutzerdefinierter Ereignisse – Warum werden benutzerdefinierte Ereignisse nicht im Berichtemenü angezeigt? | In der Spalte „Sichtbarkeit“ können Sie Standardmetriken (integrierte Metriken), benutzerspezifische Ereignisse und die im Menü, in der Metrikauswahl, im Generator für berechnete Metriken und im Segmentaufbau integrierten Ereignisse ausblenden. Diese Einstellung wirkt sich nicht auf die Datenerfassung für diese Metrik oder das Ereignis aus, sondern nur auf die Sichtbarkeit auf der Benutzeroberfläche. [[Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/metric-visibility.html) |
| Zeitstempel – Was muss ich beachten, bevor ich die Einstellungen zum Zeitstempel ändere? | Mit der Funktion „Zeitstempel optional“ können Sie Daten mit und ohne Zeitstempel ohne Datenverlust kombinieren. Offline-Daten mit Zeitstempel von einem mobilen Gerät können – mittels eines clientseitigen Zeitstempelaufrufs – mit Daten ohne Zeitstempel einer Live-Webseite kombiniert oder in die Daten jeder Plattform integriert werden. [[Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/timestamps-overview.html) |
| Besucher-ID – Wie funktioniert die Übergangsphase, und wie wird sie ermöglicht? | Wir empfehlen, eine Übergangsphase zu konfigurieren, wenn mehrere JavaScript-Dateien vorhanden sind, die Daten an dieselbe Report Suite senden, oder wenn Sie für die Site weitere Technologien wie Flash-Videomessung verwenden.  [Mehr...](https://docs.adobe.com/content/help/de-DE/id-service/using/reference/analytics-reference/grace-period.html) |
| Besucher-ID – Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID? | Der Identitätsdienst dient der Zuweisung eines eindeutigen, beständigen Identifikators zu sämtlichen Besuchern Ihrer Site. Mit dieser ID können Besucher und deren Daten für andere Lösungen in der Experience Cloud freigegeben werden. Zudem kann diese ID lösungsspezifische IDs wie die Analytics Besucher-ID ersetzen oder damit arbeiten.  [Mehr...](https://docs.adobe.com/content/help/de-DE/id-service/using/intro/overview.html) |
| Besucher-ID – Wie wird die Besucher-ID festgelegt, wenn Cookies blockiert werden? | Wenn das normale s_vi-Cookie nicht verfügbar ist, wird ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen s_fid wird mit einem Ablaufzeitraum von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen.  [Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/unique-visitors/visid-fallback.html) |
| Dynamic Tag Management – Warum wird meine DTM-Regel nicht ausgelöst? | Wenn Ihre ereignisbasierte Regel nicht ausgelöst wird, liegt vermutlich bei der Auswahl oder der Bedingung der Regel ein Fehler vor. Suchen Sie das Element auf Ihrer Website, bei dem die gewünschte Ereignisaktion auftritt, klicken Sie mit der rechten Maustaste und wählen Sie „Element überprüfen“ aus. Überprüfen Sie das markierte Skript im sich öffnenden Feld und stellen Sie sicher, dass das Targeting für das richtige Element erfolgt.  [Mehr...](https://docs.adobe.com/content/help/de-DE/dtm/using/admin/c-troubleshooting.html) |
| Wie implementiere ich Heartbeat-Video-Tracking? | [ Dieser Abschnitt](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html) enthält Anweisungen zum Herunterladen der Video-Heartbeat-SDKs und Entwickerleitfäden für Ihre Plattform. Laden Sie auch den Entwicklerleitfaden herunter, der beim Herunterladen des SDK im docs-Ordner enthalten ist. Darin finden Sie genaue Anweisungen für Video-Heartbeat. |
| Wie kann ich Cookies der richtigen Subdomäne hinzufügen? | Die Variable „cookieDomainPeriods“ bestimmt, in welcher Domäne die Analytics-Cookies „s_cc“ und „s_sq“ abgelegt werden, indem sie bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins zur Bestimmung der richtigen Domäne für Cookies der Plug-ins verwendet. Siehe [Konfigurationsvariablen](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/configuration-variables.html) |
| Tracking-Server – Wie fülle ich meinen Tracking-Server korrekt aus? | Wenn Sie eine Implementierung konfigurieren, um Daten an Adobe Analytics-Server zu senden, müssen Sie sie an das korrekte Verzeichnis senden. Ansonsten riskieren Sie verfälschte Besucherzahlen oder Datenverlust. [Mehr...](https://helpx.adobe.com/de/analytics/kb/determining-data-center.html) |
| Leistung: Kann sich ein Fehler beim Laden des externen Adobe JavaScript auf die Leistung auswirken (ob aufgrund der Internetverbindung, des Proxy, der Firewall oder einer Serviceunterbrechung bei Adobe)? | Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf die Ausführung von JavaScript auswirkt. |
| Leistung: Kann sich durch das Laden des externen Adobe JavaScript die Leistung reduzieren? | Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript auf diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden. <br>JavaScript for AppMeasurement-Komprimierung: Falls Sie Bedenken hinsichtlich der Seitengröße des Adobe JavaScript-Clients haben, empfiehlt Adobe die Komprimierung der Datei mit GZIP. GZIP wird in allen gängigen Browsern unterstützt und bietet beim Packen und Entpacken der JavaScript-Hauptdatei `s_code.js` eine höhere Performance als die JavaScript-Komprimierung. |
| Leistung: Kann sich durch das Senden von Daten über den Browser an Adobe-Dienste die Leistung reduzieren? | Die Adobe JavaScript-Datei erstellt innerhalb der HTML-Seite ein Imageobjekt, das der Browser dann von Adobe-Servern anfordert. Falls der Adobe-Server nun sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Image verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Images durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten. |
| Leistung: Kann sich ein von Adobe ausgehendes JavaScript-Ereignis auf das Verhalten oder die Funktionalität des Systems auswirken? | Nein. Lesen Sie hierzu auch die Antworten zu den vorangegangenen Fragen zur Leistung. |
| Wie kann ich erfasste Daten basierend auf von mir selbst festgelegten Bedingungen ändern? | Die Verwendung von Verarbeitungsregeln erleichtert die Datenerfassung und ermöglicht die Verwaltung der Inhalte, die an die Berichterstellung gesendet werden.  ([Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| Welche ist die aktuelle Version der s_code-Datei? | Dieser Abschnitt enthält den Versionsverlauf für AppMeasurement-Bibliotheken von Web- und mobilen Plattformen. Die aktuelle Version jeder Bibliothek kann unter „Analytics“ &gt; „Admin “ &gt; „Code-Manager“ heruntergeladen werden. [Mehr …](/help/implement/appmeasurement-release-notes/c-release-notes-mjs.md) |
| Wie kann ich eine s_code-Datei debuggen? | Der Experience Cloud Debugger ist ein kostenloses Tool von Adobe, mit dem Sie die auf einer beliebigen Seite Ihrer Site erfassten Daten anzeigen können. [Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/implementation/testing-and-validation/debugger.html) |
| Wie kann ich unterschiedliche Link-Typen verfolgen? | Dateidownloads und Exitlinks können automatisch anhand von Parametern verfolgt werden, die in der AppMeasurement für JavaScript-Datei festgelegt sind. [Mehr...](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/function-tl.html) |
| Wie kann ich Videos tracken? | JavaScript kann verwendet werden, um eine große Bandbreite an Playern zu verfolgen. Für die Verfolgung mit JavaScript fügen Sie den Code zu der Webseite hinzu, die Ihren Player enthält, und verfolgen den Player mithilfe von Ereignis-Handlern. [Mehr...](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html) |
| Wie kann ich eine mobile App tracken? | In Adobe Mobile Services können Akquise-Links mit eindeutigen Trackingcodes generiert werden. Wenn ein Benutzer eine App aus dem Apple App Store herunterlädt und ausführt, nachdem er auf den generierten Link geklickt hat, sammelt der SDK die Akquise-Daten automatisch und sendet sie an Adobe Mobile Services. [iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html), [Android](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html) |
| Wie implementiere ich Video-Tracking? | Sie können Media-Player tracken, indem Sie Funktionen erstellen, die an die Ereignis-Handler von Video-Playern angehängt werden. Damit können Sie zur gegebenen Zeit Media.open, Media.play, Media.stop und Media.close aufrufen. [Mehr...](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html) |
| Wie richte ich Erstanbieter-Cookies ein? | Analytics verwendet Cookies, um Informationen zu Variablen und Komponenten zu liefern, die nicht zwischen Bildanfragen und Browsersitzungen bestehen bleiben. Diese harmlosen Cookies stammen aus einer von Adobe gehosteten Domain und werden als Drittanbieter-Cookies bezeichnet. [Mehr...](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cert.html) |
| Wie erhalte ich ein SSL-Zertifikat? | Überprüfen Sie, ob Ihre Site das `https://`-Protokoll verwendet. Ist dies der Fall, ist die Anforderung eines CSR- und der Erwerb eines SSL-Zertifikats erforderlich. Hinweis: Ein SSL-Zertifikat ist nicht erforderlich, wenn Sie keine sicheren Seiten oder Inhalte haben. Dieser gesamte Schritt kann übersprungen werden, wenn Sie auf Ihrer Site ausschließlich das `https://`-Protokoll verwenden.  [Mehr...](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cert.html) |
| Wo finde ich Informationen über die Gültigkeit eines Zertifikats? | SSL-Zertifikate laufen jedes Jahr ab, d. h. Adobe fordert in diesem Fall ein aktualisiertes Zertifikat an. Der FPC-Spezialist warnt in diesem Fall ausreichend, dennoch wird eine proaktive Überwachung des Auslaufens empfohlen, sodass Adobe dieses aktualisierte Zertifikat erhält. [Mehr...](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) |
| Was sind Plug-ins? | AppMeasurement für JavaScript-Plug-ins sind Programme oder Funktionen, die verschiedene erweiterte Funktionen durchführen. Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an. Wenn Sie mit JavaScript Daten erfassen möchten, aber nicht genau wissen, wie Sie dabei vorgehen sollen, wenden Sie sich an Ihren Kundenbetreuer. [Mehr …](/help/implement/js-implementation/c-appmeasurement-js/plugins-support.md) |
| Wo finde ich Informationen zur Dateneinfüge-API? | Für das Senden von Daten zu Analytics stellt Adobe mehrere Methoden zur Verfügung. [Mehr...](https://helpx.adobe.com/de/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
| Was ist ein 500-Fehler? | Informationen zum internen Serverfehler, der den Status „500 Query Error“ verursachte, finden Sie unter [pageType-Variable](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/page-variables.html#concept_F67870238EF74491B5D3909A33CDB985). |