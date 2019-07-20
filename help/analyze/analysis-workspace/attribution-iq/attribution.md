---
description: 'null '
seo-description: 'null '
seo-title: Übersicht über das Zuordnungs-IQ
title: Übersicht über das Zuordnungs-IQ
uuid: bb 345642-4 f 45-4 fb 8-82 d 0-803248 dd 52 ea
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Übersicht über das Zuordnungs-IQ

>[!IMPORTANT]
>
>Zuordnungs-IQ ist für alle Kunden in Adobe Analytics Ultimate, Prime, Select und Foundation skus verfügbar.

## Geschäftswert von Attribution IQ {#section_E82B97114E1641A8AE911F57AEB3240A}

Die „Customer Journey“ ist nicht linear und lässt sich nur teilweise vorhersagen. Sie ist eher organisch, flexibel und oftmals nicht vorhersehbar. Jeder Kunde hat sein eigenes Tempo, kehrt oft zurück, steckt fest, nimmt Neustarts vor usw. Dadurch lässt es sich schwer nachvollziehen, wie sich Marketing-Maßnahmen auf die gesamte Customer Journey auswirken. Dies behindert auch das Bestreben, mehrere Datenkanäle miteinander zu verbinden, um auf Geschäftsfragen zu antworten, und führt zu unvollständigen Kundeneinblicken.

Mit Adobe Analytics Attribution IQ können moderne Datenerfassungsteams nachvollziehen, wie aussagekräftig die Interaktion in der gesamten Customer Journey ist, und auf intelligente Weise Wendepunkte identifizieren, mithilfe derer Kunden zu gewünschten Handlungen bewegt und somit die Marketinginitiativen effektiv optimiert werden können.

![](assets/attribution_iq_problem.png)

Adobe Analytics erweitert die Attribution und ermöglicht Ihnen Folgendes:

* Die Attribution über bezahlte Medien definieren: Dimensionen, Metriken, Kanäle oder Ereignisse können auf Modelle (z. B. die interne Suche) angewendet werden, nicht nur Marketing-Kampagnen.
* Den Vergleich für unbegrenzte Attributionsmodelle verwenden: Vergleichen Sie dynamisch so viele Modelle, wie Sie möchten.
* Implementierungsänderungen vermeiden: Mit der Berichtszeitverarbeitung und kontextabhängigen Sitzungen kann Customer Journey-Kontext erstellt und zur Laufzeit angewendet werden.
* Die Sitzung erstellen, die Ihrem Attributionsszenario am ehesten entspricht.
* Die Attribution nach Segmenten aufschlüsseln: Vergleichen Sie problemlos die Leistung Ihrer Marketingkanäle über ein beliebiges wichtiges Segment hinweg (z. B. Neu- mit Bestandskunden, Produkt X mit Produkt Y oder die Treueebene mit dem CLV).
* Die Analyse für die Kanalüberkreuzung und Mehrfachbearbeitung überprüfen: Verwenden Sie Mengendiagramme und Histogramme und erstellen Sie Trends anhand von Attributionsergebnissen.
* Wichtige Marketingsequenzen visuell analysieren: Erkunden Sie zur Konversion führende Pfade visuell mithilfe von mehrknotigen Fluss- und Fallout-Visualisierungen.
* Berechnete Metriken erstellen: Verwenden Sie eine beliebige Anzahl an Attributionszuordnungsmethoden.

## Wozu dient Attribution IQ? {#section_63B421E9E75B4CCEBA96726CAA37D73E}

Mit Attribution IQ in Analysis Workspace können Sie Freiformtabellen, Visualisierungen und berechneten Metriken viele neue Attributionsmodelltypen hinzufügen. Alle Attributionsmodelle weisen zwei Komponenten auf:

* Ein **Attributionsmodell** (d. h. „Erstkontakt“, „Letztkontakt“, „Linear“ usw.). Das Modell beschreibt die Verteilung der Konversionen zu den Hits in einer Gruppe.
* Ein **Attributions-Lookback-Fenster** (d. h. Besuch oder Besucher). Das Lookback-Fenster beschreibt, welche Gruppierungen der Hits für das jeweilige Modell beachtet wird.

Im folgenden Customer Journey-Beispiel werden die Marketing-Kontaktpunkte eines einzelnen Besuchers dargestellt, die drei Besuche, drei Konversionen und vier Marketingkanäle (Suche, Anzeige, Social und E-Mail) umfassen:

![](assets/attribution_example.png)

## Instanzbasierte Attribution {#section_A81DBC3B19014CE3894131F1CF72736F}

Die Attribution in Analysis Workspace verwendet die „Instanz“ einer beliebigen Dimension. Demzufolge werden die Attributionsmodelle auf die Werte angewendet, die in Analytics (nach Verarbeitungsregeln, VISTA und Verarbeitungsregeln für Marketingkanäle) weitergegeben wurden. Im Prinzip bedeutet dies, dass es für die Attributionsmodellierung keinen Unterschied zwischen einer Prop- oder eVar-Funktion (oder einer anderen Dimension) gibt. Prop-Funktionen können mit einem beliebigen der Lookback-Fenster oder Modelle, die sich unten befinden, als persistent festgelegt werden. Zudem werden die Zuordnungs- und Ablaufeinstellungen für eVar-Funktionen nicht verwendet (wie in den Administratoreinstellungen angegeben), wenn Attributions-Lookback-Fenster oder -Modelle angewendet werden.

## Attributions-Lookback-Fenster {#section_A2782BB64171431EB370CDCD4AD8030D}

Das Attributions-Lookback-Fenster ist eine Gruppierung der Hits, auf die das Attributionsmodell angewendet wird. In Analysis Workspace gibt es zwei Attributions-Lookback-Fenstereinstellungen: Besuch und Besucher.

**Besuchs-Lookback-Fenster**

