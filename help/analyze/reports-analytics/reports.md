---
title: Berichte
description: Die Dimensionen und Metriken, die Reports & Analytics für die einzelnen Berichte verwendet.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 100%

---


# Berichte

Jeder Bericht in Reports &amp; Analytics verwendet eine bestimmte Dimension und Standardmetrik. Sie können die Metrik in jedem Bericht ändern und bei Bedarf Aufschlüsselungen hinzufügen. In den folgenden Listen finden Sie, welche Dimension in den einzelnen Berichten verwendet wird.

>[!NOTE]
>
>Ihr Berichtsmenü kann je nach den Anpassungen, die ein Administrator in Ihrer Organisation vorgenommen hat, unterschiedlich aussehen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Menüanpassung](/help/admin/admin/customize-menus.md).

## Site-Metriken

Enthält Berichte, die in der Regel einen Trend hinsichtlich eines Datumsbereichs aufweisen. Enthält außerdem eindeutige Berichte, z. B. empfohlene Berichte und Echtzeitberichte.

* Meine empfohlenen Berichte: Erstellt ein Dashboard, das mehrere Reportlets für sofortige Erkenntnisse enthält.
* Schlüsselmetriken: Ein Bericht, mit dem Sie bis zu fünf Metriken gleichzeitig als Trend verfolgen können. Zeigt standardmäßig die Trends für [Seitenansichten](/help/components/metrics/page-views.md), [Besuche](/help/components/metrics/visits.md) und [Unique Visitors](/help/components/metrics/unique-visitors.md) an.
* Seitenansichten: Zeigt die Trends für die Metrik [Seitenansichten](/help/components/metrics/page-views.md) im Zeitverlauf an.
* Besuche: Zeigt die Trends für die Metrik [Besuche](/help/components/metrics/visits.md) im Zeitverlauf an.
* Besucher: Zeigt die Trends für verschiedene [Unique Visitors](/help/components/metrics/unique-visitors.md)-Metriken im Zeitverlauf an.
   * Unique Visitors: Zählt Besucher nur einmal für den gesamten ausgewählten Datumsbereich.
   * Unique Visitors pro Stunde: Zählt Besucher mehrmals bei Besuchen zu verschiedenen Stunden des ausgewählten Datumsbereichs.
   * Unique Visitors pro Tag: Zählt Besucher mehrmals bei Besuchen an verschiedenen Tagen des ausgewählten Datumsbereichs.
   * Unique Visitors pro Woche: Zählt Besucher mehrmals bei Besuchen in verschiedenen Wochen des ausgewählten Datumsbereichs.
   * Unique Visitors pro Monat: Zählt Besucher mehrmals bei Besuchen in verschiedenen Monaten des ausgewählten Datumsbereichs.
   * Unique Visitors pro Quartal: Zählt Besucher mehrmals bei Besuchen in verschiedenen Quartalen des ausgewählten Datumsbereichs. Die Quartale sind Januar–März, April–Juni, Juli–September und Oktober–Dezember.
   * Unique Visitors pro Jahr: Zählt Besucher mehrmals bei Besuchen in verschiedenen Kalenderjahren des ausgewählten Datumsbereichs.
* Zeit pro Besuch: Verwendet die Dimension [Zeit pro Besuch – Zusammengefasst](/help/components/dimensions/time-spent-per-visit.md).
* Zeit vor Ereignis: Verwendet die Dimension [Zeit vor Ereignis](/help/components/dimensions/time-prior-to-event.md).
* Einkäufe: Enthält Berichte zu einkaufsbasierten Metriken.
   * Einkaufs-Konversionstrichter: Berichtet über [Besuche](/help/components/metrics/visits.md), [Warenkörbe](/help/components/metrics/carts.md), [Bestellungen](/help/components/metrics/orders.md), [Umsatz](/help/components/metrics/revenue.md) und [Einheiten](/help/components/metrics/units.md) in einem Trichterbericht. Eine ähnliche Visualisierung wird in Analysis Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md) erreicht.
   * Umsatz: Zeigt die Trends der Metrik [Umsatz](/help/components/metrics/revenue.md) im Zeitverlauf an.
   * Bestellungen: Zeigt die Trends der Metrik [Bestellungen](/help/components/metrics/orders.md) im Zeitverlauf an.
   * Einheiten: Zeigt die Trends der Metrik [Einheiten](/help/components/metrics/units.md) im Zeitverlauf an.
