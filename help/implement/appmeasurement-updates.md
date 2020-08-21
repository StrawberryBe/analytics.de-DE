---
title: Versionshinweise für AppMeasurement für JavaScript
description: Gesammelte Versionshinweise für AppMeasurement für JavaScript.
subtopic: Release notes
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '2123'
ht-degree: 100%

---


# Versionshinweise für AppMeasurement für JavaScript

Gesammelte Versionshinweise für [!DNL AppMeasurement] für JavaScript.

<!-- https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log -->

Sie können die neueste Version von AppMeasurement im [Code-Manager](/help/admin/admin/code-manager-admin.md) herunterladen.

## Version 2.21.0

Releasedatum: **24. Juni 2020**

* Es wurde ein Problem behoben, bei dem der Activity Map-linkExclusions-Filter nicht immer für Firefox angewendet wurde.

## Version 2.20.0

Releasedatum: **5. März 2020**

* Es wurde ein sicherheitsbezogenes Problem behoben, indem die Erkennung von Internet Explorer aktualisiert wurde, um die JSLint-Warnung zu unterdrücken.

## Version 2.19.0

Releasedatum: **21. Februar 2020**

* Aktualisiertes Zielgruppen-Management-Modul auf DIL 9.4. (AN-209341)

## Version 2.18.0

Releasedatum: **13. Februar 2020**

* AppMeasurement kann nun erzwingen, dass Cookies das Secure-Attribut einschließen, indem die [`writeSecureCookies`](vars/config-vars/writesecurecookies.md)-Variable festgelegt wird. Voraussetzung für diese Variable ist, dass die gesamte Client-Website sicher bereitgestellt wird (HTTPS). (AN-204604)

## Version 2.17.0

Releasedatum: **23. August 2019**

* Unterstützung für die Neuordnung der Baidu-Abfragezeichenfolge wurde hinzugefügt. (AN-182483)
* Ein Fehler wurde behoben, aufgrund dessen alte Besucherwerte für Aufrufe angezeigt wurden, die vor dem Opt-in in einer Warteschlange warteten. (AN-184391)

## Version 2.16.0

Releasedatum: **15. August 2019**

* `sendBeacon`-Unterstützung in [!UICONTROL AppMeasurement] für Exitlinks wurde implementiert. Wenn ein Treffer `sendBeacon` verwendet und die Seite entladen wird, ist die Anforderung trotzdem abgeschlossen. Dies ist sehr nützlich für Exitlinks, da es wahrscheinlicher ist, dass der Treffer die Datenerfassungs-Server erreicht. (AN-175142)
* ECID/fid-Werte werden jetzt beim ersten Treffer zwischengespeichert, auch wenn sich die OptIn-Einstellungen ändern. (AN-175142)
* Zielgruppen-Management Modul wurde auf DIL 9.3 aktualisiert. (AN-182704)
* Scroll-Reichweiten-Tracking kann jetzt in `s.ActivityMap.trackScrollReach` über einen Schalter ein- oder ausgeschaltet werden. (AN-182754)
* AppMeasurement wurde für die Verwendung von Besucher-ID-Dienst 4.4.0 aktualisiert. (AN-182912)

## Version 2.15.0

Releasedatum: **15. Juli 2019**

* Scroll-Reichweitenverfolgung für Activity Map zur Activity Map-Erweiterung hinzugefügt (AN-172949)
* DIL 9.2 zu AppMeasurement (AN-182472) hinzugefügt

## Version 2.14.0

Releasedatum: **21. Mai 2019**

* Korrektur von Problemen mit Verwaltung des Status von Trackerparametern, wenn mehrere Treffer ausstehend sind. (AN-176931, AN-176629, DTM-12758)
* Aktualisierung von AppMeasurement, sodass Visitor.js 4.3.0 eingeschlossen ist (AN-180049)

## Version 2.13.0

Releasedatum: **10. April 2019**

* Behebung vieler gemeldeter Probleme mit clearVars. Das Problem tritt auf, wenn Treffer gesendet werden, bevor der Tracker bereit ist. Sobald der Tracker fertig ist, kann die Bibliothek Variablen festlegen, die bereits gelöscht oder geändert wurden. (AN-176931, AN-176629, DTM-12758).

## Version 2.12.0

Releasedatum: **22. Februar 2019**

