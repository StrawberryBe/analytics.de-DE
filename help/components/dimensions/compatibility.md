---
title: Kompatibilität von Analytics-Dimensionen
description: Referenz zu Analytics-Dimensionen und -Berichten.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 92%

---


# Kompatibilität von Analytics-Dimensionen

Auf dieser Seite werden Dimensionen Liste, die in den jeweiligen Analytics-Funktionen unterstützt werden.

>[!NOTE]
>
>Benutzerdefinierte Variablennamen, Classifications und Besucher-Attribute werden in dieser Liste weggelassen. Diese Dimensionswerte sind spezifisch für einzelne Report Suites.

>[!NOTE]
>
>Es gibt Überschneidungen, bei denen Analytics-Tools unterschiedliche Begriffe für ähnliche Dimensionen verwenden. Beispielsweise verwendet Reports &amp; Analytics `browserwidth` während der Verwendung durch Analysis Workspace `browserwidthbucketed`.

## Unterstützte Dimensionen sowohl in Reports &amp; Analytics als auch im Analysis Workspace

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|---|---|
| Analytics für Target | `targetraw` |
| Audiences ID | `mcaudiences` |
| Browser | `browser` |
| Browsertyp | `browsertype` |
| Kategorie | `category` |
| Städte | `geocity` |
| Farbtiefe | `colordepth` |
| Verbindungstyp | `connectiontype` |
| Cookie-Unterstützung | `cookie` |
| Länder | `geocountry` |
| Kundentreue | `customerloyalty` |
| Benutzerspezifische Konversionsvariable | `evar1`, `evar2`, etc. |
| Benutzerspezifische Insight-Variablen | `prop1`, `prop2`, etc. |
| Benutzerspezifischer Link | `customlink` |
| Tage bis Erstkauf | `daysbeforefirstpurchase` |
| Tage seit letztem Kauf | `dayssincelastpurchase` |
| Domäne | `filtereddomain` |
| Downloadlink | `downloadlink` |
| Entrypage | `entrypage` |
| Entrypage ursprünglich | `entrypageoriginal` |
| Exitlink | `exitlink` |
| Erstkontakt-Kanal | `firsttouchchannel` |
| Erstkontakt Kanaldetail | `firsttouchchanneldetail` |
| Java aktiviert | `javaenabled` |
| Sprache | `language` |
| Letztkontakt-Kanal | `lasttouchchannel` |
| Letztkontakt Kanaldetail | `lasttouchchanneldetail` |
| Listenvariablen | `listvariables` |
| Marketing-Kanal | `marketingchannel` |
| Mobilgerät - Audio-Unterstützung | `mobileaudiosupport` |
| Mobilnetzbetreiber | `mobilecarrier` |
| Mobilgerät - Farbtiefe | `mobilecolordepth` |
| Mobilgerät - Cookie-Unterstützung | `mobilecookiesupport` |
| Mobilgerät | `mobiledevicename` |
| Mobilgerätetyp | `mobiledevicetype` |
| Mobil - max. E-Mail-Länge | `mobileemaillength` |
| Mobilgerät - Bildunterstützung | `mobileimagesupport` |
| Mobilgerätehersteller | `mobilemanufacturer` |
| Mobiles Betriebssystem (nicht mehr unterstützt) | `mobileos` |
| Mobilgerät - Bildschirmhöhe | `mobilescreenheight` |
| Mobilgerät - Bildschirmgröße | `mobilescreensize` |
| Mobilgerät - Bildschirmbreite | `mobilescreenwidth` |
| Max. Länge der mobilen Browser-URL | `mobileurllength` |
| Mobilgerät - Video-Unterstützung | `mobilevideosupport` |
| Bildschirmauflösung | `monitorresolution` |
| Betriebssysteme | `operatingsystem` |
| Ursprünglich verweisende Domäne | `referringdomainoriginal` |
| Seite | `page` |
| Seiten nicht gefunden | `pagesnotfound` |
| Produkt | `product` |
| Referrer | `referrer` |
| Typ der verweisenden Stelle | `referrertype` |
| Referrer-Domäne | `referringdomain` |
| Regionen | `georegion` |
| Rückkehrhäufigkeit | `returnfrequency` |
| SC-TnT | `tntbase` |
| Suchmaschine | `searchengine` |
| Suchbegriffe | `searchenginekeyword` |
| Suchmaschine - Natürlich | `searchenginenatural` |
| Suchmaschine - bezahlt | `searchenginepaid` |
| Keyword – natürlich | `searchenginenaturalkeyword` |
| Keyword – bezahlt | `searchenginepaidkeyword` |
| Rangansicht aller Suchseiten | `searchenginepagerank` |
| Server | `server` |
| Einzelseitenbesuche | `singlepagevisits` |
| Website-Bereich | `sitesections` |
| Zeit pro Besuch – präzise | `sitetime` |
| Trackingcode | `campaign` |
| US-DMA | `geodma` |
| US-Staaten | `state` |
| Zeit vor Ereignis | `timeprior` |
| Zeit pro Besuch – Zusammengefasst | `timespent` |
| Besuchstiefe | `pathlength` |
| Besuchnummer | `visitnumber` |
| Postleitzahl | `zip` |

