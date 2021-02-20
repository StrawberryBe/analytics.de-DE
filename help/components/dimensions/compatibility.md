---
title: Kompatibilität von Analytics-Dimensionen
description: Referenz zu Analytics-Dimensionen und -Berichten.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 100%

---


# Kompatibilität von Analytics-Dimensionen

Auf dieser Seite sind die Dimensionen aufgelistet, die in ihren jeweiligen Analytics-Funktionen unterstützt werden.

>[!NOTE]
>
>Benutzerdefinierte Variablennamen, Klassifizierungen und Besucherattribute werden in dieser Liste weggelassen. Diese Dimensionselemente sind spezifisch für einzelne Report Suites.

>[!NOTE]
>
>Es gibt Überschneidungen, bei denen Analytics-Tools unterschiedliche Begriffe für ähnliche Dimensionen verwenden. Beispielsweise verwendet Reports &amp; Analytics `browserwidth`, während Analysis Workspace `browserwidthbucketed` verwendet.

## Unterstützte Dimensionen sowohl in Reports &amp; Analytics als auch im Analysis Workspace

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|---|---|
| Analytics für Target | `targetraw` |
| Zielgruppen-ID | `mcaudiences` |
| Browser | `browser` |
| Browser-Typ | `browsertype` |
| Kategorie | `category` |
| Städte | `geocity` |
| Farbtiefe | `colordepth` |
| Verbindungstyp | `connectiontype` |
| Cookie-Unterstützung | `cookie` |
| Länder | `geocountry` |
| Kundenloyalität | `customerloyalty` |
| Benutzerspezifische Konversionsvariable | `evar1`, `evar2` usw. |
| Benutzerspezifische Insight-Variablen | `prop1`, `prop2` usw. |
| Benutzerspezifischer Link | `customlink` |
| Tage bis Erstkauf | `daysbeforefirstpurchase` |
| Tage seit letztem Kauf | `dayssincelastpurchase` |
| Domäne | `filtereddomain` |
| Downloadlink | `downloadlink` |
| Entrypage | `entrypage` |
| Ursprüngliche Entrypage | `entrypageoriginal` |
| Exitlink | `exitlink` |
| Erstkontakt-Kanal | `firsttouchchannel` |
| Erstkontakt-Kanaldetail | `firsttouchchanneldetail` |
| Java aktiviert | `javaenabled` |
| Sprache | `language` |
| Letztkontakt-Kanal | `lasttouchchannel` |
| Letztkontakt-Kanaldetail | `lasttouchchanneldetail` |
| Listenvariablen | `listvariables` |
| Marketing-Kanal | `marketingchannel` |
| Mobilgerät – Audio-Unterstützung | `mobileaudiosupport` |
| Mobilnetzbetreiber | `mobilecarrier` |
| Mobilgerät – Farbtiefe | `mobilecolordepth` |
| Mobilgerät – Cookie-Unterstützung | `mobilecookiesupport` |
| Mobilgerät | `mobiledevicename` |
| Mobilgerätetyp | `mobiledevicetype` |
| Maximale mobile E-Mail-Länge | `mobileemaillength` |
| Mobilgerät – Bildunterstützung | `mobileimagesupport` |
| Mobilgerätehersteller | `mobilemanufacturer` |
| Mobiles Betriebssystem (veraltet) | `mobileos` |
| Mobilgerät – Bildschirmhöhe | `mobilescreenheight` |
| Mobilgerät – Bildschirmgröße | `mobilescreensize` |
| Mobilgerät – Bildschirmbreite | `mobilescreenwidth` |
| Maximale mobile Browser-URL-Länge | `mobileurllength` |
| Mobilgerät – Video-Unterstützung | `mobilevideosupport` |
| Bildschirmauflösung | `monitorresolution` |
| Betriebssysteme | `operatingsystem` |
| Ursprüngliche Referrer-Domäne | `referringdomainoriginal` |
| Seite | `page` |
| Seiten nicht gefunden | `pagesnotfound` |
| Produkt | `product` |
| Referrer | `referrer` |
| Referrer-Typ | `referrertype` |
| Referrer-Domäne | `referringdomain` |
| Regionen | `georegion` |
| Rückkehrhäufigkeit | `returnfrequency` |
| SC-TnT | `tntbase` |
| Suchmaschine | `searchengine` |
| Suchbegriff | `searchenginekeyword` |
| Suchmaschine  – kostenlos | `searchenginenatural` |
| Suchmaschine – bezahlt | `searchenginepaid` |
| Suchbegriff – kostenlos | `searchenginenaturalkeyword` |
| Suchbegriff – bezahlt | `searchenginepaidkeyword` |
| Rangansicht aller Suchseiten | `searchenginepagerank` |
| Server | `server` |
| Einzelseitenbesuche | `singlepagevisits` |
| Website-Bereich | `sitesections` |
| Zeit pro Besuch – präzise | `sitetime` |
| Trackingcode | `campaign` |
| US-DMA | `geodma` |
| US-Staaten | `state` |
| Zeit vor Ereignis | `timeprior` |
| Zeit pro Besuch – zusammengefasst | `timespent` |
| Besuchstiefe | `pathlength` |
| Besuchsnummer | `visitnumber` |
| Postleitzahl | `zip` |