* Aktualisiertes Zielgruppen-Management-Modul auf DIL 9.1. (AN-175255)
* GTM-Sicherheitsrichtlinie gestattet nicht das Activity Map-Modul. (AN-174679)
* Verbessertes AppMeasurement berücksichtigt Abmeldungen (Opt-out), auch wenn der Identitätsdienst bei der Anmeldung nicht genehmigt wurde. (AN-175259)

## Version 2.11.0

Releasedatum: **11. Februar 2019**

* Die Unterstützung für die neue Funktionalität der Adobe-Opt-in-Dienste in AppMeasurement wurde hinzugefügt. (AN-163546)
* Die Unterstützung zum Speichern von Linktracking-Daten im Sitzungsspeicher wurde hinzugefügt. (AN-162272)
* Der Medien-Streamtyp für Audio Analytics wird nun unterstützt. (AN-173265)

## Version 2.10.0

Releasedatum: **20. September 2018**

In dieser Version wird sichergestellt, dass die [!DNL AppMeasurement]-Bibliothek Cookies für alle Verbindungstypen korrekt sendet.

* [!DNL AppMeasurement] blockiert die Cookie-Übertragung während des POST-Vorgangs. (AN-165538)
* Drop-Unterstützung für XDomainRequest. (AN-165733)
* Die [!DNL AppMeasurement]-Standard-Cookie-Lebensdauer von wurde von fünf auf zwei Jahre reduziert. (AN-158572)
* Das Medienmodul wurde aus dem Code-Manager entfernt ([!DNL AppMeasurement]). (AN-166590)

## Version 2.9.0

Releasedatum: **24. Mai 2018**

>[!NOTE]
>
>Die Visitor API 3.0 oder höher ist erforderlich, damit Kunden den [!DNL Experience Cloud]-ID-Dienst nutzen können. Adobe empfiehlt, ein Upgrade auf die aktuelle Visitor API durchzuführen, wenn die verbundenen Codebibliotheken aktualisiert werden ([!DNL at.js], [!DNL AppMeasurement.js] usw.)

* [!DNL AppMeasurement] wurde aktualisiert, um die Verwendung der aktualisierten Besucheroberfläche für die Anforderung von IDs zu ermöglichen. (AN-151483)
* Es wurde ein Problem behoben, durch das nach der Deaktivierung von Linktracking weiterhin ein Linktracking-Cookie erstellt wurde. (AN-156332)
* Es wurde ein Problem behoben, durch das `registerPreTrackCallback` und `registerPostTrackCallback` im Falle von mehrmaligem Aufrufen die Signatur der Rückruffunktion unbrauchbar machten. (AN-158566)

## Version 2.8.2

Releasedatum: **12. April 2018**

* [!DNL AppMeasurement] wurde aktualisiert, um die aktualisierte Besucheroberfläche für die Anforderung von IDs zu verwenden. (AN-151483)
* Nach der Deaktivierung von Linktracking wird weiterhin ein Linktracking-Cookie erstellt. (AN-156332)
* Die [!DNL AppMeasurement]-Standard-Cookie-Lebensdauer von wurde von fünf auf zwei Jahre reduziert. (AN-158572)

## Version 2.8.1

Releasedatum: **29. März 2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

## Version 2.8.0

Releasedatum: **15. März 2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

* Bundle VAPI v3.1 mit [!DNL AppMeasurement] v2.8. (AN-158353)
* Umgestalteter Aufbau des Datenerfassungsendpunkts zur Vereinfachung der Freigabe. (AN-156647)
* Ergänzung von [!DNL AppMeasurement] durch Metriken für die Anfrage-Umlaufzeit. (AN-158343)

## Version 2.7.0

Releasedatum: **18. Januar 2018**

* Keine Unterstützung für IE 6 bis 9 mehr
* Aufnahme der Visitor API 3.0.0
* Aufnahme von DIL 7.00

## Version 2.6.0

Releasedatum: **9. November 2017**

Es wurde ein Problem behoben, bei dem die [!DNL AppMeasurement]-Bibliothek nicht immer die richtige Kontokombination festgelegt hat, wenn s_gl aufgerufen wurde. (AN-152153)

## Version 2.5.0

Releasedatum: **21. September 2017**

* Aufnahme von [!DNL dil.js 6.12] ([!DNL Audience Manager]-Modul)
* Aufnahme der Visitor API 2.5.0.

## Version 2.4.0

Releasedatum: **17. August 2017**

* Enthält dil.js v6.11
* Die Visitor API 2.4.0 wurde hinzugefügt

