---
title: Berichte
description: Die Dimensionen und Metriken, die von Reports & Analysen für jeden Bericht verwendet werden.
translation-type: tm+mt
source-git-commit: 1968162d856b6a74bc61f22f2e5a6b1599d04c79
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 1%

---


# Berichte

Jeder Bericht in Reports &amp; Analysen verwendet eine dedizierte Dimension und Standardmetrik. Sie können die Metrik in jedem Bericht ändern und bei Bedarf Unterteilungen hinzufügen. Die folgenden Listen geben an, welche Dimension in den einzelnen Berichten verwendet wird.

> [!NOTE] Ihr Berichtsmenü kann je nach den Anpassungen, die ein Administrator in Ihrer Organisation vorgenommen hat, unterschiedlich aussehen. See [Menu customizing](/help/admin/admin/customize-menus.md) in the Admin user guide.

## Sitemetriken 

Enthält Berichte, die in der Regel mit einem Datumsbereich einen Trend verfolgen. Enthält außerdem eindeutige Berichte, z. B. empfohlene Berichte und Echtzeitberichte.

* Meine empfohlenen Berichte: Erstellt ein Dashboard, das mehrere Reportlets für sofortige Einblicke enthält.
* Schlüsselmetriken: Ein Bericht, mit dem Sie bis zu fünf Metriken gleichzeitig als Trend verfolgen können. Trendansicht [von Ansichten](/help/components/metrics/page-views.md), [Besuchen](/help/components/metrics/visits.md)und [individuellen Besuchern](/help/components/metrics/unique-visitors.md) .
* Ansichten der Seite: Trendansicht der Metrik [&quot;Ansichten](/help/components/metrics/page-views.md) &quot;im Zeitverlauf.
* Besuche: Trendansicht der Metrik &quot; [Besuche](/help/components/metrics/visits.md) &quot;im Zeitverlauf.
* Besucher: Trendansicht verschiedener Metriken zu [individuellen Besuchern](/help/components/metrics/unique-visitors.md) im Zeitverlauf.
   * Individuelle Besucher: Zählt Besucher nur einmal für den gesamten ausgewählten Datumsbereich.
   * Individuelle Besucher pro Stunde: Zählt Besucher mehrmals, wenn sie innerhalb eines bestimmten Zeitraums besucht werden.
   * Individuelle Besucher pro Tag: Zählt Besucher mehrmals, wenn sie während verschiedener Tage des ausgewählten Datumsbereichs besucht werden.
   * Individuelle Besucher pro Woche: Zählt Besucher mehrere Male, wenn sie innerhalb eines bestimmten Zeitraums im ausgewählten Datumsbereich besucht werden.
   * Individuelle Besucher pro Monat: Zählt Besucher mehrmals, wenn sie in verschiedenen Monaten des ausgewählten Datumsbereichs besuchen.
   * Individuelle Besucher pro Quartal: Zählt Besucher mehrmals, wenn sie während eines anderen Quartals des ausgewählten Datumsbereichs besucht werden. Die Quartale sind Januar-März, April-Juni, Juli-September und Oktober-Dezember.
   * Individuelle Besucher pro Jahr: Zählt Besucher mehrmals, wenn sie in verschiedenen Kalenderjahren des ausgewählten Datumsbereichs besuchen.
* Besuchszeit pro Besuch: Verwendet die Dimension [Besuchszeit pro Besuch](/help/components/dimensions/time-spent-per-visit.md) .
* Zeit vor dem Ereignis: Verwendet die Dimension &quot; [Zeit vor Ereignis](/help/components/dimensions/time-prior-to-event.md) &quot;.
* Einkäufe: Enthält Berichte zu einkaufsbasierten Metriken.
   * Kaufkonversionstrichter: Bericht zu [Besuchen](/help/components/metrics/visits.md), [Einkaufswagen](/help/components/metrics/carts.md), [Bestellungen](/help/components/metrics/orders.md), [Umsatz](/help/components/metrics/revenue.md)und [Einheiten](/help/components/metrics/units.md) in einem Trichterbericht. Eine ähnliche Visualisierung wird in Analyse Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md)erreicht.
   * Umsatz: Trendansicht der Metrik [Umsatz](/help/components/metrics/revenue.md) im Zeitverlauf.
   * Bestellungen: Trendansicht der Metrik [Bestellungen](/help/components/metrics/orders.md) im Zeitverlauf.
   * Einheiten: Trendt die Metrikeinheiten [im Zeitverlauf](/help/components/metrics/units.md) .