## Nur in Analysis Workspace unterstützte Dimensionen

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Vormittag/Nachmittag | `timepartampm` |
| Browser-Höhe – zusammengefasst | `browserheightbucketed` |
| Browser-Breite – zusammengefasst | `browserwidthbucketed` |
| Tag | `daterangeday` |
| Tag des Monats | `timepartdayofmonth` |
| Wochentag | `dayofweek` |
| Wochentag | `timepartdayofweek` |
| Tag des Jahres | `timepartdayofyear` |
| Tage seit dem letzten Besuch | `dayssincelastvisit` |
| Einstieg benutzerdefinierte Insights | `entryprops` |
| Einstieg Listenvariablen | `entrylistvariables` |
| Entryserver | `entryserver` |
| Einstiegsbereich | `entrysitesections` |
| Ausstieg benutzerdefinierte Insights | `exitprops` |
| Ausstieg Listenvariablen | `exitlistvariables` |
| Exitpage | `exitpage` |
| Ausstiegs-Server | `exitserver` |
| Ausstiegsbereich | `exitsitesections` |
| Treffertiefe | `hitdepth` |
| Treffertyp | `hittype` |
| Stunde | `daterangehour` |
| Stunde des Tages | `timeparthourofday` |
| Detail des Marketing-Kanals | `marketingchanneldetail` |
| Minute | `daterangeminute` |
| Maximale mobile Lesezeichenlänge | `mobilebookmarklength` |
| Mobilgerätenummer | `mobiledevicenumber` |
| Mobil-DRM | `mobiledrm` |
| Mobile Informationsdienste | `mobileinformationservices` |
| Mobile Java-VM | `mobilejavavm` |
| Mobilgerät – Mail-Design | `mobilemaildecoration` |
| Mobile Netzprotokolle | `mobilenetprotocols` |
| Mobiles PTT | `mobilepushtotalk` |
| Monat | `daterangemonth` |
| Monat des Jahres | `timepartmonthofyear` |
| Betriebssystemtypen | `operatingsystemgroup` |
| Paid Search | `paidsearch` |
| Unterstützung persistenter Cookies | `persistentcookie` |
| Quartal | `daterangequarter` |
| Quartal des Jahres | `timepartquarterofyear` |
| Umfrage | `surveybase` |
| Besuchszeit pro Seite – zusammengefasst | `averagepagetime` |
| Besuchszeit pro Seite – präzise | `pagetimeseconds` |
| Nachverfolgen des Abmeldegrunds | `optoutreason` |
| Wochentag/Wochenende | `timepartweekdayweekend` |
| Woche | `daterangeweek` |
| Jahr | `daterangeyear` |

## Inhaltsorientierte Dimensionen, die nur in Analysis Workspace unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| Mediensitzungs-ID | `videosessionid` |
| Nielsen-Zugriffsmethode | `nielsenaccmethod` |
| Nielsen-App-ID | `nielsenappid` |
| Nielsen-Kanal-Asset | `nielsenchannelasset` |
| Nielsen-Content-Typ | `nielsencontenttype` |

## Dimensionen, die nur in Reports &amp; Analytics unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Browser-Höhe | `browserheight` |
| Browser-Breite | `browserwidth` |
| Unique Customers pro Tag | `dailyuniquecustomers` |
| JavaScript | `javascriptsupport` |
| JavaScript-Version | `javascriptversion` |
| Unique Customers pro Monat | `monthlyuniquecustomers` |
| Unique Customers pro Quartal | `quarterlyuniquecustomers` |
| Zeitzonen | `timezone` |
| Domänen auf oberster Ebene | `topleveldomain` |
| Bundesland des Besuchers | `legacystate` |
| Unique Customers pro Woche | `weeklyuniquecustomers` |
| Unique Customers pro Jahr | `yearlyuniquecustomers` |

