---
description: Die Zeitverarbeitung von Berichten ist eine Virtual Report Suite-Einstellung, die die Verarbeitung von Daten in zerstörungsfreien, retroaktiven Daten ermöglicht.
seo-description: Die Zeitverarbeitung von Berichten ist eine Virtual Report Suite-Einstellung, die die Verarbeitung von Daten in zerstörungsfreien, retroaktiven Daten ermöglicht.
seo-title: Berichtszeitverarbeitung
title: Berichtszeitverarbeitung
uuid: 1 a 1 d 82 ea -8 c 93-43 cc -8689-cdcf 59 c 309 b 1
translation-type: tm+mt
source-git-commit: 1e8d5af54ab22311e1c3967979c8bdc982a66d5b

---


# Berichtszeitverarbeitung

Die Zeitverarbeitung von Berichten ist eine Virtual Report Suite-Einstellung, die die Verarbeitung von Daten in zerstörungsfreien, retroaktiven Daten ermöglicht.

>[!NOTE]
>
>Die Berichtverarbeitung ist nur für Analysis Workspace verfügbar.

„Report Time Processing“ betrifft nur die Daten in der Virtual Report Suite und hat keinen Einfluss auf Daten oder Datensammlungen in der zugrunde liegenden Report Suite. Der Unterschied zwischen Report Time Processing und der herkömmlichen Analytics-Verarbeitung lässt sich mithilfe des folgenden Diagramms am besten nachvollziehen:

![](assets/google1.jpg)

Während der Datenverarbeitung in Analytics fließen die Daten durch die Datenerfassungspipeline und einen Vorverarbeitungsschritt, indem die Daten für die Berichterstellung vorbereitet werden. In diesem Schritt der Vorverarbeitung werden die Besuchsablauflogik und eVar-Persistenzlogik (unter anderem) auf die Daten angewendet, während sie erfasst werden. Der primäre Nachteil dieses Vorverarbeitungsmodells besteht darin, dass jegliche Konfiguration vorab erfolgen muss, noch bevor die Daten erfasst werden. Das heißt, dass die an den Vorverarbeitungseinstellungen vorgenommen Änderungen nur ab diesem Zeitpunkt und für neue Daten gelten. Dies ist problematisch, wenn defekte Daten eingehen oder wenn Einstellungen falsch konfiguriert wurden.

„Report Time Processing“ ist eine grundlegend andere Methode zur Verarbeitung von Analytics-Daten für die Berichterstellung. Anstatt vor dem Erfassen von Daten die Verarbeitungslogik vorab zu bestimmen, ignoriert Analytics die während des Vorverarbeitungsschritts festgelegten Daten und wendet diese Logik bei jeder Berichtsausführung an:

![](assets/google2.jpg)

Diese Verarbeitungsarchitektur ermöglicht weit flexiblere Berichterstellungsoptionen. Sie können beispielsweise die Timeout-Zeitspanne für Besuche auf nicht destruktive Art und Weise beliebig ändern. Diese Änderungen spiegeln sich retroaktiv in der eVar-Persistenz und den Segmentcontainern wider, als hätten Sie diese Einstellungen vor dem Erfassen der Daten angewendet. Zudem können Sie eine beliebige Anzahl von Virtual Report Suites mit jeweils unterschiedlichen Optionen zu Report Time Processing generieren, die auf derselben zugrunde liegenden Report Suite basieren, ohne Daten in der zugrunde liegenden Report Suite zu ändern.

„Report Time Processing“ ermöglicht zudem, dass Analytics verhindert, dass Hintergrundtreffer neue Besuche starten und dass das [mobile SDK](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) die Berichterstellung zum Starten eines neuen Besuchs anweist, sobald ein App-Startereignis ausgelöst wird.

Die folgenden Konfigurationsoptionen sind momentan für Virtual Report Suites mit aktiviertem Report Time Processing verfügbar:

<table id="table_C086C5FD10A84A1ABC081F5DE28F802D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Besuchstimeout </p> </td> 
   <td colname="col2"> <p> Die Einstellung des Besuchstimeouts definiert den Umfang der Inaktivität, der für einen Unique Visitor erforderlich ist, bevor automatisch ein neuer Besuch gestartet wird. Die Standardeinstellung lautet 30 Minuten. Wenn Sie beispielsweise das Besuchstimeout auf 15 Minuten festlegen, wird für jede Sequenz mit erfassten Treffern eine neue Besuchsgruppierung erstellt, die nach 15 Minuten Inaktivität separiert ist. Diese Einstellung beeinflusst nicht nur Ihre Besuchszahlen, sondern auch die Art und Weise der Evaluierung von Besuchssegmentcontainern und die Besuchsablauflogik für eVars, die bei einem Besuch ablaufen. Durch eine Verringerung des Besuchstimeouts erhöht sich wahrscheinlich die Gesamtzahl der Besuche in der Berichterstellung, während eine Erhöhung des Besuchstimeouts wahrscheinlich zu einer Reduzierung der Gesamtbesuche in der Berichterstellung führt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Einstellungen für Besuche mobiler Apps </p> </td> 
   <td colname="col2"> <p> Für Report Suites mit Daten, die von mobilen Apps über die <a href="https://www.adobe.io/apis/cloudplatform/mobile.html" format="html" scope="external">Adobe Mobile SDKs</a> generiert wurden, sind zusätzliche Besuchseinstellungen verfügbar. Diese Einstellungen sind nicht destruktiv und betreffen nur Treffer, die über die Mobile SDKs erfasst wurden. Sie haben keinen Einfluss auf Daten, die außerhalb der Mobile SDKs erfasst wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Starten neuer Besuche durch Hintergrundtreffer verhindern </p> </td> 
   <td colname="col2"> <p> Hintergrundtreffer werden von den Mobile SDKs erfasst, wenn sich die App in einem Hintergrundzustand befindet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Neuen Besuch bei allen App-Starts starten </p> </td> 
   <td colname="col2"> <p> Zusätzlich zum Besuchstimeout können Sie immer dann den Beginn eines Besuchs erzwingen, wenn von den Mobile SDKs ein App-Startereignis aufgezeichnet wurde. Das Inaktivitätsfenster ist dabei unerheblich. Diese Einstellung nimmt Einfluss auf die Besuchsmetrik und den Besuchssegmentcontainer sowie die Besuchsablauflogik für eVars. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beginn eines neuen Besuchs durch ein Ereignis </p> </td> 
   <td colname="col2"> <p>Eine neue Sitzung beginnt dann, wenn ein Ereignis ausgelöst wird – unabhängig davon, ob bei einer Sitzung eine Zeitüberschreitung auftrat oder nicht. Zur neuen Sitzung gehört auch das Ereignis, das sie ausgelöst hat. Zudem können Sie mehrere Ereignisse nutzen, um eine Sitzung zu starten, und eine neue Sitzung wird dann begonnen, wenn beliebige dieser Ereignisse in den Daten auftreten. Diese Einstellung wirkt sich auf Ihre Besuchszählung, den Besuchssegmentierungs-Container sowie die Besuchsablauflogik von eVars aus. </p> </td> 
  </tr> 
 </tbody> 
</table>

„Report Time Processing“ unterstützt nicht alle Metriken und Dimensionen, die in der herkömmlichen Analytics-Berichterstellung verfügbar sind. Virtual report suites utilizing Report Time Processing are only accessible in Analysis Workspace and will not be accessible in [!UICONTROL Reports &amp; Analytics], Ad Hoc Analysis, Data Warehouse, Report Builder, Data Feeds, or the reporting API.

Zudem werden bei „Report Time Processing“ nur Daten verarbeitet, die aus dem Datumsbereich der Berichterstellung stammen (nachfolgend als „Datumsfenster“ bezeichnet). Demnach bleiben auf „laufen nie ab“ festgelegte eVar-Werte für einen Besucher vor dem Datumsbereich der Berichterstellung in den Berichterstellungsfenstern nicht erhalten, und sie erscheinen nicht in Berichten. Das heißt auch, dass Kundenloyalitätsmessungen ausschließlich auf den im Berichterstellungsdatumsbereich vorhandenen Daten und nicht auf dem gesamten Verlauf vor dem Berichterstellungsdatumsbereich basieren.

Nachstehend finden Sie eine Liste der Metriken und Dimensionen, die bei Verwendung von „Report Time Processing“ momentan nicht unterstützt werden:

<table id="table_127AFE8FA1BE4F2BAB3975CA12A2FA47"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name der Metrik/Dimension </th> 
   <th colname="col2" class="entry"> Report Time Processing – Hinweise </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Analytics für Target </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Analytics für reservierte Metriken/Dimensionen der Advertising Cloud </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Einzelzugriff-Metrik </p> </td> 
   <td colname="col2"> <p> Derzeit und künftig nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Listen-Vars </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Zähler-eVars </p> </td> 
   <td colname="col2"> <p> Derzeit und künftig nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Marketingkanal-Variablen </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zu Tagen seit letztem Kauf </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Dimension nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zu Tagen bis Erstkauf </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Dimension nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zur Rückgabehäufigkeit </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Dimension nicht unterstützt. </p> <p> Ein alternativer Ansatz mithilfe einer Besuchsanzahlmetrik in einem Segment oder der Besuchsmetrik in einem Histogrammbericht kann verwendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zu Tagen seit letztem Besuch </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Dimension nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zur ursprünglichen Entrypage </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Dimension nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> eVars mit linearer Zuordnung </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimension zur ursprünglich verweisenden Domäne </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Besuchnummer </p> </td> 
   <td colname="col2"> <p> Aufgrund der Eigenschaften des Datumsfensters für die Funktion „Report Time Processing“ wird diese Metrik nicht unterstützt. </p> <p> Wenn Sie einen Bericht zur Anzahl neuer im Vergleich zu wiederkehrenden Besuchern in mobilen Apps erstellen möchten, können Sie eine berechnete Metrik einschließlich Besuchern/Besuchen in der Metrik „Anwendung installieren“ verwenden, um neue Besucher oder Besuche zu identifizieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Transaktions-ID-Data Sources </p> </td> 
   <td colname="col2"> <p> Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant. </p> </td> 
  </tr> 
 </tbody> 