* Einkaufswagen: Enthält Berichte zu Warenkorbmetriken.
   * Einkaufswagenkonversionstrichter: Berichte zu [Instanzen](/help/components/metrics/instances.md), [Einkaufswagen](/help/components/metrics/carts.md), [Kassengängen](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md)und [Umsatz](/help/components/metrics/revenue.md) in einem Trichterbericht.
   * Einkaufswagen: Trendansicht der Metrik [Einkaufswagen](/help/components/metrics/carts.md) im Zeitverlauf.
   * Warenkorb-Ansichten: Trendansicht der Metrik [Warenkorb-Ansichten](/help/components/metrics/cart-views.md) im Zeitverlauf.
   * Zusatz zum Einkaufswagen: Trendansicht der Metrik [Zusätze](/help/components/metrics/cart-additions.md) zum Warenkorb im Zeitverlauf.
   * Entnahme aus Einkaufswagen: Trendansicht der Metrik [Entnahmen aus](/help/components/metrics/cart-removals.md) Warenkorb im Zeitverlauf.
   * Kassengänge: Trendansicht der Metrik [Kassengänge](/help/components/metrics/checkouts.md) im Zeitverlauf.
* Benutzerspezifische Ereignis: Enthält alle Berichte zu benutzerspezifischen [Ereignissen](/help/components/metrics/custom-events.md) , die für Ihre Implementierung spezifisch sind.
* Bots: Zeigt Bot-bezogene Berichte an.
   * Bots: Zeigt die Bots an, die Ihre Site am häufigsten besuchen. See [Bot rules](../../admin/admin/bot-removal/bot-rules.md) in the Admin user guide.
   * Bot-Seiten: Zeigt die Seiten an, die von Bots am meisten getroffen werden.
* Echtzeit: Zeigt bestimmte Dimensionen und Metriken innerhalb von Sekunden nach der Datenerfassung an. See [Real-time reports](/help/components/c-real-time-reporting/realtime.md) for more information.

## Site-Inhalt

Enthält Berichte zu Dimensionen, die normalerweise den Site-Inhalt anzeigen. Sie können Classifications auf einige dieser Berichte anwenden. Das Anwenden von Klassifizierungen bedeutet, dass ein Bericht zu einem Menü wird, das den Quellbericht und die Klassifizierungsberichte enthält.

* Seiten: Verwendet die [Seitendimension](/help/components/dimensions/page.md) .
* Site-Abschnitt: Verwendet die Dimension &quot; [Site-Abschnitt](/help/components/dimensions/site-section.md) &quot;.
* Server: Verwendet die [Serverdimension](/help/components/dimensions/server.md) .
* Links: Enthält Berichte, die die Linktracking verwenden.
   * Ausstiegslinks: Verwendet die Dimension &quot; [Ausstiegslink](/help/components/dimensions/exit-link.md) &quot;.
   * Dateidownloads: Verwendet die Dimension &quot; [Download-Link](/help/components/dimensions/download-link.md) &quot;.
   * Benutzerspezifische Links: Verwendet die Dimension &quot; [Benutzerspezifischer Link](/help/components/dimensions/custom-link.md) &quot;.
   * Seiten nicht gefunden: Verwendet die Dimension &quot; [Seiten nicht gefunden](/help/components/dimensions/pages-not-found.md) &quot;.

## Mobile

Enthält Berichte zu älteren Mobilberichten. Diese Berichte basieren ihre Daten auf der Benutzeragenten-Zeichenfolge. Sie verwenden verschiedene [Mobildimensionen](/help/components/dimensions/mobile-dimensions.md) für ihre jeweiligen Berichte.