* Warenkorb: Enthält Berichte zu Warenkorbmetriken.
   * Warenkorb-Konversionstrichter: Berichtet über [Instanzen](/help/components/metrics/instances.md), [Warenkörbe](/help/components/metrics/carts.md), [Checkouts](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md) und [Umsatz](/help/components/metrics/revenue.md) in einem Trichterbericht.
   * Warenkörbe: Zeigt die Trends der Metrik [Warenkörbe](/help/components/metrics/carts.md) im Zeitverlauf an.
   * Warenkorbansichten: Zeigt die Trends für die Metrik [Warenkorbansichten](/help/components/metrics/cart-views.md) im Zeitverlauf an.
   * Zusatz zum Warenkorb: Zeigt die Trends der Metrik [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md) im Zeitverlauf an.
   * Entnahme aus Warenkorb: Zeigt die Trends der Metrik [Entnahme aus Warenkorb](/help/components/metrics/cart-removals.md) im Zeitverlauf an.
   * Checkouts: Zeigt die Trends der Metrik [Checkouts](/help/components/metrics/checkouts.md) im Zeitverlauf an.
* Benutzerspezifische Ereignisse: Enthält alle Berichte zu benutzerspezifischen [Ereignissen](/help/components/metrics/custom-events.md), die für Ihre Implementierung spezifisch sind.
* Bots: Zeigt Bot-bezogene Berichte an.
   * Bots: Zeigt die Bots an, die Ihre Site am häufigsten besuchen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Bot-Regeln](../../admin/admin/bot-removal/bot-rules.md).
   * Bot-Seiten: Zeigt die Seiten mit den meisten Bot-Hits an.
* Echtzeit: Zeigt bestimmte Dimensionen und Metriken innerhalb von Sekunden nach der Datenerfassung an. Weitere Informationen finden Sie unter [Echtzeitberichte](/help/components/c-real-time-reporting/realtime.md).

## Site-Content

Enthält Berichte zu Dimensionen, die normalerweise den Site-Content anzeigen. Sie können einige dieser Berichte klassifizieren. Klassifizieren bedeutet, dass ein Bericht zu einem Menü wird, das den Quellbericht und die Klassifizierungsberichte enthält.

* Seiten: Verwendet die Dimension [Seite](/help/components/dimensions/page.md).
* Sitebereich: Verwendet die Dimension [Sitebereich](/help/components/dimensions/site-section.md).
* Server: Verwendet die Dimension [Server](/help/components/dimensions/server.md).
* Links: Enthält Berichte, die Linktracking verwenden.
   * Exitlinks: Verwendet die Dimension [Exitlinks](/help/components/dimensions/exit-link.md).
   * Dateidownloads: Verwendet die Dimension [Download-Link](/help/components/dimensions/download-link.md).
   * Benutzerspezifische Links: Verwendet die Dimension [Benutzerspezifischer Link](/help/components/dimensions/custom-link.md).
   * Seiten nicht gefunden: Verwendet die Dimension [Seiten nicht gefunden](/help/components/dimensions/pages-not-found.md).

## Mobile

Enthält Berichte zu älteren Mobile-Berichten. Diese Berichte basieren ihre Daten auf der Benutzeragenten-Zeichenfolge. Sie verwenden verschiedene [Mobile-Dimensionen](/help/components/dimensions/mobile-dimensions.md) für ihre jeweiligen Berichte.

