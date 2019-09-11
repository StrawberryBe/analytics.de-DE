---
description: Führt die Standardmetriken in Adobe Analytics auf.
seo-description: Führt die Standardmetriken in Adobe Analytics auf.
seo-title: Kurzübersicht über Metriken
solution: Analytics
title: Kurzübersicht über Metriken
topic: Metriken
uuid: 34160 c 96-7 cb 3-4 e 2 f -9956-9 ffa 9 d 9 a 359 e
translation-type: tm+mt
source-git-commit: d865bfed39fdae16f9e18335f8f44978bf3958ad

---


# Kurzübersicht über Metriken

Führt die Standardmetriken in Adobe Analytics auf.

>[!NOTE]
>
>Eine Metrik (Ereignis), die unten nicht aufgeführt ist, ist eine [benutzerdefinierte Metrik](../../../components/c-variables/c-metrics/metrics-custom.md#concept_F44638FC95A44B06AEBA3A6F9D008D27) (benutzerdefiniertes Ereignis).

| Kennzahlname | Beschreibung | Typ |
|--- |--- |---|
| Durchschnittl. Seitentiefe | Zeigt an, wie tief (in Bezug auf die Seitenposition) jeder Wert während eines Besuchs durchschnittlich ausgelöst wurde. Diese Metrik gibt Aufschluss darüber, wie tief (in Bezug auf die Seitenposition) Ihre Zielgruppe während eines Besuchs eine bestimmte Seite oder einen Eigenschaftswert erreicht. „Durchschnittliche Klicktiefe“ ist für jede Variable verfügbar, für die die Pfadsetzung aktiviert ist. | Traffic |
| Durchschnittliche Besuchszeit pro Seite | Stellt die durchschnittliche Zeit dar, die während eines Besuchs auf der Seite verbracht wurde. | Traffic |
| Durchschnittliche Besuchszeit pro Site | Stellt die durchschnittliche Zeit dar, die während eines Besuchs auf der Website verbracht wurde. | Traffic |
| Absprungrate | Zeigt den Prozentsatz der Besuche mit einem einzelnen Hit an. Die Absprungrate verwendet die Absprungmetrik und wird berechnet aus: Absprünge geteilt durch Einstiege. | Traffic |
| Absprünge | Ein Besuch, der aus einem einzelnen Server-Aufruf besteht. Zum Beispiel handelt es sich bei einem einzelnen Seitenbesuch um einen Absprung, wenn ein Besucher keine Interaktion mit der Seite führt, bei der Daten zu Adobe gesendet werden, zum Beispiel durch Anklicken eines Links oder eines Videostarts. Wenn mehrere Hits bei einem Besuch empfangen werden, wird kein Absprung gezählt. | Traffic |
| Clickthrough-Rate für Kampagnen | Die Clickthrough-Rate stellt die Frequenz dar, mit der ein Trackingcode für eine bestimmte Kampagne an die Berichterstellung übergeben wurde. Wenn ein Besucher auf einen Partnerlink klickt, der mit einem dieser Trackingcodes gekennzeichnet ist, gelangt der Besucher auf Ihre Landingpage und der Trackingcode wird in s.campaign erfasst. Diese Daten werden an die Berichterstellung gesendet und es wird eine Clickthrough-Rate aufgezeichnet. | Konversion |
| Zusatz zum Warenkorb | Die Frequenz, mit der einem Warenkorb ein Produkt hinzugefügt wurde. Dieser Wert stammt aus dem scAdd-Ereignis. | Konversion |
| Öffnung des Warenkorbs | Die Frequenz, mit der ein Kunde durch Hinzufügen des ersten Produkts einen Warenkorb geöffnet hat. Erfolgt beim ersten Mal, wenn dem Warenkorb ein Produkt hinzugefügt wird. Dieser Wert stammt aus dem scOpen-Ereignis. | Konversion |
| Entnahme aus Warenkorb | Die Anzahl der Entfernungsvorgänge eines Produkts aus dem Warenkorb. Dieser Wert stammt aus dem scRemove-Ereignis. | Konversion |
| Warenkorb | Die Frequenz, mit der ein Warenkorb geöffnet oder initialisiert wurde. | Konversion |
| Warenkorbansicht | Die Frequenz, mit der die Inhalte des Warenkorbs vom Kunden angezeigt wurden. | Konversion |
| Checkouts | Ein Ereignis, das eintrifft, wenn Kunden für einen Kauf zum Checkout gehen. Der Gang zum Checkout erfolgt in der Regel unmittelbar bevor ein Kauf abgeschlossen wird und schließt grundsätzlich mit ein, dass der Kunde personenbezogene Informationen eingibt (wie zum Beispiel Versand- und Zahlungsinformationen). Sie haben die Kontrolle über die Ereignisse auf Ihrer Site, die als Checkouts gelten. Dieser Wert stammt aus dem scCheckout-Ereignis. | Konversion |
| Clickthrough-Rate | Die Clickthrough-Rate stellt die Frequenz dar, mit der ein Trackingcode für eine bestimmte Kampagne an die Berichterstellung übergeben wurde. Wenn ein Besucher auf einen Partnerlink klickt, der mit einem dieser Trackingcodes gekennzeichnet ist, gelangt der Besucher auf Ihre Landingpage und der Trackingcode wird in s.campaign erfasst. Diese Daten werden an die Berichterstellung gesendet und es wird eine Clickthrough-Rate aufgezeichnet. | Konversion |
| Kunde (neu, wiederkehrend, loyal) | Kategorien des Kundenloyalitätsberichts: Neuer Kunde: Kunde mit 0 Einkäufen.  Rückkehrender Kunde: Kunde mit 1 Einkauf.  Loyaler Kunde: Kunde mit mehr als 1 Einkauf. | Traffic |
| Rückkehrende Besucher pro Tag | Gibt an, wie viele Besucher Ihre Website an einem bestimmten Tag mehrmals besuchen. Ein Tag wird als die letzten 24 Stunden definiert. | Traffic |
| Einträge | Einstiege geben an, wie oft ein Wert als erster Wert bei einem Besuch erfasst wird. Einstiege können nur einmal pro Besuch auftreten. Wenn die Variable nicht definiert ist, dann ist dies jedoch nicht zwingend der erste Hit. | Traffic |
| Ausstiege | Gibt an, wie oft ein Wert als letzter Wert bei einem Besuch erfasst wird. Ausstiege können nur einmal pro Besuch auftreten. | Traffic |
| Instanzen | Gibt an, wie oft ein Wert für eine Variable festgelegt wurde. Instanzen werden für alle Hit-Typen gezählt, außer wenn ein Wert für eine Variable bei einem nachfolgenden Hit aufgrund der Persistenz aufgezeichnet wird. | Traffic |
| Mobilansichten | Gibt an, wie oft eine Seite angezeigt oder eine Dimension festgelegt wird, wenn der Zugriff über ein Mobilgerät stattfindet. Nur Ad-hoc-Analyse. Es wird empfohlen, anstelle der Metrik für Mobilansichten das Segment „Besuche von Mobilgeräten“ anzuwenden. | Konversion |
| Neue Interaktionen | Neue Interaktionen sind eine Marketingkanal-Berichtsmetrik, die neue Besucher zählt, die aus einem Kanal stammen. Diese Metrik führt zudem Besucher auf, die Ihre Site in den letzten 30 Tagen nicht aufgerufen haben. Eine „Neue Interaktion“ ist eine eVar, die zu Beginn eines jeden Besuchs eingestellt wird (ursprüngliche Zuordnung). First Touch-Kanäle können auch neue Interaktionen sein (je nach Ablaufeinstellung der Besucher-Interaktion). | Konversion |
| Vorfälle | Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorfälle sind nur in Ad Hoc Analysis verfügbar. | Traffic |
| Bestellungen | Die Anzahl der Bestellungen, die während des ausgewählten Zeitraums auf Ihrer Website erfolgt sind. Sie können die einzelnen Zeiträume nach anderen Metriken unterteilen, um Elemente (wie z. B. Produkte oder Kampagnen) anzuzeigen, die während des Zeitraums zu den meisten Bestellungen beitrugen. | Konversion |
| Klicktiefe | Die durchschnittliche Anzahl an Klicks, die von Benutzern ausgeführt werden, um zu einer bestimmten Seite auf der Website zu gelangen. | Traffic |
| Seitenereignisse | Seitenereignisse umfassen Bildanforderungsdaten aus nicht standardmäßigen Bildanforderungen. Quellen für nicht standardmäßige Bildanforderungen sind Downloadlinks, Exitlinks und Linktracking benutzerspezifischer Links. | Traffic |
| Seitenansichten | Eine Seitenansicht wird für jeden versandten Server-Aufruf gezählt. Diese Metrik repräsentiert die Gesamtinstanzen von Seitenansichten. TrackLink-Aufrufe werden nicht als Seitenansichten gezählt und erhöhen nicht die Seitenansichten-Metrik. | Konversion |
| Pfadansichten | Den Pfadansichtsmetriken liegen Pfaddaten zugrunde, die für alle Benutzer verfolgt werden, die persistente Cookies akzeptieren.  Der Begriff Pfadansichten wird unter Berücksichtigung der angegebenen Pfadbeschränkung verwendet, um anzugeben, wie oft eine Seite angezeigt wurde. Diese Metrik erstattet Bericht über die Anzahl der Seitenansichten für die gegebene Seite, die innerhalb des ausgewählten Pfads auftraten. Diese Metrik ist im Pfadbericht verfügbar. Pfadansichten zeigen, wie häufig eine bestimmte Folge von Seiten angezeigt wurde. | Traffic |
| Produktansichten | Instanz der festgelegten Produktansicht. Tritt auf, wenn die Produktdetailseite angezeigt wird. Dieser Wert stammt aus dem prodView-Ereignis. | Konversion |
| Neuladungen | Wird gezählt, wenn derselbe Seitenname zweimal hintereinander geladen wird. Hierdurch wird in der Regel angezeigt, dass die Seite aktualisiert wurde. Beachten Sie, dass der zweifache Besuch derselben Seite bei demselben Besuch nur als Neuladung gezählt wird, wenn beide Besuche nacheinander stattfinden. | Traffic |
| Rückkehrende Besucher | Zeigt die Anzahl der Besuche an, wobei die Besuchnummer größer als 1 ist. Bei rückkehrenden Besuchern werden Besucher ohne Cookies berücksichtigt. | Konversion |
| Umsatz | Der Umsatz wird bei einem Einkaufsereignis erfasst und ist als Gesamtdollarbetrag für die Summe der Bestellung der einzelnen Produkte definiert. Dieser Wert stammt aus dem purchase-Ereignis. | Konversion |
| Suchvorgänge | Suchvorgänge sind keine Standardmetrik. Es handelt sich dabei immer um eine angepasste Metrik.  Es handelt sich dabei um die empfohlene Standardmetrik für Suchmaschinen und Keywords. Die Metrik stellt Instanzen von Clickthroughs dar und zeigt die Seite, die in Verbindung mit einer bestimmten Suchmaschine oder einem bestimmten Keyword steht. Suchmetrikdaten können rückwirkend bis zu Beginn des Datensatzes gemeldet werden. | Konversion |
| Einzelzugriff | Der Einzelzugriff definiert sich aus der Anzahl der Besuche auf Ihrer Website, die einen einzelnen, eindeutigen Seitennamenwert enthielten. Wenn ein Benutzer Ihre Website aufruft und auf einen verfolgten Link klickt, ein Ereignis auslöst (z. B. durch den Start eines Videos) oder die Seite neu lädt, wird der Besuch weiterhin als Einzelzugriffsbesuch gewertet. Solange sich der Wert für die Variable „pageName“ nicht ändert, kann eine beliebige Anzahl an Anfragen gesendet werden, und der Besuch wird dennoch als Einzelzugriff gewertet. | Traffic |
| Besuchszeit | Metriken, die die Verweilzeit von Besuchern auf einer Seite, Site oder pro Besuch melden. | Traffic |
| Gesamt | Die Metrik insgesamt, der Wert aller Berichtszeileneinträge aus einem Berichtszeitraum. Wenn ein Filter aktuell ausgewählt ist, entspricht der Gesamtwert dem gefilterten Gesamtwert anstatt dem Report Suite-Gesamtwert. Wenn kein Filter ausgewählt ist, entspricht der Gesamtwert dem Report Suite-Gesamtwert. | ? |
| Unique Customer | (stündlich, täglich, wöchentlich, monatlich, vierteljährlich, jährlich)  Ein Unique Customer wird für den entsprechenden Zeitraum nur einmal gezählt. Eine wiederholte Zählung ist nicht möglich, ganz gleich, wie oft der Besucher zurückkehrt und etwas kauft. Ein Unique Visitor wird in einem bestimmten Zeitraum einmal beim ersten Besuch und bis zum Ablauf des Zeitraums nicht wieder gezählt. Nach Ablauf des Zeitraums wird der Unique Visitor erneut erfasst. Unique Customers werden immer als Unique Visitor gezählt, da sie zum Einkauf die Site aufsuchen müssen. | Konversion |
| Unique Visitors | Zeigt die Gesamtanzahl aller Unique Visitors für den Berichterstellungszeitraum an (kann konfiguriert werden für täglich, wöchentlich, monatlich, vierteljährlich, jährlich). | Konversion |
| Einheiten | Die Gesamteinheiten, die während des ausgewählten Zeitraums bestellt wurden. Da Sie viele Einheiten bestellt und erworben haben, ist „Einheiten“ eine wichtige Metrik, die die allgemeine Bestandsbewegung beschreibt. | Konversion |
| Besucher | Die Anzahl auf Unique Visitors Ihrer Site innerhalb einer bestimmten Zeiteinheit wie Stunde, Tag, Woche, Monat, Quartal oder Jahr. | Konversion |
| Besuche | Eine Folge von Seitenansichten während einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen.  Die Besuchsmetrik wird immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn ein Besucher zu Ihrer Site zurückkehrt. | Konversion |

