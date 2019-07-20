---
description: In der folgenden Tabelle ist aufgeführt, welchen Berichten die Variablen zugeordnet sind, mit denen Analytics-Berichte aufgefüllt werden.
keywords: Analytics-Implementierung
seo-description: In der folgenden Tabelle ist aufgeführt, welchen Berichten die Variablen zugeordnet sind, mit denen Analytics-Berichte aufgefüllt werden.
seo-title: Variable zur Berichtzuordnung
solution: Analytics
title: Variable zur Berichtzuordnung
topic: Entwickler und Implementierung
uuid: fd 81 f 97 d-dd 1 a -47 d 5-9157-b 7932 fe 13490
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Variable zur Berichtzuordnung

In der folgenden Tabelle ist aufgeführt, welchen Berichten die Variablen zugeordnet sind, mit denen Analytics-Berichte aufgefüllt werden.

Zu jeder Variablen sind die Berichte mit den verwendeten Variablen aufgeführt.

<table id="table_16443E46AC0E46509F8533D26EDE1BCC"> 
 <thead> 
  <tr> 
   <th class="entry"> Überschreiben von </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> s.pageName </td> 
   <td> <p>Konversionsberichte &gt; Pfadberichte &gt; Seitenwert </p> <p>Konversionsberichte &gt; Pfadberichte &gt; Entrypage </p> <p>Konversionsberichte &gt; Pfadberichte &gt; Ursprüngliche Entrypages </p> <p>Traffic-Berichte &gt; Datenverkehr auf der Site &gt; Seitenansichten </p> <p>Traffic-Berichte &gt; Datenverkehr auf der Site &gt; Unique Visitors pro Stunde </p> <p>Traffic-Berichte &gt; Datenverkehr auf der Site &gt; Unique Visitors pro Tag </p> <p>Traffic-Berichte &gt; Datenverkehr auf der Site &gt; Unique Visitors pro Monat </p> <p>Traffic-Berichte &gt; Datenverkehr auf der Site &gt; Unique Visitors pro Jahr </p> <p>Traffic-Berichte &gt; Besucherprofil &gt; Von wichtigen Besuchern angezeigte Seiten </p> <p>Traffic-Berichte &gt; Segmentierung &gt; Bevorzugte Seiten </p> <p>Pfadberichte &gt; Seiten &gt; Seitenzusammenfassung </p> <p>Pfadberichte &gt; Seiten &gt; Seitenwert </p> <p>Pfadberichte &gt; Seiten &gt; Bevorzugte Seiten </p> <p>Pfadberichte &gt; Seiten &gt; Neuladungen </p> <p>Pfadberichte &gt; Seiten &gt; Klick auf Seite </p> <p>Pfadberichte &gt; Seiten &gt; Besuchszeit pro Seite </p> <p>Pfadberichte &gt; Einstiege und Ausstiege &gt; Entrypages </p> <p>Pfadberichte &gt; Einstiege und Ausstiege &gt; Exitpages </p> <p>Pfadberichte &gt; Einstiege und Ausstiege &gt; Exitlinks </p> <p>Pfadberichte &gt; Vollständige Pfade &gt; Vollständige Pfade </p> <p>Pfadberichte &gt; Vollständige Pfade &gt; Längste Pfade </p> <p>Pfadberichte &gt; Vollständige Pfade &gt; Pfadlänge </p> <p>Pfadberichte &gt; Vollständige Pfade &gt; Zeit pro Besuch </p> <p>Pfadberichte &gt; Vollständige Pfade &gt; Einzelseitenbesuche </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; Vorherige Seite </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; Nächste Seite </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; Vorheriger Seitenfluss </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; Nächster Seitenfluss </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; PathFinder </p> <p>Pfadberichte &gt; Erweiterte Analyse &gt; Trichteranalyse </p> <p> <b>HINWEIS:</b> In sämtlichen oben aufgeführten <span class="wintitle">Traffic</span>berichten (mit Ausnahme von <span class="wintitle">Bevorzugte Seiten</span>), wird, wenn die Variable <span class="wintitle">s.pageName</span> nicht festgelegt ist, die URL verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> s.server </td> 
   <td> Traffic-Berichte &gt; Segmentierung &gt; Bevorzugte Server </td> 
  </tr> 
  <tr> 
   <td> s.pageType </td> 
   <td> Pfadberichte &gt; Seiten &gt; Seiten nicht gefunden </td> 
  </tr> 
  <tr> 
   <td> s.channel </td> 
   <td> <p>Konversionsberichte &gt; Site-Pfadberichte &gt; Sitebereich </p> <p>Traffic-Berichte &gt; Segmentierung &gt; Bevorzugte Sitebereiche </p> </td> 
  </tr> 
  <tr> 
   <td> s.prop1 - s.prop20 </td> 
   <td> Traffic-Berichte &gt; Custom Insight &gt; Custom Insight 1–20 </td> 
  </tr> 
  <tr> 
   <td> s.campaign </td> 
   <td> <p>Konversionsberichte &gt; Kampagnen &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Kampagnen &gt; Trackingcode </p> </td> 
  </tr> 
  <tr> 
   <td> s.state </td> 
   <td> Konversionsberichte &gt; Besucherprofil &gt; Status </td> 
  </tr> 
  <tr> 
   <td> s.zip </td> 
   <td> Konversionsberichte &gt; Besucherprofil &gt; PLZ/Postleitzahlen </td> 
  </tr> 
  <tr> 
   <td> s.events </td> 
   <td> <p>Konversionsberichte &gt; Einkäufe &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Einkäufe &gt; Umsatz </p> <p>Konversionsberichte &gt; Einkäufe &gt; Bestellungen </p> <p>Konversionsberichte &gt; Einkäufe &gt; Einheiten </p> <p>Konversionsberichte &gt; Warenkorb &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Warenkorb &gt; Warenkorb </p> <p>Konversionsberichte &gt; Warenkorb &gt; Warenkorbansichten </p> <p>Konversionsberichte &gt; Warenkorb &gt; Zusatz zum Warenkorb </p> <p>Konversionsberichte &gt; Warenkorb &gt; Entnahme aus Warenkorb </p> <p>Konversionsberichte &gt; Warenkorb &gt; Checkouts </p> <p>Konversionsberichte &gt; Benutzerspezifische Ereignisse &gt; Benutzerspezifisches Ereignis 1-20 </p> <p>Konversionsberichte &gt; Produkte &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Produkte &gt; Cross-Sell </p> <p>Konversionsberichte &gt; Produkte &gt; Kategorien </p> <p>Konversionsberichte &gt; Kampagnen &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Kundentreue &gt; Kundentreue </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage bis Erstkauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage seit letztem Kauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Besuchsnummer </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Tag </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Monat </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Jahr </p> <p>Konversionsberichte &gt; Site-Pfad &gt; Seitenwert </p> </td> 
  </tr> 
  <tr> 
   <td> s.products </td> 
   <td> <p>Konversionsberichte &gt; Einkäufe &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Einkäufe &gt; Umsatz </p> <p>Konversionsberichte &gt; Einkäufe &gt; Bestellungen </p> <p>Konversionsberichte &gt; Einkäufe &gt; Einheiten </p> <p>Konversionsberichte &gt; Warenkorb &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Produkte &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Produkte &gt; Cross-Sell </p> <p>Konversionsberichte &gt; Produkte &gt; Kategorien </p> <p>Konversionsberichte &gt; Kampagnen &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Kundentreue &gt; Kundentreue </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage bis Erstkauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage seit letztem Kauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Besuchsnummer </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Tag </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Monat </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Jahr </p> <p>Konversionsberichte &gt; Site-Pfad &gt; Seitenwert </p> </td> 
  </tr> 
  <tr> 
   <td> s.purchaseID </td> 
   <td> <p>Konversionsberichte &gt; Einkäufe &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Einkäufe &gt; Umsatz </p> <p>Konversionsberichte &gt; Einkäufe &gt; Bestellungen </p> <p>Konversionsberichte &gt; Einkäufe &gt; Einheiten </p> <p>Konversionsberichte &gt; Warenkorb &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Produkte &gt; Konversionen und Durchschnittswerte </p> <p>Konversionsberichte &gt; Produkte &gt; Cross-Sell </p> <p>Konversionsberichte &gt; Kundentreue &gt; Kundentreue </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage bis Erstkauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Tage seit letztem Kauf </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Besuchsnummer </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Tag </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Monat </p> <p>Konversionsberichte &gt; Verkaufszyklus &gt; Unique Customers pro Jahr </p> <p>Konversionsberichte &gt; Site-Pfad &gt; Seitenwert </p> </td> 
  </tr> 
  <tr> 
   <td> s.eVar1 - s.eVar20 </td> 
   <td> Konversionsberichte &gt; Benutzerdefinierte Variablen &gt; Benutzerspezifische eVar 1-20 </td> 
  </tr> 
  <tr> 
   <td> s.linkName </td> 
   <td> Traffic-Berichte &gt; Custom Insight &gt; Benutzerspezifische Links </td> 
  </tr> 
  <tr> 
   <td> s.hier1 - s.hier5 </td> 
   <td> Traffic-Berichte &gt; Hierarchien &gt; Hierarchie 1-5 </td> 
  </tr> 
 </tbody> 
</table>