* Geräte: Verwendet die Dimension [Mobilgerät](/help/components/dimensions/mobile-dimensions.md).
* Gerätetyp: Verwendet die Dimension [Mobilgerätetyp](/help/components/dimensions/mobile-dimensions.md).
* Hersteller: Verwendet die Dimension [Mobilgerätehersteller](/help/components/dimensions/mobile-dimensions.md).
* Bildschirmgröße: Verwendet die Dimension [Mobilgerät – Bildschirmgröße](/help/components/dimensions/mobile-dimensions.md).
* Bildschirmhöhe: Verwendet die Dimension [Mobilgerät – Bildschirmhöhe](/help/components/dimensions/mobile-dimensions.md).
* Bildschirmbreite: Verwendet die Dimension [Mobilgerät – Bildschirmbreite](/help/components/dimensions/mobile-dimensions.md).
* Cookie-Unterstützung: Verwendet die Dimension [Mobilgerät – Cookie-Unterstützung](/help/components/dimensions/mobile-dimensions.md).
* Bildunterstützung: Verwendet die Dimension [Mobilgerät – Bildunterstützung](/help/components/dimensions/mobile-dimensions.md).
* Farbtiefe: Verwendet die Dimension [Mobilgerät – Farbtiefe](/help/components/dimensions/mobile-dimensions.md).
* Audio-Unterstützung: Verwendet die Dimension [Mobilgerät – Audio-Unterstützung](/help/components/dimensions/mobile-dimensions.md).
* Video-Unterstützung: Verwendet die Dimension [Mobilgerät – Video-Unterstützung](/help/components/dimensions/mobile-dimensions.md).
* Betriebssystem (veraltet): Verwendet die Dimension [Mobiles Betriebssystem (veraltet)](/help/components/dimensions/mobile-dimensions.md).

## Pfade

Enthält Berichte, mit denen Sie Pfaddaten für Besucher anzeigen können.

* Nächster Seitenfluss: Verwendet einen Flussbericht auf dem Dimensionselement der obersten Seite. Pfadansichten ähneln [Instanzen](/help/components/metrics/instances.md). Sie können das gemeldete Dimensionselement ändern. Ein ähnlicher Bericht steht in Analysis Workspace mit einer [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md) zur Verfügung.
* Nächste Seite: Nimmt das Dimensionselement der obersten Seite und zeigt die nächsten Seiten an, die der Besucher besucht hat.
* Vorheriger Seitenfluss: Verwendet einen Flussbericht auf dem Dimensionselement der obersten Seite. Ein ähnlicher Bericht steht in Analysis Workspace mit einer [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md) zur Verfügung.
* Vorherige Seite: Nimmt das Dimensionselement der obersten Seite und zeigt die vorherigen Seiten an, die der Besucher besucht hat.
* Fallout: Ermöglicht die Auswahl von Seitendimensionselementen in Schritten und zeigt den Anteil der Personen an, die diesem Pfad gefolgt sind bzw. nicht gefolgt sind. Ein ähnlicher Bericht steht in Analysis Workspace mit einer [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md) zur Verfügung.
* Vollständige Pfade: Zeigt einzelne Pfade als Dimensionselemente an. In Analysis Workspace eingestellt. Verwenden Sie stattdessen die [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md).
* PathFinder: Stellt mehrere Berichtstypen bereit, mit denen Sie Pfade analysieren können (in Analysis Workspace eingestellt).
* Pfadlänge: Verwendet die Dimension [Besuchstiefe](/help/components/dimensions/visit-depth.md).
* Seitenanalyse
   * Seitenzusammenfassung: Nimmt das Dimensionselement der obersten Seite und zeigt eine Trend-Ansicht an. Zeigt außerdem Einstiegspunkte, vorherige Seiten, Ausstiegspunkte und nächste Seiten für dieses Dimensionselement der obersten Seite an.
   * Neuladungen: Verwendet die Dimension [Seite](/help/components/dimensions/page.md) mit der Metrik [Neuladungen](/help/components/metrics/reloads.md).
   * Besuchszeit pro Seite: Verwendet die Dimension [Besuchszeit pro Seite – Zusammengefasst](/help/components/dimensions/time-spent-on-page.md).
   * Klicks pro Seite: Nimmt das Dimensionselement der obersten Seite und zeigt die Anzahl der Klicks an, die erforderlich waren, um bei einem bestimmten Besuch zu dieser Seite zu gelangen.