## Version 2.3.0

Releasedatum: **20. Juli 2017**

* Fehler behoben, bei dem `s.Util.getQueryParam` `#` erfasst hat
* `dil.js` v6.10 wurde hinzugefügt (AN-145701)

## Version 2.2.0

Releasedatum: **8. Juni 2017**

* Unterstützung für mehrere [!DNL AppMeasurement]-Instanziierungsaufträge. (AN-138237)
* Aufnahme von Version 2.2.0 der Visitor API. (AN-144042)

## Version 2.1.0

Releasedatum: **20. April 2017**

* Die letzte Version von `dil.js` wurde hinzugefügt (AN-140396).
* Der Parameter `adobe_mc_ref`, der die verweisende Stelle der Seite außer Kraft setzt, wird jetzt unterstützt. (AN-131920)
* Die Visitor API 2.1.0 wurde wieder hinzugefügt. (AN-140873)
* Parameter `mcorgid` hinzugefügt. (AN-139586)
* Der Parameter „cp“ (customerPerspective) wurde hinzugefügt. (AN-140897)

## Version 2.0.0

Releasedatum: **9. März 2017**

* Zu einem neuen Build-Prozess gewechselt, für den eine Aktualisierung der Versionsnummer auf 2.0.0 erforderlich ist. (AN-137878)
* mboxMCSDID-Bearbeitung wurde in die korrekte Stelle verschoben, an der der Tracking-Anruf getätigt wird. (AN-138483)

## Version 1.8.0

Releasedatum: **19. Januar 2017**

* Visitor API 2.0.0 miteinbeziehen
* Funktionsaufrufe und -überprüfungen wurden neu sequenziert, damit die SDID nach einem vollständigen Überprüfungsabbruch verbraucht wird. (AN-134364)
* `s.registerPreTrackCallback`- und `s.registerPostTrackCallback`-Hooks hinzugefügt. (AN-134567)

## Version 1.7.0

Aktualisiert: **11. November 2016**

* Die Visitor API 1.10.1 wurde hinzugefügt.
* Aktualisierung des [!DNL Audience Manager]-Moduls mit Demdex Integration Library (DIL) 6.6 (AN-132065)
* Aufnahme der Visitor API 1.9.0. (AN-132072)
* Aktualisierung des [!DNL AppMeasurement] [!DNL Audience Manager]-Moduls mit DIL 6.5 und zusätzlichen Konfigurationen (AN-129411)
* Aufnahme der Visitor API 1.8.0 (AN-129887)

## Version 1.6.4

Aktualisiert: **18. August 2016**

* [!DNL AppMeasurement] wurde aktualisiert, um AMCV-Cookies zu lesen und zu schreiben. (AN-127098)
* Aufnahme der Visitor API 1.7.0.

>[!NOTE]
>
>Siehe auch die folgenden Versionshinweise für [!DNL JavaScript]-Version 1.6.3, die aktualisierte Anforderungen für den Experience Cloud ID-Dienst enthalten.

## Version 1.6.3

Aktualisiert: **4. August 2016**

* Es wurde ein Problem behoben, durch das [!DNL AppMeasurement] Anforderungsverbindungen frühzeitig beendete. (AN-126448)

>[!IMPORTANT]
>
>Version 1.6.0 des [!DNL Experience Cloud] ID-Diensts *erfordert* [!DNL AppMeasurement] für [!DNL JavaScript]-Version 1.6.3 oder höher. Wenn Sie auf Version 1.6.0 des Experience Cloud ID-Diensts aktualisieren möchten, stellen Sie sicher, dass Sie [!DNL AppMeasurement]-Code der Version 1.6.3 oder höher verwenden.

## Version 1.6.2

Releasedatum: **21. Juli 2016**

* Aufnahme der Visitor API 1.6.0.
* Es wurde ein Fehler behoben, durch den [!DNL AppMeasurement] die falsche verschleierte Methode in der Benutzer-API aufgerufen hat. (AN-126006)
* Es wurde ein Problem behoben, durch das der [!DNL JavaScript]-Fehler „Attribut nur gültig für v:image“ ausgelöst wurde. (AN-124009)

## Version 1.6.1

Releasedatum: **16. Juni 2016**

* Aufnahme der Visitor API 1.5.7.
* Die Behandlung des Link-Klick-Trackings in Firefox, bei der nicht das vollständige Ereignis gestartet wurde, wurde repariert.

## Version 1.6

