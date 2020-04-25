---
title: Kompatibilität von Analytics-Dimensionen
description: Referenz zu Analytics-Dimensionen und -Berichten.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Kompatibilität von Analytics-Dimensionen

Dieser Referenzartikel listet die unterstützten Dimensionen/Berichte sowohl in Reports &amp; Analytics als auch in Analysis Workspace, nur in Analysis Workspace und nur in Reports &amp; Analytics auf.

Bitte beachten Sie:

* Diese Listen sind nicht vollständig. Für jede Report Suite kann ein bestimmter Satz von Produktvariablen aktiviert sein oder auch nicht. Zudem kann für jede beliebige Report Suite eine beliebige Anzahl von benutzerdefinierten Variablen aktiviert oder deaktiviert oder den Produktvariablen zugeordnet werden. Wir haben auf Besucherattribute und Classifications verzichtet, da sie für jede Report Suite eindeutig sind.

* Es gibt einige Fälle von Überlagerungen, in denen Analytics-Werkzeuge unterschiedliche Begriffe für im Wesentlichen dasselbe verwenden, zum Beispiel: `browserwidth` und `browserwidthbucketed`.

## Unterstützte Dimensionen sowohl in Reports &amp; Analytics als auch im Analysis Workspace

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|---|---|
| Analytics für Target | targetraw |
| Audiences ID | mcaudiences |
| Browser | browser |
| Browsertyp | browsertype |
| Kategorie | category |
| Städte | geocity |
| Farbtiefe | colorDepth |
| Verbindungstyp | connectiontype |
| Cookie-Unterstützung | Cookie |
| Länder | geocountry |
| Kundentreue | customerloyalty |
| Benutzerspezifische Konversionsvariable | evar1, evar2 usw. |
| Benutzerspezifische Insight-Variablen | prop1, prop2 usw. |
| Anwenderspezifischer Link | customlink |
| Tage bis Erstkauf | daysbeforefirstpurchase |
| Tage seit letztem Kauf | dayssincelastpurchase |
| Domäne | filtereddomain |
| Downloadlink | downloadlink |
| Entrypage | entrypage |
| Entrypage ursprünglich | entrypageoriginal |
| Exitlink | Exitlink |
| Erstkontakt Kanal | firsttouchchannel |
| Erstkontakt Kanaldetail | firsttouchchanneldetail |
| Java aktiviert | javaEnabled |
| Sprache | language |
| Letztkontakt Kanal | lasttouchchannel |
| Letztkontakt Kanaldetail | lasttouchchanneldetail |
| Listenvariablen | listvariables |
| Marketingkanal | marketingchannel |
| Mobilgerät - Audio-Unterstützung | mobileaudiosupport |
| Mobilnetzbetreiber | mobilecarrier |
| Mobilgerät - Farbtiefe | mobilecolordepth |
| Mobilgerät - Cookie-Unterstützung | mobilecookiesupport |
| Mobilgerät | mobiledevicename |
| Mobilgerätetyp | mobiledevicetype |
| Mobil - max. E-Mail-Länge | mobileemaillength |
| Mobilgerät - Bildunterstützung | mobileimagesupport |
| Mobilgerätehersteller | mobilemanufacturer |
| Mobiles Betriebssystem (nicht mehr unterstützt) | mobileos |
| Mobilgerät - Bildschirmhöhe | mobilescreenheight |
| Mobilgerät - Bildschirmgröße | mobilescreensize |
| Mobilgerät - Bildschirmbreite | mobilescreenwidth |
| Max. Länge der mobilen Browser-URL | mobileurllength |
| Mobilgerät - Video-Unterstützung | mobilevideosupport |
| Bildschirmauflösung | monitorresolution |
| Betriebssysteme | operatingsystem |
| Ursprünglich verweisende Domäne | referringdomainoriginal |
| Seite | Seite |
| Seiten nicht gefunden | pagesnotfound |
| Product | product |
| Verweisende Stelle | referrer |
| Typ der verweisenden Stelle | referrertype |
| Verweisende Domäne | referringdomain |
| Regionen | georegion |
| Rückkehrhäufigkeit | returnfrequency |
| SC-TnT | tntbase |
| Suchmaschine | searchengine |
| Keywords | searchenginekeyword |
| Suchmaschine - natürlich | searchenginenatural |
| Suchmaschine - bezahlt | searchenginepaid |
| Keyword – natürlich | searchenginenaturalkeyword |
| Keyword – bezahlt | searchenginepaidkeyword |
| Rangansicht aller Suchseiten | searchenginepagerank |
| Server | server |
| Einzelseitenbesuche | singlepagevisits |
| Website-Bereich | sitesections |
| Zeit pro Besuch – präzise | sitetime |
| Trackingcode | Kampagne |
| US-DMA | geodma |
| US-Staaten | state |
| Zeit vor Ereignis | timeprior |
| Zeit pro Besuch – zusammengefasst | timespent |
| Besuchstiefe | pathlength |
| Besuchnummer | visitnumber |
| Postleitzahl | zip |

