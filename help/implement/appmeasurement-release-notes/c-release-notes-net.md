---
description: 'null'
subtopic: Release notes
title: Windows Silverlight, NET, IIS, XBOX
topic: Developer and implementation
uuid: 15c20bca-4886-4d57-9957-fe99743851ea
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Windows Silverlight, NET, IIS, XBOX{#windows-silverlight-net-iis-xbox}

>[!IMPORTANT]
>
>Diese SDKs werden nicht mehr unterstützt oder werden nicht mehr von Adobe verteilt.

> [!NOTE] Schalten Sie die Debug-Protokollierung ein, um die aktuelle Bibliotheksversion zu suchen.

## Version 1.4.2 {#section_2B70F52C4D214A43844CCEC6B45037F0}

Releasedatum: **August 2014**

* Die Unterstützung für [!DNL Microsoft Silverlight Analytics Framework] wurde entfernt. Adobe unterstützt oder verteilt die [!DNL Microsoft Silverlight Analytics Framework]-Integration nicht mehr für [!DNL AppMeasurement].

* Es wurden interne Veränderungen zur Unterstützung neuer Funktionen vorgenommen.

## Version 1.4.1 {#section_9134F77804BF472291DA7243FAC89C2B}

Releasedatum: **März 2013**

* Ausnahmefehler behoben, der beim Abrufen des Standard-Referrers in [!DNL Silverlight] außerhalb eines Browserkontexts und einer ordnungsgemäß offengelegten SSL-Eigenschaft in der [!DNL Microsoft Silverlight Analytics Framework]-Komponente auftrat.

## Version 1.4 {#section_2F4ADA4628EC43B480177C3DDB3D1CFA}

Releasedatum: **Februar 2013**

* Es werden nun URLs mit mehr als 255 Byte unterstützt, um die Erweiterung des Felds „Seiten-URL“ in den Adobe-Datenerfassungsservern zu unterstützen. Seiten-URLs, die länger als 255 Byte sind, werden geteilt, wobei die ersten 255 Byte im Parameter `g=` auftauchen und die verbleibenden Byte später in der Abfragezeichenfolge im Suchparameter `-g=` auftauchen. Damit wird vermieden, dass lange URLs, die im Browser abgeschnitten werden, Vorrang vor anderen Daten haben, während gleichzeitig lange URLs erfasst werden können.

* Eine neue Methode für den Fallback der Besuchererkennung wurde hinzugefügt. Weitere Informationen finden Sie im Abschnitt [Erkennen Unique Visitors](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_identifying_unique_visitors.html).
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
   If(media.event=="CLOSE") { 
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

* Unterstützung und neuer Build für die [!DNL iOS]-Phone-Plattform einschließlich Offline-Verfolgung.
* Unterstützung für den doRequest-Delegate, um außer Kraft zu setzen, wie Anforderungen für Verfolgungsdaten gesendet werden.
* Unterstützung für contextData, welches die Verarbeitungsregeln auf Serverseite (nur v15) aktiviert.
* Unterstützung für leichte Server-Aufrufe (aktuell in Beta-Version).
* Unterstützung für die Zuweisung eines anderen Werts als 1 zu einem Zählereignis in der Ereignisliste.
* Unterstützung für neue Methode der Videoverfolgung über die Konversion von eVars und Ereignissen (aktuell in Beta-Version).

