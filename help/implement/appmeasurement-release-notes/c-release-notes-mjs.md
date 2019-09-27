---
description: Gesammelte Versionshinweise für AppMeasurement für JavaScript.
seo-description: Gesammelte Versionshinweise für AppMeasurement für JavaScript.
seo-title: AppMeasurement für JavaScript
solution: Analytics
subtopic: Versionshinweise
title: AppMeasurement für JavaScript
topic: Entwickler und Implementierung
uuid: 1440013d-d266-4dce-9807-8b9adac73315
translation-type: tm+mt
source-git-commit: 3c5cc9275c9978caf57e4e29704e23405ac24b65

---


# AppMeasurement für JavaScript{#appmeasurement-for-javascript}

Cumulative release notes for [!DNL AppMeasurement] for JavaScript.

<!-- 

<p>https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log </p>

 -->

The latest version of each library can be downloaded in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]**.

## Versions 2.17.0

Releasedatum: **23. August 201**

| Funktion/Fehlerbehebung | Beschreibung |
| -----------| ---------- |
| Baidu-Unterstützung wurde hinzugefügt | Unterstützung für die Neuordnung der Baidu-Abfragezeichenfolge wurde hinzugefügt. |
| Fehlerbehebung | Ein Fehler wurde behoben, aufgrund dessen alte Besucherwerte für Aufrufe angezeigt wurden, die vor dem Opt-in in einer Warteschlange warteten. |

## Version 2.16.0

Releasedatum: **15. August 2019**

| Funktion | Beschreibung |
| -----------| ---------- |
| `sendBeacon` Unterstützung für Exitlinks | `sendBeacon`-Unterstützung in [!UICONTROL AppMeasurement] für Exitlinks wurde implementiert. Dies verbessert das Ausstiegs-Linktracking und erhöht wahrscheinlich den Traffic. `SendBeacon` wird nicht im Kontext einer Seite, sondern im Kontext des Browsers ausgeführt. Das heißt, wenn eine Seite mit entladen wird, `sendBeacon`wird die Anforderung dennoch abgeschlossen. Dies ist sehr nützlich für Ausstiegslinks, da es viel wahrscheinlicher wird, dass die Ausstiegslink-Anforderung abgeschlossen wird. |
| ECID/fid-Werte | ECID/fid-Werte werden jetzt beim ersten Treffer zwischengespeichert, auch wenn sich die OptIn-Einstellungen ändern. |
| DIL 9.3 | Zielgruppen-Management Module wurde auf DIL 9.3 aktualisiert |
| Scroll Reach Tracking | Scroll Reach Tracking kann jetzt in s.ActivityMap.trackScrollReach über einen Schalter ein- oder ausgeschaltet werden. |
| Besucher-ID-Dienst 4.4.0 | AppMeasurement wurde für die Verwendung von Besucher-ID-Dienst 4.4.0 aktualisiert. |

## Version 2.15.0

Releasedatum: **15. Juli 2019**

* Activity Map-Verfolgung für Bildlauf zur Activity Map-Erweiterung hinzugefügt (AN-172949)
* DIL 9.2 zu AppMeasurement hinzugefügt (AN-182472)

## Version 2.14.0

Releasedatum: **21. Mai 2019**

* Korrektur von Problemen mit Verwaltung des Status von Trackerparametern, wenn mehrere Treffer ausstehend sind. (AN-176931, AN-176629, DTM-12758)
* Aktualisierung von AppMeasurement, sodass Visitor.js 4.3.0 eingeschlossen ist (AN-180049)

## Version 2.13.0

Releasedatum: **10. April 2019**

Behebung vieler gemeldeter Probleme mit clearVars. Das Problem tritt auf, wenn Treffer gesendet werden, bevor der Tracker bereit ist. Sobald der Tracker fertig ist, kann die Bibliothek Variablen festlegen, die bereits gelöscht oder geändert wurden. (AN-176931, AN-176629, DTM-12758).

## Version 2.12.0

Release Date: **02/22/2019**