## Nur in Analysis Workspace unterstützte Dimensionen

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Vormittag/Nachmittag | timepartampm |
| Browserhöhe – zusammengefasst | browserheightbucketed |
| Browserbreite – zusammengefasst | browserwidthbucketed |
| Tag | daterangeday |
| Tag des Monats | timepartdayofmonth |
| Wochentag | dayofweek |
| Wochentag | timepartdayofweek |
| Tag des Jahres | timepartdayofyear |
| Tage seit dem letzten Besuch | daysSinceLastVisit |
| Eingabe benutzerdefinierter Insights | entryprops |
| Eingabe-Listenvariablen | entrylistvariables |
| Entryserver | entryserver |
| Einstiegsbereich | entrysitesections |
| Benutzerdefinierte Insights beenden | exitprops |
| Listenvariablen verlassen | exitlistvariables |
| Exitpage | exitpage |
| Server verlassen | exitserver |
| Bereich der Website verlassen | exitsitesections |
| Treffertiefe | hitdepth |
| Treffertyp | hittype |
| Stunde | daterangehour |
| Stunde des Tages | timeparthourofday |
| Detail des Marketingkanals | marketingchanneldetail |
| Minute | daterangeminute |
| Mobil - max. Lesezeichen-Länge | mobilebookmarklength |
| Mobilgerätenummer | mobiledevicenumber |
| Mobil-DRM | mobiledrm |
| Mobile Informationsdienste | mobileinformationservices |
| Mobil Java VM | mobilejavavm |
| Mobilgerät – Mail-Design | mobilemaildecoration |
| Mobile Netzprotokolle | mobilenetprotocols |
| Mobilgerät – Push To Talk | mobilepushtotalk |
| Monat | daterangemonth |
| Monat des Jahres | timepartmonthofyear |
| Betriebssystemtypen | operatingsystemgroup |
| Paid Search | paidsearch |
| Dauerhafte Cookie-Unterstützung | persistentcookie |
| Quartal | daterangequarter |
| Viertel des Jahres | timepartquarterofyear |
| Umfrage | surveybase |
| Besuchszeit pro Seite – zusammengefasst | averagepagetime |
| Besuchszeit pro Seite – präzise | pagetimeseconds |
| Nachverfolgung der Gründe für den Ausstieg | optoutreason |
| Wochentag/Wochenende | timepartweekdayweekend |
| Woche | daterangeweek |
| Jahr | daterangeyear |

## Inhaltsorientierte Dimensionen, die nur in Analysis Workspace unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Activity Map XY | clickmapxy |
| Mediensession-ID | videosessionid |
| Nielsen-Zugriffsmethode | nielsenaccmethod |
| Nielsen-App-ID | nielsenappid |
| Nielsen-Channel-Asset | nielsenchannelasset |
| Nielsen-Content-Typ | nielsencontenttype |

## Dimensionen, die nur in Reports &amp; Analytics unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Browserhöhe | browserheight |
| Browserbreite | browserwidth |
| Unique Customers pro Tag | dailyuniquecustomers |
| JavaScript | javascriptsupport |
| JavaScript-Version | javascriptversion |
| Unique Customers pro Monat | monthlyuniquecustomers |
| Unique Customers pro Quartal | quarterlyuniquecustomers |
| Zeitzonen | timezone |
| Domänen auf oberster Ebene | topleveldomain |
| Bundesstaat des Besuchers | legacystate |
| Unique Customers pro Woche | weeklyuniquecustomers |
| Unique Customers pro Jahr | yearlyuniquecustomers |

## Vorkonfigurierte Berichte in Reports &amp; Analytics

Reports &amp; Analytics enthält mehrere vorkonfigurierte Berichte, die entweder nicht auf eine bestimmte Dimension verweisen oder der Bericht verwendet eine Klasse von Dimensionen. Diese Berichte sind hier aufgeführt:

* Länge der Lesezeichen-URL
* Browser
* Browsertypen
* Kampagnenkonversionstrichter
* Warenkorbkonversionstrichter
* Städte
* Klicks pro Seite
* Länder
* Cross-Sell
* Benutzerspez. Ereignistrichter
* Design-Mail-Unterstützung
* Gerätenr.-Übertragung (EIN/AUS)
* Domänen
* DRM
* Entrypages
* Exitpage
* Fallout
* Vollständige Pfade
* ICities
* Informationsdienste
* Java-Version
* Sprachen
* Längste Pfade
* Gleichzeitige Medienbetrachter
* Medien-Tagesbericht
* Medien-Detail
* Medien-Übersicht
* Bildschirmauflösungen
* Netzprotokolle
* Netscape Plug-ins
* Nächste Seite
* Nächster Seitenfluss
* Betriebssysteme
* Betriebssystemtypen
* Klicktiefe
* Seitenzusammenfassung
* PathFinder
* Vorheriger Seitenfluss
* Vorherige Seite
* PTT
* Produktkonversionstrichter
* Einkaufskonversionstrichter
* Referrerdomänen
* Regionen
* Neuladungen
* Suchmaschinen – Alle
* Suchmaschinen – Kostenlos
* Suchmaschinen – Gebührenpflichtig
* Suchkeywords – Alle
* Suchkeywords – Kostenlos
* Suchkeywords – Gebührenpflichtig
* Details zur Ziel-Aktivität
* Besuchszeit pro Seite
* Zeitzonen
* Domänen auf oberster Ebene
* U.S. DMA (Designierter Marktbereich)
* US-Bundesstaaten
* Besuchnummer
* Homepage des Besuchers

## Inhaltsorientierte Dimensionen, die sowohl von Reports &amp; Analytics als auch vom Analysis Workspace unterstützt werden

### Video (Media Analytics)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Inhalt | video |
| Inhaltssegment | videosegment |
| Content-Typ | videocontenttype |
| Name des Anzeigenplayers | videoadplayername |
| Anzeigenposition innerhalb der Werbeunterbrechung | videoadinpod |
| Dropped Frames | videoqoedroppedframecountevar |
| Fehler | videoqoeerrorcountevar |
| Durchschnittliche Bitrate | videoqoebitrateaverageevar |
| Bitratenänderungen | videoqoebitratechangecountevar |
| Gesamtpufferdauer | videoqoebuffertimeevar |
| Pufferereignisse | videoqoebuffercountevar |
| Zeit bis Start | videoqoetimetostartevar |
| Anzeigen-Pod | videoadpod |
| Media-Pfad | videopath |
| Werbung | videoad |
| Inhalts-Player-Name | videoplayername |
| Inhaltskanal | videochannel |
| Kapitel | videochapter |
| Inhaltsname (Variable) | videoname |
| Inhaltsdauer (Variable) | videolength |
| Anzeigename (Variable) | videoadname |
| Anzeigenlänge (Variable) | videoadlength |
| Show | videoshow |
| Staffel | videoseason |
| Episode | videoepisode |
| Netzwerk | videonetwork |
| Sendungstyp | videoshowtype |
| Anzeige-Ladevorgänge | videoadload |
| MVPD | videomvpd |
| Tagesteil | videodaypart |
| Advertiser | videoadadvertiser |
| Kampagnen-ID | videoadcampaign |
| Genre | videogenre |
| Streamtyp | videostreamtype |
| Player SDK Fehler-IDs | videoqoeplayersdkerrors |
| Externe Fehler-IDs | videoqoeexternalerrors |
| Medien-Feed-Typ | videofeedtype |
| Medien-Einstiegspfad | entryvideopath |
| Medien-Ausstiegspfad | exitvideopath |
| Einstiegs-Genre | entryvideogenre |
| Ausstiegs-Genre | exitvideogenre |
| Einstieg Player SDK Fehler-IDs | entryvideoqoeplayersdkerrors |
| Ausstieg Player SDK Fehler-IDs | exitvideoqoeplayersdkerrors |
| Externe Einstiegs-Fehler-IDs | entryvideoqoeexternalerrors |
| Externe Ausstiegs-Fehler-IDs | exitvideoqoeexternalerrors |

### Adobe Social

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Begriffe | socialterm |
| Soziale Plattformen/Eigenschaften | socialcontentprovider |
| Autoren | socialauthor |
| Sprache | sociallanguage |
| Breitengrad/Längengrad | sociallatlong |
| Asset-Trackingcodes | socialassettrackingcode |
| Eigene Social-Eigenschaften | socialaccountandappids |
| Eigene Post-IDs | socialownedpostids |
| Eigene Social-Definitionen | socialinteractiontype |
| Eigene Eigenschaften-IDs | socialownedpropertyid |
| Eigenes Eigentum vs. Anwendung | socialownedpropertypropertyvsapp |
| Name der eigenen Eigenschaft | socialownedpropertyname |
| Eigene Definitionseigenschaft vs. Post | socialowneddefinitionpropertyvspost |
| Eigener Definition-Insight-Typ | socialowneddefinitioninsighttype |
| Eigener Definition-Insight-Wert | socialowneddefinitioninsightvalue |
| Eigene Definition-Metrik | socialowneddefinitionmetric |
| Asset | socialmediaid |

