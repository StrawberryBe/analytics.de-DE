---
description: In der folgenden Tabelle sind die Zuordnungen von Berichten und Variablen aufgeführt oder angegeben, in welchen Berichten und Variablen diese verwendet werden.
keywords: Analytics-Implementierung
seo-description: In der folgenden Tabelle sind die Zuordnungen von Berichten und Variablen aufgeführt oder angegeben, in welchen Berichten und Variablen diese verwendet werden.
seo-title: Zuordnung von Berichten zu Variablen
solution: Analytics
title: Zuordnung von Berichten zu Variablen
topic: Entwickler und Implementierung
uuid: 4707660c-4be5-425c-a690-7bc6df4cc0fa
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Zuordnung von Berichten zu Variablen

In der folgenden Tabelle sind die Zuordnungen von Berichten und Variablen aufgeführt oder angegeben, in welchen Berichten und Variablen diese verwendet werden.

**Konversionsberichte** In der folgenden Tabelle sind die Konversion-Variablen aufgeführt, mit denen die einzelnen Berichte aufgefüllt werden:

| Einkäufe |
|---|
| Konversionen und Durchschnittswerte | s.events, s.products, s.purchaseID | „s.events“ auf Einkauf, Produktdetail, Bestellnummer festlegen |
| Umsatz | s.events, s.products, s.purchaseID | „s.events“ auf Einkauf, Produktdetail, Bestellnummer festlegen |
| Bestellungen | s.events, s.products, s.purchaseID | „s.events“ auf Einkauf, Produktdetail, Bestellnummer festlegen |
| Einheiten | s.events, s.products, s.purchaseID | „s.events“ auf Einkauf, Produktdetail, Bestellnummer festlegen |

| Warenkorb |
|---|
| Konversionen und Durchschnittswerte | s.events, s.products, s.purchaseID |  |
| Korb | s.events | „s.events“ auf „scOpen“ festlegen |
| Warenkorbansicht | s.events | „s.events“ auf „scView“ festlegen |
| Zusatz zum Warenkorb | s.events | „s.events“ auf „scAdd“ festlegen |
| Entnahme aus Warenkorb | s.events | „s.events“ auf „scRemove“ festlegen |
| Checkouts | s.events | „s.events“ auf „scCheckout“ festlegen |

| Benutzerspezifische Ereignisse |
|---|
| Benutzerspezifisches Ereignis 1 | s.events | Mit „event1“ bis „event100“ auffüllen |
| … | … | Mit „event1“ bis „event100“ auffüllen |
| Benutzerspezifisches Ereignis 100 | s.events | Mit „event1“ bis „event100“ auffüllen |

| Produkte |
|---|
| Konversionen und Durchschnittswerte | s.events, s.products, s.purchaseID |  |
| Produkte | s.products, s.events | Kann je nach den Metriken in der rechten Spalte unterschiedlich sein |
| Querverkauf | s.products, s.events, s.purchaseID | Kann je nach den Metriken in der rechten Spalte unterschiedlich sein |
| Kategorien | s.products | Kann je nach den Metriken in der rechten Spalte unterschiedlich sein |

| Kampagnen |
|---|
| Konversionen und Durchschnittswerte | s.products, s.events, s.campaign |  |
| Trackingcode | s.campaign |  |
| Bericht | Keine | Definiert in [!DNL Analytics] |
| Kampagnen | Keine | Definiert in [!DNL Analytics] |

| Kundentreue |
|---|
| Kundentreue | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |

| Verkaufszyklus |
|---|
| Tage bis Erstkauf | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Tage seit letztem Kauf | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Besuchnummer | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Unique Customers pro Tag | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Unique Customers pro Monat | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Unique Customers pro Jahr | s.products, s.events, s.purchaseID | Variablen werden auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |

| Suchmethoden |
|---|
| Referrerdomänen | Keine | Automatisch von der JS-Datei festgelegt |
| Ursprünglich Referrerdomänen | Keine | Automatisch von der JS-Datei festgelegt |
| Suchmaschinen | Keine | Automatisch von der JS-Datei festgelegt |
| Suchkeywords | Keine | Automatisch von der JS-Datei festgelegt |

| Besucherprofil |
|---|
| Domänen auf oberster Ebene | Keine | Automatisch von der JS-Datei festgelegt |
| Sprachen | Keine | Automatisch von der JS-Datei festgelegt |
| Zeitzonen | Keine | Automatisch von der JS-Datei festgelegt |
| Status | s.state | Variable wird auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| PLZ/Postleitzahlen | s.zip | Variable wird auf der Bestätigungsseite für die Bestellung („Vielen Dank!“) festgelegt |
| Domänen | Keine | Automatisch von der JS-Datei festgelegt |

| Technologie |
|---|
| Browser | Keine | Automatisch von der JS-Datei festgelegt |
| Betriebssysteme | Keine | Automatisch von der JS-Datei festgelegt |
| Bildschirmauflösungen | Keine | Automatisch von der JS-Datei festgelegt |

| Site-Pfad |
|---|
| Seitenwert | s.pageName, s.products, s.events, s.purchaseID |  |
| Entrypages | s.pageName |  |
| Ursprüngliche Entrypages | s.pageName |  |
| Seiten pro Besuch | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Besuchszeit pro Site | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Sitebereiche | [!UICONTROL s.channel] | Entspricht dem [!UICONTROL Kanal]bericht im Bereich [!UICONTROL Traffic]-Berichte |

| Benutzerdefinierte Variablen |
|---|
| Benutzerdefinierte „Variable eVar 1“ | [!UICONTROL s.eVar] 1 |  |
| Benutzerdefinierte „Variable eVar 2“ | [!UICONTROL s.eVar] 2 |  |
| Benutzerdefinierte „Variable eVar 3“ | [!UICONTROL s.eVar] 3 |  |
| … |  |  |
| Benutzerdefinierte „Variable eVar 75“ | [!UICONTROL s.eVar] 75 |  |