* Aktualisiertes Zielgruppen-Management Module auf DIL 9.1. (AN-175255)
* GTM-Sicherheitsrichtlinie gestattet nicht das Activity Map-Modul. (AN-174679)
* Verbesserte AppMeasurement, um die Abmeldung zu berücksichtigen, wenn der Identitätsdienst nicht in der Abmeldung genehmigt wurde. (AN-175259)

## Version 2.11.0

Release Date: **02/11/2019**

* Die Unterstützung für die neue Funktionalität der Opt-in-Dienste in AppMeasurement wurde hinzugefügt. (AN-163546)
* Die Unterstützung zum Speichern von Linktracking-Daten im Sitzungsspeicher wurde hinzugefügt. (AN-162272)
* Der Medien-Streamtyp für Audio Analytics wird nun unterstützt. (AN-173265)

## Version 2.10.0 {#section_0788526EF23049C9AEB1EE5E8FC985DD}

Release Date: **09/20/2018**

This release ensures that the [!DNL AppMeasurement] library submits cookies correctly for all connection types.

* [!DNL AppMeasurement] blockiert die Cookie-Übertragung während des POST-Vorgangs. (AN-165538)
* Drop-Unterstützung für XDomainRequest. (AN-165733)
* Reduce [!DNL AppMeasurement] default cookie lifetime from five to two years. (AN-158572)
* Remove the Media Module from the Code Manager ( [!DNL AppMeasurement]) (AN-166590)

## Version 2.9.0 {#section_E973B8A628F348AA9A1A1599CFE37DB9}

Releasedatum: **24.05.2018**

>[!NOTE]
>
>Visitor API 3.0 or higher is required for customers using the [!DNL Experience Cloud] ID Service. Adobe recommends upgrading to the latest Visitor API version whenever associated code libraries are updated ( [!DNL at.js], [!DNL AppMeasurement.js], and so forth.)

* Updated [!DNL AppMeasurement] to use the updated Visitor interface for requesting IDs. (AN-151483)
* Es wurde ein Problem behoben, durch das nach der Deaktivierung von Linktracking weiterhin ein Linktracking-Cookie erstellt wurde. (AN-156332)
* Es wurde ein Problem behoben, durch das `registerPreTrackCallback` und `registerPostTrackCallback` im Falle von mehrmaligem Aufrufen die Signatur der Rückruffunktion unbrauchbar machten. (AN-158566)

## Version 2.8.2 {#section_B70EAEDAB087464482DB04EC4187200D}

Releasedatum: **12.04.2018**

* Update [!DNL AppMeasurement] to use the updated visitor interface for requesting IDs. (AN-151483)
* Nach der Deaktivierung von Linktracking wird weiterhin ein Linktracking-Cookie erstellt. (AN-156332)
* Reduce [!DNL AppMeasurement] default cookie lifetime from five to two years. (AN-158572)

## Version 2.8.1 {#section_6C1C4091F2EE4C90B6F3D7EE783DD884}

Releasedatum: **29.03.2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

## Version 2.8.0 {#section_A23AD604D34C497C9318D3EB211B7927}

Releasedatum: **15.03.2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

* Bundle VAPI v3.1 with [!DNL AppMeasurement] v2.8. (AN-158353)
* Umgestalteter Aufbau des Datenerfassungsendpunkts zur Vereinfachung der Freigabe. (AN-156647)
* Add request round-trip timing metrics to [!DNL AppMeasurement]. (AN-158343)

## Version 2.7.0 {#section_2C047D410B614CEE950DBBC75F035033}

Releasedatum: **18.01.2018**

* Keine Unterstützung für IE 6 bis 9 mehr
* Aufnahme der Visitor API 3.0.0
* Aufnahme von DIL 7.00

## Version 2.6.0 {#section_229356205EAB4D05890A00B39C42A650}

Releasedatum: **09.11.2017**

Fixed an issue where [!DNL AppMeasurement] library does not always set the correct account combination when s_gl is called. (AN-152153)

## Version 2.5.0 {#section_3C0006D526CA405FA0C47E2D991012BA}