* Geräte: Verwendet die Dimension &quot; [Mobilgerät](/help/components/dimensions/mobile-dimensions.md) &quot;.
* Gerätetyp: Verwendet die Dimension [Mobilgerätetyp](/help/components/dimensions/mobile-dimensions.md) .
* Hersteller: Verwendet die Dimension [Mobilhersteller](/help/components/dimensions/mobile-dimensions.md) .
* Bildschirmgröße: Verwendet die Bildschirmgröße für [Mobilgeräte](/help/components/dimensions/mobile-dimensions.md) .
* Bildschirmhöhe: Verwendet die [Bildschirmhöhe](/help/components/dimensions/mobile-dimensions.md) für Mobilgeräte.
* Bildschirmbreite: Verwendet die Bildschirmbreite [von](/help/components/dimensions/mobile-dimensions.md) Mobile.
* Cookie-Unterstützung: Verwendet die Dimension zur Unterstützung von [Mobile-Cookies](/help/components/dimensions/mobile-dimensions.md) .
* Bildunterstützung: Verwendet die Dimension &quot; [Mobile-Bildunterstützung](/help/components/dimensions/mobile-dimensions.md) &quot;.
* Farbtiefe: Verwendet die Farbtiefendimension für [Mobilgeräte](/help/components/dimensions/mobile-dimensions.md) .
* Audiounterstützung: Verwendet die Dimension [Mobile Audiounterstützung](/help/components/dimensions/mobile-dimensions.md) .
* Videounterstützung: Verwendet die Dimension &quot; [Mobile-Videounterstützung](/help/components/dimensions/mobile-dimensions.md) &quot;.
* Betriebssystem (nicht mehr unterstützt): Verwendet die Dimension [Mobile-Betriebssystem (nicht mehr unterstützt)](/help/components/dimensions/mobile-dimensions.md) .

## Pfade

Enthält Berichte, mit denen Sie Pfaddaten für Besucher anzeigen können.

* Nächster Seitenfluss: Verwendet einen Flussbericht auf dem Dimensionswert der obersten Seite. Path-Ansichten ähneln [Instanzen](/help/components/metrics/instances.md). Sie können den gemeldeten Dimensionswert ändern. Ein ähnlicher Bericht im Arbeitsbereich für Analysen steht mit einer [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md)zur Verfügung.
* Nächste Seite: nimmt den Dimensionswert der obersten Seite und zeigt die nächsten Seiten an, zu denen Besucher gegangen sind.
* Vorheriger Seitenfluss: Verwendet einen Flussbericht auf dem Dimensionswert der obersten Seite. Ein ähnlicher Bericht in Analyse Workspace steht mit einer [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md)zur Verfügung.
* Vorherige Seite: Führt den Dimensionswert der obersten Seite und zeigt Ihnen die vorherigen Seiten an, von denen die Besucher kamen.
* Trichteranalyse: Ermöglicht die Auswahl von Seitendimensionswerten in Schritten und zeigt den Anteil der Personen an, die diesem Pfad gefolgt sind bzw. nicht gefolgt sind. Ein ähnlicher Bericht im Arbeitsbereich für Analysen steht mit einer [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md)zur Verfügung.
* Vollständige Pfade: Zeigt einzelne Pfade als Dimensionswerte an. im Arbeitsbereich für Analysen müde; Verwenden Sie stattdessen die [Flussvisualisierung](../analysis-workspace/visualizations/c-flow/flow.md) .
* PathFinder: Stellt mehrere Berichtstypen bereit, mit denen Sie Pfade analysieren können (in Analyse Workspace eingestellt).
* Pfadlänge: Verwendet die Dimension [Besuchstiefe](/help/components/dimensions/visit-depth.md) .
* Seitenanalyse
   * Seitenzusammenfassung: Führt den Dimensionswert der obersten Seite und zeigt eine Trendansicht an. Zeigt außerdem Einstiegspunkte, vorherige Seiten, Ausstiegspunkte und nächste Seiten für diesen Wert der Dimension der obersten Seite an.
   * Neuladungen: Verwendet die [Seitendimension](/help/components/dimensions/page.md) mit der Metrik &quot; [Neuladungen](/help/components/metrics/reloads.md) &quot;.
   * Besuchszeit pro Seite: Verwendet die Dimension &quot; [Besuchszeit pro Seite - Zusammengefasst](/help/components/dimensions/time-spent-on-page.md) &quot;.
   * Klicks pro Seite: Führt den Dimensionswert der obersten Seite und zeigt die Anzahl der Klicks an, die erforderlich waren, um zu dieser Seite bei einem bestimmten Besuch zu gelangen.
* Einstiege und Ausstiege
   * Entrypages: Verwendet die Dimension &quot; [Entrypages](/help/components/dimensions/entry-dimensions.md) &quot;.
   * Ursprüngliche Entrypages: Verwendet die ursprüngliche Dimension der [Entrypage](/help/components/dimensions/entry-dimensions.md) .
   * Einzelseitenbesuche: Verwendet die Dimension &quot; [Seite](/help/components/dimensions/page.md) &quot;mit dem von Adobe bereitgestellten Segment &quot;Einzelseitenbesuche&quot;.
   * Ausstiegsseiten: Verwendet die Dimension &quot; [Ausstiegsseiten](/help/components/dimensions/exit-dimensions.md) &quot;.