## Nur in Analysis Workspace unterstützte Dimensionen

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Vormittag/Nachmittag | `timepartampm` |
| Browserhöhe – zusammengefasst | `browserheightbucketed` |
| Browserbreite – zusammengefasst | `browserwidthbucketed` |
| Tag | `daterangeday` |
| Tag des Monats | `timepartdayofmonth` |
| Wochentag | `dayofweek` |
| Wochentag | `timepartdayofweek` |
| Tag des Jahres | `timepartdayofyear` |
| Tage seit dem letzten Besuch | `dayssincelastvisit` |
| Eingabe benutzerdefinierter Insights | `entryprops` |
| Eingabe-Listenvariablen | `entrylistvariables` |
| Entryserver | `entryserver` |
| Einstiegsbereich | `entrysitesections` |
| Benutzerdefinierte Insights beenden | `exitprops` |
| Listenvariablen verlassen | `exitlistvariables` |
| Exitpage | `exitpage` |
| Server verlassen | `exitserver` |
| Bereich der Website verlassen | `exitsitesections` |
| Treffertiefe | `hitdepth` |
| Treffertyp | `hittype` |
| Stunde | `daterangehour` |
| Stunde des Tages | `timeparthourofday` |
| Detail des Marketingkanals | `marketingchanneldetail` |
| Minute | `daterangeminute` |
| Mobil - max. Lesezeichen-Länge | `mobilebookmarklength` |
| Mobilgerätenummer | `mobiledevicenumber` |
| Mobil-DRM | `mobiledrm` |
| Mobile Informationsdienste | `mobileinformationservices` |
| Mobil Java VM | `mobilejavavm` |
| Mobilgerät – Mail-Design | `mobilemaildecoration` |
| Mobile Netzprotokolle | `mobilenetprotocols` |
| Mobilgerät – Push To Talk | `mobilepushtotalk` |
| Monat | `daterangemonth` |
| Monat des Jahres | `timepartmonthofyear` |
| Betriebssystemtypen | `operatingsystemgroup` |
| Paid Search | `paidsearch` |
| Dauerhafte Cookie-Unterstützung | `persistentcookie` |
| Quartal | `daterangequarter` |
| Viertel des Jahres | `timepartquarterofyear` |
| Umfrage | `surveybase` |
| Besuchszeit pro Seite – zusammengefasst | `averagepagetime` |
| Besuchszeit pro Seite – präzise | `pagetimeseconds` |
| Nachverfolgung der Gründe für den Ausstieg | `optoutreason` |
| Wochentag/Wochenende | `timepartweekdayweekend` |
| Woche | `daterangeweek` |
| Jahr | `daterangeyear` |

## Inhaltsorientierte Dimensionen, die nur in Analysis Workspace unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| Mediensession-ID | `videosessionid` |
| Nielsen-Zugriffsmethode | `nielsenaccmethod` |
| Nielsen-App-ID | `nielsenappid` |
| Nielsen-Channel-Asset | `nielsenchannelasset` |
| Nielsen-Content-Typ | `nielsencontenttype` |

