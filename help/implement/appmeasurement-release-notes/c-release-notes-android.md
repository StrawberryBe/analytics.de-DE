---
description: Gesammelte Versionshinweise für die mobile Android-Bibliothek.
seo-description: Gesammelte Versionshinweise für die mobile Android-Bibliothek.
seo-title: Android
solution: Analytics, Experience Cloud
subtopic: Versionshinweise
title: Android
topic: Entwickler und Implementierung
uuid: 32232d28-3459-4f78-bb00-ca3163c63461
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Android{#android}

Gesammelte Versionshinweise für die mobile Android-Bibliothek.

>[!NOTE]
>
>Um die aktuelle Bibliotheksversion zu finden, aktivieren Sie die Debug-Protokollierung.

Downloads mobiler Bibliotheken stehen über [GitHub](https://github.com/Adobe-Marketing-Cloud/mobile-services) und über [Developer Connection](https://marketing.adobe.com/developer/gallery/app-measurement-for-android-1) zur Verfügung.

## Version 4.13.4 {#section_E4743079D8E64B9C890180A025C94B44}

The [!DNL Android] SDK version 4.13.4 (Feb 16, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C0197701CB9B45E596818AF0BE5AC4F2"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> In-App-Nachrichten </p> </td> 
   <td colname="2"> <p> Es wurde ein Fehler behoben, durch den beim Festlegen der Zielgruppe die Verwendung der richtigen Anwendungsversion verhindert wurde. Er trat auf, wenn ein Benutzer eine Aktualisierung der Anwendungsversion ohne neuen Lebenszyklusstart durchgeführt hat.  </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Lebenszyklus </p> </td> 
   <td colname="2"> <p> Es wurde ein Fehler behoben, durch den unter Umständen die ordnungsgemäße Meldung einer Aktualisierung der Anwendungsversion verhindert wurde. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Akquise </p> </td> 
   <td colname="2"> <p> Es wurde ein Fehler behoben, der dazu führte, dass verzögerte Deep-Links nicht beim ersten Start ausgelöst wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.3 {#section_1C235192E9FB46E2A651017C1CF24A7F}

The [!DNL Android] SDK version 4.13.3 (Jan 19, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5E744C8C9D064E999EB5055A8E3A99C5"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> In-App-Nachrichten </p> </td> 
   <td colname="2"> <p> Es wurde ein Problem behoben, das die Anzeige von Warnhinweisen ohne Clickthrough-Schaltfläche verhinderte. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Analytics</span> </p> </td> 
   <td colname="2"> <p> Verbesserte Handhabung des schreibgeschützten Datenbankzugriffs. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Universelle Links </p> </td> 
   <td colname="2"> <p> Es wurde ein Fehler behoben, der dazu führte, dass an Akquisedaten angehängte verzögerte Deep-Links bei Folge-Launches aktiviert wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.2 {#section_CEA2FF01EA414A32A8D164D981FBE71F}

The [!DNL Android] SDK version 4.13.2 (Nov 10, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_812CAB7DDC364DAABB7CDEDE55532E39"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Besucher-ID-Service </p> </td> 
   <td colname="2"> <p>Added timestamp and Experience Cloud Organization ID to <code> adobe_mc</code> parameter. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Deep-Linking </p> </td> 
   <td colname="2"> <p>Beim Aufrufen von <code>trackAdobeDeepLink</code> werden ab sofort Variablen mit dem Präfix „<code>adb</code>“ und „<code>ctx</code>“ ordnungsgemäß verarbeitet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.1 {#section_647C43BA95A3485381AC2E8DEAA6D2E4}

The [!DNL Android] SDK version 4.13.1 (Oct 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_1D1AFD90F8BB4F59869FD417ED9C45AB"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Akquise </p> </td> 
   <td colname="2"> Das SDK unterstützt jetzt die ordnungsgemäße Rückgabe benutzerdefinierter Akquisedaten über <code>AdobeDataCallback</code>-Aufrufe. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Akquise </p> </td> 
   <td colname="2"> Das SDK speichert nun Variablen der verweisenden Stelle und benutzerdefinierte Variablen von Google Play und gibt sie ordnungsgemäß in <code>AdobeDataCallback</code> zurück. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target </p> </td> 
   <td colname="2"> Besucher-ID-Service-Parameter werden jetzt in <span class="keyword">Target</span>-Aufrufen über <code>mboxParams</code> übergeben. </td> 
  </tr> 
 </tbody> 
</table>

**Fehlerkorrekturen**

* Es wurde ein Fehler behoben, durch den Datenaufrufe an das Telefon in manchen Fällen das Zeitlimit überschritten.

## Version 4.13.0 {#section_03370D8F93AE4B7A81C4B03910086556}

The [!DNL Android] SDK version 4.13.0 (Sept 15, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AACF8B9BE89A4057B0396F487F82CF99"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App-Nachrichten </p> </td> 
   <td colname="2"> <p>Neue Funktion: Es wurde ein neuer Nachrichtentyp hinzugefügt, der einen Deep-Link-URI öffnet. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Verfolgen von Deep-Links </p> </td> 
   <td colname="2"> <p>Neue Funktion: Die Möglichkeit zur Aktivierung der Verfolgung von verzögerten Deep-Links eines Drittanbieters wurde hinzugefügt. </p> <p> 
     <ul id="ul_DA54F09098A546B6A320E6B9F2937DAD"> 
      <li id="li_B483AEBE02F34E21B2CC731FC77448E8"><code> processAdobeDeepLink</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.12.0 {#section_3FBC1C24267141C08A60E288662160D8}

The [!DNL Android] SDK version 4.12.0 (Aug 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_3BDD15254859475CBE5E27870619FF3A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Besucher-ID-Service </p> </td> 
   <td colname="2"> <p> Neue Methode hinzugefügt, mit der die Besucher-ID an eine angegebene URL angehängt werden kann, um die Identität an eine webbasierte Implementierung zu übertragen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.11.0 {#section_34B295F3697F4AD6B6A6B8DD70AD1ECA}

The [!DNL Android] SDK version 4.11.0 (June 22, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C3DC3890E81744828DE8946AE8067E1A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target-Methoden </p> </td> 
   <td colname="2"> <p>Sie können jetzt die folgende neue <span class="keyword">Target</span>-Methode verwenden: </p> <p> 
     <ul id="ul_D0594A9ABFD8448186DED87599A0E50E"> 
      <li id="li_A4B0ECDF200C438BB1AB24D613453A68"><code> loadRequest</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.10.0 {#section_262928ABA971490EA6B8E277E17BDD89}

The [!DNL Android] SDK version 4.10.0 (May 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_E6B19BD9903A41D9AAF0035CD66756B5"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Target-Methoden </td> 
   <td colname="2"> <p>Eine neue Syntax und ein neues Beispiel für die Methode <code>loadRequest</code> wurden hinzugefügt. </p> <p>Die folgenden neuen <span class="keyword">Target</span>-Methoden wurden hinzugefügt: </p> <p> 
     <ul id="ul_B32C3B3931764F21948E36384B775642"> 
      <li id="li_3421E7F78F3A4DDA8FF004903FC8C75E">setThirdPartyID </li> 
      <li id="li_0836075699C5480EB3D6B742FCF6D508">getThirdPartyID </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.9.0 {#section_7393D3A5EA61431D9E7C07ECE176D17C}

The [!DNL Android] SDK version 4.9.0 (May 5, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_7D893A6E12554E9CA9AF2B03DA4C1A4B"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Opt-out- und Datenschutzeinstellungen </td> 
   <td colname="2"> <p>Sie können Deep-Linking in Ihre Anwendungen implementieren, um Benutzer zu App- oder Weblink-Zielen weiterzuleiten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.8.3 {#section_9BB3DFBECC434AC6B3D7C18AA9BC895C}

The [!DNL Android] SDK version 4.8.3 (February 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_6DE145BC30154B9FADCE584A9737018D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Opt-out- und Datenschutzeinstellungen </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> Android</span> SDK 4.8.3, privacy settings set via the <code> setPrivacyStatus</code> method affect activity from <span class="keyword"> Analytics</span>, <span class="keyword"> Target</span> , and <span class="keyword"> Audience Manager</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.8.0 {#section_18FA091344644B43AA0E226241FF90DC}

The [!DNL Android] SDK version 4.8.0 (November 2, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C47B9AEB2BB649CFA1D5CF04093B497B"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Neue Methoden des Experience Cloud-Besucher-ID-Diensts </td> 
   <td colname="2"> <p>Die folgenden Methoden wurden hinzugefügt: </p> 
    <ul id="ul_6B85F8A4826642BEB373225CA760D799"> 
     <li id="li_72B94B8CECB94229827BFCB06671DFC9"><code> syncIdentifer</code> </li> 
     <li id="li_CD0C6B6CEA064FDD8B109E01AEC63F5C"><code> syncIdentifiers</code> </li> 
     <li id="li_620A2D94F97A4451919F0867CA82B25D"><code> getIdentifiers</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> Neue ADBMobile JSON-Konfigurationsvariable </td> 
   <td colname="2"> <p>Folgende Variable wurde hinzugefügt: </p> 
    <ul id="ul_7FF76521C59343A4ABC9573C3CD5DC38"> 
     <li id="li_1381E3EF082B4D7DBD131D8EC62F94D2"><code> analyticsForwardingEnabled</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"><span class="keyword"> PhoneGap-Plugin-Methoden</span> </td> 
   <td colname="2"> <p>Die folgenden neuen Methoden wurden hinzugefügt </p> <p><b>Konfigurationsmethoden</b> </p> <p> 
     <ul id="ul_98C5E7B5C79446EEA00F0E7CBC213301"> 
      <li id="li_B403C06E57A0450CBB4ABAD45170C681">setPushIdentifier </li> 
      <li id="li_6D76C40601544D4FA13FD44F390C83CE">setAdvertisingIndentifier </li> 
      <li id="li_7D03005DBD9E4AC7BB78BA162CDC8153">keepLifecycleSessionAlive </li> 
      <li id="li_3DDE07508B764E679AF2ACECC4D935CB">trackingSendQueuedHits </li> 
     </ul> </p> <p><b>Target-Methoden</b> </p> <p> 
     <ul id="ul_9B6002F5642B4D888FBD0A8D44EF32DB"> 
      <li id="li_5C1C9EA770E048E48723528F346712B4">targetClearCookies </li> 
     </ul> </p> <p><b>Akquisemethoden</b> </p> <p> 
     <ul id="ul_2015BFF019E64D5685A25E20D4B4A79B"> 
      <li id="li_D450F60189904C43BDAC5D658324AEAA">acquisitionCampaignStartForApp </li> 
     </ul> </p> <p><b>Audience Manager-Methoden</b> </p> <p> 
     <ul id="ul_7D5F339A1A004593AE1D5C26A5A495C5"> 
      <li id="li_2F44037A508D49308F42961FDFB6486C">audienceGetVisitorProfile </li> 
      <li id="li_4F8F43C875384A74ADD48D4197C2ACFD">audienceGetDpuuid </li> 
      <li id="li_B38B6700AF2F4B9FA80CC6774B5B14E7">audienceGetDpid </li> 
      <li id="li_12579B472B404ABAA12DFBDBB22A0C30">audienceSetDpidAndDpuuid </li> 
      <li id="li_2CA997AF9FE241FD961BB0A9B50E14D9">audienceSignalWithData </li> 
      <li id="li_3545CB51B6B7409D8CE2B97E291267E6">audienceReset </li> 
     </ul> </p> <p><b>Besucher-ID-Service-Methoden</b> </p> <p> 
     <ul id="ul_746B8A36715D4075B11C42F9FE82F538"> 
      <li id="li_A15AFA632E8C4C8D931CAB48B9A29ADB">visitorGetMarketingCloudId </li> 
      <li id="li_D80DD8DDE6AB4CB6BEE37DAA9BB28A98">visitorSyncIdentifiers </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.6.1 {#section_98CC97CF0F0C48F7855130044386845A}

The [!DNL Android] SDK version 4.6.1 (September 24, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_80693083398F472F8A4E7861606E602D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Android SDK Version 4.6.1</span> </p> </td> 
   <td colname="2"> <p>SDK 4.6.0 or earlier supports <span class="keyword"> Android</span> 2.2(API 8) - <span class="keyword"> Android</span> 5.1.1 (API 22) </p> <p>SDK 4.6.1 or later supports <span class="keyword"> Android</span> 2.3(API 9) or later </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.6 {#section_ADF6F871CF3C4E2381464D62DA6E1EB1}

The [!DNL Android] SDK version 4.6 (September 17, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_35D0692698EF49AE8204F2AEB57CABD7"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Push Messaging to <span class="keyword"> Analytics</span> Segments </p> </td> 
   <td colname="2"> <p><span class="keyword"> Adobe Mobile Services</span> und das <span class="keyword">Adobe Mobile</span>-SDK ermöglichen es Ihnen, Push-Nachrichten an <span class="keyword">Analytics</span>-Segmente zu senden. Mit dem SDK können Sie darüber hinaus auf einfache Weise Benutzer erfassen, die Ihre App durch Aufrufen der Push-Nachricht geöffnet haben. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Akquisemethoden </p> </td> 
   <td colname="2"> <p>Ermöglichen es Entwicklern, eine App-Akquisekampagne so zu starten, als hätte der Benutzer einen Link aufgerufen. Dies ist hilfreich, wenn Sie manuell Akquiselinks erstellen oder die App Store-Umleitung selbst verarbeiten möchten. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Postbacks </p> </td> 
   <td colname="2"> <p>Mit Postbacks können Sie durch ein SDK erfasste Daten an einen Drittanbieterserver senden. Mit denselben Triggern und Eigenschaften wie bei der Anzeige einer In-App-Nachricht können Sie das SDK so konfigurieren, dass es benutzerdefinierte Daten an ein Drittanbieterziel sendet. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Kennungen </p> </td> 
   <td colname="2"> <p>Die folgenden neuen Kennungen wurden hinzugefügt: </p> <p> 
     <ul id="ul_84AD959FC65C445BB119F69657AB4AF8"> 
      <li id="li_418FD9EE570F491F9704F72AC70EEE8D"><code> setPushIdentifier</code> </li> 
      <li id="li_B350606A504449E5AAE208B1E590E2CA"> <code> submitAdvertisingIdentifierTask</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.5 {#section_6E7614D4AEA24B7E81C4FC094882F062}

The [!DNL Android] SDK version 4.5 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_BF98A1E904EB4314828AC58A2A6E7016"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Android Wearable-Erweiterung</span> </p> </td> 
   <td colname="2"> <p>Starting in <span class="keyword"> Android</span> SDK version 4.5, a new <span class="keyword"> Android</span> extension lets you collect data from your <span class="keyword"> Android</span> Wearable app. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.4 {#section_8D7FC183081E4BCFA8ADC33FB55E057C}

The [!DNL Android] SDK version 4.4 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_E8628F3806E24A0FB7157847D97C7B7A"> 
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
   <td colname="1"> <p>Beacon tracking support in <span class="keyword"> PhoneGap</span> </p> </td> 
   <td colname="2"> <p>Die Aufrufe <code>trackBeacon</code> und <code>clearCurrentBeacon</code><span class="keyword"> sind jetzt in PhoneGap verfügbar</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.3 {#section_789F3DA3DD3146CAA126B303F62D1A1A}

Releasedatum: **24. November 2014**

* Neu: Adobe Experience Cloud ID-Integration
* Verbesserte Debug-Protokolle für mehr Klarheit
* Potenzieller Absturz beim Abrufen von In-App-Nachrichten behoben.

## Version 4.2 {#section_EDF95BA0301C4B54AAE839768917D439}

Releasedatum: **16. Oktober 2014**

* Neu: Funktionen für In-App-Nachrichten
* Neu: Speicherort für Konfigurationsdatei kann nun beim Anwendungsstart angegeben werden.
* Neu: Interessante Orte können nun automatisch aktualisiert werden, ohne dass eine neue Konfigurationsdatei erforderlich ist.
* New - [!DNL Analytics] calls are now sent as HTTP POST requests.
* Problem behoben, bei dem Anwendungsabstürze in bestimmten Szenarien nicht richtig protokolliert wurden.
* Protokollmeldungen optimiert und detailliertere Protokolldaten bei aktiviertem debugLogging hinzugefügt.
* Mehrere Leistungs- und Stabilitätsverbesserungen.

## Version 4.1.7 {#section_DD98F9A4F00A457AA79D223CB1113A06}

Releasedatum: **4. August 2014**

* Problem behoben, bei dem der Lebenszyklustreffer nicht gesendet wurde, wenn das Referrer-Timeout über 5 Sekunden lag und das Offline-Tracking deaktiviert war.

## Version 4.1.6 {#section_B665DF1A4FB249539D73569B52FA8786}

Releasedatum: **17. Juli 2014**

* Schutzmechanismen für Ausnahmefehler hinzugefügt, die auftraten, wenn die Datenbank beschädigt wurde oder nicht erstellt werden konnte.
* Schutzmechanismen für Probleme hinzugefügt, die auftraten, wenn die Konfigurationsdatei nicht geladen werden konnte (für gewöhnlich aufgrund eines Null-Kontexts).
* Schutzmechanismen für Ausnahmefehler hinzugefügt, die beim Aktualisieren der Kontextdaten einer zeitgesteuerten Aktion auftraten.

## Version 4.1.1 {#section_E5EFA05CEE9D486BA6B5C12B1102C117}

Releasedatum: **23. April 2014**

* Potenzielles Problem behoben, das auftrat, wenn das Referrer-Tracking aktiviert war und ein Tracking-Aufruf vor dem Lebenszyklus durchgeführt wurde.

## Version 4.1.0 {#section_266B62F5B6A44F5F8E6AB8ED1870C4A3}

Releasedatum: **17. April 2014**

* Neu: Bluetooth-Beacon-Verfolgung.
* Neu: Bei Anwendungen, bei denen Zeitstempel aktiviert sind, werden Absturztreffer auf die richtige Sitzung zurückdatiert.
* Neu: Bei Anwendungen, bei denen Zeitstempel aktiviert sind, wird die vorherige Sitzung in einem Treffer gesendet, der auf die richtige Sitzung zurückdatiert ist. (nicht länger vorherige Sitzung).
* Neu: Trefferbatching.
* Korrektur der Google Play-Referrer-Verfolgung mit einem konfigurierbaren Timeout, um verzögerte Google-Referrer-Daten zuzulassen.
* Es wurden StrictMode-Warnungen behoben, die in bestimmten Szenarien auftreten konnten.
* Es wurde ein Problem behoben, das sehr selten dazu führen konnte, dass die Bibliothek gesperrt wurde, wenn bestimmte Methoden in einer bestimmten Reihenfolge aufgerufen wurden.

## Version 4.0.4 {#section_DCFAC758872D42F0BF0CCFCDDEA05E41}

Releasedatum: **24. Februar 2014**

* Problem behoben, das eine erweiterte Medien-Wiedergabezeit verursachte, wenn Stopp und später Schließen aufgerufen wurde, ohne dass andere Aufrufe dazwischen lagen.
* Problem gelöst, bei dem der Medien-Schließen-Treffer gesendet wurde, obwohl die Medien über einen beliebigen Zeitraum hinweg nicht wiedergegeben wurden.

## Version 4.0.3 {#section_FCC3D7D22EBF4A2FA949A4E88AD89F5C}

Releasedatum: **20. Februar 2014**

* Added safety to network code to prevent crash caused by [!DNL Android] bug: https://code.google.com/p/android/issues/detail?id=54072

## Version 4.0.2 {#section_5A7F4D5D9CBD4B79B3B590A2C3F4D0F9}

Releasedatum: **30. Januar 2014**

* Problem behoben, bei dem mehrere Treffer gesendet wurden, wenn die Datenbank beschädigt war.
* Problem behoben, das im Durchschnitt hohe Sitzungslängen verursachte, wenn ein Gerät über die korrekten Zeiteinstellungen verfügte.

## Version 3.2.5 {#section_A6E60DB42241481DA62F660344128F53}

Releasedatum: **30. Januar 2014**

* Schutzmechanismen für beschädigte Datenbanken hinzugefügt, um zu vermeiden, dass sich Treffer wiederholen.
* Maximale Sitzungslänge hinzugefügt, um extrem lange Sitzungen bei nicht korrekten Gerätezeiten zu vermeiden.

## Version 4.0.1 {#section_5F58DBABDAA049FE9070E46989B2E9A9}

Releasedatum: **14. November 2013**

* Fehlerhafte Formatierung der trackLocation-Daten unter bestimmten Gebietsschemas behoben.

## Version 4.0.0 {#section_79DCFAAF1DCB404898E3BE389AC835A6}

Releasedatum: **27. September 2013**

[!DNL Android] SDK 4.x für Experience Cloud-Lösungen ist jetzt mit den folgenden neuen Funktionen verfügbar:

* Deutliche Leistungsverbesserungen. Die gesamte Verarbeitung erfolgt nun in Hintergrund-Threads; das SDK ist absolut Thread-sicher.
* Geografischer Standort und Orte von Interesse
* Lebenszeitwert
* Zeitgesteuerte Ereignisse
* Anmelde-/Abmeldeverwaltung
* Audience Manager-Unterstützung
* Lifecycle metrics passed to [!DNL Target] as mbox parameters
* Bezüglich Kontextdaten und Verarbeitungsregeln standardisiert

## Version 3.2.3 {#section_E3464DDC3B4844CF9CC5FC3E35C5C785}

Releasedatum: **23. September 2013**

* Problem in Audience Manager behoben, bei dem Null-Werte oder -Schlüssel im Parameter nicht erlaubt waren.

## Version 3.2.2 {#section_7D631AA2474F4DBAA043703629E3ECC6}

Releasedatum: **12. September 2013**

* Problem behoben, bei dem Medienereignisse in linkTrackEvents nicht zur Anfrage hinzugefügt wurden.
* Potenzieller Ausnahmefehler behoben, der auftrat, wenn ContextData geändert wurde, nachdem sie an einen Tracking-Aufruf übergeben wurde.

## Version 3.2.1 {#section_D269F9145B2844B6855423A30B125D5C}

Releasedatum: **16. August 2013**

* SSL-Verbindungen nutzen nun eine strenge Hostvalidierung.
* Problem behoben, bei dem Treffer einige Sekunden lang schnell erneut versucht wurden, wenn die Netzwerkverbindung getrennt wurde und offlineTracking deaktiviert war.

## Version 3.2 {#section_ABD4D192E3FF4240B1451262EAEE4F17}

Releasedatum: **6. August 2013**

* Unterstützung für Adobe Audience Manager hinzugefügt.
* Lebenszyklusdaten werden jetzt mit Ziel-Mbox-Anfragen gesendet, wenn das Lebenszyklus-Tracking aktiviert ist.
* Problem behoben, bei dem SQLite das Schließen von Cursorn erzwang, wodurch unnötige Protokolleinträge entstanden.

## Version 3.1.0 {#section_836B4F580B1C436FABD524A91857F882}

Releasedatum: **13. Juni 2013**

* Offlinespeicher für Verwendung von SQLite aktualisiert.
* Fehler behoben, bei dem das Offlinelimit auf den Standardwert (1000) zurückgesetzt wurde.
* startActivity aktualisiert, um Aktivitäts- oder Anwendungskontexte zu akzeptieren.
* Fehler behoben, bei dem das Festlegen von 0 für lifecycleSessionTimeout über die Anwendung hinweg zu mehreren Startereignissen führte.

## Version 3.0.8 {#section_51F50CD81C6A40C8BCF62F6F332A0800}

Releasedatum: **18. April 2013**

* Codierungsproblem mit einigen UTF-8-Zeichen behoben.

## Version 3.0.7 {#section_0F3FEE2886EB4AB7BA288891FF6B6BCD}

Releasedatum: **18. April 2013**

* Problem behoben, bei dem die Länge der vorherigen Sitzung in manchen Fällen fehlerhaft berechnet wurde.
* Neue Besucher-IDs basieren nicht länger auf deviceID oder subscriberID.
* Potenzieller Absturz behoben, der beim Codieren von Sonderzeichen in Variablen auftrat.

## Version 3.0.6 {#section_72F3F9CB95BF4076AD882B3270F77B87}

Releasedatum: **21. März 2013**

* Problem behoben, bei dem die visitorID nicht gelesen werden konnte, ohne vorher festgelegt worden zu sein.
* Benennungskonventionen in einigen Fehlerprotokollen geändert, um für mehr Klarheit zu sorgen.
* Zugriffsfähigkeit mehrerer Basisklassen geändert, um Verwirrung zu vermeiden.
* Mehrere Leistungsverbesserungen

## Version 3.0.5 {#section_0540FF6477D74D1F8274E9340EDE7E16}

Releasedatum: **21. Februar 2013**

* Aufgrund der Thread-Optimierung ist die Einstellung `offlineThrottleDelay` veraltet und nicht mehr erforderlich. Die Einstellung ist noch vorhanden, um die Rückwärtskompatibilität zu gewährleisten, hat jedoch keine Auswirkung mehr.
* Das potenzielle Problem im Offline-Treffer-Cachespeicher wurde behoben.
* Die Warnmeldung, die beim Festlegen von hierarchischen Variablen über #5 erschien, wurde entfernt.
* Fixed issue that could cause OSVersion to be misreported on versions of [!DNL Android] &gt; 4.0.
* Mehrere Leistungsverbesserungen.
* Eine potenzielle Ausnahme, die durch eine falsch zusammengesetzte URL verursacht werden konnte, wurde entfernt.

## Version 3.0.4 {#section_69ADA2ACD9DE436692152C3836B14EEF}

Releasedatum: **November 2012**

* Eine Konfigurationsvariable `lifecycleSessionTimeout` wurde hinzugefügt, durch die Sie angeben können, wie viel Zeit in Sekunden zwischen verschiedenen Startvorgängen einer Anwendung verstreichen muss, damit ein Startvorgang als neue Sitzung gilt.
* Die Möglichkeit zum Festlegen eines Zeitüberschreitungswerts für die Berechnung der Sitzungslänge über eine Konfigurationseinstellung `lifecycleSessionTimeout` wurde hinzugefügt.
* Behobene Sicherheitsprobleme:

## Version 3.0.3 {#section_F16E1A36AE3F4CBC92E4925D6DCCFADE}

Releasedatum: **Oktober 2012**

* Die [Kampagnen-Rückverfolgung für Google Play](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/android/index.html?f=referrer) wird nun unterstützt.

## Version 3.0.2 {#section_CB24859B34804F9391BA1BF8DF29CC86}

Releasedatum: **September 2012**

* Behebung eines Problems, bei dem Treffer für Schließen manchmal eine Schleife im Medienmonitor verursachen können.

## Version 3.0.1 {#section_541CE15B340E414AA018A0EFAEE459F0}

Releasedatum: **August 2012**

* Context override parameters are now sent in as `Hashmap<String, Object>` (they were formerly `Hashmap<String, String>`).

## Version 3.0 {#section_2955C0AF3A23476B8CF06C469DE3284C}

Releasedatum: **Juli 2012**

Erstes Release.

## Frühere Android-Version (1.x) {#section_F2CC015616184D55AC6D6529DFC9A18B}

The following release notes apply to the 1.x version of [!DNL AppMeasurement] for [!DNL Android]. Wir empfehlen unseren Kunden, so bald als möglich auf die Version 3.x aufzurüsten.

## Version 1.2.3 {#section_5189CCE11EEF4350844B1490D0A9F534}

Releasedatum: **März 2012**

* Es wurde ein Problem behoben, durch das beim Übergeben von Daten unter Verwendung von Kontextdaten eine Ausnahme verursacht wurde.

## Version 1.2.2 {#section_C42925D94F3A429EB1299B96A6EEF6DF}

Releasedatum: **Februar 2012**

Ein Fehler wurde behoben, bei dem geringere Linktracking-Aufrufe die Werte pev1-pev3 doppelt URL-codierten.

Ein Zeitstempel wurde zu Variablen hinzugefügt, die mit geringeren Verfolgungsaufrufen (trackLight) verwendet werden.

## Version 1.2.1 {#section_21845E8A7D0C48B38CB90F0D4C5696AF}

Releasedatum: **Januar 2012**

* Added [!DNL Android] 3.x and 4.x compatibility.
* Implemented a UUID for visitor ID on [!DNL Android] devices that do not have SIM cards (For example, Kindle Fire).

## Version 1.2 {#section_EC83BE1F00BF481EA1C74A63E4B90F65}

Releasedatum: **Juni 2011**

* Die Bibliothek wurde aktualisiert, um die Geräte-ID für den Besucher-ID-Wert zu verwenden, wenn keine SIM-Karte in das Gerät eingefügt wird. Standardmäßig verwendet die Bibliothek die Abonnenten-ID als Besucher-ID, die nicht verfügbar ist, wenn keine SIM-Karte eingelegt ist.

## Version 1.1.4 {#section_C602EC5C11594669A8797B736D240D2C}

Releasedatum: **April 2011**

* Unterstützung für alle Tablets einschließlich Xoom.
* Fähigkeit zum Durchsuchen der Report Suites und Metriken beim Ausführen eines Berichts.
* Unterstützung für contextData, welches die Verarbeitungsregeln auf Serverseite (nur v15) aktiviert.
* Unterstützung für leichte Serveraufrufe (aktuell in Beta-Version).