Releasedatum: **21. April 2016**

* Das [!DNL AppMeasurement] Activity Map-Module wurde in das [!DNL AppMeasurement]-Standardmodul integriert, sodass Sie nur noch eine [!DNL .js]-Datei referenzieren müssen. Zusätzlich ist die Activity Map-Verfolgung standardmäßig aktiviert. (AN-112689)
* Ein Kürzungsproblem wurde behoben, das durch die Reihenfolge der Abfragezeichenfolgenvariablen in [!DNL AppMeasurement] entstand, sodass *`pageURLRest`* zuletzt kommt. (AN-114647)

## Version 1.5.4

Releasedatum: **17. März 2016**

* Aufnahme der Visitor API 1.5.4
* Abmeldeunterstützung für Visitor API 1.5.4 (und höher)

## Version 1.5.3

Releasedatum: **21. Januar 2016**

* Feste Behandlung des [!DNL Audience Manager]-Moduls, wenn POSTs zum Verfolgen von Aufrufen verwendet werden. (AN-115381)
* Der Rest der Seiten-URL („-g“) wurde an das Ende der Abfragezeichenfolge für die Verfolgungsanforderung verschoben. (AN-114647)

## Version 1.5.2

Releasedatum: **5. November 2015**

* Aufnahme der Visitor API 1.5.3.
* Erkennung von IE11 für URL-Trunkierung 2047 (AN-114914) behoben.

## Version 1.5.1

Releasedatum: **17. September 2015**

* Aufnahme der Visitor API 1.5.2
* [!DNL Audience Manager]-Modul aktualisiert, um AAM DIL 6.2 zu verwenden – Abrufen von Kunden-IDs aus VisitorAPI.js und Übergeben der IDs bei einem /event-Aufruf an AAM. (AN-104978)

## Version 1.5

Releasedatum: **18. Juni 2015**

* Unterstützung für Visitor API 1.5, die die Methode *`getCustomerIDs`* verwendet, um Kunden-IDs und authentifizierte Status zu erfassen und die IDs mit Datenerfassungsanforderungen zu senden.
* Das Erstellen eines doppelten zielangebenden iFrames im **[!UICONTROL AudienceManagement]**-Modul (DIL 6.1) wurde korrigiert
* In Version 1.4.5. beschriebenes, bekanntes Problem behoben.

## Version 1.4.5

Releasedatum: **21. Mai 2015**

