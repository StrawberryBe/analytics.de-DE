---
description: 'Die meisten Mobilgeräte akzeptieren Browser-Cookies. Wenn Geräte allerdings keine Cookies akzeptieren, werden Wireless-Geräte anhand einer anderen Methode eindeutig identifiziert. '
keywords: Analytics-Implementierung
seo-description: 'Die meisten Mobilgeräte akzeptieren Browser-Cookies. Wenn Geräte allerdings keine Cookies akzeptieren, werden Wireless-Geräte anhand einer anderen Methode eindeutig identifiziert. '
seo-title: Identifizieren von Mobilgeräten
solution: Analytics
title: Identifizieren von Mobilgeräten
topic: Entwickler und Implementierung
uuid: 22587 dd 1-cead -485 b-a 4 d 8-94 dfb 7 cd 6662
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Identifizieren von Mobilgeräten

Die meisten Mobilgeräte akzeptieren Browser-Cookies. Wenn Geräte allerdings keine Cookies akzeptieren, werden Wireless-Geräte anhand einer anderen Methode eindeutig identifiziert. 

Adobe hat eine Reihe von HTTP-[Abonnenten-ID-Headern](../../../implement/js-implementation/c-unique-visitors/visid-mobile.md#section_60D6EAC0D16945A89DD5A7ADF3B8298D) identifiziert, über die die meisten Mobilgeräte eindeutig identifiziert werden können. Diese Header enthalten oftmals die Telefonnummer des Geräts (in Klartext- oder Hashform) oder andere IDs. Die meisten aktuellen Geräte verfügen über einen oder mehrere der Header, anhand derer das Gerät eindeutig identifiziert werden kann, und alle Adobe-Datenerfassungsserver verwenden diese Header dann automatisch anstelle einer Besucher-ID.

In a typical image request, a '1' in the path ( `/b/ss/rsid/1`) causes Adobe servers to return a gif image and to attempt to set a persistent [!UICONTROL visitor ID] cookie ( `AMCV_` or `s_vi`). Wenn das Gerät allerdings basierend auf den HTTP-Headern als Mobilgerät erkannt wird, wird eine „5“ anstelle der „1“ übergeben. Dies gibt an, dass ein Bild im WBMP-Format zurückgegeben werden soll und dass unsere Liste mit bekannten Wireless-Headern (kein Cookie) zur Identifizierung des Geräts verwendet werden soll.

In der folgenden Tabelle wird die Reihenfolge der verwendeten ID-Methoden basierend auf dem Rückgabebild-Typwert („1“ oder „5“) im Pfad aufgeführt:

<table id="table_07B0E55D5DAA4552A5CBC6937D47A857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Reihenfolge der ID-Methoden </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code> /1/</code> </td> 
   <td colname="col2"> <p>Standardeinstellung: </p> 
    <ul id="ul_E37E9919658A492C92187BAA18D33AB6"> 
     <li id="li_1A9E39C7CFB24C68AA07C8E85D33A858">Benutzerspezifische Besucher-ID </li> 
     <li id="li_0DC8D17828C848BEB614C6E47C090064">Cookie </li> 
     <li id="li_52706792FAD14F459266E3A672F92EA1">Abonnenten-ID-Header </li> 
     <li id="li_ECAD713D22314338BB5C92167DC0BB02"> IP-Adresse, Benutzeragent, Gateway-IP-Adresse </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> /5/ /5.1/ /5.5/</code> </td> 
   <td colname="col2"> <p>Gerät wurde als Wireless-Gerät erkannt, oder <code>/5/</code> wurde manuell in der Bildanforderung gesendet: </p> 
    <ul id="ul_624BEDFA3E1243CF9B42081D8B8EFFFB"> 
     <li id="li_D65761D23B684DB59BC23E92C9098122">Benutzerspezifische Besucher-ID </li> 
     <li id="li_ADBA806B74CA43EFA8612301E06106C6">Abonnenten-ID-Header </li> 
     <li id="li_79DFD0DEAA1242C09A03E8134A40F799">Cookie </li> 
     <li id="li_A462B9120FC6443480D62F37D456747E">IP-Adresse, Benutzeragent, Gateway-IP-Adresse </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch eine „1“ oder eine „5“ in manuellen Bildanforderungen übergeben. Achten Sie aber darauf, dass sich diese Codes gegenseitig ausschließen. Wenn Sie also immer „5“ übergeben, wird kein Cookie genutzt, wenn dies unterstützt wird. Sie können einen eigenen Mechanismus einfügen, um festzustellen, ob ein Gerät Cookies unterstützt, und dann anstelle der „5“ eine „1“ im Bild übergeben. Die Verbesserungen hinsichtlich der Genauigkeit, die so erzielt werden können, sind dabei nur bei Geräten möglich, die Cookies unterstützen.

## Abonnenten-ID-Header {#section_60D6EAC0D16945A89DD5A7ADF3B8298D}

Die Methode mit Abonnenten-IDs zur Benutzeridentifizierung ist in der Regel zuverlässiger als ein Cookie, da Cookies möglicherweise gelöscht oder nicht zugelassen werden oder weil es möglicherweise Probleme mit der Verwaltung von Gateway-Cookies gibt.

Sie können Änderungen an der Identifizierung von Besuchern optimieren, wenn Sie sich der White-List des Mobilnetzbetreibers hinzufügen lassen, den die Besucher nutzen. Um Zugang zur Besucher-ID des Mobilnetzbetreibers zu erhalten, wenden Sie sich an den Mobilnetzbetreiber, und lassen Sie Ihre Domäne die White-List aufnehmen. Wenn Sie in der White-List eines Mobilnetzbetreibers eingetragen sind, haben Sie Zugang zu Abonnenten-ID-Headern, was sonst nicht der Fall wäre.

In der folgenden Liste sind die Header aufgeführt, mit denen Wireless-Geräte identifiziert werden. Der Algorithmus für die Verarbeitung der Header beinhaltet

1. die Extrahierung des HTTP-Header-Schlüssels (der Name des Headers, wie „X-Up-Calling-Line-ID“)
1. das Entfernen aller Zeichen, die keine Buchstaben sind (A–Z und a–z)
1. das Konvertieren des Header-Schlüssels in Kleinbuchstaben
1. den Vergleich des Schlüsselendes mit denen in der folgenden Tabelle, um eine Übereinstimmung zu finden:

| Header | Typ | Beispiel |
|---|---|---|
| callinglineid | ID | X-Up-Calling-Line-ID: 8613802423312 |
| subno | ID | x-up-subno: swm_10448371100_vmag.mycingular.net |
| clientid | ID | ClientID: eGtUpsqEO19zVHmbOkgaPVI-@sprintpcs.com |
| uid | ID | x-jphone-uid: a2V4Uh21XQH9ECNN |
| clid | ID | X-Hts_clid: 595961714786 |
| deviceid | ID | rim-device-id: 200522ae |
| forwardedfor | ID oder IP-Adresse | X-Forwarded-For: 127.0.0.1 |
| msisdn | ID oder IP-Adresse | X-Wap-msisdn: 8032618185 |
| clientip | IP-Adresse | Client-ip: 10.9.41.2 |
| wapipaddr | IP-Adresse | X-WAPIPADDR: 10.48.213.162 |
| huaweinasip | IP-Adresse | x-huawei-NASIP: 211.139.172.70 |
| userip | IP-Adresse | UserIP: 70.214.81.241 |
| ipaddress | IP-Adresse | X-Nokia-ipaddress: 212.97.227.125 |
| subscriberinfo | IP-Adresse | X-SUBSCRIBER-INFO: IP=10.103.132.128 |

So würde zum Beispiel „callinglineid“ mit „X-Up-Calling-Line-ID“ und „nokia-callinglineid“ übereinstimmen. Anhand des Header-Typs erkennen wir, was im Header stehen soll. Die Reihenfolge der Einträge in der Liste gibt die Priorität der Header wieder (wenn z. B. ein „callinglineid“-Header vorhanden ist, wird er anstelle von „subno“ verwendet).

Sie können [dynamische Variablen](../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262) verwenden, um spezielle Werte aus einem Header zu extrahieren.