## Dimensionen, die nur in Reports &amp; Analytics unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Browserhöhe | `browserheight` |
| Browserbreite | `browserwidth` |
| Unique Customers pro Tag | `dailyuniquecustomers` |
| JavaScript | `javascriptsupport` |
| JavaScript-Version | `javascriptversion` |
| Unique Customers pro Monat | `monthlyuniquecustomers` |
| Unique Customers pro Quartal | `quarterlyuniquecustomers` |
| Zeitzonen | `timezone` |
| Domänen auf oberster Ebene | `topleveldomain` |
| Bundesstaat des Besuchers | `legacystate` |
| Unique Customers pro Woche | `weeklyuniquecustomers` |
| Unique Customers pro Jahr | `yearlyuniquecustomers` |

## Inhaltsorientierte Dimensionen, die sowohl von Reports &amp; Analytics als auch vom Analysis Workspace unterstützt werden

### Video (Media Analytics)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Inhalt | `video` |
| Inhaltssegment | `videosegment` |
| Content-Typ | `videocontenttype` |
| Name des Anzeigenplayers | `videoadplayername` |
| Anzeigenposition innerhalb der Werbeunterbrechung | `videoadinpod` |
| Dropped Frames | `videoqoedroppedframecountevar` |
| Fehler | `videoqoeerrorcountevar` |
| Durchschnittliche Bitrate | `videoqoebitrateaverageevar` |
| Bitratenänderungen | `videoqoebitratechangecountevar` |
| Gesamtpufferdauer | `videoqoebuffertimeevar` |
| Pufferereignisse | `videoqoebuffercountevar` |
| Zeit bis Start | `videoqoetimetostartevar` |
| Anzeigen-Pod | `videoadpod` |
| Media-Pfad | `videopath` |
| Werbung | `videoad` |
| Inhalts-Player-Name | `videoplayername` |
| Inhaltskanal | `videochannel` |
| Kapitel | `videochapter` |
| Inhaltsname (Variable) | `videoname` |
| Inhaltsdauer (Variable) | `videolength` |
| Anzeigename (Variable) | `videoadname` |
| Anzeigenlänge (Variable) | `videoadlength` |
| Show | `videoshow` |
| Staffel | `videoseason` |
| Episode | `videoepisode` |
| Netzwerk | `videonetwork` |
| Sendungstyp | `videoshowtype` |
| Anzeige-Ladevorgänge | `videoadload` |
| MVPD | `videomvpd` |
| Tagesteil | `videodaypart` |
| Advertiser | `videoadadvertiser` |
| Kampagnen-ID | `videoadcampaign` |
| Genre | `videogenre` |
| Streamtyp | `videostreamtype` |
| Player SDK Fehler-IDs | `videoqoeplayersdkerrors` |
| Externe Fehler-IDs | `videoqoeextneralerrors` |
| Medien-Feed-Typ | `videofeedtype` |
| Medien-Einstiegspfad | `entryvideopath` |
| Medien-Ausstiegspfad | `exitvideopath` |
| Einstiegs-Genre | `entryvideogenre` |
| Ausstiegs-Genre | `exitvideogenre` |
| Einstieg Player SDK Fehler-IDs | `entryvideoqoeplayersdkerrors` |
| Ausstieg Player SDK Fehler-IDs | `exitvideoqoeplayersdkerrors` |
| Externe Einstiegs-Fehler-IDs | `entryvideoqoeextneralerrors` |
| Externe Ausstiegs-Fehler-IDs | `exitvideoqoeextneralerrors` |

### Adobe Social

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Begriffe | `socialterm` |
| Soziale Plattformen/Eigenschaften | `socialcontentprovider` |
| Autoren | `socialauthor` |
| Sprache | `sociallanguage` |
| Breitengrad/Längengrad | `sociallatlong` |
| Asset-Trackingcodes | `socialassettrackingcode` |
| Eigene Social-Eigenschaften | `socialaccountandappids` |
| Eigene Post-IDs | `socialownedpostids` |
| Eigene Social-Definitionen | `socialinteractiontype` |
| Eigene Eigenschaften-IDs | `socialownedpropertyid` |
| Eigenes Eigentum vs. Anwendung | `socialownedpropertypropertyvsapp` |
| Name der eigenen Eigenschaft | `socialownedpropertyname` |
| Eigene Definitionseigenschaft vs. Post | `socialowneddefinitionpropertyvspost` |
| Eigener Definition-Insight-Typ | `socialowneddefinitioninsighttype` |
| Eigener Definition-Insight-Wert | `socialowneddefinitioninsightvalue` |
| Eigene Definition-Metrik | `socialowneddefinitionmetric` |
| Asset | `socialmediaid` |

