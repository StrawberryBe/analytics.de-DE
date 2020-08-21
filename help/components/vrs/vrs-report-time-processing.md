---
description: „Berichtszeitverarbeitung“ ist eine virtuelle Report Suite-Einstellung zur zerstörungsfreien, rückwirkenden Verarbeitung von Daten.
title: Berichtszeitverarbeitung
uuid: 1a1d82ea-8c93-43cc-8689-cdcf59c309b1
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '1426'
ht-degree: 100%

---


# Berichtszeitverarbeitung

„Berichtszeitverarbeitung“ ist eine virtuelle Report Suite-Einstellung zur zerstörungsfreien, rückwirkenden Verarbeitung von Daten.

>[!NOTE]
>
>Die Berichtszeitverarbeitung ist nur für Analysis Workspace verfügbar.

„Berichtszeitverarbeitung“ betrifft nur die Daten in der Virtual Report Suite und hat keinen Einfluss auf Daten oder Datensammlungen in der zugrunde liegenden Report Suite. Der Unterschied zwischen Berichtszeitverarbeitung und der herkömmlichen Analytics-Verarbeitung lässt sich mithilfe des folgenden Diagramms am besten nachvollziehen:

![Google1](assets/google1.jpg)

Während der Datenverarbeitung in Analytics fließen die Daten durch die Datenerfassungspipeline und einen Vorverarbeitungsschritt, indem die Daten für die Berichterstellung vorbereitet werden. In diesem Schritt der Vorverarbeitung werden die Besuchsablauflogik und eVar-Persistenzlogik (unter anderem) auf die Daten angewendet, während sie erfasst werden. Der primäre Nachteil dieses Vorverarbeitungsmodells besteht darin, dass jegliche Konfiguration vorab erfolgen muss, noch bevor die Daten erfasst werden. Das heißt, dass die an den Vorverarbeitungseinstellungen vorgenommen Änderungen nur ab diesem Zeitpunkt und für neue Daten gelten. Dies ist problematisch, wenn defekte Daten eingehen oder wenn Einstellungen falsch konfiguriert wurden.

„Berichtszeitverarbeitung“ ist eine grundlegend andere Methode zur Verarbeitung von Analytics-Daten für die Berichterstellung. Anstatt vor dem Erfassen von Daten die Verarbeitungslogik vorab zu bestimmen, ignoriert Analytics die während des Vorverarbeitungsschritts festgelegten Daten und wendet diese Logik bei jeder Berichtsausführung an:

![Google2](assets/google2.jpg)

Diese Verarbeitungsarchitektur ermöglicht weit flexiblere Berichterstellungsoptionen. Sie können beispielsweise die Timeout-Zeitspanne für Besuche auf nicht destruktive Art und Weise beliebig ändern. Diese Änderungen spiegeln sich retroaktiv in der eVar-Persistenz und den Segmentcontainern wider, als hätten Sie diese Einstellungen vor dem Erfassen der Daten angewendet. Zudem können Sie eine beliebige Anzahl von Virtual Report Suites mit jeweils unterschiedlichen Optionen zu Berichtszeitverarbeitung generieren, die auf derselben zugrunde liegenden Report Suite basieren, ohne Daten in der zugrunde liegenden Report Suite zu ändern.

„Berichtszeitverarbeitung“ ermöglicht zudem, dass Analytics verhindert, dass Hintergrundtreffer neue Besuche starten und dass das [mobile SDK](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) die Berichterstellung zum Starten eines neuen Besuchs anweist, sobald ein App-Startereignis ausgelöst wird.

Die folgenden Konfigurationsoptionen sind momentan für Virtual Report Suites mit aktiviertem Berichtszeitverarbeitung verfügbar:

* **Besuchstimeout:** Die Einstellung des Besuchstimeouts definiert den Umfang der Inaktivität, der für einen Unique Visitor erforderlich ist, bevor automatisch ein neuer Besuch gestartet wird. Die Standardeinstellung lautet 30 Minuten. Wenn Sie beispielsweise das Besuchstimeout auf 15 Minuten festlegen, wird für jede Sequenz mit erfassten Treffern eine neue Besuchsgruppierung erstellt, die nach 15 Minuten Inaktivität separiert ist. Diese Einstellung beeinflusst nicht nur Ihre Besuchszahlen, sondern auch die Art und Weise der Evaluierung von Besuchssegmentcontainern und die Besuchsablauflogik für eVars, die bei einem Besuch ablaufen. Durch eine Verringerung des Besuchstimeouts erhöht sich wahrscheinlich die Gesamtzahl der Besuche in der Berichterstellung, während eine Erhöhung des Besuchstimeouts wahrscheinlich zu einer Reduzierung der Gesamtbesuche in der Berichterstellung führt.
* **Besuchseinstellungen für Mobile Apps:** Für Report Suites mit Daten, die von Mobile Apps über die [Adobe Mobile SDKs](https://www.adobe.io/apis/cloudplatform/mobile.html) generiert wurden, sind zusätzliche Besuchseinstellungen verfügbar. Diese Einstellungen sind nicht destruktiv und betreffen nur Treffer, die über die Mobile SDKs erfasst wurden. Sie haben keinen Einfluss auf Daten, die außerhalb der Mobile SDKs erfasst wurden.
* **Starten neuer Besuche durch Hintergrundtreffer verhindern:** Hintergrundtreffer werden von den Mobile SDKs erfasst, wenn die App im Hintergrund ausgeführt wird.
* **Starten neuer Besuche bei allen App-Starts:** Zusätzlich zum Besuchstimeout können Sie immer dann den Beginn eines Besuchs erzwingen, wenn von den Mobile SDKs ein App-Startereignis aufgezeichnet wurde. Das Inaktivitätsfenster ist dabei unerheblich. Diese Einstellung nimmt Einfluss auf die Besuchsmetrik und den Besuchssegmentcontainer sowie die Besuchsablauflogik für eVars.
* **Starten neuer Besuche mit Ereignis:** Eine neue Sitzung beginnt dann, wenn ein Ereignis ausgelöst wird – unabhängig davon, ob bei einer Sitzung eine Zeitüberschreitung auftrat oder nicht. Zur neuen Sitzung gehört auch das Ereignis, das sie ausgelöst hat. Zudem können Sie mehrere Ereignisse nutzen, um eine Sitzung zu starten, und eine neue Sitzung wird dann begonnen, wenn beliebige dieser Ereignisse in den Daten auftreten. Diese Einstellung wirkt sich auf Ihre Besuchszählung, den Besuchssegmentierungs-Container sowie die Besuchsablauflogik von eVars aus.

„Berichtszeitverarbeitung“ unterstützt nicht alle Metriken und Dimensionen, die in der herkömmlichen Analytics-Berichterstellung verfügbar sind. Virtual Report Suites mit Berichtszeitverarbeitung sind nur in Analysis Workspace zugänglich, während der Zugriff über [!UICONTROL Reports &amp; Analytics], Ad Hoc Analysis, Data Warehouse, Report Builder, Daten-Feeds oder die Reporting-API nicht möglich ist.

Zudem werden bei „Berichtszeitverarbeitung“ nur Daten verarbeitet, die aus dem Datumsbereich der Berichterstellung stammen (nachfolgend als „Datumsfenster“ bezeichnet). Demnach bleiben auf „laufen nie ab“ festgelegte eVar-Werte für einen Besucher vor dem Datumsbereich der Berichterstellung in den Berichterstellungsfenstern nicht erhalten, und sie erscheinen nicht in Berichten. Das heißt auch, dass Kundenloyalitätsmessungen ausschließlich auf den im Berichterstellungsdatumsbereich vorhandenen Daten und nicht auf dem gesamten Verlauf vor dem Berichterstellungsdatumsbereich basieren.

Nachstehend finden Sie eine Liste der Metriken und Dimensionen, die bei Verwendung von „Berichtszeitverarbeitung“ momentan nicht unterstützt werden:

* **Analytics for Target:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Analytics for Advertising Cloud – reservierte Metriken/Dimensionen:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Metrik „Einzelzugriff“:** Dauerhaft nicht unterstützt.
* **Listenvariablen:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Zähler-eVars:** Dauerhaft nicht unterstützt.
* **Marketing-Kanal-Variablen:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Dimension „Tage seit letztem Kauf“:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Dimension nicht unterstützt.
* **Dimension „Tage bis Erstkauf“:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Dimension nicht unterstützt.
* **Dimension „Rückkehrhäufigkeit“:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Dimension nicht unterstützt. Ein alternativer Ansatz mithilfe einer Besuchsanzahlmetrik in einem Segment oder der Besuchsmetrik in einem Histogrammbericht kann verwendet werden.
* **Dimension „Tage seit dem letzten Besuch“:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Dimension nicht unterstützt.
* **Dimension „Ursprüngliche Entrypage“:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Dimension nicht unterstützt.
* **eVars für die lineare Zuordnung:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Dimension „Ursprünglich verweisende Domäne“:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **Besuchnummer:** Aufgrund der Eigenschaften des Datumsfensters für die Berichtszeitverarbeitung wird diese Metrik nicht unterstützt. Als Alternative zu mobilen Apps können Sie eine berechnete Metrik verwenden, die Besucher/Besuche mit der Metrik „App-Installation“umfasst, um neue Besucher oder Besuche zu identifizieren.
* **Transaktions-ID-Data Sources:** Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.

Nachstehend finden Sie eine Liste mit Dimensionen und Metriken, die je nach den ausgewählten Einstellungen für „Berichtszeitverarbeitung“ betroffen sind:

* Wenn „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist, treten die folgenden Änderungen ein. Weitere Informationen finden Sie unter [kontextbezogene Sitzungserstellung](vrs-mobile-visit-processing.md).
   * **Absprünge/Absprungrate:** Hintergrundtreffer, denen kein Vordergrundtreffer folgt, werden nicht als Absprung betrachtet und tragen nicht zur Absprungrate bei.
   * **Zeit pro Besuch in Sekunden:** Nur Besuche mit Treffern im Vordergrund tragen zu dieser Metrik bei.
   * **Zeit pro Besuch:** Nur Besuche, die Treffer im Vordergrund enthalten, tragen zu dieser Metrik bei.
   * **Dimensionen und Metriken „Einstieg/Ausstieg“:** In dieser Dimension werden nur Einstiege und Ausstiege von Besuchen mit Treffern im Vordergrund angezeigt.
   * **Metrik „Unique Visitors“** „Unique Visitors“ umfasst keine Besucher, die im Datumsbereich der Berichterstellung nur Hintergrundtreffer hatten.
* **Besuche:** Besuche spiegeln die konfigurierten Einstellungen der Virtual Report Suite wider, die sich von der zugrunde liegenden Report Suite unterscheiden können.
* **Serialisierte Ereignisse mit Ereignis-ID:** Ereignisse, die die Ereignisserialisierung mit einer Ereignis-ID verwenden, werden nur für Ereignisse dedupliziert, die innerhalb des Datumsbereichs der Berichterstellung für einen Besucher auftreten. Diese Ereignisse werden aufgrund des Datumsfensters für die Berichtszeitverarbeitung nicht global für alle Daten oder Besucher dedupliziert.
* **Käufe/Umsatz/Bestellungen/Einheiten:** Wenn die Einkaufs-ID verwendet wird, werden diese Metriken aufgrund des Datumsfensters für die Berichtszeitverarbeitung nur für doppelte Einkaufs-IDs dedupliziert, die innerhalb des Datumsbereichs der Berichterstellung für einen Besucher auftreten (anstatt global für alle Termine oder Besucher).
* **Nicht-Merchandising-eVars/reservierte eVars:** Die in einer eVar festgelegten Werte werden aufgrund des Datumsfensters für die Berichtszeitverarbeitung nur dann beibehalten, wenn der Wert innerhalb des Datumsbereichs für die Berichterstellung festgelegt wurde. Zudem können zeitbasierte Abläufe eine Stunde zu früh oder zu spät ablaufen, wenn sich die Persistenz über eine Zeitumstellung erstreckt.
* **Merchandising-eVars/reservierte eVars:** Siehe oben. Zudem wird bezüglich der Konversionssyntax „Beliebige Treffer“ verwendet, wenn die Bindung auf „Beliebiges Ereignis“ festgelegt ist.
* **Treffertyp:** Diese Dimension gibt an, ob es sich bei einem Treffer um einen Vorder- oder Hintergrundtreffer handelt.