Releasedatum: **21.09.2017**

* Aufnahme von [!DNL dil.js 6.12] ( [!DNL Audience Manager] Modul)

* Aufnahme der Visitor API 2.5.0.

## Version 2.4.0 {#section_60D01A128AEE4A97AC492DF8FBE1E7A3}

Releasedatum: **17.08.2017**

* Enthält dil.js v6.11
* Die Visitor API 2.4.0 wurde hinzugefügt

## Version 2.3.0 {#section_D8F9BFF0D4E44E0F876840360D56E815}

Releasedatum: **20.07.2017**

* Es wurde ein Fehler behoben, durch den [!DNL s.Util.getQueryParam] den Wert # abrief.
* Added v6.10 of [!DNL dil.js] (AN-145701)

## Version 2.2.0 {#section_5E23F21413B1443B9A3021CCC9578C4B}

Releasedatum: **08.06.2017**

* Added support for multiple [!DNL AppMeasurement] instantiation order. (AN-138237)
* Aufnahme von Version 2.2.0 der Visitor API. (AN-144042)

## Version 2.1.0 {#section_5FE53738F9124C86811DFA08923B6F7B}

* Die letzte Version von [!DNL dil.js] wurde hinzugefügt (AN-140396).
* Added support for `adobe_mc_ref` parameter which overrides the page referrer. (AN-131920)
* Die Visitor API 2.1.0 wurde wieder hinzugefügt. (AN-140873)
* Parameter `mcorgid` hinzugefügt. (AN-139586)
* Der Parameter „cp“ (customerPerspective) wurde hinzugefügt. (AN-140897)

## Version 2.0.0 {#section_4C4A502CDFC84F06914EB16CE77736D1}

Releasedatum: **09.03.2017**

* Zu einem neuen Build-Prozess gewechselt, für den eine Aktualisierung der Versionsnummer auf 2.0.0 erforderlich ist. (AN-137878)
* mboxMCSDID-Bearbeitung wurde in die korrekte Stelle verschoben, an der der Tracking-Anruf getätigt wird. (AN-138483)

## Version 1.8.0 {#section_617B2F09F3494C04901E364ACEDE17E1}

Releasedatum: **19.01.2017**

* Visitor API 2.0.0 miteinbeziehen
* Funktionsaufrufe und -überprüfungen wurden neu sequenziert, damit die SDID nach einem vollständigen Überprüfungsabbruch verbraucht wird. (AN-134364)
* Es wurden folgende Prä- und Post-Tracking-Aufruf-Hooks hinzugefügt. (AN-134567)

   * s.registerPreTrackCallback
   * s.registerPostTrackCallback
   Diese Funktionen verwenden als Parameter: den Rückruf (eine Funktion) und die Parameter für diese Funktion. Beispiel:

   ```
   s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
       console.log("pre track callback"); 
       console.dir(requestUrl); // Request URL 
       console.dir(a); // param1 
       console.dir(b); // param2 
       console.dir(c); // param3 
   }, "param1", "param2", "param3");
   ```

   Der Rückruf wird über die `requestUrl` und sämtliche Parameter aufgerufen, die weitergegeben werden, wenn der Rückruf registriert wird. Das geschieht entweder vor oder nach dem Tracking-Anruf, abhängig davon, welche Methode bei der Registrierung des Rückrufs verwendet wird. Die Reihenfolge, in der diese Rückrufe aufgerufen werden, steht nicht fest. Rückrufe, die in der Funktion „Pre“ registriert sind, werden aufgerufen, nachdem die finale Tracking-URL erstellt wurde. Die „Post“-Rückrufe werden auf einen erfolgreichen Tracking-Anruf hin aufgerufen (wenn der Tracking-Anruf fehlschlägt, werden diese Funktionen nicht aufgerufen). Mit `registerPreTrackCallback` registrierte Rückrufe beeinträchtigen den Tracking-Anruf nicht. Außerdem wird das Aufrufen jeglicher Tracking-Methoden in jeglichen registrierten Rückrufen nicht empfohlen, da es zu einer Endlosschleife führen könnte.