* Die iOS SDK-Version 4.5 enthält eine neue iOS-Erweiterung, die Ihnen das Erfassen der Nutzungsdaten von Ihren Apple Watch-Apps, Today Widgets, Photo Editing Widgets und allen anderen Apps der iOS-Erweiterung erlaubt. Siehe [Implementierung der iOS-Erweiterung](https://docs.adobe.com/content/help/de-DE/mobile-services/ios/ios-ext/ios-ext.html) im Mobile Services-Benutzerhandbuch.
* Die Android SDK-Version 4.5 enthält eine neue Android-Erweiterung, die Ihnen das Erfassen der Nutzungsdaten von Ihrer Android Wearable App ermöglicht. Siehe [Android Wearables](https://docs.adobe.com/content/help/de-DE/mobile-services/android/wearables-android/android-wearable.html) im Mobile Services-Benutzerhandbuch.
* Aufnahme der Visitor API 1.4.
* AudienceManagement-Modul für die Verwendung von DIL-Version 6.0 aktualisiert.

>[!NOTE]
>
>**Bekanntes Problem**: In den Visitor API-/[!DNL AppMeasurement] [!DNL Audience Manager]-Modulintegrationen gibt es zwei iFrame-Anfragen zum Veröffentlichen von Zielgruppen, die in IE6-9 gestellt werden: `//fast.<subdomain>.demdex.net/dest5.html` und `//fast.<subdomain>.demdex.net/dest4.html`. Die richtige Einstellung ist – wie in anderen Browsern – nur Folgendes zu laden: `//fast.<subdomain>.demdex.net/dest5.html`.

## Version 1.4.4

Releasedatum: **16. April 2015**

* Sie können nun benutzerdefinierte Kontextdatenvariablen in Lebenszyklusmetriken verwenden.
* Die Aufrufe `trackBeacon` und `clearCurrentBeacon` sind jetzt in PhoneGap verfügbar.
* Fehlerbehebung hinzugefügt, die die Profil-ID des Light-Server-Aufrufs nach dem Aufruf `trackLight` löscht.

## Version 1.4.3

Releasedatum: **19. Februar 2015**

* Die Verarbeitung aller verzögerten Tracking-Aufrufe wurde vereinheitlicht. Dadurch werden Probleme mit während der Verzögerung zurückgestellten Variablen, z. B. dem angeklickten Objekt, behoben.
* Geändert, sodass kein automatisches Referrer-Tracking nach dem ersten Tracking-Aufruf stattfindet. Der zweite, dritte usw. Tracking-Aufruf (im Regelfall Linktracking) zählen somit den Referrer nicht doppelt, wenn *`s.referrer`* vor dem ersten Tracking-Aufruf manuell eingestellt wurde.
* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.5.

## Version 1.4.2

Releasedatum: **15. Januar 2015**

* Die Verarbeitung des Vorab-Renderings von WebKits wurde korrigiert, um die Verfolgung vorab gerenderter Seiten, die nicht angezeigt werden, zu verhindern.
* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.4 sowie ein aktualisiertes **[!UICONTROL AudienceManagement]**-Modul mit DIL-Version 5.5.

## Version 1.4.1

Releasedatum: **18. September 2014**

* Es wurde eine `tagContainerMarker`-Variable hinzugefügt, die in der Implementierung die Angabe von bis zu 4 Zeichen ermöglicht. Diese Zeichen werden zusammen mit einer zusätzlichen Gedankenstrich-Zeichenbegrenzung an die Versionszeichenfolge angehängt. Diese Variable wird im dynamischen Tag-Management verwendet.

   ```js
   // JavaScript
   s.tagContainerMarker = "D1.0";
   
   // Data Collection request
   //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
   ```

   Die 4 Zeichen sind auf in URL-Dateipfaden zulässige Zeichen beschränkt, dazu zählen beispielsweise alphanumerische Zeichen und Punkte.

* Auf doppelt getaggten Seiten mit H-Code wurde eine Schleife behoben, die während des automatischen Linktrackings auftreten kann (Herunterladen und Beenden), wenn das erzwungene Linktracking aktiviert ist (Standardeinstellung in Webkit-Browsern). Zudem wurde eine allgemeine Schutzmaßnahme für das automatische Linktracking hinzugefügt, um ähnliche Schleifen zu verhindern. Durch diese Schutzmaßnahme wird das automatische Linktracking für wiederholte Klicks auf *dasselbe* Objekt auf ein 10-Sekunden-Intervall beschränkt. Diese Schutzmaßnahme gilt nur für das automatische Linktracking. Demzufolge werden Aufrufe mit manuellem Linktracking (s.tl) nicht beschränkt. Klicks auf verschiedene Objekte sind von dieser Schutzmaßnahme ebenfalls nicht betroffen und werden verfolgt.
* Die Verarbeitung eines angeklickten Objekts mit erforderlicher Verzögerung wurde korrigiert.
* Es wurde ein Problem behoben, das bei einem Aufruf von s.t über eine Link-Klickfunktion zu einer doppelten Seitenansichtszahl geführt hat, wenn die Visitor API noch nicht über die benötigten Werte verfügt.
* HTTP-POST-Unterstützung.

   >[!IMPORTANT]
   >
   >Damit ein [!DNL Analytics]-Aufruf in [!DNL AppMeasurement] die POST-Methode anstelle der GET-Methode verwendet (eine Methode, [gekürzte URLs in IE](https://helpx.adobe.com/de/analytics/kb/shortening-image-request-urls.html) aufzulösen), müssen Sie die neueste Besucher-ID-Dienst-Implementierung für Experience Cloud verwenden.

## Version 1.4

Releasedatum: **21. August 2014**

* Das Tracking von Browser-Plug-ins (Abfrage-Parameter `p`) wurde entfernt, da Plug-ins in Version 15 nicht mehr gemeldet werden.
* Die Download-Zip-Datei wurde um das **[!UICONTROL AudienceManagement]**-Modul ergänzt.
* Unterstützung für zusätzliche eVars (76 bis 250) und Ereignisse (101 bis 1000) hinzugefügt.

>[!NOTE]
>
>H-Code unterstützt diese zusätzlichen eVars und Ereignisse nicht.

## Version 1.3.2

Releasedatum: **19. Juni 2014**

* Die Handhabung der Kennzeichnungen „Fertig“ und „Warten“ für Visitor API-Felder, darunter die veraltete [!DNL Analytics]-Besucher-ID, die Probleme verursachte, wurde korrigiert.
* Der Besucher-ID-Dienst 1.3 unterstützt ab sofort neue Funktionen.

## Version 1.3.1

Releasedatum: **22. Mai 2014**

* [!DNL AppMeasurement] für die Funktion [!DNL JavaScript] `s_gi` konnte Instanzen, die mit dem H-Code `s_gi` erstellt wurden, nicht korrekt finden. Beachten Sie, dass sich dieses Problem nur bei einigen Implementierungen mit dualem Tagging auswirkte, in denen sich [!DNL AppMeasurement] für[!DNL JavaScript] und H-Code auf derselben Seite mit separaten Instanzen befanden und `s_gi` verwendet wurde, um Instanzen nach Report Suite zu finden.

## Version 1.3

Releasedatum: **17. April 2014**

* Unterstützung des [Experience Cloud-Besucher-ID-Dienstes](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html).

## Version 1.2.4

Releasedatum: **13. März 2014**

* Fehlerbehebungen für Puls-Video.

## Version 1.2.3

Releasedatum: **20. Februar 2014**

* Fehlerbehebungen für Puls-Video.

## Version 1.2.2

Releasedatum: **6. Februar 2014**

* Ein Kompatibilitätsproblem mit dem [!DNL Audience Manager]-DIL-Modul wurde behoben. Auch [!DNL Audience Manager]-Kunden müssen ein Update des DIL-Moduls auf Version 4.8 durchführen.

## Version 1.2.1

Releasedatum: **15. November 2013**

* Für die Heartbeat-Videomessung verwendete Seitenereignisse korrigiert.

## Version 1.2

Releasedatum: **14. November 2013**

* Unterstützung für [Heartbeat-Videomessungen](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html) hinzugefügt.
* `VisitorAPI.js` wurde hinzugefügt, um den [Besucher-ID-Dienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) zu unterstützen.

## Version 1.1.1

* Verhinderte, dass ein Linktracking-Aufruf von Opera-Browsern für Links gesendet wurde, die mit „opera:“ beginnen („opera:“ ähnelt „about:“ und „chrome:“ in anderen Browsern).
* Allen Bildobjekten wurde `alt=""` hinzugefügt, um dem Accessible Video and Communications Act zu entsprechen.

## Version 1.1

Releasedatum: **18. September 2013**

* Problem mit der Unterstützung für das Platzieren des Bibliotheks- und Seiten-Codes im Tag `head` behoben.
* Fehlende Unterstützung für Modul `onLoad` wurde hinzugefügt.

## Version 1.0.3

Releasedatum: **15. August 2013**

* Unterstützung für Implementierung über Adobe Tag-Management hinzugefügt.
* Ein Problem wurde behoben, bei dem verhindert wurde, dass Hierarchievariablen für das [!DNL AppMeasurement]-Objekt festgelegt wurden.

## Version 1.0.2

Releasedatum: **18. Juli 2013**

* Hashes/Fragmentbezeichner werden nun beim automatischen Linktracking ignoriert. Zuvor wurde die folgende URL automatisch verfolgt, weil das gesamte `href` auf `.pdf` endete:

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   Nun werden Hashes/Fragmentbezeichner ignoriert, sodass der Link nur verfolgt wird, wenn der Dateiname mit einer passenden Erweiterung endet.

## Version 1.0.1

Releasedatum: **23. Mai 2013**

Eine neue [!DNL JavaScript] [!DNL AppMeasurement]-Bibliothek ist jetzt im Code-Manager verfügbar. Diese Bibliothek bietet die gleichen Kernfunktionen wie [!DNL s_code.js], ist jedoch schlanker und schneller und kann sowohl für mobile als auch für Desktop-Websites verwendet werden.

* 3-bis 7-mal schneller als der H.25-Code.
* Dekomprimiert nur 21 k und komprimiert im GZIP-Format nur 8 k (H.25-Code dekomprimiert 33 k und komprimiert im GZIP-Format 13 k).
* Native Unterstützung des Abrufens von Abfrageparametern, des Lesens und Schreibens von Cookies und des Durchführens des erweiterten Linktrackings.
* Handlich und schnell genug zur Verwendung bei Websites für Mobilgeräte, stabil genug für die Verwendung bei vollwertigem Web für Desktops, ermöglicht Ihnen die Nutzung einer einzigen Bibliothek für alle Webumgebungen.