Beim Besuchs-Lookback-Fenster handelt es sich um eine beliebige Sequenz an Aktivitäten, die standardmäßig nach 30 Minuten Inaktivität getrennt werden. [Kontextabhängige Sitzungen](https://marketing.adobe.com/resources/help/en_US/reference/vrs-mobile-visit-processing.html) werden jedoch auch über die [Berichtszeitverarbeitung](https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html) unterstützt, wenn Sie diese Standardeinstellung ändern möchten. Wenn Sie das Besuchs-Attributions-Lookback-Fenster in einer Virtual Report Suite (VRS) mit einer benutzerdefinierten Sitzung verwenden, verwendet das Attributions-Lookback-Fenster die benutzerdefinierte Besuchsdefinition als Grundlage der zugehörigen Berechnung. Im obigen Beispiel wird jeder Besuch als ein unabhängiger Attributions-Lookback erachtet.

**Besucher-Lookback-Fenster**

Das Besucher-Lookback-Fenster bezieht die Gesamtheit der Hits eines Besuchers im Berichtsfenster Ihres Arbeitsbereichs sowie die vollständigen Monate, die das Berichtsfenster umfassen, mit ein. Wenn der Berichtsfenster-Datumsbereich beispielsweise zwischen dem 15. September und dem 30. September liegt, ist der Besucher-Lookback-Datumsbereich zwischen dem 1. September und dem 30. September. Weitere Informationen in Bezug auf das Besucher-Lookback-Fenster finden Sie unter [Data appearing outside the reporting window](https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html) (Außerhalb des Berichtsfensters angezeigte Daten).

**Beispiel zum Attributions-Lookback-Fenster**

Wir wenden ein lineares Modell (teilt allen Kontaktpunkten ein gleiches Guthaben zu) auf unser obiges Beispiel an, um die Auswirkung von Attributions-Lookback-Fenstern zu veranschaulichen:

Bei Verwendung des **Besuchs-Attributions-Lookback-Fensters** wird die Konversion der einzelnen Besuche unabhängig verteilt:

* Die/$ 10 vom ersten Besuch würden gleichmäßig auf Search, Display, Social und E-Mail aufgeteilt, je nach Empfang/$ 2,50.
* Beim zweiten Besuch erhalten die Suchen und E-Mail jeweils eine Hälfte der/$ 5-Konvertierung, sodass E-Mail und Suche jeweils ein weiteres/$ 2,50 erhalten.
* Schließlich erhält E-Mail beim endgültigen Besuch alle Gutschriften für die/$ 2-Konvertierung.

Im **Besucher-Lookback-Fenster** werden alle Konversionen zusammen berücksichtigt, auch wenn die Berechnung etwas komplexer ist, da mehrere Konversionen vorliegen.

* Die erste/$ 10-Konversion würde gleichmäßig auf Search, Display, Social und E-Mail aufgeteilt.
* Die zweite/$ 5-Konversion würde dann auf die Kanäle in diesem Besuch sowie auf die vorherigen Kanäle aus dem vorherigen Besuch aufgeteilt: Search = (2/6) */$ 5 =/$ 1,67, Display = (1/6) */$ 5 =/$ 0.83, Social = (1/6) */$ 5 =/$ 0,83, Email = (2/6) */$ 5 =/$ 1,67.
* Schließlich würde die letzte Konversion auf alle Kanäle des Besuchers aufgeteilt werden: Search = (2/7) */$ 2 =/$ 0,57, Display = (1/7) */$ 2 =/$ 0,29, Social = (1/7) */$ 2 =/$ 0,29, Email = (3/7) */$ 2 =/$ 0,86.

Zusammenfassung der Ergebnisse in Tabellenform:

| Kanal | Umsatz (Linear/Besuch) | Umsatz (Linear/Besucher) |
|---|---|---|
| Durchsuchen | /$5.00 | /$4.74 |
| Anzeige | /$2.50 | /$3.62 |
| Social | /$2.50 | /$3.62 |
| E-Mail | /$7.00 | /$5.02 |
| Gesamt | /$17.00 | /$17.00 |

Dieser Unterschied im Attributions-Lookback-Fenster funktioniert bei allen im Folgenden beschriebenen Attributionsmodellen ähnlich.

## Attributionsmodelle {#section_4B9E7F83AE0B451A992397E55C3F5871}

Analysis Workspace unterstützt zehn unterschiedliche Attributionsmodelle: Erstkontakt, Letztkontakt, selber Kontakt, linear, U-förmig, J-Kurve, umgekehrtes J, Zeitverlauf, Beitrag und benutzerdefiniert. Details dazu finden Sie mit begleitenden Beispielen im Folgenden:

<table id="table_A3EB34CD52314F0393FF0D12E5F9779D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Benutzeroberflächensymbol </th> 
   <th colname="col2" class="entry"> Attributionsmodell </th> 
   <th colname="col3" class="entry"> Definition </th> 
   <th colname="col4" class="entry"> Verwendungsbereiche </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/last_touch.PNG" id="image_7D574182B1564109B0F1C3DD4FD9E8E9" /> </p> </td> 
   <td colname="col2"> <p>Letztkontakt </p> </td> 
   <td colname="col3"> <p>Das Modell „Letztkontakt“ billigt dem Kontaktpunkt 100 % zu, der unmittelbar vor der Konversion auftritt. Im obigen Fall erhält der E-Mail-Kanal das Guthaben für die gesamten 17 USD in einem Besuchs- oder Besucher-Lookback, da „E-Mail“ direkt vor allen drei Konversionen auftrat. </p> </td> 
   <td colname="col4"> <p>Dies ist das einfachste und gängigste Attributionsmodell. Es wird häufig für Konversionen mit einem kurzen Berücksichtigungszyklus verwendet. </p> <p>Letztkontakt wird häufig durch Teams verwendet, die das Suchmaschinenmarketing verwalten oder Schlüsselwörter für die interne Suche analysieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/first_touch.png" id="image_D8CD48CB39D64A0386CBA38397BB69B0" /> </p> </td> 
   <td colname="col2"> <p>Erstkontakt </p> </td> 
   <td colname="col3"> <p>Das Modell „Erstkontakt“ billigt dem Kontaktpunkt 100 % zu, der im Attributions-Lookback-Fenster zuerst auftritt. </p> <p>Im obigen Beispiel mit Besuchs-Lookback erhält der Kanal „Suche“ 10 USD + 5 USD = 15 USD und der Kanal „E-Mail“ 2 USD. Bei einem Besucher-Lookback erhält der Kanal „Suche“ die gesamten 17 USD, da er zuerst über alle Hits im Berichtsfenster hinweg erfolgt ist. </p> </td> 
   <td colname="col4"> <p>Dies ist ein weiteres allgemeines Attributionsmodell, das sich für die Analyse von Marketingkanälen eignet, die das Markenbewusstsein oder die Kundenakquise ankurbeln sollen. </p> <p>Erstkontakt wird häufig von Marketingteams vom Typ „Anzeige“ oder „Social“ verwendet, eignet sich jedoch auch großartig für das Bewerten der Produktempfehlungseffektivität vor Ort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/same_touch.png" id="image_7E093A65BA4048F0B46E1110D9569C84" /> </p> </td> 
   <td colname="col2"> <p>Selber Kontakt </p> </td> 
   <td colname="col3"> <p>Das Modell „Selber Kontakt“ billigt dem Hit 100 % zu, bei dem die Konversion auftrat. </p> <p>Im obigen Beispiel erfolgte jede Konversion in einem nachfolgenden Hit aus dem vorherigen Marketingkontaktpunkt. Daher werden die gesamten 17 USD dem Linienelement „Keine“ im Bericht zugeteilt. </p> </td> 
   <td colname="col4"> <p>Dies ist ein hilfreiches Modell beim Evaluieren des zum Zeitpunkt der Konversion angezeigten Inhalts oder Kundenerlebnisses. Produkt- oder Designteams verwenden dieses oftmals, um die Effektivität einer Seite zu bewerten, auf der die Konversion auftritt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/linear.png" id="image_FB96E57837EE47B5B6AE0066CC6DCF45" /> </p> </td> 
   <td colname="col2"> <p>Linear </p> </td> 
   <td colname="col3"> <p>Das Modell „Linear“ ist ein Mehrkontaktmodell, das jedem zu einer Konversion führenden Hit ein identisches Guthaben zuweist. </p> <p>In Szenarien, in denen mehrere Bestellungen im selben Besuchs- oder Besucher-Lookback erfolgen, erhalten alle vor der Konversion auftretenden Kanäle ein identisches Guthaben. </p> </td> 
   <td colname="col4"> <p>Dieses Modell eignet sich für Konversionen mit längeren Berücksichtigungszyklen oder Kundenerlebnissen, für die eine häufigere/konsistente Kundeninteraktion erforderlich ist. </p> <p>Die lineare Attribution wird oft von Teams genutzt, die die Benachrichtigungseffektivität mobiler Apps messen, oder mit abonnementbasierten Produkten verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/u_shaped.png" id="image_625BB199056D453E8DA8FA283A990DDD" /> </p> </td> 
   <td colname="col2"> <p>U-förmig </p> </td> 
   <td colname="col3"> <p>Das Modell „U-förmig“ weist der ersten und letzten Interaktion jeweils 40 % des Guthabens zu und teilt die verbleibenden 20 % unter den dazwischen befindlichen Interaktionen auf. </p> <p>In Attributions-Lookback mit nur einem Kontaktpunkt erhält der einzelne Kontaktpunkt 100 % des Guthabens. In Fällen mit nur zwei Kontaktpunkte erhalten sie jeweils 50 % des Guthabens. </p> </td> 
   <td colname="col4"> <p>Dieses Modell eignet sich großartig für Personen, welche die zuerst oder zuletzt (eingeführt oder geschlossen) in einer Konversion auftretenden Interaktionen einschätzen, die unterstützenden Interaktionen jedoch weiterhin anerkennen möchten. </p> <p>Die U-förmige Attribution wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden, jedoch Kanälen mehr Guthaben zuteilen möchten, die eine Konversion begründet oder abgeschlossen haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/j_shaped.png" id="image_D062FD7277A947BC9802F8BDFC139427" /> </p> </td> 
   <td colname="col2"> <p>J-förmig </p> </td> 
   <td colname="col3"> <p>Das Modell „J-förmig“ weist der letzten Interaktion 60 % und der ersten Interaktion 20 % des Guthabens zu und teilt die verbleibenden 20 % unter den dazwischen befindlichen Interaktionen auf. </p> <p>In Attributions-Lookbacks mit nur einem Kontaktpunkt erhält der einzelne Kontaktpunkt 100 % des Guthabens. In Fällen mit nur zwei Kontaktpunkten erhält der letzte Kontaktpunkt 75 % und der erste Kontaktpunkt 25 %. </p> </td> 
   <td colname="col4"> <p>Dieses Modell eignet sich analog zum U-förmigen Modell großartig für Personen, welche die zuerst oder zuletzt (eingeführt oder geschlossen) in einer Konversion auftretenden Interaktionen einschätzen, jedoch die bei der Konversion geschlossene Interaktion hervorheben möchten. </p> <p>Die J-förmige Attribution wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden und Kanälen mehr Guthaben zuteilen möchten, die eine Konversion abgeschlossen haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/inverse_j.png" id="image_20FFD4C9C9714901B3F54C049D129BC6" /> </p> </td> 
   <td colname="col2"> <p>Umgekehrtes J </p> </td> 
   <td colname="col3"> <p>Das Modell „Umgekehrtes J“ weist der ersten Interaktion 60 % und der letzten Interaktion 20 % des Guthabens zu und teilt die verbleibenden 20 % unter den dazwischen befindlichen Interaktionen auf. </p> <p>In Attributions-Lookbacks mit nur einem Kontaktpunkt erhält der einzelne Kontaktpunkt 100 % des Guthabens. In Fällen mit nur zwei Kontaktpunkten erhält der erste Kontaktpunkt 75 % und der letzte Kontaktpunkt 25 %. </p> </td> 
   <td colname="col4"> <p>Dieses Modell eignet sich analog zum U-förmigen Modell großartig für Personen, welche die zuerst oder zuletzt (eingeführt oder geschlossen) in einer Konversion auftretenden Interaktionen einschätzen, jedoch die Interaktion hervorheben möchten, welche die Konversion begründet hat. </p> <p>Die Attribution mit umgekehrtem J wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden und Kanälen, die eine Konversion initiiert haben, mehr Guthaben zuteilen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/custom.png" id="image_D46A787AC72248C7B28C402F5515B099" /> </p> </td> 
   <td colname="col2"> <p>Benutzerspezifisch </p> </td> 
   <td colname="col3"> <p>Das benutzerdefinierte Modell ist ein positionsbasiertes Modell, mit dem Sie die Gewichtungen angeben können, die Sie den ersten (starter), letzten (closer) und mittleren (player) Interaktionen geben möchten. </p> <p>Die angegebenen Werte werden auf 100 % normalisiert, selbst wenn die eingegebenen Zahlen zusammen nicht 100 ergeben. In Attributions-Lookbacks mit nur einem Kontaktpunkt erhält der einzelne Kontaktpunkt 100 % Guthaben. In Fällen mit nur zwei Kontaktpunkten wird zudem der Parameter „player“ ignoriert, wobei die ersten und letzten Interaktionen anhand der Modellparametergewichtungen „starter“ und „closer“ gewichtet und dabei auf 100 % normalisiert werden. </p> </td> 
   <td colname="col4"> <p>Wenn sich die von Adobe Analytics bereitgestellten Standardeinstellungen für Ihre Organisation nicht eignen, können Sie mithilfe eines benutzerdefinierten Modells die Gewichtungen angeben, die sich am besten für Ihre Organisation eignen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/time_decay.png" id="image_7976721B60454944BF516FCF8484D3A2" /> </p> </td> 
   <td colname="col2"> <p>Zeitverlauf </p> </td> 
   <td colname="col3"> <p>Das Modell „Zeitverlauf“ folgt einem exponentiellen Ausklang mit einem benutzerdefinierten „Half-Life“-Parameter (standardmäßig sieben Tage). </p> <p>Die Gewichtung der einzelnen Kanäle hängt von der zwischen dem Kontaktpunkt und der letztendlichen Konversion vergangenen Zeit ab und wird mit der Formel „2^(-t/halflife)“ ermittelt, wobei „t“ der Dauer zwischen einem Kontaktpunkt und einer Konversion entspricht. Bei Lookbacks mit einem einzelnen Kontaktpunkt erhält der eine Kontaktpunkt 100 % des Guthabens. Für Lookbacks mit zwei Kontaktpunkten verhält sich das Guthaben proportional zur Zeit von der Konversion. </p> </td> 
   <td colname="col4"> <p>Dies ist ein gutes Modell für Teams, die Promotions über eine vorab festgelegte Anzahl von Tagen betreiben und jüngst aufgetretene Kanäle hervorheben möchten. </p> <p>Die Attribution „Zeitverlauf“ wird oft von Videowerbung betreibenden Teams oder von Teams verwendet, die ihr Marketing um ein wichtiges Ereignis mit einem vorab festgelegten Datum (beispielsweise eine Konferenz oder ein Sportereignis) herum planen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><img  src="assets/participation.png" id="image_19DD3CA5C0F24F05835D8522C6708DE4" /> </p> </td> 
   <td colname="col2"> <p>Beitrag </p> </td> 
   <td colname="col3"> <p>„Beitrag“ teilt allen eindeutigen Kontaktpunkten oder Kanälen in einem Attributions-Lookback-Fenster 100 % des Guthabens zu. Mit „Beitrag“ wird die Gesamtanzahl der Konversionen in Ihrem Bericht im Vergleich zu anderen Attributionsmodellen vergrößert. Beachten Sie, dass „Beitrag“ Kanäle dedupliziert, die mehrere Male in einem einzelnen Attributions-Lookback-Fenster auftreten, bevor das Guthaben gewährt wird. </p> <p>Im obigen Beispiel erhalten „Suche“, „Anzeige“, „Social“ und „E-Mail“ bei Vorhandensein eines Besucher-Lookback-Fensters 17 USD. Im selben Beispiel mit einem Besuchs-Lookback-Fenster erhält „Suche“ 15 USD, „Anzeige“ 10 USD, „Social“ 10 USD und „E-Mail“ 17 USD. </p> </td> 
   <td colname="col4"> <p>Dieses Modell ist exzellent für die Analyse und Ermittlung geeignet, um nachzuvollziehen, wie oft Ihre Endbenutzer oder Kunden bestimmten Kanälen, Seiten oder Interaktionen zur Verfügung gestellt werden. </p> <p>Medienteams verwenden dieses Modell oftmals zum Berechnen der Content Velocity. Einzelhandelsorganisationen verwenden dieses Modell oftmals, um nachzuvollziehen, welche Teile ihrer App oder Website sich auf dem kritischen Pfad der Konversion befinden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Marketingkanäle und Verarbeitungsregeln für Marketingkanäle {#section_FCBF08A9D7C94B67B7AD76E8633E7916}

„Erstkontakt Kanal“ und „Letztkontakt Kanal“ sowie „Erstkontakt Kanaldetail“ und „Letztkontakt Kanaldetail“ können mit den neuen Attributionsmodellen verwendet werden. Sie sollten jedoch stattdessen zwei neue Dimensionen verwenden, um künftig für Ihre Teams Verwirrung zu verhindern: **Marketingkanäle** und **Marketingkanaldetail**. Sie agieren auf genau die gleiche Weise, übernehmen jedoch nicht die verwirrende Unterscheidung „Erstkontakt“ und „Letztkontakt“ im Namen. Wenn kein Attributionsmodell angewendet wird, führen „Marketingkanäle“ und „Marketingkanaldetail“ jeweils zu denselben Ergebnissen wie „Letztkontakt Kanal“ und „Letztkontakt Kanaldetail“.

Wenn die Attributionsmodelle auf „Erstkontakt Kanal“ oder „Letztkontakt Kanal“ angewendet werden, werden die Attributionseinstellungen durch das von Ihnen ausgewählte Attributionsmodell überschrieben. Auch wenn der Name der Dimension möglicherweise „Erstkontakt Kanal“ lautet, wird (beispielsweise) bei Auswahl des Modells „Linear“ in den Ergebnissen anstelle von „Erstkontakt“ die lineare Attribution berücksichtigt.

Da Marketingkanalvariablen von herkömmlichen Besuchen abhängen (wie durch die während des Datenerfassungsvorgangs angewendeten Verarbeitungsregeln für Marketingkanäle definiert), sind sie zudem für die Verwendung mit kontextabhängigen Sitzungen nicht berechtigt.

## Attribution für Classification-Aufschlüsselungen {#section_F9DE21758C4643879BE05EEAE9A34E5A}

Attributionsmodelle können auf beliebige Werte und deren Classification angewendet werden. Unter Bedingungen, in denen ein klassifizierter Wert durch den zugehörigen Schlüssel aufgeschlüsselt wird, enthält Analytics nur die dem bestimmten angegebenen Wert zugeordneten Schlüssel. Zum Beispiel wird bei einem linearen Attributionsmodell, das auf einen angegebenen eVar-Wert mit den Werten „Apfel“, „Banane“ und „Karotte“ angewendet ist, die für die Werte „Früchte“ und „Gemüse“ klassifiziert sind, wobei der Wert „Gemüse“ durch den eVar-Basiswert aufgeschlüsselt ist, nur „Karotte“ in der Aufschlüsselung angezeigt. Analog dazu zeigt der nach dem eVar-Basiswert aufgeschlüsselte Wert „Früchte“ nur „Apfel“ und „Banane“ in den Aufschlüsselungsergebnissen an, selbst wenn das Attributionsguthaben auf alle drei eVar-Basiswerte verteilt wurde.

Dieses Verhalten gilt auch für Berichte, in denen die Dimensionen „Marketingkanäle“ durch die Dimensionen „Marketingkanaldetails“ aufgeschlüsselt werden.

## Attribution für Aufschlüsselungen {#section_B2E87C768B6B4DBFA8EB7DB5E2DF881E}

Mit Analysis Workspace können Sie Werte durch andere Dimensionen aufschlüsseln und dieselben oder andere Attributionseinstellungen für die Aufschlüsselung angeben. Beispielsweise ist auf eine Kanaldimension eine lineare Attribution angewendet. Durch das Aufschlüsseln von Kanal nach Kampagne können Sie jedoch ein anderes Attributionsmodell auf Kampagnenebene angeben.

Dies ist hilfreich für Teams, die nur über ein Attributionsmodell auf Kanalebene (zur gleichmäßigen Aufteilung unter Kanälen) verfügen, jedoch einzelne Teams besitzen, die ein getrenntes Attributionsmodell für ihre einzelnen Kampagnen verwenden möchten und die Gesamtwerte für ihre Kampagnen benötigen, um abzugleichen, was auf Kanalebene zugeordnet wurde.

## „Keine“ in der Attribution {#section_BC71DA030E45487AA3C3F6ED247A3C4A}

Der Zeileneintrag „Keine“ ist ein Zeileneintrag, der alle aufgetretenen Konversionen erfasst, bei denen kein Wert für die Dimension vorhanden war. Der Zeileneintrag „Keine“ trat bisher nur in eVar-Berichten oder anderen Dimensionen auf, die Persistenz aufwiesen. Wenn Attributionsmodelle angewendet werden, kann es vorkommen, dass der Zeileneintrag „Keine“ angezeigt wird, wo er zuvor nicht vorhanden war. Dies ist normalerweise dann der Fall, wenn Attributionsmodelle auf prop-Funktionen angewendet werden, durch die der Zeileneintrag „Keine“ erzeugt wird.

## Attribution für mehrwertige Variablen

Einige Dimensionen in Analytics können mehrere Werte auf einem einzigen Treffer enthalten, zum Beispiel listVars, die Produktvariable, Listen-Prop oder Merchandising-eVars. Mit Analysis Workspace können Sie Attribution IQ auf jede dieser Arten von Variablen auf der Trefferebene anwenden. U-förmige Attribution (40/20/40) als Beispiel für einen einzelnen Besuch:

| Trefferzahl | Mehrwertige Variable | Konversionsereignis | Prozentuale Beteiligung für den Treffer (U-förmig) |
|--- |--- |---|---|
| 1 | A,B,C | - | 40 % |
| 2 | D | - | 20 % |
| 3 | E,F | 1 | 40 % |

In diesem Fall wurden A, B und C alle zur gleichen Zeit auf Treffer 1, D allein auf Treffer 2, E und F auf Treffer 3 eingestellt.

Attribution IQ gibt alle prozentuale Beteiligung für den Treffer zu allen beim Treffer vorhandenen Werten an. In unserem vorherigen Beispiel erhalten A, B und C alle 40 % bzw. 0,4 Konversionen, D 20 % bzw. 0,2 Konversionen, E und F jeweils 40 % der Konversionen bzw. 0,4. Ein Bericht mit U-förmiger Attribution zu den obigen Treffern würde folgendermaßen ausfallen:

| Mehrwertige Variable | Konversionen (U-geformt/Besuch) |
|--- |---|
| A | .4 |
| B | .4 |
| C | .4 |
| D | .2 |
| E | .4 |
| F | .4 |
| Gesamt | 1 |

>[!NOTE]
>Aufgrund der Zuordnung von Attributmodellen auf Trefferebene entspricht die Summe jedes Zeilenelements Ihres Berichts möglicherweise nicht dem Gesamtwert, da jeder Wert, der die prozentuale Gutschrift erhält, zu dem Treffer passt, in dem er enthalten war.