## Version 1.7.0 {#section_A93F24391B1043F4A435D1AA76D9E4F0}

Aktualisiert: **10.11.2016**

* Die Visitor API 1.10.1 wurde hinzugefügt.

## Version 1.7.0 {#section_107CDB8468AE4B06B900DCDEE5AD2F0A}

Aktualisiert: **20.10.2016**

* Update [!DNL Audience Manager] module with Demdex Integration Library (DIL) 6.6. (AN-132065)
* Aufnahme der Visitor API 1.9.0. (AN-132072)

## Version 1.7.0 {#section_945311938EE2480A9A697BFE1E5B2AA7}

Aktualisiert: **15.09.2016**

* Update [!DNL AppMeasurement] [!DNL Audience Manager] Module mit DIL 6.5 und zusätzlichen Konfigurationen (AN-129411)

* Aufnahme der Visitor API 1.8.0 (AN-129887)

## Version 1.6.4 {#section_7C40FE01EA5B43E486098FCAC8FA5EC3}

Aktualisiert: **18.08.2016**

* Updated [!DNL AppMeasurement] to read and write AMCV cookies. (AN-127098)
* Aufnahme der Visitor API 1.7.0.

>[!NOTE]
>
>Also see the following release notes for [!DNL JavaScript] version 1.6.3, which includes updated requirements for Experience Cloud ID service.

## Version 1.6.3 {#section_34C75470A84B461A89FEF8CFF7B94090}

Aktualisiert: **04.08.2016**

* Fixed an issue where [!DNL AppMeasurement] prematurely terminated request connections. (AN-126448)

>[!IMPORTANT]
>
>Version 1.6.0 of the [!DNL Experience Cloud] ID service *requires* [!DNL AppMeasurement] for [!DNL JavaScript] version 1.6.3 or higher. If you want to upgrade to version 1.6.0 of the Experience Cloud ID service, please make sure you are using [!DNL AppMeasurement] code verison 1.6.3 or higher.

## Version 1.6.2 {#section_419CBF264B5741DABB005AFDC6197C0D}

Releasedatum: **21. Juli 2016**

* Aufnahme der Visitor API 1.6.0.
* Fixed an issue causing [!DNL AppMeasurement] to call the wrong obfuscated method in the Visitor API. (AN-126006)
* Fixed an issue causing the [!DNL JavaScript] error: "Attribute only valid on v:image". (AN-124009)

<!-- 

<note type="important">
  Adobe strongly recommends upgrading to version 1.6.2 or higher. This version requires Visitor API 1.6.0, and vice-versa. 
</note>

 -->

## Version 1.6.1 {#section_E69F5883F84F4D2CAE25D385F56C6AF6}

Releasedatum:**16. Juni 2016**

Aufnahme der Visitor API 1.5.7.

## Version 1.6.1 {#section_5927689A57164EC99BA501B4FDF0AE8F}

Releasedatum: **19. Mai 2016**

[!DNL JavaScript] Version 1.5.6

* Aufnahme der Visitor API 1.5.6
* Die Behandlung des Klick-Trackings von Links in Firefox, bei der nicht das vollständige Ereignis gestartet wurde, wurde repariert.

## Version 1.6 {#section_B132B272FC2E43E9A24198F459E29403}

Releasedatum: **21. April 2016**

* The [!DNL AppMeasurement] [!DNL Activity Map] module has been integrated in the [!DNL AppMeasurement] standard module, so that you only have to reference one [!DNL .js] file. Außerdem ist die [!DNL Activity Map] Verfolgung standardmäßig aktiviert. (AN-112689)

* Fixed a truncation issue occurring with the order of query-string variables in [!DNL AppMeasurement], so that *`pageURLRest`* is last. (AN-114647)

## Version 1.5.4 {#section_A230E5F656734ABD9917388790A37B5D}

Releasedatum: **17. März 2016**

* Aufnahme der Visitor API 1.5.4
* Abmeldeunterstützung für Visitor API 1.5.4 (und höher)

