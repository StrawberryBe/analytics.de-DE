---
description: Gesammelte Versionshinweise für iOS.
seo-description: Gesammelte Versionshinweise für iOS.
seo-title: iOS
solution: Analytics, Marketing Cloud
subtopic: Versionshinweise
title: iOS
topic: Entwickler und Implementierung
uuid: cc 98 f 8 f 2-f 619-4 b 31-abf 9-e 43 f 4 deac 64 f
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# iOS{#ios}

Gesammelte Versionshinweise für iOS.

>[!NOTE]
>
>Aktivieren Sie die Debug-Protokollierung, um die aktuelle Bibliotheksversion zu finden.

Downloads mobiler Bibliotheken stehen über [GitHub](https://github.com/Adobe-Marketing-Cloud/mobile-services) und über [Developer Connection](https://marketing.adobe.com/developer/gallery/app-measurement-for-ios) zur Verfügung.

[Dokumentation zu 4.x](https://marketing.adobe.com/resources/help/en_US/mobile/ios/)

[Dokumentation zu 3.x](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/ios/)

## Version 4.13.4 {#section_BF05D33CEF6E42358C8089441449449B}

The [!DNL iOS] SDK version 4.13.4 (Feb 16, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_657D643E874D47C099F2F43519C9C1C7"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App-Nachrichten </p> </td> 
   <td colname="2"> <p> Es wurde ein Fehler behoben, durch den beim Festlegen der Zielgruppe die Verwendung der richtigen Anwendungsversion verhindert wurde. Er trat auf, wenn ein Benutzer eine Aktualisierung der Anwendungsversion ohne neuen Lebenszyklusstart durchgeführt hat.  </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Akquise </p> </td> 
   <td colname="2"> <p> Es wurde eine dreisekündige Verzögerung vor API-Aufrufen für Apple Search Ad-Daten bei Anwendungsinstallationen (gemäß Empfehlungen in der Dokumentation) hinzugefügt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.3 {#section_39618D2B29F942FCBF37E4F5507AA131}

The [!DNL iOS] SDK version 4.13.3 (Jan 19, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_341D35BF18714139A95CA5491899185D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App-Nachrichten </p> </td> 
   <td colname="2"> <p> Sie können jetzt Vollbildnachrichten deaktivieren, wenn VoiceOver aktiv ist. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Analytics</span> </p> </td> 
   <td colname="2"> <p> Verbesserte Handhabung des schreibgeschützten Datenbankzugriffs. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Allgemein </p> </td> 
   <td colname="2"> <p> Es wurde ein Problem behoben, das in manchen Fällen zum Absturz führen konnte, wenn während der Verwendung von App-Gruppen eine Nachverfolgungsmethode aus dem Hintergrund aufgerufen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.2 {#section_CB0DFFDB38FE4D14A84423DF40BF8FD3}

The [!DNL iOS] SDK version 4.13.2 (Nov 10, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AA26B14D271948FFBA44D4D06E3B71AA"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Besucher-ID-Service </p> </td> 
   <td colname="2"> <p> Zeitstempel und Marketing Cloud-Organisations-ID wurden dem <code>adobe_mc</code>-Parameter hinzugefügt. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Konfiguration </p> </td> 
   <td colname="2"> <p> Ungültige IDFAs (00000000-0000-0000-0000-000000000000) wurden an das SDK über <code>setAdvertisingIdentifier</code> weitergegeben: wird ignoriert. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Deep-Linking </p> </td> 
   <td colname="2"> <p>Beim Aufrufen von <code>trackAdobeDeepLink</code> werden ab sofort Variablen mit dem Präfix „<code>adb</code>“ und „<code>ctx</code>“ ordnungsgemäß verarbeitet. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Akquise </p> </td> 
   <td colname="2"> <p>Daten von Apple Search-Anzeigen werden nun zusammen mit Ihren Akquisedaten versendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.13.1 {#section_18C8A7166EFD4E67AC0F7C06DFBBFE6A}

The [!DNL iOS] SDK version 4.13.1 (Oct 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5B67A6B8B79D4783BA8DCDA7C2ACA765"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> Akquise </p> </td> 
   <td colname="2"> <p> Das SDK unterstützt jetzt die ordnungsgemäße Rückgabe benutzerdefinierter Akquisedaten über <code>AdobeDataCallback</code>-Aufrufe. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target </p> </td> 
   <td colname="2"> <p><span class="keyword"> Besucher-ID-Service</span>-Parameter werden jetzt in <span class="keyword">Target</span>-Aufrufen über <code>mboxParams</code> übergeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fehlerkorrekturen**

* Es wurde ein Problem behoben, das zu einem Absturz führen konnte, wenn gleichzeitig versucht wurde, eine neue ID mit der VisitorID zu synchronisieren und Nachverfolgungstreffer an [!DNL Adobe Analytics] zu senden.
* Fixed an issue that was causing build warnings when targeting [!DNL iOS] versions older than 8.

## Version 4.13.0 {#section_F72A3357994E4887A9F3967F0FBFFCDD}

The [!DNL iOS] SDK version 4.13.0 (Sep 15, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_FD6156E58FF54BA2BEED7398BC780C46"> 
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
 </tbody> 
</table>

## Version 4.12.0 {#section_2AD26AABBB434833AE961C8D71C9AFE8}

The [!DNL iOS] SDK version 4.12.0 (Aug 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_CC3CD01203ED4BDA9BC26427E925C70D"> 
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
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App-Nachrichten </p> </td> 
   <td colname="2"> <p>Es wurde ein Problem behoben, durch das unter Umständen beim Einstellen des Attributs „target“ auf „_blank“ in einem HTML-Tag innerhalb einer benutzerdefinierten Vollbildnachricht ein Absturz verursacht wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.11.0 {#section_3ABABE0F0B964EB48BD482CCE260A13D}

The [!DNL iOS] SDK version 4.11.0 (June 22, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_14B23402BA3B41238F419CA57341B8F5"> 
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
     <ul id="ul_93CDE46E39C9431DA9104664F175708B"> 
      <li id="li_903FAC68526B4B7CB6555DC577CE493A"><code> targetLoadRequestWithName:defaultContent:profileParameters:orderParameters:mboxParameters:requestLocationParameters:callback:</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.10.0 {#section_F0D6D7FD89DE4DF5A121B05FA093CC5B}

The [!DNL iOS] SDK version 4.10.0 (May 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AC447B6E4D55489F803923BF5D1D6653"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target-Methoden </p> </td> 
   <td colname="2"> <p>Sie können jetzt die folgenden neuen <span class="keyword">Target</span>-Methoden verwenden: </p> <p> 
     <ul id="ul_D0594A9ABFD8448186DED87599A0E50E"> 
      <li id="li_A4B0ECDF200C438BB1AB24D613453A68"><code> targetLoadRequestWithName:defaultContent:profileParameters:orderParameters:mboxParameters:callback:</code> </li> 
      <li id="li_C0FADBB3CEE141AE951CBD49F3A52642"><code> targetThirdPartyID</code> </li> 
      <li id="li_3E1B3725D9EE4ECE9DB0EB1A9E7682A4"><code> targetSetThirdPartyID:</code> </li> 
      <li id="li_659E295610F541819DD7486FC5177012"><code> targetPcID</code> </li> 
      <li id="li_B00ADCF98B6D4694BB7664DB42CDFF99"><code> targetSessionID</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>TVJS-Methoden </p> </td> 
   <td colname="2"> <p>Sie können jetzt die folgenden neuen <span class="keyword">Target</span>-TVJS-Methoden verwenden: </p> <p> 
     <ul id="ul_AED76A2B99534CF3A472AC0381B2618C"> 
      <li id="li_AA731652996C4A19A8E02D5D6B8BDC93"><code> targetThirdPartyID</code> </li> 
      <li id="li_744A63A62A8045E49C75F9D7AED5D75E"><code> targetSetThirdPartyID</code> </li> 
      <li id="li_72BC8D96FE0549A695D90B924FA80A02"> <code> targetPcID</code> </li> 
      <li id="li_FB7A9435B9994DB89FA80C2B2218C047"> <code> targetSessionID</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Adobe Target für TVML/TVJS </p> </td> 
   <td colname="2"> <p>Sie können jetzt die folgenden Eigenschaftsnamen verwenden, wenn Sie Ihr <code>ADBTarget</code>-Element konfigurieren: </p> <p> 
     <ul id="ul_A0CEE891AE644B47ABD6F7425ACD464D"> 
      <li id="li_2EB0C3CA52014F45BA1EC07703E821B8"><code> id</code> </li> 
      <li id="li_069D996CED534EE88A1EC82684E470D5"><code> total</code> </li> 
      <li id="li_97F290C03FFD46B8A1E78B7BF2021F55"> <code>purchasedProductIds</code> </li> 
      <li id="li_FAAC4BB12DF9491DA21F161711A7707D"> <code> mboxParameters</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.9.0 {#section_DA97D7294B214067A4904B9738450759}

The [!DNL iOS] SDK version 4.9.0 (May 5, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_0B3A0F44549C4DA48C7639048C030065"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Deep-Linking </p> </td> 
   <td colname="2"> <p>Sie können Deep-Linking in Ihre Anwendungen implementieren, um Benutzer zu App- oder Weblink-Zielen weiterzuleiten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.8.6 {#section_0150641B44CF4F6CBE2B21002F8EAB30}

The [!DNL iOS] SDK version 4.8.6 (March 9, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5175CFFCA30B4DDBACFB23532111CB8A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Nachverfolgen von App-Abstürzen </p> </td> 
   <td colname="2"> <p>The <span class="keyword"> iOS</span> SDK version 4.8.6 contains critical changes that prevent false crashes from being reported. Wir empfehlen dringend eine Aktualisierung auf Version 4.8.6. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.8.5 {#section_F42EB64F91024748893E89575F2E4487}

[!DNL iOS] Die SDK-Version 4.8.5 (18. Februar 2016) umfasst die folgenden Änderungen:

<table frame="all" colsep="1" rowsep="1" id="table_AB225AF04A374421BDD8A972506ACD06"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Opt-out- und Datenschutzeinstellungen </p> </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> iOS</span> SDK 4.8.5, privacy settings set via the <code> setPrivacyStatus</code> method affect activity from <span class="keyword"> Analytics</span>, <span class="keyword"> Target</span>, and <span class="keyword"> Audience Manager</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.8.0 {#section_2CF142C8C2D24B529559DAF76F851BBF}

The [!DNL iOS] SDK version 4.8.0 (November 2, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_9DB41F070D66498FACF1A9C135603C7A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Neue Methoden beim Marketing Cloud-Besucher-ID-Dienst </td> 
   <td colname="2"> <p>Die folgenden neuen Methoden wurden hinzugefügt: </p> 
    <ul id="ul_55D8F29ADE3746C484FEC7893FA9EF23"> 
     <li id="li_19F8AF546EEB45EBB5849EA6EB3CE6A3"><code> visitorSyncIdentifiers:authenticationState:</code> </li> 
     <li id="li_1AF1CF62B3ED442D81B438ECBF981583"><code> visitorSyncIdentifierWithType:identifier:authenticationState: </code> </li> 
     <li id="li_C116F0DA8E2A449A8B76637961C2100C"><code> visitorGetIDs</code> </li> 
    </ul> <p>Die Methode <code>visitorSyncIdentifiers:identifiers</code> wurde in <code>visitorSyncIdentifiers:</code> geändert </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> Neue TVJS-Methoden </td> 
   <td colname="2"> <p>Die folgenden neuen Methoden wurden hinzugefügt: </p> 
    <ul id="ul_4C7F4BB1CF744444ABAA9F13BA98749E"> 
     <li id="li_5DAB089D115843CCA0A53873D6D676F0"><code> visitorSyncIdentifiersAuthenticationState</code> </li> 
     <li id="li_EDE2D1301E8648DB88A18D8C9F6A22C5"><code> visitorSyncIdentifierWithTypeIdentifierAuthenticationState</code> </li> 
     <li id="li_2CCED3C707774597934A2F08BC690B15"><code> visitorGetIDsJs</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> Neue ADBMobile JSON-Konfigurationsvariable </td> 
   <td colname="2"> <p>Folgende Variable wurde hinzugefügt: </p> 
    <ul id="ul_95065BC06FD540D2937D11111799F77F"> 
     <li id="li_7C8C68A41FBA4D098D6803E71D4CCF7A"><code> analyticsForwardingEnabled</code> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.7.0 {#section_B37B1CAF065346E9A2073A06AB7AFEC2}

The [!DNL iOS] SDK version 4.7.0 (October 15, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_3CCA327B859B498D828B2E056A075BEC"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> Unterstützung von tvOS </td> 
   <td colname="2"> <p>tvOS wird für Apple TV unterstützt. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> Unterstützung für „App Transport Security“ </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> iOS</span> 9, Apple introduced App Transport Security, a set of requirements that conforms to best practices for secure connections. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> PhoneGap-Plugin-Methoden</span> </p> </td> 
   <td colname="2"> <p>Die folgenden neuen Methoden wurden hinzugefügt: </p> <p><b>Konfigurationsmethoden</b> </p> <p> 
     <ul id="ul_98C5E7B5C79446EEA00F0E7CBC213301"> 
      <li id="li_B403C06E57A0450CBB4ABAD45170C681">setPushIdentifier </li> 
      <li id="li_6D76C40601544D4FA13FD44F390C83CE">setAdvertisingIndentifier </li> 
      <li id="li_7D03005DBD9E4AC7BB78BA162CDC8153">keepLifecycleSessionAlive </li> 
      <li id="li_3DDE07508B764E679AF2ACECC4D935CB">trackingSendQueuedHits </li> 
     </ul> </p> <p><b>Tracking-Methoden</b> </p> <p> 
     <ul id="ul_9B6002F5642B4D888FBD0A8D44EF32DB"> 
      <li id="li_5C1C9EA770E048E48723528F346712B4">trackPushMessageClickthrough </li> 
     </ul> </p> <p>Neue Target-Methode: </p> <p> 
     <ul id="ul_E6A481FCD49D4CF48A4B0636312FCD19"> 
      <li id="li_6604FBB05C4E4988A04CB376D6667C79">targetClearCookies </li> 
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
     </ul> </p> <p><b>App-Erweiterungen und Apple Watch-Methoden</b> </p> <p> 
     <ul id="ul_66B1E1AC4A6D4970B0C77A46EA14ABA7"> 
      <li id="li_1EA7A063FED04E0585D463837A7555CE">setAppGroup </li> 
      <li id="li_5869EAB018C94EE4AC28B3EE62D9F0EF">syncSettings </li> 
      <li id="li_983A98CAEBAD404EBCE1D70CB0B52BA3">initializeWatch </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.6 {#section_D091872501DA49C1A18CDC33C84B8256}

The [!DNL iOS] SDK version 4.6 (September 17, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_084C27B1A75A4A2EB84822242E37ED35"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Push Messaging to <span class="keyword"> Analytics</span> Segments </p> </td> 
   <td colname="2"> <p> <span class="keyword"> Adobe Mobile Services</span> und das <span class="keyword">Adobe Mobile</span>-SDK ermöglichen es Ihnen, Push-Nachrichten an <span class="keyword">Analytics</span>-Segmente zu senden. Mit dem SDK können Sie darüber hinaus auf einfache Weise Benutzer erfassen, die Ihre App durch Aufrufen der Push-Nachricht geöffnet haben. </p> </td> 
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
     <ul id="ul_22EF89556F6B481ABE0D1B9C5EE70B55"> 
      <li id="li_C41F6FAC0B334B89B8B5D1A517CA2301"> <code> setPushIdentifier</code> </li> 
      <li id="li_B7893FB0453340EDB4290BC0B47BF096"><code> setAdvertisingIdentifier</code> </li> 
      <li id="li_85EF5F2B8837497B90F782946283622E">Das <code>trackPushMessageClickThrough</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Unterstützung für WatchKit für WatchOS 2 </p> </td> 
   <td colname="2"> <p>Unterstützung für WatchKit für WatchOS 2 wurde hinzugefügt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.5 {#section_53DFAF8CFD614F69B3168014EF84DE9F}

The [!DNL iOS] SDK version 4.5 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_A69D0B8DA45348B8A5D6A014126F97C2"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> Funktion </th> 
   <th colname="2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> iOS-Erweiterung</span> </p> </td> 
   <td colname="2"> <p>Starting in <span class="keyword"> iOS</span> SDK version 4.5, a new <span class="keyword"> iOS</span> extension lets you collect usage data from your Apple Watch Apps, Today Widgets, Photo Editing widgets, and all the other <span class="keyword"> iOS</span> extension apps. </p> <p>We strongly recommend that you use the <span class="keyword"> iOS</span> SDK rather than using your own wrapper. </p> <p>Apple bietet einen Satz APIs, über die die Watch-Anwendung mit der übergeordneten Anwendung kommunizieren (Anfragen an die übergeordnete Anwendung senden und Antworten erhalten) kann. </p> <p>Es ist zwar möglich, Tracking-Daten als Wörterbuch von der Watch-Anwendung an die übergeordnete Anwendung zu senden und die übergeordnete Anwendung anschließend über eine beliebige Tracking-Methode zum Senden der Daten aufzufordern, jedoch gibt es bei dieser Methode Einschränkungen. </p> <p>Wenn ein Benutzer die Watch-Anwendung verwendet, läuft die übergeordnete Anwendung meistens im Hintergrund, und es ist nur sicher, <code>TrackActionInBackground</code>, <code>TrackLocation</code> und <code>TrackBeacon</code> aufzurufen. Andere Tracking-Methoden aufzurufen würde Lebenszyklusdaten beeinträchtigen, also sollten Sie nur diese drei Methoden verwenden, um Daten von der Watch-Anwendung zu senden. </p> <p>Even if these three tracking methods meet your requirements, we recommend using the <span class="keyword"> iOS</span> SDK because the SDK for watch app includes all <span class="keyword"> Mobile</span> features except in-app messaging. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.4 {#section_0B7A98761BF0400986C368E154A3B00B}

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
   <td colname="1"> <p>Beacon tracking support in <span class="keyword"> PhoneGap</span> </p> </td> 
   <td colname="2"> <p>Die Aufrufe <code>trackBeacon</code> und <code>clearCurrentBeacon</code><span class="keyword"> sind jetzt in PhoneGap verfügbar</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 4.3 {#section_0FD2B2C4F54E4A9E8C6D0CD2F103BB9A}

Releasedatum: **24. November 2014**

* Neu: Integration der Adobe Marketing Cloud ID
* Verbesserte Debug-Protokolle für mehr Klarheit

## Version 4.2 {#section_806710F7720C410DAB46376C0A7A283E}

Releasedatum: **16. Oktober 2014**

* Neu: Funktionen für In-App-Nachrichten
* Neu: Speicherort für Konfigurationsdatei kann nun beim Anwendungsstart angegeben werden.
* Neu: Interessante Orte können nun automatisch aktualisiert werden, ohne dass eine neue Konfigurationsdatei erforderlich ist.
* New - [!DNL Analytics] calls are now sent as HTTP POST requests.
* Protokollmeldungen optimiert und detailliertere Protokolldaten bei aktiviertem debugLogging hinzugefügt.
* Mehrere Leistungs- und Stabilitätsverbesserungen.

## Version 4.1.3 {#section_8D679B676F604E0B9A64748569185368}

Releasedatum: **18. September 2014**

* Resolved potential crash that could occur if Audience Manager Submit Signal call or [!DNL Target] Load Request call failed due to an unknown network error.

## Version 4.1.2 {#section_6128902E5AE142C4A95D2FB3053188F8}

Releasedatum: **5. August 2014**

* Deadlock-Problem behoben, das bei der Konfiguration von privacyStatus:optunknown und offlineEnabled:false auftrat.

Releasedatum: **4. August 2014**

* Problem behoben, bei dem der Lebenszyklustreffer nicht gesendet wurde, wenn das Referrer-Timeout über 5 Sekunden lag und das Offline-Tracking deaktiviert war.

Releasedatum: **17. April 2014**

* Bluetooth-Beacon-Tracking.
* App-Akquise-Analyse.
* Bei Anwendungen, bei denen Zeitstempel aktiviert sind, werden Absturztreffer auf die richtige Sitzung zurückdatiert.
* Bei Anwendungen, bei denen Zeitstempel aktiviert sind, wird die vorherige Sitzung in einem Treffer gesendet, der auf die richtige Sitzung zurückdatiert ist (nicht länger vorherige Sitzung).
* Stapelverarbeitung von Treffern.

## Version 4.0.2 {#section_B78AE82CDFAD44DCAC6D61E0B80BF4C8}

Releasedatum: **20. Februar 2014**

* Problem behoben, das ein fehlerhaftes Verhalten verursachte, wenn dasselbe Medienelement zweimal hintereinander geöffnet wurde, ohne das vorherige Element zu schließen.

## Version 4.0.1 {#section_A6D017015BC742F69B6EE4A461D00FD7}

Releasedatum: **30. Januar 2014**

* Problem behoben, bei dem mehrere Treffer gesendet wurden, wenn die Datenbank beschädigt war.
* Problem behoben, das im Durchschnitt hohe Sitzungslängen verursachte, wenn ein Gerät über die korrekten Zeiteinstellungen verfügte.

## Version 3.3.2 {#section_6D12768F20C44BA4A0D1EA607D367147}

Releasedatum: **30. Januar 2014**

* Problem behoben, das im Durchschnitt hohe Sitzungslängen verursachte, wenn ein Gerät über die korrekten Zeiteinstellungen verfügte.

## Version 4.0.0 {#section_79DCFAAF1DCB404898E3BE389AC835A6}

Releasedatum: **27. September 2013**

[!DNL iOS] SDK 4. x für Marketing Cloud-Lösungen ist jetzt verfügbar und bietet die folgenden neuen Funktionen:

* Deutliche Leistungsverbesserungen. Die gesamte Verarbeitung erfolgt nun in Hintergrund-Threads; das SDK ist absolut Thread-sicher.
* Geografischer Standort und Orte von Interesse
* Lebenszeitwert
* Zeitgesteuerte Ereignisse
* Anmelde-/Abmeldeverwaltung
* Audience Manager-Unterstützung
* Lifecycle metrics passed to [!DNL Target] as mbox parameters
* Bezüglich Kontextdaten und Verarbeitungsregeln standardisiert

## Version 3.3.0 {#section_28FB7CD64D6C49BF93E321587F1E8950}

Releasedatum: **23. September 2013**

* Unterstützung für ARM64- und X64 Simulator-Architekturen (iPhone 5s) hinzugefügt.

## Version 3.2.1 {#section_3E73A76401664C54B32C7F3BE8BE36E3}

Releasedatum: **16. August 2013**

* Durch Entfernen ungenutzten Codes optimiert.
* Potenzieller Absturz behoben, der auftrat, wenn clearVars in einem Szenario mit Threads verwendet wurde.

## Version 3.2 {#section_A51E0EB26EF246DABE27234C77598D99}

Releasedatum: **6. August 2013**

* Unterstützung für Adobe Audience Manager hinzugefügt.
* Lifecycle data is now sent with [!DNL Target] Mbox requests when lifecycle tracking is enabled.

## Version 3.1.8 {#section_849BCD1D4379433D874B8A0E0099E2B1}

Releasedatum: **20. Juni 2013**

* Fixed a bug introduced in 3.1.7 that was causing issues with lifecycle on devices below [!DNL iOS] 5.0.

## Version 3.1.7 {#section_EC59B76EE3A343D5921E906EB0A8DB49}

Releasedatum: **23. Mai 2013**

* Code hinzugefügt, um zu verhindern, dass übermäßige Lebenszyklustreffer über Standortbenachrichtigungen und Zeitungskiosk-Benachrichtigungen gesendet werden, die eine Anwendung starten.

## Version 3.1.6 {#section_4617D7A41D0841BEBD5829001DC74854}

Releasedatum: **18. April 2013**

* Problem behoben, bei dem die Länge der vorherigen Sitzung in manchen Fällen fehlerhaft berechnet wurde.

## Version 3.1.5 {#section_620AA594868F47619A514AF3C1EAC93B}

Releasedatum: **21. März 2013**

* `ADMS_Measurement.visitorID` wird jetzt mit dem Standardwert vorausgefüllt.

## Version 3.1.4 {#section_B04D1A4858A84A19AA65A57609C9F53F}

Releasedatum: **21. Februar 2013**

* Aufgrund der Thread-Optimierung ist die Einstellung `offlineThrottleDelay` veraltet und nicht mehr erforderlich. Die Einstellung ist noch vorhanden, um die Rückwärtskompatibilität zu gewährleisten, hat jedoch keine Auswirkung mehr.

## Version 3.1.3 {#section_CCFAE5A29FB14DAD9A9F14FE8EE09B75}

Releasedatum: **November 2012**

* Potenzielles EXEC_BAD_Access-Problem beim manuellen Einstellen der Produktvariablen behoben.
* Potenzieller Absturz bei ungültiger Auswahl bei Mbox-Timeout behoben.
* Unterstützung für Anzeigen-Tracking zur Medienmessung hinzugefügt.

## Version 3.1.2 {#section_25C8A6B67AB9487BA5DEB4DB196AE4BC}

Releasedatum: **Oktober 2012**

* Eine Konfigurationsvariable `lifecycleSessionTimeout` wurde hinzugefügt, durch die Sie angeben können, wie viel Zeit in Sekunden zwischen verschiedenen Startvorgängen einer Anwendung verstreichen muss, damit ein Startvorgang als neue Sitzung gilt.
* Behebung eines Problems im Medienmodul, das dazu führte, dass Ereignisse, die für das Messobjekt festgelegt wurden, Ereignisse außer Kraft setzten, die vom Medienmodul festgelegt wurden.
* Fixed an issue that caused an exception when allocating an mbox through the [!DNL Target] integration.

## Version 3.1.0 {#section_0F3E939885DE4DF1B7430DF5F5749AD2}

Releasedatum: **September 2012**

* Die armv7s-Architektur wird nun unterstützt
* Die armv6-Architektur wird nun nicht mehr unterstützt
* Minimum supported [!DNL iOS] SDK is now 4.3

## Version 3.0.2 {#section_1224693620524D6C8CCAB7707483536E}

Releasedatum: **August 2012**

* Kunden, die einen Medienmonitor-Delegate verwenden, sehen nun keine zwei Schließereignisse mehr
* Behebung eines Problems, bei dem Treffer für Schließen manchmal eine Schleife im Medienmonitor verursachen können

## Version 3.0 {#section_D28F56359EC04EDC8521BE93750AE90D}

Releasedatum: **Juli 2012**

Erstes Release.

**Verbesserungen**

* Die Funktion „Automatische Verfolgung“ wurde hinzugefügt
* Die Größe der Bibliothek wurde auf ca. 90k im finalen Build verringert.
* Die Methoden „trackEvents“ und „trackAppState“ wurden hinzugefügt
* Die Unterstützung für Kontextdaten und deren Funktion wurde verbessert. (Es wird empfohlen, Kontextdaten für alle gesendeten Informationen zu verwenden.)
* Die Verfolgung wurde vereinfacht, sodass eine Basisimplementierung der Verfolgung in 5 Minuten eingerichtet werden kann.

**Änderungen**

* [!DNL AppMeasurement] Klasse ist jetzt ADMS_ Measurement
* ADMS_Measurement fungiert nun als ordnungsgemäßes Singleton
* Getter und Setter für eVars, Props, Lists, Hiers, Pevs wurden geändert
* Alle Variablen, die als „Verfolgungsaufrufe“ weitergeleitet wurden, gelten nur für diesen Aufruf.

**Änderung der folgenden Variablen**

| Frühere Version (2.x) | Aktuelle Version (3.x) |
|---|---|
| account | reportSuiteIDs |
| dc | dataCenter |
| pageName | appState |
| contextData | persistentContextData |
| state | geoState |
| zip | geoZip |
| server | appSection |
| debugTracking | debugLogging |
| trackOffline | offlineTrackingEnabled |
| offlineLimit | offlineHitLimit |
| OfflineThrottleDelay | offlineThrottleDelay |

**Die folgenden Variablen werden für einen anderen Zweck verwendet**

* linkURL (gesendet mit trackLinkURL:)
* linkName (gesendet mit trackLinkURL:)
* linkType (gesendet mit trackLinkURL:)
* lightProfileID (gesendet mit trackLight:)
* lightStoreForSeconds (gesendet mit trackLight:)
* lightIncrementBy (gesendet mit trackLight:)
* trackingServerSecure (trackingServer wird verwendet, wenn SSL eingeschaltet ist)

**Die folgenden Variablen wurden entfernt:**

* timestamp
* userAgent
* dynamicVariablePrefix
* visitorNamespace
* pageURL
* pageType
* referrer
* linkLeaveQueryString
* usePlugins
* useBestPractices (überarbeitet von der AutoTracking)
* Delegate
* retrieveLightData
* deleteLightProfiles
* retrieveLightProfiles

## Frühere iOS-Version (2.x) {#section_5F76C3DA854D4BAEA636A68B3811142B}

The following release notes apply to the 2.x version of [!DNL AppMeasurement] for [!DNL iOS]. Wir empfehlen unseren Kunden, so bald als möglich auf die Version 3.x aufzurüsten.

## Version 2.1.12 {#section_85C073B86B684D52A14E8038379F56DD}

Releasedatum: **April 2012**

* Erweiterte Unterstützung für die Videomessung in 
* Behebung von Problemen in Bezug auf linktrackvars und Kontextdaten.
* Es wurden einige zusätzliche Leistungsverbesserungen vorgenommen.

## Version 2.1.11 {#section_F0AF2D4E5F504D798EEB95BE8FE61B4C}

Releasedatum: **März 2012**

* Es wurde ein Problem behoben, durch das bei der Offline-Verfolgung das Senden von Daten unter bestimmten Umständen beendet wurde.

## Version 2.1.10 {#section_07C24EC83AA94A6AA6AB3DE7E8D6227F}

Releasedatum: **Februar 2012**

* Ein Fehler wurde behoben, bei dem unter bestimmten Umständen eine EXC_BAD_ACCESS-Ausnahme verursacht wurde, wenn mehrere Threads gleichzeitig versuchten, einen Verfolgungsaufruf durchzuführen.
* Ein Zeitstempel wurde zu Variablen hinzugefügt, die mit geringeren Verfolgungsaufrufen (trackLight) verwendet werden.

## Version 2.1.8 {#section_ACC6974CE3F741E58786CA8048F04521}

Releasedatum: **Januar 2012**

* Die Leistung des Tracking-Threads wurde deutlich optimiert.
* Der Offline-Treffer-Speicherort wurde an einen Speicherort verschoben, der nicht mit iCloud synchronisiert wird, um Best Practice von iCloud einzuhalten.
* Die Bibliothek wurde entsprechend dem FAT-Binärformat von Apple aktualisiert, sodass Sie die spezifische Bibliothek nicht mehr in Ihre Build-Architektur aufnehmen müssen.

## Version 2.1.6 {#section_63B4967C537847C28D33EBB92CC15695}

Releasedatum: **November 2011**

* Added support for [!DNL iOS] 5.
* [!DNL AppMeasurement] für wurde aktualisiert und verwendet jetzt nicht mehr den veralteten UDID-Wert als Standardwert für visitorID.[!DNL iOS] Wenn Sie in Ihrer Anwendung eine benutzerdefinierte visitorID festlegen (z. B. `s.visitorID = @12345`), wirkt sich diese Änderung nicht darauf aus. Wenn Sie eine benutzerdefinierte visitorID festlegen, wird nicht die UDID als Wert für visitorID verwendet. Stattdessen wird beim ersten Starten eine zufällige visitorID generiert und in einem Benutzerstandardschlüssel gespeichert. This key is used by [!DNL AppMeasurement] from that point forward. Dieser Schlüssel wird auch während des Standardprozesses zur Anwendungssicherung gespeichert und wiederhergestellt.

* Updated calls from the [!DNL iOS] Best Practices plug-in that are not associated with a page view to send hits using trackLink. Dadurch wird verhindert, dass diese Treffer Seitenansichten mit dem Standardwert „Anwendungsname/Version“ aufzeichnen.

## Version 2.1.3 {#section_E39666D780554B7398900C39C285CDB8}

Releasedatum: **Oktober 2011**

* Verbesserungen beim Umgang mit Stellvertretungsregeln. This fixes an issue that caused the [!DNL iOS] Best Practices Plug-in to crash when bringing the application out of the background.

## Version 2.1.2 {#section_21014073AF804EFC8231047D8847485C}

Releasedatum: **September 2011**

* Der Header wurde aktualisiert, um die Verwendung von Prop und eVar 51–75 zu aktivieren.

## Version 2.1.1 {#section_8FB3D7C77C884E2AB982103BF7E3312A}

Releasedatum: **August 2011**

* Fähigkeit zum Durchsuchen der Report Suites und Metriken beim Ausführen eines Berichts.
* Unterstützung für Kontextdaten, welche die Verarbeitungsregeln auf Serverseite (nur v15) aktivieren.
* Unterstützung für leichte Serveraufrufe (aktuell in Beta-Version).