> [!NOTE] Andere Berichte können in diesem Ordner angezeigt werden. Es handelt sich dabei um andere Dimensionen, z. B. Props, bei denen die [Pfadsetzung unter den Report Suite-Einstellungen aktiviert](../../admin/admin/c-traffic-variables/traffic-var.md) ist.

## Traffic-Quellen

Enthält Bericht, der Aufschluss darüber gibt, woher Besucher kamen, bevor sie zu Ihrer Site gelangten. Diese Berichte funktionieren nur dann ordnungsgemäß, wenn Sie unter den Report Suite-Einstellungen die Filter für [interne URLs](../../admin/admin/internal-url-filter-admin.md) korrekt festlegen.

* Suchbegriffe - alle: Verwendet die Dimension [Suchbegriff](/help/components/dimensions/search-keyword.md) .
* Suchbegriffe - gebührenpflichtig: Verwendet die Dimension [Suchbegriff - Gebührenpflichtig](/help/components/dimensions/search-keyword.md) .
* Suchbegriffe - kostenlos: Verwendet die Dimension [Suchbegriff - Kostenlos](/help/components/dimensions/search-keyword.md)
* Suchmaschinen - alle: Verwendet die [Suchmaschinendimension](/help/components/dimensions/search-engine.md) .
* Suchmaschinen - gebührenpflichtig: Verwendet die Dimension [Suchmaschine - Gebührenpflichtig](/help/components/dimensions/search-engine.md) .
* Suchmaschinen - kostenlos: Verwendet die [Suchmaschine - kostenlose](/help/components/dimensions/search-engine.md) Dimension.
* Rangansicht aller Suchseiten: Verwendet die Dimension &quot; [Alle Suchseitenrang](/help/components/dimensions/all-search-page-rank.md) &quot;.
* Verweisende Domänen: Verwendet die Dimension &quot; [Verweisende Domäne](/help/components/dimensions/referring-domain.md) &quot;
* Ursprünglich verweisende Domänen: Verwendet die Dimension &quot; [Ursprünglich verweisende Domäne](/help/components/dimensions/original-referring-domain.md) &quot;
* Werber: Verwendet die Dimension &quot; [Werber](/help/components/dimensions/referrer.md) &quot;.
* Werber: Verwendet die [Dimension &quot;Werber&quot;](/help/components/dimensions/referrer-type.md) .

## Kampagnen

Enthält Berichte, die sich in erster Linie auf die Dimension [Rückverfolgungscode](/help/components/dimensions/tracking-code.md) beziehen.

* Kampagne-Konversionstrichter: Berichte zu Durchklickraten, [Kassengängen](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md)und [Umsatz](/help/components/metrics/revenue.md) in einem Trichterbericht. Die Clickthrough-Metrik ähnelt der Metrik [Instanzen](/help/components/metrics/instances.md) im Kontext der Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) . Eine ähnliche Visualisierung wird in Analyse Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md)erreicht.
* Rückverfolgungscode: Verwendet die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) .

## Produkte

Enthält Berichte, die sich hauptsächlich auf die [Produktdimension](/help/components/dimensions/product.md) beziehen.

* Produktkonversionstrichter: Berichte zu [Ansichten](/help/components/metrics/product-views.md), [Zusätze](/help/components/metrics/cart-additions.md)zum Warenkorb, [Kassengänge](/help/components/metrics/checkouts.md), [Bestellungen](/help/components/metrics/orders.md), [Einheiten](/help/components/metrics/units.md)[](/help/components/metrics/revenue.md) undUmsatzin einem Trichterbericht. Eine ähnliche Visualisierung wird in Analyse Workspace mithilfe der [Fallout-Visualisierung](../analysis-workspace/visualizations/fallout/fallout-flow.md)erreicht.
* Produkte: Verwendet die Dimension &quot; [Produkte](/help/components/dimensions/product.md) &quot;.
* Querverkauf: Zeigt häufig zusammen verkaufte Produkte an (in Analyse Workspace eingestellt).
* Kategorien: Verwendet die Dimension [Kategorie](/help/components/dimensions/category.md) .