## Version 1.5.3 {#section_796927A1BBF74DF6A1A4B9477E0BD20E}

Releasedatum: **21. Januar 2016**

* Fixed handling of [!DNL Audience Manager] module when POSTs are used for tracking calls. (AN-115381)
* Der Rest der Seiten-URL („-g“) wurde an das Ende der Abfragezeichenfolge für die Verfolgungsanforderung verschoben. (AN-114647)

## Version 1.5.2 {#section_17CFD0BBC8744447BDFCC833883BC93E}

Releasedatum: **5. November 2015**

* Aufnahme der Visitor API 1.5.3.
* Erkennung von IE11 für URL-Trunkierung 2047 (AN-114914) behoben.

## Version 1.5.1 {#section_432F3C69DDBB49C983D7CB0876C2152F}

Releasedatum: **17. September 2015**

* Aufnahme der Visitor API 1.5.2

## Version 1.5.1 {#section_077DA135C1A5466EB00C44A3C3E472F8}

Releasedatum: **29. August 2015**

* Aufnahme der Visitor API 1.5.1.

## Version 1.5.1 {#section_3C9637EDB058479184731067897E857C}

Releasedatum: **16. Juli 2015**

* Updated [!DNL Audience Manager] module to use AAM DIL 6.2 - getCustomer IDs from VisitorAPI.js and pass them in /event call to AAM. (AN-104978)

## Version 1.5 {#section_8809DBD822E440C6B5B7FF41E5DF3015}

Releasedatum: **18. Juni 2015**

* Unterstützung für Visitor API 1.5, die die Methode *`getCustomerIDs`* verwendet, um Kunden-IDs und authentifizierte Status zu erfassen und die IDs mit Datenerfassungsanforderungen zu senden.
* Fixed the creation of duplicate destinationing iframe in **[!UICONTROL AudienceManagement]** module (DIL 6.1)
* In Version 1.4.5. beschriebenes, bekanntes Problem behoben.

## Version 1.4.5 {#section_FA2E94DF78614ACE9944660E14EF3A75}

Releasedatum: **21. Mai 2015**

<table id="table_E0F3EF51FED44420AC97ACF0684554D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="keyword"> iOS-Erweiterung</span> </p> </td> 
   <td colname="col2"> <p> Starting in <span class="keyword"> iOS </span> SDK version 4.5, a new <span class="keyword"> iOS </span> extension lets you collect usage data from your Apple Watch Apps, Today Widgets, Photo Editing widgets, and all the other <span class="keyword"> iOS </span> extension apps. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/ios_ext.html" format="https" scope="external">Implementieren der iOS-Erweiterung </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="keyword"> Android Wearable-Erweiterung</span> </p> </td> 
   <td colname="col2"> <p> Starting in <span class="keyword"> Android </span> SDK version 4.5, a new <span class="keyword"> Android </span> extension lets you collect data from your <span class="keyword"> Android </span> Wearable app. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/android_wearable.html" format="https" scope="external">Android Wearable-Erweiterung </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

* Aufnahme der Visitor API 1.4.
* AudienceManagement-Modul für die Verwendung von DIL-Version 6.0 aktualisiert.

**Bekanntes Problem**

In den Integrationen Visitor API/ [!DNL AppMeasurement] [!DNL Audience Manager] Module gibt es zwei iFrame-Anfragen zur Veröffentlichung von Zielgruppen, die in IE6-9 gestellt werden: `//fast.<subdomain>.demdex.net/dest5.html` und `//fast.<subdomain>.demdex.net/dest4.html`. The correct behavior, as seen in other browsers, is to only load `//fast.<subdomain>.demdex.net/dest5.html`.

## Version 1.4.4 {#section_C069FA04496C4F7DAC165B04E836CF1F}

Releasedatum: **16. April 2015**