</table>

Nachstehend finden Sie eine Liste mit Dimensionen und Metriken, die je nach den ausgewählten Einstellungen für „Report Time Processing“ betroffen sind:

<table id="table_491E48C55BC84917B4A8EACBF04C939F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name der Metrik/Dimension </th> 
   <th colname="col2" class="entry"> Report Time Processing – Hinweise </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Metrik für Unique Visitors </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, beinhalten Unique Visitors keine Besucher, für die im Datumsbereich der Berichterstellung nur Hintergrundtreffer vorlagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Besuche </p> </td> 
   <td colname="col2"> <p> Die Besuche spiegeln die konfigurierten Einstellungen der Virtual Report Suite wider, die sich von der zugrunde liegenden Report Suite unterscheiden können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Serialisierte Ereignisse mit Ereignis-IDs </p> </td> 
   <td colname="col2"> <p> Ereignisse, für die die Ereignis-Serialisierung mit einer Ereignis-ID verwendet wird, werden aufgrund des Datumsfensters für die Funktion „Report Time Processing“ nur für Ereignisse dedupliziert, die innerhalb des Datumsbereichs der Berichterstellung für einen Besucher auftreten (anstatt global für alle Termine oder Besucher). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Einkäufe/Umsatz/Bestellungen/Einheiten </p> </td> 
   <td colname="col2"> <p> Wenn die Einkaufs-ID verwendet wird, werden diese Metriken aufgrund des Datumsfensters für die Funktion „Report Time Processing“ nur für doppelte Einkaufs-IDs dedupliziert, die innerhalb des Datumsbereichs der Berichterstellung für einen Besucher auftreten (anstatt global für alle Termine oder Besucher). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Bounces/Bounce-Rate </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, werden Hintergrundtreffer, die nicht von einem Vordergrundtreffer gefolgt werden, als Bounce betrachtet, und sie tragen nicht zur Bounce-Rate bei. Weitere Details finden Sie unter <a href="../../components/vrs/vrs-mobile-visit-processing.md#concept_EC51308E4FD14E149F1B5D63C0AB34BD" format="dita" scope="local"> Kontextbezogene Sessionisierung</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Verbrachte Zeit in Sekunden pro Besuch </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, tragen nur Besuche mit Vordergrundtreffern zu dieser Metrik bei. Weitere Details finden Sie unter <a href="../../components/vrs/vrs-mobile-visit-processing.md#concept_EC51308E4FD14E149F1B5D63C0AB34BD" format="dita" scope="local"> Kontextbezogene Sessionisierung</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Verbrachte Zeit pro Besuch </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, tragen nur Besuche mit Vordergrundtreffern zu dieser Metrik bei. Weitere Details finden Sie unter <a href="../../components/vrs/vrs-mobile-visit-processing.md#concept_EC51308E4FD14E149F1B5D63C0AB34BD" format="dita" scope="local"> Kontextbezogene Sessionisierung</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Einträge </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, werden nur Einstiege für Besuche berücksichtigt, die einen Vordergrundtreffer enthalten. Weitere Details finden Sie unter <a href="../../components/vrs/vrs-mobile-visit-processing.md#concept_EC51308E4FD14E149F1B5D63C0AB34BD" format="dita" scope="local"> Kontextbezogene Sessionisierung</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Nicht-Merchandising-eVars/reservierte eVars </p> </td> 
   <td colname="col2"> <p> Die in einer eVar festgelegten Werte werden aufgrund des Datumsfensters für die Funktion „Report Time Processing“ nur dann beibehalten, wenn der Wert innerhalb des Datumsbereichs für die Berichterstellung festgelegt wurde. </p> <p> Zudem können zeitbasierte Abläufe eine Stunde zu früh oder zu spät ablaufen, wenn sich die Persistenz über eine Zeitumstellung erstreckt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Merchandising-eVars/reservierte eVars </p> </td> 
   <td colname="col2"> <p> Siehe oben. </p> <p> Zudem wird bezüglich der Konversionssyntax „Beliebige Treffer“ verwendet, wenn die Bindung auf „Beliebiges Ereignis“ festgelegt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ein- und Ausstiegsdimensionen </p> </td> 
   <td colname="col2"> <p> Wenn die Funktion „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, werden in dieser Dimension nur Ein- und Ausstiege für Besuche mit Vordergrundtreffern angezeigt. Weitere Details finden Sie unter <a href="../../components/vrs/vrs-mobile-visit-processing.md#concept_EC51308E4FD14E149F1B5D63C0AB34BD" format="dita" scope="local"> Kontextbezogene Sessionisierung</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Treffertyp </p> </td> 
   <td colname="col2"> <p> Diese Dimension gibt an, ob es sich bei einem Treffer um einen Vorder- oder Hintergrundtreffer handelt. </p> </td> 
  </tr> 
 </tbody> 
</table>