* Ein- und Ausstiege
   * Entrypages: Verwendet die Dimension [Entrypages](/help/components/dimensions/entry-dimensions.md).
   * Ursprüngliche Entrypages: Verwendet die Dimension [Ursprüngliche Entrypage](/help/components/dimensions/entry-dimensions.md).
   * Einzelseitenbesuche: Verwendet die Dimension [Seite](/help/components/dimensions/page.md), auf die das von Adobe bereitgestellte Segment „Einzelseitenbesuche“ angewendet wurde.
   * Exitpages: Verwendet die Dimension [Exitpages](/help/components/dimensions/exit-dimensions.md).

>[!NOTE]
>
>In diesem Ordner können andere Berichte angezeigt werden. Es handelt sich dabei um andere Dimensionen, wie z. B. Eigenschaften, bei denen die [Pfade unter den Report Suite-Einstellungen aktiviert](../../admin/admin/c-traffic-variables/traffic-var.md) sind.

## Traffic-Quellen

Enthält Berichte, die Aufschluss darüber geben, woher Besucher kamen, bevor sie zu Ihrer Site gelangten. Diese Berichte funktionieren nur dann ordnungsgemäß, wenn Sie die [internen URL-Filter](../../admin/admin/internal-url-filter-admin.md) unter den Report Suite-Einstellungen korrekt festlegen.

* Suchbegriffe - Alle: Verwendet die Dimension [Suchbegriff](/help/components/dimensions/search-keyword.md).
* Suchbegriffe - Gebührenpflichtig: Verwendet die Dimension [Suchbegriff - Gebührenpflichtig](/help/components/dimensions/search-keyword.md).
* Suchbegriffe - Kostenlos: Verwendet die Dimension [Suchbegriff - Kostenlos](/help/components/dimensions/search-keyword.md).
* Suchmaschinen - Alle: Verwendet die Dimension [Suchmaschine](/help/components/dimensions/search-engine.md).
* Suchmaschinen - Gebührenpflichtig: Verwendet die Dimension [Suchmaschine – Gebührenpflichtig](/help/components/dimensions/search-engine.md).
* Suchmaschinen - Kostenlos: Verwendet die Dimension [Suchmaschine – Kostenlos](/help/components/dimensions/search-engine.md).
* Rangansicht aller Suchseiten: Verwendet die Dimension [Rangansicht aller Suchseiten](/help/components/dimensions/all-search-page-rank.md).
* Referrerdomänen: Verwendet die Dimension [Referrerdomäne](/help/components/dimensions/referring-domain.md).
* Ursprüngliche Referrerdomänen: Verwendet die Dimension [Ursprüngliche Referrerdomäne](/help/components/dimensions/original-referring-domain.md).
* Referrers: Verwendet die Dimension [Referrer](/help/components/dimensions/referrer.md).
* Referrer-Typen: Verwendet die Dimension [Referrer-Typ](/help/components/dimensions/referrer-type.md).

## Kampagnen

Enthält Berichte, die sich in erster Linie auf die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) beziehen.

* Kampagnen-Konversionstrichter: Berichtet über Clickthroughs, [Checkouts](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md) und [Umsatz](/help/components/metrics/revenue.md) in einem Trichterbericht. Die Clickthrough-Metrik ähnelt der Metrik [Instanzen](/help/components/metrics/instances.md) im Kontext der Dimension [Trackingcode](/help/components/dimensions/tracking-code.md). Eine ähnliche Visualisierung wird in Analysis Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md) erreicht.
* Trackingcode: Verwendet die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md).

## Produkte

Enthält Berichte, die sich in erster Linie auf die Dimension [Produkt](/help/components/dimensions/product.md) beziehen.

* Produkt-Konversionstrichter: Berichtet über [Produktansichten](/help/components/metrics/product-views.md), [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md), [Checkouts](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md), [Einheiten](/help/components/metrics/units.md) und [Umsatz](/help/components/metrics/revenue.md) in einem Trichterbericht. Eine ähnliche Visualisierung wird in Analysis Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md) erreicht.
* Produkte: Verwendet die Dimension [Produkte](/help/components/dimensions/product.md).
* Cross-Sell: Zeigt Produkte an, die häufig zusammen verkauft werden (in Analysis Workspace nicht mehr verfügbar).
* Kategorien: Verwendet die Dimension [Kategorie](/help/components/dimensions/category.md).