## Besuchertreue

Enthält Berichte zu Besuchern, die zu Ihrer Site zurückkehren.

* Rückkehrhäufigkeit: Verwendet die Dimension [Rückkehrhäufigkeit](/help/components/dimensions/return-frequency.md) .
* Rückkehrende Besuche: Trendansicht der Metrik &quot; [Besuche](/help/components/metrics/visits.md) &quot;im Zeitverlauf mit Anwendung des von Adobe bereitgestellten Segments &quot;Rückkehrende Besucher&quot;.
* Besuch Nr.: Verwendet die Dimension [Besuchsnummer](/help/components/dimensions/visit-number.md) .
* Verkaufszyklus: Ordner für Berichte zum Kauf.
   * Kundentreue: Verwendet die Dimension &quot; [Kundentreue](/help/components/dimensions/customer-loyalty.md) &quot;.
   * Tage vor dem ersten Kauf: Verwendet die Dimension &quot; [Tage vor dem ersten Kauf](/help/components/dimensions/days-before-first-purchase.md) &quot;.
   * Tage seit dem letzten Kauf: Verwendet die Dimension &quot; [Tage seit dem letzten Kauf](/help/components/dimensions/days-since-last-purchase.md) &quot;.
   * Individuelle Kunden pro Tag: Trendansicht von [individuellen Besuchern](/help/components/metrics/unique-visitors.md) pro Tag im Zeitverlauf mit Anwendung des von Adobe bereitgestellten Segments &quot;Käufer&quot;.
   * Individuelle Kunden pro Woche: Trendt [wöchentliche individuelle Besucher](/help/components/metrics/unique-visitors.md) im Zeitverlauf mit angewendetem von Adobe bereitgestelltem &quot;Käufer&quot;-Segment.
   * Individuelle Kunden pro Monat: Trendt individuelle [Besucher](/help/components/metrics/unique-visitors.md) pro Monat mit Anwendung des von Adobe bereitgestellten &quot;Käufern&quot;-Segments.
   * Individuelle Kunden pro Quartal: Trendt [vierteljährliche individuelle Besucher](/help/components/metrics/unique-visitors.md) im Zeitverlauf mit dem von Adobe bereitgestellten &quot;Käufer&quot;-Segment. Die Quartale sind Januar-März, April-Juni, Juli-September und Oktober-Dezember.
   * Unique Customers pro Jahr: Trendt [Unique Besucher](/help/components/metrics/unique-visitors.md) im Laufe der Zeit mit Anwendung des von Adobe bereitgestellten &quot;Käufern&quot;-Segments.

## Besucherprofil

Enthält Berichte darüber, wer Ihre Site besucht.

* Geosegmentation: Berichte darüber, woher auf der Welt die Treffer auf Ihrer Site kamen.
   * Länder: Verwendet die [Dimension &quot;Länder](/help/components/dimensions/countries.md) &quot;.
   * Region: Verwendet die [Dimension &quot;Regionen](/help/components/dimensions/regions.md) &quot;.
   * Städte: Verwendet die [Dimension &quot;Städte](/help/components/dimensions/cities.md) &quot;.
   * US-Bundesstaaten: Verwendet die [US-amerikanische](/help/components/dimensions/us-states.md) Dimension.
   * US DMA: Verwendet die [US-DMA](/help/components/dimensions/us-dma.md) -Dimension.