<table frame="all" colsep="1" rowsep="1" id="table_812CAB7DDC364DAABB7CDEDE55532E39"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Benutzerdefinierte Daten mit Lebenszyklusmetriken </p> </td> 
   <td colname="2"> <p>Sie können nun benutzerdefinierte Kontextdaten-Variablen in Lebenszyklusmetriken verwenden. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Beacon tracking support in <span class="keyword"> PhoneGap </span> </p> </td> 
   <td colname="2"> <p>Die Aufrufe <code>trackBeacon</code> und <code>clearCurrentBeacon</code><span class="keyword"> sind jetzt in PhoneGap verfügbar </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Fehlerbehebung hinzugefügt, die die Profil-ID des Light-Server-Aufrufs nach dem Aufruf `trackLight` löscht.

## Version 1.4.3 {#section_C307052BA42248ADB1969AE7A2593177}

Releasedatum: **19. Februar 2015**

* Die Verarbeitung aller verzögerten Tracking-Aufrufe wurde vereinheitlicht. Dadurch werden Probleme mit während der Verzögerung zurückgestellten Variablen, z. B. dem angeklickten Objekt, behoben.
* Geändert, sodass kein automatisches Referrer-Tracking nach dem ersten Tracking-Aufruf stattfindet. Der zweite, dritte usw. Tracking-Aufruf (im Regelfall Linktracking) zählen somit den Referrer nicht doppelt, wenn *`s.referrer`* vor dem ersten Tracking-Aufruf manuell eingestellt wurde.
* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.5.

## Version 1.4.2 {#section_0A0BE40D32144A338231022F97B0E72B}

Releasedatum: **15. Januar 2015**

* Die Verarbeitung des Vorab-Renderings von WebKits wurde korrigiert, um die Verfolgung vorab gerenderter Seiten, die nicht angezeigt werden, zu verhindern.
* The distribution zip was updated to include Visitor API 1.3.4 and an updated **[!UICONTROL AudienceManagement]** module that includes DIL version 5.5.

## Version 1.4.1 {#section_616FF936062F44E8B70032D18AAAFC5F}

Releasedatum: **18. September 2014**

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
   >For an [!DNL Analytics] call to use the POST method instead of the GET method in [!DNL AppMeasurement] (a method of solving [truncated URLs in IE](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html)), you must be using the latest [Visitor ID Service](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid_implement.html) implementation for Experience Cloud.

## Version 1.4 {#section_56ADFF9416B14ABCB3862B00F72B30A1}

Releasedatum: **21. August 2014**

* Das Tracking von Browser-Plug-ins (Abfrage-Parameter `p`) wurde entfernt, da Plug-ins in Version 15 nicht mehr gemeldet werden.
* Addition of the **[!UICONTROL AudienceManagement]** Module in the download zip.