## Inhaltsorientierte Dimensionen, die sowohl von Reports &amp; Analytics als auch vom Analysis Workspace unterstützt werden

### Video (Media Analytics)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Inhalt | `video` |
| Inhaltssegment | `videosegment` |
| Content-Typ | `videocontenttype` |
| Name des Anzeigen-Players | `videoadplayername` |
| Anzeigenposition innerhalb der Werbeunterbrechung | `videoadinpod` |
| Gelöschte Frames | `videoqoedroppedframecountevar` |
| Fehler | `videoqoeerrorcountevar` |
| Durchschnittliche Bitrate | `videoqoebitrateaverageevar` |
| Bitratenänderungen | `videoqoebitratechangecountevar` |
| Gesamtpufferdauer | `videoqoebuffertimeevar` |
| Pufferereignisse | `videoqoebuffercountevar` |
| Zeit bis Start | `videoqoetimetostartevar` |
| Anzeigen-Pod | `videoadpod` |
| Medienpfad | `videopath` |
| Anzeige | `videoad` |
| Inhalts-Player-Name | `videoplayername` |
| Inhaltskanal | `videochannel` |
| Kapitel | `videochapter` |
| Inhaltsname (Variable) | `videoname` |
| Inhaltsdauer (Variable) | `videolength` |
| Anzeigename (Variable) | `videoadname` |
| Anzeigenlänge (Variable) | `videoadlength` |
| Serie | `videoshow` |
| Staffel | `videoseason` |
| Folge | `videoepisode` |
| Netzwerk | `videonetwork` |
| Sendungstyp | `videoshowtype` |
| Anzeige-Ladevorgänge | `videoadload` |
| MVPD | `videomvpd` |
| Tagesteil | `videodaypart` |
| Advertiser | `videoadadvertiser` |
| Kampagnen-ID | `videoadcampaign` |
| Genre | `videogenre` |
| Stream-Typ | `videostreamtype` |
| Player-SDK-Fehler-IDs | `videoqoeplayersdkerrors` |
| Externe Fehler-IDs | `videoqoeextneralerrors` |
| Medien-Feed-Typ | `videofeedtype` |
| Medien-Einstiegspfad | `entryvideopath` |
| Medien-Ausstiegspfad | `exitvideopath` |
| Einstiegs-Genre | `entryvideogenre` |
| Ausstiegs-Genre | `exitvideogenre` |
| Einstieg-Player-SDK-Fehler-IDs | `entryvideoqoeplayersdkerrors` |
| Ausstieg-Player-SDK-Fehler-IDs | `exitvideoqoeplayersdkerrors` |
| Einstieg – Externe Fehler-IDs | `entryvideoqoeextneralerrors` |
| Ausstieg – Externe Fehler-IDs | `exitvideoqoeextneralerrors` |

### Adobe Social

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Begriffe | `socialterm` |
| Soziale Plattformen/Eigenschaften | `socialcontentprovider` |
| Autoren | `socialauthor` |
| Sprache | `sociallanguage` |
| Breitengrad/Längengrad | `sociallatlong` |
| Asset-Trackingcodes | `socialassettrackingcode` |
| Eigene Social-Media-Präsenzen | `socialaccountandappids` |
| Eigene Post-IDs | `socialownedpostids` |
| Eigene Social-Media-Definitionen | `socialinteractiontype` |
| Eigene Eigenschafts-IDs | `socialownedpropertyid` |
| Eigene Eigenschaften vs. Anwendung | `socialownedpropertypropertyvsapp` |
| Eigener Eigenschaftsname | `socialownedpropertyname` |
| Eigene Definitionseigenschaft vs. Post | `socialowneddefinitionpropertyvspost` |
| Eigene Definition – Insight-Typ | `socialowneddefinitioninsighttype` |
| Eigene Definition – Insight-Wert | `socialowneddefinitioninsightvalue` |
| Eigene Definition – Metrik | `socialowneddefinitionmetric` |
| Asset | `socialmediaid` |

