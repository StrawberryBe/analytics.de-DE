---
description: Gesammelte Versionshinweise für Flash. Flash-Apps mit „ActionScript“ können am Desktop und im Web gemessen werden.
seo-description: Gesammelte Versionshinweise für Flash. Flash-Apps mit „ActionScript“ können am Desktop und im Web gemessen werden.
seo-title: Flash-Flex
solution: Analytics
subtopic: Versionshinweise
title: Flash-Flex
topic: Entwickler und Implementierung
uuid: 2 ee 7 fb 92-9 b 62-44 d 4-bd 93-6 dff 26764 b 7 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Flash-Flex{#flash-flex}

Gesammelte Versionshinweise für Flash. Flash-Apps mit „ActionScript“ können am Desktop und im Web gemessen werden.

>[!NOTE]
>
>Aktivieren Sie die Debug-Protokollierung, um die aktuelle Bibliotheksversion zu finden.

<!-- 

https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=omtrcache&title=AppMeasurement+Change+Log

 -->

## 20. April 2017 {#section_8521EC2B68E24203A0F1B14A9D2652D2}

**Version 4.0.3 **

* Aufnahme der Visitor API 1.6.1.

## August 18, 2016 {#section_D72EF20672174249B864997905D7552A}

** 4.0.2 - Update**

Aufnahme der Visitor API 1.6.0.

## May 19, 2016 {#section_061305CFC1E040E69E3CDF4078C17AE4}

** 4.0.1 - Update**

Aufnahme der Visitor API 1.5.6

## April 21, 2016 {#section_6EFC6DBEB9E1460DB344A8278F9FC696}

Adobe has released a [security update APSB16-13](https://helpx.adobe.com/security/products/analytics/apsb16-13.html) for the [!DNL AppMeasurement] for Flash library. Durch diese Aktualisierung wurde eine wesentliche Sicherheitslücke in der Bibliothek behoben, die allerdings nur bei Aktivierung von `debugTracking` vorhanden ist und Ihr System für [DOM-basierte XSS-Angriffe](https://www.owasp.org/index.php/DOM_Based_XSS) anfällig macht.

>[!IMPORTANT]
>
>This issue affects [!DNL AppMeasurement] for Flash only when `debugTracking` has been enabled ( `debugTracking` is disabled in the default configuration). **Wenn Sie betroffen sind, empfehlen wir Ihnen dringend,`debugTracking`sofort zu deaktivieren.** Im Folgenden finden Sie einen Beispielcode:

```
public var s:AppMeasurement; 
s = new AppMeasurement(); 
s.debugTracking = false; // set to false or remove line 
                         // for default "disabled” behavior 
```

Betroffene Versionen sind [!DNL AppMeasurement] für Flash Version 4.0 und früher auf allen Plattformen.

>[!NOTE]
>
>Due to security reasons, we will no longer be distributing an AS2 version of [!DNL AppMeasurement] for Flash. Wir unterstützen aber weiterhin die Datenerfassung durch bestehende AS2-Projekte. Wir empfehlen Kunden allerdings dringend, ein Upgrade ihrer Implementierungen auf AS3 durchzuführen und die neuesten Sicherheitsfunktionen von [!DNL AppMeasurement] für Flash zu installieren.

[!DNL AppMeasurement] Für Flash-Kunden, die von diesem Problem betroffen sind, müssen Projekte mit der aktualisierten Bibliothek, die für den Download über die [!DNL Analytics] Konsole [verfügbar ist, neu erstellt werden (](https://help.adobe.com/en_US/Flex/4.0/UsingFlashBuilder/WS6f97d7caa66ef6eb1e63e3d11b6c4d0d21-7feb.html#WS6f97d7caa66ef6eb1e63e3d11b6c4d0d21-7f88) AN -121780)

## November 5, 2015 {#section_18C1A1C82EA844E78A1D563E66DE3FCF}

Version 4.0 - Update:

* Aufnahme der Visitor API 1.5.3.

## September 17, 2015 {#section_319911C0F080452981F8C8BEA2880463}

Version 4.0 - Update:

* Aufnahme der Visitor API 1.5.2.

## August 20, 2015 {#section_1BEA10285E9F4863B89B4B713DBB20DB}

Version 4.0 - Update:

* Aufnahme der Visitor API 1.5.1.

## June 18, 2015 {#section_2ACB18A1693244D6A49B53F4E17F0C30}

Version 4.0 - Update

* Aufnahme der Visitor API 1.5.
* Verwenden Sie die Methode „Visitor API 1.5+ getCustomerIDs“, um Kunden-IDs und den Status der Authentifizierung abzurufen, und senden Sie sie mit Datensammlungsanfragen (AN-102131).

## 21. Mai 2015 {#section_F5EFCC451F13499F9AA53326AE5926F1}

Version 3.9.2 - Update:

* Aufnahme der Visitor API 1.4

## February 19, 2015 {#section_95ADF1725CE7415D956944A28182E69B}

Version 3.9.2:

* Aufnahme der Visitor API 1.3.5.
* Geändert, sodass kein automatisches Referrer-Tracking nach dem ersten Tracking-Aufruf stattfindet. Der zweite, dritte usw. Tracking-Aufruf (im Regelfall Linktracking) zählen somit den Referrer nicht doppelt, wenn *`s.referrer`* vor dem ersten Tracking-Aufruf manuell eingestellt wurde. (AN-92647)
* Removal of deprecated [!UICONTROL Heartbeat] video tracking embedded in the Media module. The supported [!UICONTROL Heartbeat] video tracking has been moved to a separate Video [!DNL Analytics] library.

## September 18, 2014 {#section_80939868A2284961BF620851B000294F}

Version 3.9.1:

* Added cookie support testing to Flash (k = Y/N query-string variable) and pf=1 to query-string when cookie support test is possible (browser with [!DNL JavaScript] access).
* Der Besucher-ID-Dienst 1.3.2 unterstützt ab sofort neue Funktionen.

## 21. August 2014 {#section_F7CA56E42B6548D3BE5A0D020BCEE97A}

Version 3.9:

* Variablen für Längen- und Breitengrad hinzugefügt.
* Der Besucher-ID-Dienst 1.3.1 unterstützt ab sofort neue Funktionen.

## Version 3.8.1 {#section_29A2A0A20D9B43A1B57E5ED299C6EAF3}

Releasedatum: **19. Juni 2014**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* Der Besucher-ID-Dienst 1.3 unterstützt ab sofort neue Funktionen.

## Version 3.8 {#section_3F75C4D0C9BE470B95838DDB2CDCA79F}

Releasedatum: **17. April 2014**

* Unterstützung des [Marketing Cloud-Besucher-ID-Dienstes](https://marketing.adobe.com/resources/help/en_US/mcvid/).

## Version 3.7.3 {#section_1159B2AB56F54903A6FBFB7047AEC1C5}

Releasedatum: **13. März 2014**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## Version 3.7.2 {#section_D6DCE5FE846A45F1A2CED237E8AAEFE9}

Releasedatum: **6. Februar 2014**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## Version 3.7.1 {#section_DC79F108AB5E42189A8EC7D87697AE0B}

Releasedatum: **14. November 2013**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## Version 3.7 {#section_7239878DCD724FD0B9BC900821A4DA96}

Releasedatum: **17. Oktober 2013**

* Unterstützung für [Puls-Video-Tracking](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/).
* VisitorAPI.swc wurde hinzugefügt, um den [Besucher-ID-Dienst](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_service#) zu unterstützen.
* Unterstützung für Flash Player 9 mit ActionScript 3 entfernt. Für ActionScript 3 ist Flash Player-Version 10 (oder höher) erforderlich.

## Version 3.6.2 {#section_57FB21568BDD48F7882F00AD630E6CE8}

Releasedatum: **18. September 2013**

* Interne Änderungen zur Unterstützung eines anstehenden Beta-Releases.

## Version 3.5.5 {#section_149CAF8AF39741C2B9F6A015F7FB8C61}

Releasedatum: **15. August 2013**

* Erneutes In-die-Warteschlange-Versetzen fehlgeschlagener Anfragen deaktiviert, wenn Offline-Tracking deaktiviert ist.

## Version 3.5.4 {#section_3429BD7DE2B64110BEE3A3850E58A0F7}

Releasedatum: **21. Februar 2013**

* Problem mit der URL-Verschlüsselung/-Entschlüsselung in ActionScript 2 behoben.

## Version 3.5.3 {#section_5192BC1C8BF547D1A5A92863686601DD}

Releasedatum: **31. Januar 2013**

* Es werden nun URLs mit mehr als 255 Byte unterstützt, um die Erweiterung des Felds „Seiten-URL“ in den Adobe-Datenerfassungsservern zu unterstützen. Page URLs longer than 255 bytes are split, with the first 255 bytes appearing in the `g=` parameter, with the remaining bytes appearing later in the query sting in the `-g=` query parameter. Damit wird vermieden, dass lange URLs, die im Browser abgeschnitten werden, Vorrang vor anderen Daten haben, während gleichzeitig lange URLs erfasst werden können.

* Eine neue Methode für den Fallback der Besuchererkennung wurde hinzugefügt. Weitere Informationen finden Sie im Abschnitt [Erkennen Unique Visitors](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_identifying_unique_visitors).
* Es wurde ein neues `abort`-Flag hinzugefügt, das in `doPlugins` eingestellt werden kann. Wird dieses Flag auf „true“ gesetzt, fährt die [!DNL AppMeasurement]-Bibliothek nicht mit dem Rückverfolgungsaufruf fort. Das abort-Flag wird bei jedem Rückverfolgungsaufruf zurückgesetzt. Wenn also auch ein nachfolgender Rückverfolgungsaufruf abgebrochen werden muss, muss das Flag erneut in `doPlugins` eingestellt werden.

   ```js
   s.doPlugins = function(s) { 
        s.campaign = s.getQueryParam("cid"); 
        if ((!s.campaign) && (!s.events)) { 
             s.abort = true; 
        } 
   };
   ```

   Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.

## Version 3.5.2 {#section_77727E343EC14B869020358183DAB2DB}

Releasedatum: **8. November 2012**

* Internal updates for [!DNL Audience Manager] integration.

## Version 3.5.1 {#section_F6345AC9F4994D6F97BBCF399B02BB21}

Releasedatum: **22. Oktober 2012**

* Die ActionScript 3-Builds wurden geändert, um Einstellungen für `s.charSet` zu ignorieren, da wir immer UTF-8 verwenden.

## Version 3.5 {#section_7DC183DD46CF42FE85F42E7AB8915D99}

Release Date: **September 13, 2012**
**Important change to variable binding**: In version 3.5, an option to disable variable binding was added for customers who need to start and end literal string values with curly braces. Die Variablenbindung mit geschweiften Klammern wird primär verwendet, wenn OSMF-Videoplayer mit XML-Tags konfiguriert werden:

```
<autoTrackMediaName>{media.player.metadata(https://www.corp1.com/,episodeID)}</autoTrackMediaName>
```

Ein neues Attribut namens `autoBind` ist verfügbar, welches das Standardverhalten in XML-Tags außer Kraft setzt:

```
<autoTrackMediaName autoBind=false>{123}</autoTrackMediaName>
```

Setting `autoBind` to `false` causes the value to be considered a literal string and variable binding is not used. When this attribute is not set to `false` the behavior in XML tags remains the same.

**Auswirkung auf den ActionScript-Code**

Though not commonly used, this syntax is also available to bind [!DNL AppMeasurement] variables in your ActionScript code. If you are unsure whether or not you are using variable binding, search your code for [!DNL AppMeasurement] variable values that start and end with curly braces. Beispiel:

```
s.eVar1 = "{source}";
```

Wenn Sie die Variablenbindung verwenden, sollten Sie diesen Code ändern, damit die neue Methode `bindVariable` angewendet wird:

```
s.bindVariable("eVar1","source");
```

Anstatt jeden Speicherort zu verändern können Sie das Verhalten vor Version 3.5 wiederherstellen, indem Sie `autoBindVariablesByValue` auf „true“ festlegen:

```
s.autoBindVariablesByValue = true;
```

**Weitere Fehlerbehebungen:**

* Korrektur eines Problems, das dazu führen konnte, dass das Video-beendet-Ereignis nicht gesendet wird, wenn eine benutzerspezifische `media.monitor`-Methode verwendet wird, die das Medium-schließen-Ereignis verfolgt:

   ```
   If(media.event==”CLOSE”) { 
   … 
   } 
   ```

## Version 3.4.9 {#section_5F2566CF954242D0A7205DA0B257DABA}

Releasedatum: **19. Juli 2012**

* Added a master-only meta policy, see [https://www.adobe.com/devnet/flashplayer/articles/fplayer9_security.html](https://www.adobe.com/devnet/flashplayer/articles/fplayer9_security.html).

## Version 3.4.8 {#section_7501E04F6A854D50BFF0F287607A796F}

Releasedatum:**21. Juni 2012**

* In AS3-Builds wird nun immer UTF-8 verwendet. Dadurch werden Probleme mit Zeichenfolgen für einige Multibyte-Sprachen verhindert.

## Version 3.4.7 {#section_B26A014D13B14878816472E394FBAAA6}

Releasedatum: **26. April 2012**

Videomessung: Es wurde ein Problem mit inkonsistenten Zeitversatzwerten im Brightcove-Player behoben. Wenn der Zeitversatz jetzt als Null gemeldet wird, verwenden wir beim Abschluss die Länge als Zeitversatz. Damit werden Probleme mit der neuen Methode zur Verfolgung von Abschlüssen mithilfe eines Zeitversatzwerts behoben.

## Version 3.4.6 {#section_273B76A58745486E9715D9F5C2AEC433}

Releasedatum: **19. Januar 2012**

* Aktualisierung der Video-Nachverfolgung: Neue Methode zur Verfolgung von Videoaufrufen mit vollständiger Wiedergabe.

## Version 3.4.5 {#section_DEDF0BEF6BF4458CA00896799E5BA67C}

Releasedatum: **8. September 2011**

* Aktiviert Props mit einem Nullwert „0“. Früher wurden Props mit einem solchen Nullwert nicht gesendet.

## Version 3.4.3 {#section_6C930AA0E95045BCA9AD4096B63657C9}

Releasedatum: **Mai 2011**

* In OSMF wurden Probleme behoben, die bei der Verwendung von Proxy-Plug-ins für die Verfolgung von OSMF-Videoplayer auftraten. Diese Fehlerbehebung aktiviert die Verfolgung von OSMF ProxyElements, wenn das Element, für das sie als Proxy fungieren, nicht verfolgt wird.
* Ein Problem, das beim Messen von Video auf Flash Player 9.0.16 einen Fehler verursachte, wurde behoben.