Unterstützung für [zusätzliche eVars](https://marketing.adobe.com/resources/help/en_US/sc/implement/evars_events.html) (76 bis 250) und Ereignisse (101 bis 1000) hinzugefügt.

>[!NOTE]
>
>H-Code unterstützt keine zusätzlichen eVars und Ereignisse.

[!DNL JavaScript]

## Version 1.3.2 {#section_402A4142C4B846DE945FD59DAD9D9298}

Releasedatum: **19. Juni 2014**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* Der Besucher-ID-Dienst 1.3 unterstützt ab sofort neue Funktionen.

## Version 1.3.1 {#section_5E65422B9C1E4437A2473B119A14163E}

Releasedatum: **22. Mai 2014**

* [!DNL AppMeasurement] für [!DNL JavaScript] Funktion nicht korrekt gefunden Instanzen, die mit H-Code erstellt wurden `s_gi``s_gi` . Note that this issue only impacted some dual tagging implementations where [!DNL AppMeasurement] for [!DNL JavaScript] and H code were on the same page with separate instances, and `s_gi` was being used to find instances by report suite.

## Version 1.3 {#section_56B2C625368E4A5BA1E8770A8C78117D}

Releasedatum: **17. April 2014**

* Support for the [Experience Cloud Visitor ID service](https://marketing.adobe.com/resources/help/en_US/mcvid/).

## Version 1.2.4 {#section_94D9521FDBAB4224994B1671A9BD036B}

Releasedatum: **13. März 2014**

* Fehlerbehebungen für Puls-Video.

## Version 1.2.3 {#section_7ED201192D05463DA9B1990EC281B142}

Releasedatum: **20. Februar 2014**

* Fehlerbehebungen für Puls-Video.

## Version 1.2.2 {#section_E6CDDDB8EE214ADCBF3047EC42711F13}

Releasedatum: **6. Februar 2014**

* Fixed a compatibility issue with the [!DNL Audience Manager] DIL module. [!DNL Audience Manager] Kunden müssen auch auf Version 4.8 des DIL-Moduls aktualisieren.

## Version 1.2.1 {#section_6DA9384BC2C84698952D51FFB3732019}

Releasedatum: **15. November 2013**

* Für [Puls-Videomessung](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/) verwendete Seitenereignisse korrigiert.

## Version 1.2 {#section_BDBE0C3D15F04856ABC6F111DDE6C8DB}

Releasedatum: **14. November 2013**

* Erweiterte Unterstützung für [Puls-Videomessungen](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/).
* [!DNL VisitorAPI.js] wurde hinzugefügt, um den [Besucher-ID-Dienst](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_service#.html) zu unterstützen.

## Version 1.1.1 {#section_31F06384039648BB99F4BD630B685794}

* Verhinderte, dass ein Linktracking-Aufruf von Opera-Browsern für Links gesendet wurde, die mit „opera:“ beginnen („opera:“ ähnelt „about:“ und „chrome:“ in anderen Browsern).
* Added `alt=""` to all Image objects to comply with Accessible Video and Communications Act.

## Version 1.1 {#section_4508FF0A14AE46DF96A08B5C6703E123}

Releasedatum: **18. September 2013**

* Problem mit der Unterstützung für das Platzieren des Bibliotheks- und Seiten-Codes im Tag `head` behoben.
* Added missing module `onLoad` support.

## Version 1.0.3 {#section_A74A78C30067480AB36C54A06706DF89}

Releasedatum: **15. August 2013**

* Unterstützung für Implementierung über Adobe Tag-Management hinzugefügt.
* Fixed an issue that prevented hierarchy variables from being set on the [!DNL AppMeasurement] object.

## Version 1.0.2 {#section_C3BDD9A19EF84467A8FDC283AEAE2DB5}

Releasedatum: **18. Juli 2013**

* Hashes/Fragmentbezeichner werden nun beim automatischen Linktracking ignoriert. Previously the following URL was automatically tracked since the entire `href` ended in `.pdf`:

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   Nun werden Hashes/Fragmentbezeichner ignoriert, sodass der Link nur verfolgt wird, wenn der Dateiname mit einer passenden Erweiterung endet.

## Version 1.0.1 {#section_3758B0C47171436ABB4B29F5924BE893}

Releasedatum: **23. Mai 2013**

A new [!DNL JavaScript] [!DNL AppMeasurement] library is now available in Code Manager. Diese Bibliothek bietet die gleichen Kernfunktionen wie [!DNL s_code.js], ist jedoch schlanker und schneller und kann sowohl für mobile als auch für Desktop-Websites verwendet werden.

* 3-bis 7-mal schneller als der H.25-Code.
* Dekomprimiert nur 21 k und komprimiert im GZIP-Format nur 8 k (H.25-Code dekomprimiert 33 k und komprimiert im GZIP-Format 13 k).
* Native Unterstützung des Abrufens von Abfrageparametern, des Lesens und Schreibens von Cookies und des Durchführens des erweiterten Linktrackings.
* Handlich und schnell genug zur Verwendung bei Websites für Mobilgeräte, stabil genug für die Verwendung bei vollwertigem Web für Desktops, ermöglicht Ihnen die Nutzung einer einzigen Bibliothek für alle Webumgebungen.

See [AppMeasurement for Javascript](https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html) in the [!DNL Analytics] Implementation Guide.

>[!NOTE]
>
>Some plug-ins are not supported in this new version. Einzelheiten finden Sie unter [Plug-In-Unterstützung](https://marketing.adobe.com/resources/help/en_US/sc/implement/plugins_support.html).