* Sprachen: Verwendet die [Dimension &quot;Sprache](/help/components/dimensions/language.md) &quot;.
* Zeitzonen: Verwendet die Zeitzonendimension (wird in Analyse Workspace eingestellt). Dimensionswerte sind der GMT-Offset des Treffers.
* Domäne: Verwendet die [Dimension &quot;Domäne](/help/components/dimensions/domain.md) &quot;.
* Domäne oberster Ebene: Verwendet die Dimension &quot;Domäne auf oberster Ebene&quot;(wird in Analyse Workspace eingestellt). Die [Domänendimension](/help/components/dimensions/domain.md) wird in Kategorien auf höherer Ebene gruppiert, in der Regel nach Land der Domäne.
* Technologie: Ordner mit Berichten, die den Besucher beim Zugriff auf Ihre Site aufzeigen.
   * Browser: Verwendet die [Browser](/help/components/dimensions/browser.md) -Dimension.
   * Browsertyp: Verwendet die Dimension [Browsertyp](/help/components/dimensions/browser-type.md) .
   * Browserbreite: Verwendet die Dimension [Browserbreite - Zusammengefasst](/help/components/dimensions/browser-width.md) .
   * Browserhöhe: Verwendet die [Browserhöhe - zusammengefasste](/help/components/dimensions/browser-height.md) Dimension.
   * Betriebssystem: Verwendet die [Betriebssystemdimension](/help/components/dimensions/operating-systems.md) .
   * Betriebssystemtyp: Verwendet die Dimension [Betriebssystemtypen](/help/components/dimensions/operating-system-types.md) .
   * Bildschirmfarbtiefe: Verwendet die [Farbtiefendimension](/help/components/dimensions/color-depth.md) .
   * Bildschirmauflösung: Verwendet die Dimension [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md) .
   * Java: Verwendet die [Java-aktivierte](/help/components/dimensions/java-enabled.md) Dimension.
   * JavaScript: Verwendet die Dimension &quot;JavaScript aktiviert&quot;(wird in Analyse Workspace eingestellt). Dimensionswerte sind &quot;Aktiviert&quot;, &quot;Deaktiviert&quot;oder &quot;Unbekannt&quot;, je nachdem, ob JavaScript im Browser aktiviert ist.
   * JavaScript-Version: verwendet die Dimension &quot;JavaScript-Version&quot;(wird in Analyse Workspace eingestellt). Dimensionswerte zeigen die JavaScript-Version, die der Browser verwendet.
   * Cookies: Verwendet die [Cookie-Unterstützungsdimension](/help/components/dimensions/cookie-support.md) .
   * Verbindungstypen: Verwendet die [Dimension Verbindungstyp](/help/components/dimensions/connection-type.md) .
   * Mobilnetzbetreiber: Verwendet die Dimension &quot; [Mobilnetzbetreiber](/help/components/dimensions/mobile-dimensions.md) &quot;.
* Status des Besuchers: Verwendet die Statusdimension (wird in Analyse Workspace eingestellt). Dimensionswerte stammen aus der [`state`](../../implement/vars/page-vars/state.md) Variablen.
* Postleitzahl des Besuchers: Verwendet die [Zip-Code](/help/components/dimensions/zip-code.md) -Dimension.

## Benutzerdefinierte Konvertierung

Enthält Berichte, die spezifisch für Ihre Implementierung gelten. Benutzerspezifische Konversionsberichte verwenden [eVars](/help/components/dimensions/evar.md) als Dimension.

## Benutzerspezifischer Traffic

Enthält Berichte, die spezifisch für Ihre Implementierung gelten. Benutzerspezifische Traffic-Berichte verwenden [Props](/help/components/dimensions/prop.md) als Dimension.

## Marketing-Kanäle

Enthält Berichte mit [Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Kanal-Übersichtsbericht: Ein benutzerdefinierter Bericht, der spezifisch für Reports &amp; Analysen ist. Verwendet Marketing-Kanal als Dimensionswerte, wobei Metriken die First Touch- oder Last Touch-Zuordnung verwenden.
* First Touch-Kanal: Verwendet die Dimension &quot; [First Touch-Kanal](/help/components/dimensions/first-touch-channel.md) &quot;.
* First Touch-Kanal: Verwendet die Detaildimension des [First Touch-Kanals](/help/components/dimensions/first-touch-detail.md) .
* Last Touch-Kanal: Verwendet die Dimension &quot; [Last Touch-Kanal](/help/components/dimensions/last-touch-channel.md) &quot;.
* Letztkontakt Kanal: Verwendet die Detaildimension des [Last Touch-Kanals](/help/components/dimensions/last-touch-detail.md) .

## Lesezeichen

Enthält Berichte, die Sie mit einem Lesezeichen versehen haben. Weitere Informationen finden Sie unter [Lesezeichen](bookmarks.md) .

## Dashboards

Enthält von Ihnen erstellte Dashboard. Weitere Informationen finden Sie unter [Dashboards](dashboard.md) .

## Ziele 

Enthält von Ihnen erstellte Zielgruppen. Weitere Informationen finden Sie unter [Zielgruppen](targets.md) .

> [!NOTE] Wenn Sie Ihren Bericht nicht auf dieser Hilfeseite finden, kann es sein, dass Ihr Administrator Ordner umbenannt oder angepasst hat. See [Menu customizing](/help/admin/admin/customize-menus.md) in the Admin user guide.
