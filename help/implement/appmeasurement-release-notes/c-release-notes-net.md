---
description: 'null '
seo-description: 'null '
seo-title: Windows Silverlight, NET, IIS, XBOX
solution: Analytics
subtopic: Versionshinweise
title: Windows Silverlight, NET, IIS, XBOX
topic: Entwickler und Implementierung
uuid: 15 c 20 bca -4886-4 d 77-9957-fe 99743851 ea
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Windows Silverlight, NET, IIS, XBOX{#windows-silverlight-net-iis-xbox}

>[!IMPORTANT]
>
>Diese sdks wurden sunset und werden nicht mehr von Adobe unterstützt oder verteilt.

>[!NOTE]
>
>Aktivieren Sie die Debug-Protokollierung, um die aktuelle Bibliotheksversion zu finden.

## Version 1.4.2 {#section_2B70F52C4D214A43844CCEC6B45037F0}

Releasedatum: **August 2014**

* Removed support for the [!DNL Microsoft Silverlight Analytics Framework]. Adobe is no longer supporting or distributing the [!DNL Microsoft Silverlight Analytics Framework] integration for [!DNL AppMeasurement].

* Es wurden interne Veränderungen zur Unterstützung neuer Funktionen vorgenommen.

## Version 1.4.1 {#section_9134F77804BF472291DA7243FAC89C2B}

Releasedatum: **März 2013**

* Fixed exception with getting default referrer in [!DNL Silverlight] outside of a browser context and properly exposed SSL property in the [!DNL Microsoft Silverlight Analytics Framework] component.

## Version 1.4 {#section_2F4ADA4628EC43B480177C3DDB3D1CFA}

Releasedatum: **Februar 2013**

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

## Version 1.3.8 {#section_03089199E2DE4199B32F6821DDAED7BD}

Releasedatum: **September 2012**

* Korrektur eines Problems, das dazu führen konnte, dass das Video-beendet-Ereignis nicht gesendet wird, wenn eine benutzerspezifische `media.monitor`-Methode verwendet wird, die das Medium-schließen-Ereignis verfolgt:

   ```
   If(media.event==”CLOSE”) { 
   … 
   } 
   ```

## Version 1.3.7 {#section_32AA8AE0CED4495496D25BF9246AE8AB}

Releasedatum: **April 2012**

* Hinzugefügte Unterstützung für [!DNL XBOX].

## Version 1.3.6 {#section_9F2738FA31CD48C4877AB92281EC67A9}

Releasedatum: **Februar 2012**

* [!DNL iOS] Phone 7: Ein Fehler wurde behoben, bei dem offlineThrottleDelay nicht richtig angewandt wurde.
* Ein Zeitstempel wurde zu Variablen hinzugefügt, die mit geringeren Verfolgungsaufrufen (trackLight) verwendet werden.

## Version 1.3.5 {#section_28BBDE7D187547A4AACCA60E5154DCD2}

Releasedatum: **Januar 2012**

* Aktualisierung der Video-Nachverfolgung: Neue Methode zur Verfolgung von Videoaufrufen mit vollständiger Wiedergabe. Siehe [Videos in Adobe Analytics messen](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/index.html).

## Version 1.3.4 {#section_43788EE6B57E4B2DBEED68BE6954D9CA}

* New support and build for [!DNL iOS] Phone platform including offline tracking.
* Unterstützung für den doRequest-Delegate, um außer Kraft zu setzen, wie Anforderungen für Verfolgungsdaten gesendet werden.
* Unterstützung für contextData, welches die Verarbeitungsregeln auf Serverseite (nur v15) aktiviert.
* Unterstützung für leichte Server-Aufrufe (aktuell in Beta-Version).
* Unterstützung für die Zuweisung eines anderen Werts als 1 zu einem Zählereignis in der Ereignisliste.
* Unterstützung für neue Methode der Videoverfolgung über die Konversion von eVars und Ereignissen (aktuell in Beta-Version).