### Mobile SDK

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Erster Starttermin | `mobileinstalldate` |
| App-ID | `mobileappid` |
| Launch-Nummer | `mobilelaunchnumber` |
| Tage seit der ersten Verwendung | `mobiledayssincefirstuse` |
| Tage seit der letzten Verwendung | `mobiledayssincelastuse` |
| Stunde des Tages (SDK) | `mobilehourofday` |
| Wochentag (SDK) | `mobiledayofweek` |
| Betriebssystem (SDK) | `mobileosenvironment` |
| Tage seit letztem Upgrade | `mobiledayssincelastupgrade` |
| Starts seit letztem Upgrade | `mobilelaunchessincelastupgrade` |
| Gerätename (SDK) | `mobiledevice` |
| Betriebssystemversion (SDK) | `mobileosversion` |
| Beacon-Major-Wert | `mobilebeaconmajor` |
| Beacon-Minor-Wert | `mobilebeaconminor` |
| Beacon-UUID | `mobilebeaconuuid` |
| Beacon-Nähe | `mobilebeaconproximity` |
| Standort (bis 10 km) | `latlon1` |
| Standort (bis 100 m) | `latlon23` |
| Standort (bis 1 m) | `latlon45` |
| Zielpunkt-Bezeichnung | `pointofinterest` |
| Entfernung zum Zentrum des Zielpunkts | `pointofinterestdistance` |
| Ortungsgenauigkeit | `mobileplaceaccuracy` |
| Kategorie des Orts | `mobileplacecategory` |
| Ort-ID | `mobileplaceid` |
| Einstieg-Beacon-Major-Wert | `entrymobilebeaconmajor` |
| Ausstieg-Beacon-Major-Wert | `exitmobilebeaconmajor` |
| Einstieg-Beacon-Minor-Wert | `entrymobilebeaconminor` |
| Ausstieg-Beacon-Minor-Wert | `exitmobilebeaconminor` |
| Einstieg-Beacon-UUID | `entrymobilebeaconuuid` |
| Ausstieg-Beacon-UUID | `exitmobilebeaconuuid` |
| Einstieg-Beacon-Nähe | `entrymobilebeaconproximity` |
| Ausstieg-Beacon-Nähe | `exitmobilebeaconproximity` |

### Adobe Advertising Cloud (AMO)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| AMO EF ID | `amo_ef_id` |
| AMO-ID | `amo_cid` |

### Activity Map

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Activity Map-Link nach Region | `clickmaplinkbyregion` |
| Activity Map-Region | `clickmapregion` |
| Activity Map-Link | `clickmaplink` |
| Activity Map-Seite | `clickmappage` |

### Nielsen-Integration

Weitere Informationen zur Umsetzung dieser Integration finden Sie unter [Nielsen-Erweiterung](https://exchange.adobe.com/experiencecloud.details.101361.html).

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Nielsen-Anzeigenmodell | `nielsenadmodel` |
| Nielsen-Segment C | `nielsensegmentc` |
| Nielsen-Segment B | `nielsensegmentb` |
| Nielsen-Segment A | `nielsensegmenta` |
| Nielsen-Inhalts-ID | `nielsencontentid` |
| Nielsen-Asset/-Programm | `nielsenasset` |
| Nielsen-VCID | `nielsenvcid` |
| Nielsen Opt-out | `nielsenoptout` |
| Nielsen-Client-ID und -VCID | `nielsenclientidvcid` |
| Nielsen-Client-ID | `nielsenclientid` |
| Einstieg-Nielsen-Ausschluss | `entrynielsenoptout` |
| Ausstieg-Nielsen-Ausschluss | `exitnielsenoptout` |
| Einstieg-Nielsen-Client-ID und -VCID | `entrynielsenclientidvcid` |
| Ausstieg-Nielsen-Client-ID und -VCID | `exitnielsenclientidvcid` |
| Einstieg-Nielsen-Client-ID | `entrynielsenclientid` |
| Ausstieg-Nielsen-Client-ID | `exitnielsenclientid` |

### Adobe Experience Manager (AEM)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Element-ID | `aemassetid` |
| Asset-Quelle | `aemassetsource` |
| Angeklickte Asset-ID | `aemclickedassetid` |
| Einstieg-Asset-ID | `entryaemassetid` |
| Ausstieg-Asset-ID | `exitaemassetid` |

### Adobe Campaign

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Adobe Campaign – ID der ausgeführten Bereitstellung | `ac_delivery_internal_name` |