## Traffic-Berichte {#section_76A74C3D7B60461D9ADE0E5E183DD777}

In der folgenden Tabelle sind die [!UICONTROL Traffic]-Variablen aufgeführt, mit denen die einzelnen Berichte aufgefüllt werden:

| Berechnete Metriken |
|---|
| Keine | Keine | Keine |

| Site-Traffic |
|---|
| Seitenansichten | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Unique Visitors pro Stunde | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Unique Visitors pro Tag | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Unique Visitors pro Monat | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Unique Visitors pro Jahr | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Besuche | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Dateiladungen | Keine | Wird (je nach Einstellungen der JS-Variablen) automatisch von der JS-Datei verfolgt |

| Suchmethoden |
|---|
| Referrerdomänen | Keine | Automatisch von der JS-Datei festgelegt |
| Verweisende Stellen | Keine | Automatisch von der JS-Datei festgelegt |
| Suchmaschinen | Keine | Automatisch von der JS-Datei festgelegt |
| Suchkeywords | Keine | Automatisch von der JS-Datei festgelegt |
| Rückkehrhäufigkeit | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Rückkehrende Besucher pro Tag | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Rückkehrende Besucher | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Besuch-Nr. | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |

| Besucherprofil |
|---|
| Domänen | Keine | Automatisch von der JS-Datei festgelegt |
| Domänen auf oberster Ebene | Keine | Automatisch von der JS-Datei festgelegt |
| Sprachen | Keine | Automatisch von der JS-Datei festgelegt |
| Zeitzonen | Keine | Automatisch von der JS-Datei festgelegt |
| Besucherdetails | Keine | Automatisch von der JS-Datei festgelegt |
| Letzte 100 Besucher | Keine | Wird von Geschäftsregeln in [!DNL Analytics] ausgerechnet |
| Homepage des Benutzers | Keine | Automatisch von der JS-Datei festgelegt |
| Wichtige Besucher | Keine | Basiert auf der IP-Adresse des Besuchers |
| Von wichtigen Besuchern angezeigte Seiten | Keine | Basiert auf der IP-Adresse des Besuchers |

| Geo-Segmentierung |
|---|
| Länder | Keine | Basiert auf der IP-Adresse des Besuchers |
| U.S. Bundesstaaten | Keine | Basiert auf der IP-Adresse des Besuchers |
| DMA | Keine | Basiert auf der IP-Adresse des Besuchers |
| Internationale Städte | Keine | Basiert auf der IP-Adresse des Besuchers |
| Städte in den USA | Keine | Basiert auf der IP-Adresse des Besuchers |

| Technologie |
|---|
| Browsertypen | Keine | Automatisch von der JS-Datei festgelegt |
| Browser | Keine | Automatisch von der JS-Datei festgelegt |
| Mobilgeräte | Keine | Automatisch von der JS-Datei festgelegt |
| Browserbreite | Keine | Automatisch von der JS-Datei festgelegt |
| Browserhöhe | Keine | Automatisch von der JS-Datei festgelegt |
| Betriebssysteme | Keine | Automatisch von der JS-Datei festgelegt |
| Bildschirmfarbtiefe | Keine | Automatisch von der JS-Datei festgelegt |
| Bildschirmauflösungen | Keine | Automatisch von der JS-Datei festgelegt |
| Netscape-Plug-ins | Keine | Automatisch von der JS-Datei festgelegt |
| Java | Keine | Automatisch von der JS-Datei festgelegt |
| JavaScript | Keine | Automatisch von der JS-Datei festgelegt |
| JavaScript-Version | Keine | Automatisch von der JS-Datei festgelegt |
| Cookies | Keine | Automatisch von der JS-Datei festgelegt |
| Verbindungstypen | Keine | Automatisch von der JS-Datei festgelegt |
| Segmentierung |

| Segmentierung |
|---|
| Bevorzugte Seiten | s.pageName |  |
| Bevorzugte Site-Abschnitte | s.channel |  |
| Bevorzugte Server | s.server |  |

| Custom Insight |
|---|
| Benutzerspezifische Links | s.linkName | Muss benutzerdefiniert implementiert werden |
| Custom Insight 1 | s.prop1 |  |
| … | … |  |
| Custom Insight 75 | s.prop75 |  |

| Hierarchien |
|---|
| Hierarchie 1 | s.hier1 |  |
| … | … |  |
| Hierarchie 5 | s.hier5 |  |

## Pfadsetzungsberichte {#section_85E0A2396B894659A6BE572819263E95}

In der folgenden Tabelle sind die Pathing-Variablen aufgeführt, mit denen die einzelnen Berichte in [!DNL Analytics] aufgefüllt werden:

| Seiten |
|---|
| Seitenzusammenfassung | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Seitenwert | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Bevorzugte Seiten | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Neuladungen | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Klicks pro Seite | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Besuchszeit pro Seite | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Seiten nicht gefunden | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |

| Ein- und Ausstiege |
|---|
| Entrypages | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Exitpages | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Exitlinks | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |

| Vollständige Pfade |
|---|
| Vollständige Pfade | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Längste Pfade | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Path Length | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Zeit pro Besuch | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Einzelseitenbesuche | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |

| Erweiterte Analyse |
|---|
| Vorherige Seite | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Nächste Seite | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Vorheriger Seitenfluss | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Nächster Seitenfluss | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| PathFinder | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
| Trichteranalyse | s.pageName (oder andere pfadfähige Variable) | Hängt auch von internen Geschäftsregeln ab |
