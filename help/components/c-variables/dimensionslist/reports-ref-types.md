---
description: Wenn Sie die Referrer bei jedem Besuch verfolgen und aufzeichnen, können Sie feststellen, wie Ihre Besucher bei jedem Besuch zu Ihrer Site gefunden haben.
seo-description: Wenn Sie die Referrer bei jedem Besuch verfolgen und aufzeichnen, können Sie feststellen, wie Ihre Besucher bei jedem Besuch zu Ihrer Site gefunden haben.
seo-title: Typ der verweisenden Stelle
solution: Analytics
title: Typ der verweisenden Stelle
topic: 'Berichte    '
uuid: 7 f 63 d 327-d 223-4537-a 722-4780 aae 05 c 2 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Typ der verweisenden Stelle

Wenn Sie die Referrer bei jedem Besuch verfolgen und aufzeichnen, können Sie feststellen, wie Ihre Besucher bei jedem Besuch zu Ihrer Site gefunden haben.

In der folgenden Liste sind die verschiedenen Arten von verweisenden Stellen definiert:

**Andere Websites**: Andere verweisende Websites werden aufgezeichnet, wenn Besucher auf einen Link auf einer Seite einer anderen Website klicken (die nicht Bestandteil Ihrer Website ist) und daraufhin zu Ihrer Website gelangen.

**Suchmaschinen**: Verweisende Suchmaschinen werden aufgezeichnet, wenn Besucher eine Suchmaschine verwenden, um auf Ihre Website zuzugreifen. Der Wert für die verweisende Stelle muss für Adobe als Suchmaschine zu erkennen sein. Dieser Wert darf nicht aus einer Subdomäne bestehen, die nicht als Suchmaschine gilt ([!DNL mail.yahoo.com] ist beispielsweise keine Suchmaschine, da diese Domäne für E-Mails verwendet wird).

**[!UICONTROL Soziale Netzwerke:]** Der Wert für die verweisende Stelle muss für Adobe als soziales Netzwerk erkennbar sein. Siehe die [Liste der sozialen Netzwerke](https://helpx.adobe.com/analytics/kb/list-social-networks.html).

**E-Mail**: Eine verweisende Domäne wird als eine E-Mail-Verweisende Domäne betrachtet, wenn Besucher auf einen per E-Mail gesendeten Link klicken, der das Protokoll [!DNL imap://] enthält, oder [!DNL mail://] zu Ihrer Site gelangen. So würden beispielsweise alle Nachrichten, die von [!DNL https://mail.yahoo.com] kommen, nicht als verweisende E-Mail-Stelle gelten, weil das Protokoll [!DNL https://] :// lautet. E-Mails von Outlook sind in der Zeile „Eingegeben/Mit Lesezeichen versehen“ aufgeführt, während Referrer mit dem HTTP-Protokoll, deren Domäne eine bekannte Suchmaschine ist, in der Zeile „Suchmaschine“ aufgeführt sind.

**Eingegeben/mit Lesezeichen versehen**: Verweisende Stellen in Form von Eingaben/Lesezeichen werden verzeichnet, wenn Besucher die URL Ihrer Website direkt in ihren Browser eingeben oder über Lesezeichen auf Ihre Site zugreifen. Mobile devices report a referrer type of *`typed/bookmarked`* if there is no referrer on the first hit of the visit.

**[!UICONTROL Innerhalb Ihrer Site]**: Diese Elemente sind URLs, die von den internen URL-Filtern vergeben werden. These items are not counted as *`referrer instances`* but can be seen when reporting on other metrics.

## Typen der verweisenden Stellen nach Schnittstelle {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketing Reports &amp; Analytics (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad-hoc-Analysen </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Typen verzeichneter verweisender Stellen </td> 
   <td colname="col2"> 
    <ul id="ul_EFC8E81EC6DF4CC2AC0E290244FD5859"> 
     <li id="li_686FCAEB04054B9F8A7D2434E8C49F04">Andere Websites </li> 
     <li id="li_C232868230AA4A54958B524F3D8FDA35"> Suchmaschinen </li> 
     <li id="li_A89BFD0468F74ED7822F64BE4A7332AE"> Social </li> 
     <li id="li_C824E6F7F6E748DD827A95B105ADBADD"> Eingaben/Lesezeichen </li> 
    </ul> <p> In diesem Bericht werden nur zwei vordefinierte Metriken angezeigt: Instanzen und Unique Visitors. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_FD81EB3C1BD949A39C5A9E9688D25271"> 
     <li id="li_6099E7E03F3843D484808258A332BBE9">Andere Websites </li> 
     <li id="li_5AABC02DA7964D578BF8404DA819245D"> Suchmaschinen </li> 
     <li id="li_B18907AC7FA1429A893B57634EB7DC6F"> Social </li> 
     <li id="li_7674B67897994E1FA99BCD9B604BCB6E"> Eingaben/Lesezeichen </li> 
    </ul> </td> 
   <td colname="col4"> 
    <ul id="ul_C37ADBEC31D04295BF5CDEA25DB5191A"> 
     <li id="li_81A642C96C674669BA00B2DACA534B8A">Andere Websites </li> 
     <li id="li_29B9DA9F2AAD46A69886D34D5E6E43D4"> Suchmaschinen </li> 
     <li id="li_E381EEF111F248F99EE39600D616B7C2"> Social </li> 
     <li id="li_596377F4D3C248BEA5191EE2985A2B13"> Eingaben/Lesezeichen </li> 
     <li id="li_A7A72D3D6B9A4CCFB43EDA77ABFDEDBC"> In Ihrer Site </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Hinweise {#section_B83A3571D64E4E7792712FAF740D7955}

* Die verweisende Stelle, der Typ der verweisenden Stelle und die verweisende Domäne werden beim ersten Treffer jedes Besuchs festgelegt, oder während eines Besuchs, wenn es sich um eine externe verweisende Stelle handelt (z. B. wenn ein Besucher Ihre Site verlässt, eine Suchmaschine verwendet und zur Site zurückkehrt, bevor der erste Besuch abläuft). Diese Werte werden gleichzeitig festgelegt und bleiben für die Dauer des Besuchs persistent.
* Nicht alle Typen von verweisenden Stellen werden in diesem Bericht aufgelistet. Das bedeutet, dass die Besuche der gesamten Site nicht mit den Besuchen in diesem Bericht übereinstimmen.

## Berichte – Verlauf {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

| Datum | Ändern |
|---|---|
| 16.01.2014 | Data Warehouse wurde aktualisiert, um der Logik von Marketing Reports &amp; Analytics zu entsprechen. Vor diesem Datum war der Typ der verweisenden Stelle nicht für die Dauer des Besuchs persistent. |