### Mobile SDK

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Erster Starttermin | mobileinstalldate |
| App-ID | mobileappid |
| Startanzahl | mobilelaunchnumber |
| Tage seit der ersten Verwendung | mobiledayssincefirstuse |
| Tage seit der letzten Verwendung | mobiledayssincelastuse |
| Stunde des Tages (SDK) | mobilehourofday |
| Wochentag (SDK) | mobiledayofweek |
| Betriebssystem (SDK) | mobileosenvironment |
| Tage seit letztem Upgrade | mobiledayssincelastupgrade |
| Starts seit letztem Upgrade | mobilelaunchessincelastupgrade |
| Gerätename (SDK) | mobiledevice |
| Betriebssystemversion (SDK) | mobileosversion |
| Beacon Major | mobilebeaconmajor |
| Beacon Minor | mobilebeaconminor |
| Beacon UUID | mobilebeaconuuid |
| Beacon-Nähe | mobilebeaconproximity |
| Standort (bis 10 km) | latlon1 |
| Standort (bis 100 m) | latlon23 |
| Standort (bis 1 m) | latlon45 |
| Zielpunkt-Bezeichnung | pointofinterest |
| Entfernung zum Zentrum des Zielpunkts | pointofinterestdistance |
| Genauigkeit der Position | mobileplaceaccuracy |
| Kategorie Platz | mobileplacecategory |
| Platz-ID | mobileplaceid |
| Einstieg Beacon Major | entrymobilebeaconmajor |
| Ausstieg Beacon Major | exitmobilebeaconmajor |
| Einstieg Beacon Minor | entrymobilebeaconminor |
| Ausstieg Beacon Minor | exitmobilebeaconminor |
| Einstieg Beacon UUID | entrymobilebeaconuuid |
| Ausstieg Beacon UUID | exitmobilebeaconuuid |
| Einstieg Beacon-Nähe | entrymobilebeaconproximity |
| Ausstieg Beacon-Nähe | exitmobilebeaconproximity |

### Adobe Advertising Cloud (AMO)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| AMO EF ID | amo_ef_id |
| AMO-ID | amo_cid |

### Activity Map

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Activity Map-Link nach Region | clickmaplinkbyregion |
| Activity Map-Region | clickmapregion |
| Activity Map-Link | clickmaplink |
| Activity Map-Seite | clickmappage |

### Nielsen-Integration

Weitere Informationen zur Umsetzung dieser Integration finden Sie unter [Nielsen-Partnerschaft](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html).

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Nielsen-Anzeigenmodell | nielsenadmodel |
| Nielsen-Segment C | nielsensegmentc |
| Nielsen-Segment B | nielsensegmentb |
| Nielsen-Segment A | nielsensegmenta |
| Nielsen Inhalts-ID | nielsencontentid |
| Nielsen-Asset/-Programm | nielsenasset |
| Nielsen VCID | nielsenvcid |
| Nielsen Opt-out | nielsenoptout |
| Nielsen Kunden-ID + VCID | nielsenclientidvcid |
| Nielsen Kunden-ID | nielsenclientid |
| Einstieg Nielsen Opt-out | entrynielsenoptout |
| Ausstieg Nielsen Opt-out | exitnielsenoptout |
| Einstieg Nielsen Kunden-ID + VCID | entrynielsenclientidvcid |
| Ausstieg Nielsen Kunden-ID + VCID | exitnielsenclientidvcid |
| Einstieg Nielsen Kunden-ID | entrynielsenclientid |
| Ausstieg Nielsen Kunden-ID | exitnielsenclientid |

### Adobe Experience Manager (AEM)

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Element-ID | aemassetid |
| Asset-Quelle | aemassetsource |
| Angeklickte Asset-ID | aemclickedassetid |
| Einstieg Asset-ID | entryaemassetid |
| Ausstieg Asset-ID | exitaemassetid |

### Adobe Campaign

| Dimensionsname (in Analytics-UI sichtbar) | Dimensionen-ID (verwendet in API-Requests) |
|--- |--- |
| Adobe Campaign – ID der ausgeführten Bereitstellung | ac_delivery_internal_name |
