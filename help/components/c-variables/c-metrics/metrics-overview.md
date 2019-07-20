---
description: Führt die Standardmetriken in Adobe Analytics auf.
seo-description: Führt die Standardmetriken in Adobe Analytics auf.
seo-title: Metrik Kurzreferenz
solution: Analytics
title: Kurzübersicht zu Metriken
topic: Metriken
uuid: 34160 c 96-7 cb 3-4 e 2 f -9956-9 ffa 9 d 9 a 359 e
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kurzübersicht zu Metriken

Führt die Standardmetriken in Adobe Analytics auf.

>[!NOTE]
>
>Any metric (event) not listed below is a [custom metric](../../../components/c-variables/c-metrics/metrics-custom.md#concept_F44638FC95A44B06AEBA3A6F9D008D27) (event).

<table id="table_CF4480B640BD4C81B4B32121FED5C96A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kennzahlname </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Durchschnittliche Klicktiefe </td> 
   <td colname="col2"> Zeigt an, wie tief (in Bezug auf die Seitenposition) jeder Wert während eines Besuchs durchschnittlich ausgelöst wurde. Diese Metrik gibt Aufschluss darüber, wie tief (in Bezug auf die Seitenposition) Ihre Zielgruppe während eines Besuchs eine bestimmte Seite oder einen Eigenschaftswert erreicht. „Durchschnittliche Klicktiefe“ ist für jede Variable verfügbar, für die die Pfadsetzung aktiviert ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Durchschnittliche Besuchszeit pro Seite </td> 
   <td colname="col2"> Stellt die durchschnittliche Zeit dar, die während eines Besuchs auf der Seite verbracht wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Durchschnittliche Besuchszeit pro Site </td> 
   <td colname="col2"> Stellt die durchschnittliche Zeit dar, die während eines Besuchs auf der Website verbracht wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Absprungrate </td> 
   <td colname="col2"> Zeigt den Prozentsatz der Besuche mit einem einzelnen Hit an. Die Absprungrate verwendet die Absprungmetrik und wird berechnet aus: Absprünge geteilt durch Einstiege. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Absprünge </td> 
   <td colname="col2"> Ein Besuch, der aus einem einzelnen Server-Aufruf besteht. Zum Beispiel handelt es sich bei einem einzelnen Seitenbesuch um einen Absprung, wenn ein Besucher keine Interaktion mit der Seite führt, bei der Daten zu Adobe gesendet werden, zum Beispiel durch Anklicken eines Links oder eines Videostarts. Wenn mehrere Hits bei einem Besuch empfangen werden, wird kein Absprung gezählt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Clickthrough-Rate für Kampagnen </td> 
   <td colname="col2"> Die Clickthrough-Rate stellt die Frequenz dar, mit der ein Trackingcode für eine bestimmte Kampagne an die Berichterstellung übergeben wurde. Wenn ein Besucher auf einen Partnerlink klickt, der mit einem dieser Trackingcodes gekennzeichnet ist, gelangt der Besucher auf Ihre Landingpage und der Trackingcode wird in s.campaign erfasst. Diese Daten werden an die Berichterstellung gesendet und es wird eine Clickthrough-Rate aufgezeichnet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zusatz zum Warenkorb </td> 
   <td colname="col2"> Die Frequenz, mit der einem Warenkorb ein Produkt hinzugefügt wurde. Dieser Wert stammt aus dem scAdd-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Öffnung des Warenkorbs </td> 
   <td colname="col2"> Die Frequenz, mit der ein Kunde durch Hinzufügen des ersten Produkts einen Warenkorb geöffnet hat. Erfolgt beim ersten Mal, wenn dem Warenkorb ein Produkt hinzugefügt wird. Dieser Wert stammt aus dem scOpen-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Entnahme aus Warenkorb </td> 
   <td colname="col2"> Die Anzahl der Entfernungsvorgänge eines Produkts aus dem Warenkorb. Dieser Wert stammt aus dem scRemove-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Warenkorb </td> 
   <td colname="col2"> Die Frequenz, mit der ein Warenkorb geöffnet oder initialisiert wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Warenkorbansicht </td> 
   <td colname="col2"> Die Frequenz, mit der die Inhalte des Warenkorbs vom Kunden angezeigt wurden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Checkouts </td> 
   <td colname="col2"> Ein Ereignis, das eintrifft, wenn Kunden für einen Kauf zum Checkout gehen. Der Gang zum Checkout erfolgt in der Regel unmittelbar bevor ein Kauf abgeschlossen wird und schließt grundsätzlich mit ein, dass der Kunde personenbezogene Informationen eingibt (wie zum Beispiel Versand- und Zahlungsinformationen). Sie haben die Kontrolle über die Ereignisse auf Ihrer Site, die als Checkouts gelten. Dieser Wert stammt aus dem scCheckout-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Clickthrough-Rate </td> 
   <td colname="col2">Die Clickthrough-Rate stellt die Frequenz dar, mit der ein Trackingcode für eine bestimmte Kampagne an die Berichterstellung übergeben wurde. When a visitor clicks on an affiliate link that has been tagged with one of these tracking codes, the visitor is taken to your landing page and the tracking code is captured in <span class="varname"> s.campaign</span>. Diese Daten werden an die Berichterstellung gesendet und es wird eine Clickthrough-Rate aufgezeichnet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kunde (neu, wiederkehrend, loyal) </td> 
   <td colname="col2">Kategorien des Kundenloyalitätsberichts: <p>Neuer Kunde: Kunde mit 0 Einkäufen. </p> <p>Rückkehrender Kunde: Kunde mit 1 Einkauf. </p> <p>Loyaler Kunde: Kunde mit mehr als 1 Einkauf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rückkehrende Besucher pro Tag </td> 
   <td colname="col2"> Gibt an, wie viele Besucher Ihre Website an einem bestimmten Tag mehrmals besuchen. Ein Tag wird als die letzten 24 Stunden definiert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einstiege </td> 
   <td colname="col2"> Einstiege geben an, wie oft ein Wert als erster Wert bei einem Besuch erfasst wird. Einstiege können nur einmal pro Besuch auftreten. Wenn die Variable nicht definiert ist, dann ist dies jedoch nicht zwingend der erste Hit. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ausstiege </td> 
   <td colname="col2"> Gibt an, wie oft ein Wert als letzter Wert bei einem Besuch erfasst wird. Ausstiege können nur einmal pro Besuch auftreten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Instanzen </td> 
   <td colname="col2"> Gibt an, wie oft ein Wert für eine Variable festgelegt wurde. Instanzen werden für alle Hit-Typen gezählt, außer wenn ein Wert für eine Variable bei einem nachfolgenden Hit aufgrund der Persistenz aufgezeichnet wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lebensdauer </td> 
   <td colname="col2"> Die Gesamtsumme einer bestimmten Erfolgsmetrik für einen einzelnen Benutzer, z. B. die Gesamtanzahl der Besuche auf Lebensdauer eines Benutzers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobilansichten </td> 
   <td colname="col2"> Gibt an, wie oft eine Seite angezeigt oder eine Dimension festgelegt wird, wenn der Zugriff über ein Mobilgerät stattfindet. Nur Ad-hoc-Analyse. Es wird empfohlen, anstelle der Metrik für Mobilansichten das Segment „Besuche von Mobilgeräten“ anzuwenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Neue Interaktionen </td> 
   <td colname="col2"> Neue Interaktionen sind eine Marketingkanal-Berichtsmetrik, die neue Besucher zählt, die aus einem Kanal stammen. Diese Metrik führt zudem Besucher auf, die Ihre Site in den letzten 30 Tagen nicht aufgerufen haben. Eine „Neue Interaktion“ ist eine eVar, die zu Beginn eines jeden Besuchs eingestellt wird (ursprüngliche Zuordnung). First Touch-Kanäle können auch neue Interaktionen sein (je nach Ablaufeinstellung der Besucher-Interaktion). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vorfälle </td> 
   <td colname="col2"> Die Frequenz, mit der ein bestimmter Wert erfasst wird, plus die Anzahl der Seitenansichten, für die dieser Wert weiter besteht. Das heißt, Vorfälle sind die Summe der Seitenansichten und der Seitenereignisse. Vorfälle sind nur in Ad Hoc Analysis verfügbar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestellungen </td> 
   <td colname="col2"> Die Anzahl der Bestellungen, die während des ausgewählten Zeitraums auf Ihrer Website erfolgt sind. Sie können die einzelnen Zeiträume nach anderen Metriken unterteilen, um Elemente (wie z. B. Produkte oder Kampagnen) anzuzeigen, die während des Zeitraums zu den meisten Bestellungen beitrugen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klicktiefe </td> 
   <td colname="col2"> Die durchschnittliche Anzahl an Klicks, die von Benutzern ausgeführt werden, um zu einer bestimmten Seite auf der Website zu gelangen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Seitenereignisse </td> 
   <td colname="col2"> Seitenereignisse umfassen Bildanforderungsdaten aus nicht standardmäßigen Bildanforderungen. Quellen für nicht standardmäßige Bildanforderungen sind Downloadlinks, Exitlinks und Linktracking benutzerspezifischer Links. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Seitenansichten </td> 
   <td colname="col2"> Eine Seitenansicht wird für jeden versandten Server-Aufruf gezählt. Diese Metrik repräsentiert die Gesamtinstanzen von Seitenansichten. TrackLink-Aufrufe werden nicht als Seitenansichten gezählt und erhöhen nicht die Seitenansichten-Metrik. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pfadansichten </td> 
   <td colname="col2"> <p>Den Pfadansichtsmetriken liegen Pfaddaten zugrunde, die für alle Benutzer verfolgt werden, die persistente Cookies akzeptieren. </p> <p>Der Begriff Pfadansichten wird unter Berücksichtigung der angegebenen Pfadbeschränkung verwendet, um anzugeben, wie oft eine Seite angezeigt wurde. Diese Metrik erstattet Bericht über die Anzahl der Seitenansichten für die gegebene Seite, die innerhalb des ausgewählten Pfads auftraten. Diese Metrik ist im Pfadbericht verfügbar. Pfadansichten zeigen, wie häufig eine bestimmte Folge von Seiten angezeigt wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Produktansichten </td> 
   <td colname="col2"> Instanz der festgelegten Produktansicht. Tritt auf, wenn die Produktdetailseite angezeigt wird. Dieser Wert stammt aus dem prodView-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Neuladungen </td> 
   <td colname="col2"> Wird gezählt, wenn derselbe Seitenname zweimal hintereinander geladen wird. Hierdurch wird in der Regel angezeigt, dass die Seite aktualisiert wurde. Beachten Sie, dass der zweifache Besuch derselben Seite bei demselben Besuch nur als Neuladung gezählt wird, wenn beide Besuche nacheinander stattfinden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rückkehrende Besucher </td> 
   <td colname="col2"> Zeigt die Anzahl der Besuche an, wobei die Besuchnummer größer als 1 ist. Bei rückkehrenden Besuchern werden Besucher ohne Cookies berücksichtigt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Umsatz </td> 
   <td colname="col2"> Der Umsatz wird bei einem Einkaufsereignis erfasst und ist als Gesamtdollarbetrag für die Summe der Bestellung der einzelnen Produkte definiert. Dieser Wert stammt aus dem purchase-Ereignis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Suchvorgänge </td> 
   <td colname="col2"> <p>Suchvorgänge sind keine Standardmetrik. Es handelt sich dabei immer um eine angepasste Metrik. </p> <p>Es handelt sich dabei um die empfohlene Standardmetrik für Suchmaschinen und Keywords. Die Metrik stellt Instanzen von Clickthroughs dar und zeigt die Seite, die in Verbindung mit einer bestimmten Suchmaschine oder einem bestimmten Keyword steht. Suchmetrikdaten können rückwirkend bis zu Beginn des Datensatzes gemeldet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einzelzugriff </td> 
   <td colname="col2"> Der Einzelzugriff definiert sich aus der Anzahl der Besuche auf Ihrer Website, die einen einzelnen, eindeutigen Seitennamenwert enthielten. Wenn ein Benutzer Ihre Website aufruft und auf einen verfolgten Link klickt, ein Ereignis auslöst (z. B. durch den Start eines Videos) oder die Seite neu lädt, wird der Besuch weiterhin als Einzelzugriffsbesuch gewertet. Solange sich der Wert für die Variable „pageName“ nicht ändert, kann eine beliebige Anzahl an Anfragen gesendet werden, und der Besuch wird dennoch als Einzelzugriff gewertet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchszeit </td> 
   <td colname="col2"> Metriken, die die Verweilzeit von Besuchern auf einer Seite, Site oder pro Besuch melden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gesamt </td> 
   <td colname="col2"> Die Metrik insgesamt, der Wert aller Berichtszeileneinträge aus einem Berichtszeitraum. Wenn ein Filter aktuell ausgewählt ist, entspricht der Gesamtwert dem gefilterten Gesamtwert anstatt dem Report Suite-Gesamtwert. Wenn kein Filter ausgewählt ist, entspricht der Gesamtwert dem Report Suite-Gesamtwert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Unique Customer </td> 
   <td colname="col2"> <p>(stündlich, täglich, wöchentlich, monatlich, vierteljährlich, jährlich) </p> <p>Ein Unique Customer wird für den entsprechenden Zeitraum nur einmal gezählt. Eine wiederholte Zählung ist nicht möglich, ganz gleich, wie oft der Besucher zurückkehrt und etwas kauft. Ein Unique Visitor wird in einem bestimmten Zeitraum einmal beim ersten Besuch und bis zum Ablauf des Zeitraums nicht wieder gezählt. Nach Ablauf des Zeitraums wird der Unique Visitor erneut erfasst. Unique Customers werden immer als Unique Visitor gezählt, da sie zum Einkauf die Site aufsuchen müssen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Unique Visitors </td> 
   <td colname="col2"> Zeigt die Gesamtanzahl aller Unique Visitors für den Berichterstellungszeitraum an (kann konfiguriert werden für täglich, wöchentlich, monatlich, vierteljährlich, jährlich). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einheiten </td> 
   <td colname="col2"> Die Gesamteinheiten, die während des ausgewählten Zeitraums bestellt wurden. Da Sie viele Einheiten bestellt und erworben haben, ist „Einheiten“ eine wichtige Metrik, die die allgemeine Bestandsbewegung beschreibt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besucher </td> 
   <td colname="col2"> Die Anzahl auf Unique Visitors Ihrer Site innerhalb einer bestimmten Zeiteinheit wie Stunde, Tag, Woche, Monat, Quartal oder Jahr. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche </td> 
   <td colname="col2"> <p>Eine Folge von Seitenansichten während einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen. </p> <p>Die Besuchsmetrik wird immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn ein Besucher zu Ihrer Site zurückkehrt. </p> </td> 
  </tr> 
 </tbody> 
</table>