### Mobile SDK

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Erster Starttermin | `mobileinstalldate` |
| App-ID | `mobileappid` |
| Startanzahl | `mobilelaunchnumber` |
| Tage seit der ersten Verwendung | `mobiledayssincefirstuse` |
| Tage seit der letzten Verwendung | `mobiledayssincelastuse` |
| Stunde des Tages (SDK) | `mobilehourofday` |
| Wochentag (SDK) | `mobiledayofweek` |
| Betriebssystem (SDK) | `mobileosenvironment` |
| Tage seit letztem Upgrade | `mobiledayssincelastupgrade` |
| Starts seit letztem Upgrade | `mobilelaunchessincelastupgrade` |
| Gerätename (SDK) | `mobiledevice` |
| Betriebssystemversion (SDK) | `mobileosversion` |
| Beacon Major | `mobilebeaconmajor` |
| Beacon Minor | `mobilebeaconminor` |
| Beacon UUID | `mobilebeaconuuid` |
| Beacon-Nähe | `mobilebeaconproximity` |
| Standort (bis 10 km) | `latlon1` |
| Standort (bis 100 m) | `latlon23` |
| Standort (bis 1 m) | `latlon45` |
| Zielpunkt-Bezeichnung | `pointofinterest` |
| Entfernung zum Zentrum des Zielpunkts | `pointofinterestdistance` |
| Genauigkeit der Position | `mobileplaceaccuracy` |
| Kategorie Platz | `mobileplacecategory` |
| Platz-ID | `mobileplaceid` |
| Einstieg Beacon Major | `entrymobilebeaconmajor` |
| Ausstieg Beacon Major | `exitmobilebeaconmajor` |
| Einstieg Beacon Minor | `entrymobilebeaconminor` |
| Ausstieg Beacon Minor | `exitmobilebeaconminor` |
| Einstieg Beacon UUID | `entrymobilebeaconuuid` |
| Ausstieg Beacon UUID | `exitmobilebeaconuuid` |
| Einstieg Beacon-Nähe | `entrymobilebeaconproximity` |
| Ausstieg Beacon-Nähe | `exitmobilebeaconproximity` |

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

For more information on how to implement this integration, see the [Nielsen Extension](https://exchange.adobe.com/experiencecloud.details.101361.html).

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Nielsen-Anzeigenmodell | `nielsenadmodel` |
| Nielsen-Segment C | `nielsensegmentc` |
| Nielsen-Segment B | `nielsensegmentb` |
| Nielsen-Segment A | `nielsensegmenta` |
| Nielsen Inhalts-ID | `nielsencontentid` |
| Nielsen-Asset/-Programm | `nielsenasset` |
| Nielsen VCID | `nielsenvcid` |
| Nielsen Opt-out | `nielsenoptout` |
| Nielsen Kunden-ID + VCID | `nielsenclientidvcid` |
| Nielsen Kunden-ID | `nielsenclientid` |
| Einstieg Nielsen Opt-out | `entrynielsenoptout` |
| Ausstieg Nielsen Opt-out | `exitnielsenoptout` |
| Einstieg Nielsen Kunden-ID + VCID | `entrynielsenclientidvcid` |
| Ausstieg Nielsen Kunden-ID + VCID | `exitnielsenclientidvcid` |
| Einstieg Nielsen Kunden-ID | `entrynielsenclientid` |
| Ausstieg Nielsen Kunden-ID | `exitnielsenclientid` |

### Adobe Experience Manager (AEM)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Element-ID | `aemassetid` |
| Asset-Quelle | `aemassetsource` |
| Angeklickte Asset-ID | `aemclickedassetid` |
| Einstieg Asset-ID | `entryaemassetid` |
| Ausstieg Asset-ID | `exitaemassetid` |

### Adobe Campaign

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Adobe Campaign – ID der ausgeführten Bereitstellung | `ac_delivery_internal_name` |