## Besuchertreue

Enthält Berichte zu Besuchern, die zu Ihrer Site zurückkehren.

* Rückkehrhäufigkeit: Verwendet die Dimension [Rückkehrhäufigkeit](/help/components/dimensions/return-frequency.md).
* Erneute Besuche: Zeigt die Trends für die Metrik [Besuche](/help/components/metrics/visits.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Erneute Besuche“ an.
* Besuchsnummer: Verwendet die Dimension [Besuchsnummer](/help/components/dimensions/visit-number.md).
* Verkaufszyklus: Ordner für kaufbezogene Berichte.
   * Kundentreue: Verwendet die Dimension [Kundentreue](/help/components/dimensions/customer-loyalty.md).
   * Tage bis Erstkauf: Verwendet die Dimension [Tage bis Erstkauf](/help/components/dimensions/days-before-first-purchase.md).
   * Tage seit letztem Kauf: Verwendet die Dimension [Tage seit letztem Kauf](/help/components/dimensions/days-since-last-purchase.md).
   * Unique Customers pro Tag: Zeigt die Trends für [Unique Visitors pro Tag](/help/components/metrics/unique-visitors.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Käufer“ an.
   * Unique Customers pro Woche: Zeigt die Trends für [Unique Visitors pro Woche](/help/components/metrics/unique-visitors.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Käufer“ an.
   * Unique Customers pro Monat: Zeigt die Trends für [Unique Visitors pro Monat](/help/components/metrics/unique-visitors.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Käufer“ an.
   * Unique Customers pro Quartal: Zeigt die Trends für [Unique Visitors pro Quartal](/help/components/metrics/unique-visitors.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Käufer“ an. Die Quartale sind Januar–März, April–Juni, Juli–September und Oktober–Dezember.
   * Unique Customers pro Jahr: Zeigt die Trends für [Unique Visitors pro Jahr](/help/components/metrics/unique-visitors.md) im Zeitverlauf unter Anwendung des von Adobe bereitgestellten Segments „Käufer“ an.

## Besucherprofil

Enthält Berichte darüber, wer Ihre Site besucht.

* GeoSegmentation: Berichte darüber, von wo auf der Welt Zugriffe auf Ihre Website stammen.
   * Länder: Verwendet die Dimension [Länder](/help/components/dimensions/countries.md).
   * Region: Verwendet die Dimension [Regionen](/help/components/dimensions/regions.md).
   * Städte: Verwendet die Dimension [Städte](/help/components/dimensions/cities.md).
   * US-Bundesstaaten: Verwendet die Dimension [US-Bundesstaaten](/help/components/dimensions/us-states.md).
   * US DMA: Verwendet die Dimension [US DMA](/help/components/dimensions/us-dma.md).
* Sprachen: Verwendet die Dimension [Sprache](/help/components/dimensions/language.md).
* Zeitzonen: Verwendet die Zeitzonendimension (in Analysis Workspace nicht mehr verfügbar). Die Dimensionselemente sind der GMT-Versatz des Treffers.
* Domäne: Verwendet die Dimension [Domäne](/help/components/dimensions/domain.md).
* Domäne auf oberster Ebene: Verwendet die Dimension „Domäne auf oberster Ebene“ (in Analysis Workspace nicht mehr verfügbar). Sie gruppiert die Dimension [Domänen](/help/components/dimensions/domain.md) in Kategorien auf höherer Ebene, in der Regel nach Land der Domäne.
* Technologie: Ordner mit Berichten darüber, was der Besucher für den Zugriff auf Ihre Site verwendet hat.
   * Browser: Verwendet die Dimension [Browser](/help/components/dimensions/browser.md).
   * Browsertyp: Verwendet die Dimension [Browsertyp](/help/components/dimensions/browser-type.md).
   * Browserbreite: Verwendet die Dimension [Browserbreite – Zusammengefasst](/help/components/dimensions/browser-width.md).
   * Browserhöhe: Verwendet die Dimension [Browserhöhe – Zusammengefasst](/help/components/dimensions/browser-height.md).
   * Betriebssystem: Verwendet die Dimension [Betriebssysteme](/help/components/dimensions/operating-systems.md).
   * Betriebssystemtyp: Verwendet die Dimension [Betriebssystemtypen](/help/components/dimensions/operating-system-types.md).
   * Bildschirmfarbtiefe: Verwendet die Dimension [Farbtiefe](/help/components/dimensions/color-depth.md).
   * Bildschirmauflösung: Verwendet die Dimension [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md).
   * Java: Verwendet die Dimension [Java aktiviert](/help/components/dimensions/java-enabled.md).
   * JavaScript: Verwendet die Dimension „JavaScript aktiviert“ (in Analysis Workspace nicht mehr verfügbar). Die Dimensionselemente sind „Aktiviert“, „Deaktiviert“ oder „Unbekannt“, je nachdem, ob JavaScript im Browser aktiviert ist.
   * JavaScript Version: Verwendet die Dimension „JavaScript Version“ (in Analysis Workspace nicht mehr verfügbar). Die Dimensionselemente zeigen die JavaScript-Version, die der Browser verwendet.
   * Cookies: Verwendet die Dimension [Cookie-Unterstützung](/help/components/dimensions/cookie-support.md).
   * Verbindungstypen: Verwendet die Dimension [Verbindungstyp](/help/components/dimensions/connection-type.md).
   * Mobilnetzbetreiber: Verwendet die Dimension [Mobilnetzbetreiber](/help/components/dimensions/mobile-dimensions.md).
* Bundesstaat des Besuchers: Verwendet die Dimension „Bundesstaat“ (in Analysis Workspace nicht mehr verfügbar). Die Dimensionselemente stammen aus der Variablen [`state`](../../implement/vars/page-vars/state.md).
* PLZ/Postleitzahlen des Besuchers: Verwendet die Dimension [Postleitzahl](/help/components/dimensions/zip-code.md).

## Benutzerspezifische Konversion

Enthält Berichte, die spezifisch für Ihre Implementierung gelten. Benutzerspezifische Konversionsberichte verwenden [eVars](/help/components/dimensions/evar.md) als Dimension.

## Benutzerspezifischer Traffic

Enthält Berichte, die spezifisch für Ihre Implementierung gelten. Benutzerspezifische Traffic-Berichte verwenden [Props](/help/components/dimensions/prop.md) als Dimension.

## Marketing-Kanäle

Enthält Berichte mit [Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Kanalübersichtsbericht: Ein benutzerspezifischer Bericht speziell für Reports &amp; Analytics. Verwendet Marketing-Kanäle als Dimensionselemente, wobei Metriken die Erstkontakt- und Letztkontakt-Attribution verwenden.
* Erstkontaktkanal: Verwendet die Dimension [Erstkontaktkanal](/help/components/dimensions/first-touch-channel.md).
* Erstkontaktkanaldetail: Verwendet die Dimension [Erstkontaktkanaldetail](/help/components/dimensions/first-touch-detail.md).
* Letztkontaktkanal: Verwendet die Dimension [Letztkontaktkanal](/help/components/dimensions/last-touch-channel.md).
* Letztkontaktkanaldetail: Verwendet die Dimension [Letztkontaktkanaldetail](/help/components/dimensions/last-touch-detail.md).

## Lesezeichen

Enthält Berichte, die Sie mit einem Lesezeichen versehen haben. Weitere Informationen finden Sie unter [Lesezeichen](bookmarks.md).

## Dashboards

Enthält von Ihnen erstellte Dashboard. Weitere Informationen finden Sie unter [Dashboards](dashboard.md).

## Zielgruppen

Enthält von Ihnen erstellte Zielgruppen. Weitere Informationen finden Sie unter [Zielgruppen](targets.md).

>[!NOTE]
>
>Wenn Sie Ihren Bericht auf dieser Hilfeseite nicht finden können, hat Ihr Administrator möglicherweise Ordner umbenannt oder angepasst. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Menüanpassung](/help/admin/admin/customize-menus.md).
