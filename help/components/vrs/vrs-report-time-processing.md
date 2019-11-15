---
description: Die Berichtszeitverarbeitung ist eine Einstellung für eine Virtual Report Suite, mit der Daten nicht zerstörerisch und rückwirkend verarbeitet werden können.
title: Berichtszeitverarbeitung
uuid: 1a1d82ea-8c93-43cc-8689-cdcf59c309b1
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Berichtszeitverarbeitung

Die Berichtszeitverarbeitung ist eine Einstellung für eine Virtual Report Suite, mit der Daten nicht zerstörerisch und rückwirkend verarbeitet werden können.

> [!NOTE] Die Verarbeitung der Berichtszeit ist nur für den Analysis Workspace verfügbar.

„Report Time Processing“ betrifft nur die Daten in der Virtual Report Suite und hat keinen Einfluss auf Daten oder Datensammlungen in der zugrunde liegenden Report Suite. Der Unterschied zwischen Report Time Processing und der herkömmlichen Analytics-Verarbeitung lässt sich mithilfe des folgenden Diagramms am besten nachvollziehen:

![Google1](assets/google1.jpg)

Während der Datenverarbeitung in Analytics fließen die Daten durch die Datenerfassungspipeline und einen Vorverarbeitungsschritt, indem die Daten für die Berichterstellung vorbereitet werden. In diesem Schritt der Vorverarbeitung werden die Besuchsablauflogik und eVar-Persistenzlogik (unter anderem) auf die Daten angewendet, während sie erfasst werden. Der primäre Nachteil dieses Vorverarbeitungsmodells besteht darin, dass jegliche Konfiguration vorab erfolgen muss, noch bevor die Daten erfasst werden. Das heißt, dass die an den Vorverarbeitungseinstellungen vorgenommen Änderungen nur ab diesem Zeitpunkt und für neue Daten gelten. Dies ist problematisch, wenn defekte Daten eingehen oder wenn Einstellungen falsch konfiguriert wurden.

„Report Time Processing“ ist eine grundlegend andere Methode zur Verarbeitung von Analytics-Daten für die Berichterstellung. Anstatt vor dem Erfassen von Daten die Verarbeitungslogik vorab zu bestimmen, ignoriert Analytics die während des Vorverarbeitungsschritts festgelegten Daten und wendet diese Logik bei jeder Berichtsausführung an:

![Google2](assets/google2.jpg)

Diese Verarbeitungsarchitektur ermöglicht weit flexiblere Berichterstellungsoptionen. Sie können beispielsweise die Timeout-Zeitspanne für Besuche auf nicht destruktive Art und Weise beliebig ändern. Diese Änderungen spiegeln sich retroaktiv in der eVar-Persistenz und den Segmentcontainern wider, als hätten Sie diese Einstellungen vor dem Erfassen der Daten angewendet. Zudem können Sie eine beliebige Anzahl von Virtual Report Suites mit jeweils unterschiedlichen Optionen zu Report Time Processing generieren, die auf derselben zugrunde liegenden Report Suite basieren, ohne Daten in der zugrunde liegenden Report Suite zu ändern.

„Report Time Processing“ ermöglicht zudem, dass Analytics verhindert, dass Hintergrundtreffer neue Besuche starten und dass das [mobile SDK](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) die Berichterstellung zum Starten eines neuen Besuchs anweist, sobald ein App-Startereignis ausgelöst wird.

Die folgenden Konfigurationsoptionen sind momentan für Virtual Report Suites mit aktiviertem Report Time Processing verfügbar:

* **** Besuchszeitlimit: Die Timeout-Einstellung für Besuche definiert die Inaktivität, die ein individueller Besucher haben muss, bevor ein neuer Besuch automatisch gestartet wird. Die Standardeinstellung lautet 30 Minuten. Wenn Sie beispielsweise das Besuchstimeout auf 15 Minuten festlegen, wird für jede Sequenz mit erfassten Treffern eine neue Besuchsgruppierung erstellt, die nach 15 Minuten Inaktivität separiert ist. Diese Einstellung beeinflusst nicht nur Ihre Besuchszahlen, sondern auch die Art und Weise der Evaluierung von Besuchssegmentcontainern und die Besuchsablauflogik für eVars, die bei einem Besuch ablaufen. Durch eine Verringerung des Besuchstimeouts erhöht sich wahrscheinlich die Gesamtzahl der Besuche in der Berichterstellung, während eine Erhöhung des Besuchstimeouts wahrscheinlich zu einer Reduzierung der Gesamtbesuche in der Berichterstellung führt.
* **** Einstellungen für Mobile App-Besuche: Für Report Suites, die Daten enthalten, die von mobilen Apps über die [Adobe Mobile SDKs](https://www.adobe.io/apis/cloudplatform/mobile.html)generiert wurden, stehen zusätzliche Besuchseinstellungen zur Verfügung. Diese Einstellungen sind nicht destruktiv und betreffen nur Treffer, die über die Mobile SDKs erfasst wurden. Sie haben keinen Einfluss auf Daten, die außerhalb der Mobile SDKs erfasst wurden.
* **** Verhindern, dass Hintergrundtreffer einen neuen Besuch starten: Hintergrundtreffer werden von den Mobile-SDKs erfasst, wenn sich die App im Hintergrund befindet.
* **** Bei jedem App-Start einen neuen Besuch starten: Zusätzlich zum Timeout für Besuche können Sie den Start eines Besuchs erzwingen, sobald ein App-Startereignis von den Mobile-SDKs aufgezeichnet wurde, unabhängig vom Fenster "Inaktivität". Diese Einstellung nimmt Einfluss auf die Besuchsmetrik und den Besuchssegmentcontainer sowie die Besuchsablauflogik für eVars.
* **** Neuen Besuch mit Ereignis starten: Eine neue Sitzung beginnt, wenn ein Ereignis ausgelöst wird, unabhängig davon, ob eine Sitzung abgelaufen ist. Zur neuen Sitzung gehört auch das Ereignis, das sie ausgelöst hat. Zudem können Sie mehrere Ereignisse nutzen, um eine Sitzung zu starten, und eine neue Sitzung wird dann begonnen, wenn beliebige dieser Ereignisse in den Daten auftreten. Diese Einstellung wirkt sich auf Ihre Besuchszählung, den Besuchssegmentierungs-Container sowie die Besuchsablauflogik von eVars aus.

„Report Time Processing“ unterstützt nicht alle Metriken und Dimensionen, die in der herkömmlichen Analytics-Berichterstellung verfügbar sind. Virtual report suites utilizing Report Time Processing are only accessible in Analysis Workspace and will not be accessible in [!UICONTROL Reports &amp; Analytics], Ad Hoc Analysis, Data Warehouse, Report Builder, Data Feeds, or the reporting API.

Zudem werden bei „Report Time Processing“ nur Daten verarbeitet, die aus dem Datumsbereich der Berichterstellung stammen (nachfolgend als „Datumsfenster“ bezeichnet). Demnach bleiben auf „laufen nie ab“ festgelegte eVar-Werte für einen Besucher vor dem Datumsbereich der Berichterstellung in den Berichterstellungsfenstern nicht erhalten, und sie erscheinen nicht in Berichten. Das heißt auch, dass Kundenloyalitätsmessungen ausschließlich auf den im Berichterstellungsdatumsbereich vorhandenen Daten und nicht auf dem gesamten Verlauf vor dem Berichterstellungsdatumsbereich basieren.

Nachstehend finden Sie eine Liste der Metriken und Dimensionen, die bei Verwendung von „Report Time Processing“ momentan nicht unterstützt werden:

* **** Analytics für Target: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Analytics für Advertising Cloud - reservierte Metriken/Dimensionen: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Einzelzugriffsmetrik: Dauerhaft nicht unterstützt.
* **** Listenvariablen: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Zähler-eVars: Dauerhaft nicht unterstützt.
* **** Marketingkanalvariablen: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Dimension Tage seit letztem Kauf: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Dimension nicht unterstützt.
* **** Dimension Tage bis Erstkauf: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Dimension nicht unterstützt.
* **** Dimension der Rückkehrhäufigkeit: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Dimension nicht unterstützt. Ein alternativer Ansatz mithilfe einer Besuchsanzahlmetrik in einem Segment oder der Besuchsmetrik in einem Histogrammbericht kann verwendet werden.
* **** Dimension Tage seit dem letzten Besuch: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Dimension nicht unterstützt.
* **** Ursprüngliche Dimension der Einstiegsseite: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Dimension nicht unterstützt.
* **** eVars zur linearen Zuordnung: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Dimension der ursprünglich verweisenden Domäne: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.
* **** Besuch-Nr.: Aufgrund der Art des Datumsfensters für die Berichtverarbeitung wird diese Metrik nicht unterstützt. Als Alternative zu mobilen Apps können Sie eine berechnete Metrik verwenden, die Besucher/Besuche mit der Metrik "App-Installation"umfasst, um neue Besucher oder Besuche zu identifizieren.
* **** Transaktions-ID-Datenquellen: Derzeit nicht unterstützt. Eine künftige Unterstützung ist geplant.

Nachstehend finden Sie eine Liste mit Dimensionen und Metriken, die je nach den ausgewählten Einstellungen für „Report Time Processing“ betroffen sind:

* Wenn "Starten eines neuen Besuchs verhindern"aktiviert ist, werden die folgenden Änderungen vorgenommen. Weitere Informationen finden Sie unter [Kontextsensibilisierung](vrs-mobile-visit-processing.md) .
   * **** Absprünge/Absprungrate: Hintergrundtreffer, denen kein Vordergrundtreffer folgt, werden nicht als Absprung betrachtet und tragen nicht zur Absprungrate bei.
   * **** Zeit pro Besuch: Nur Besuche, die Treffer im Vordergrund enthalten, tragen zu dieser Metrik bei.
   * **** Zeit pro Besuch: Nur Besuche, die Treffer im Vordergrund enthalten, tragen zu dieser Metrik bei.
   * **** Einstiegs-/Ausstiegsdimensionen und -metriken: In dieser Dimension werden nur Einstiege und Ausstiege von Besuchen mit Treffern im Vordergrund angezeigt.
   * **** Metrik Unique Visitors: Unique Visitors umfasst keine Besucher, die im Berichtsdatumsbereich nur Hintergrundtreffer hatten.
* **** Besuche: Die Besuche spiegeln alle Einstellungen wider, die die Virtual Report Suite konfiguriert hat. Diese können sich von der Basis-Report Suite unterscheiden.
* **** Serialisierte Ereignisse mit Ereignis-IDs: Ereignisse, die die Ereignis-Serialisierung mit einer Ereignis-ID verwenden, werden nur für Ereignisse dedupliziert, die innerhalb des Berichtsdatumsbereichs für einen Besucher auftreten. Diese Ereignisse werden aufgrund der Datumsanzeige im Bericht nicht global für alle Daten oder Besucher dedupliziert.
* **** Käufe/Umsatz/Bestellungen/Einheiten: Wenn die Kauf-ID verwendet wird, werden diese Metriken nur für doppelte Kauf-IDs dedupliziert, die innerhalb des Berichtsdatumsbereichs für einen Besucher auftreten, und nicht für alle Daten oder Besucher weltweit aufgrund des Datumsfensters für die Berichtverarbeitung.
* **** Nicht-Merchandising-eVars/reservierte eVars: Die in einer eVar festgelegten Werte bleiben nur erhalten, wenn der Wert aufgrund des Datumsfensters für die Berichtverarbeitung im Berichtsdatumsbereich festgelegt wurde. Darüber hinaus können zeitbasierte Abläufe eine Stunde zu früh oder eine Stunde zu spät ablaufen, wenn die Persistenz sich über eine Sommerzeitänderung erstreckt.
* **** Merchandising eVars/Reservierte eVars: Siehe oben. Zudem wird bezüglich der Konversionssyntax „Beliebige Treffer“ verwendet, wenn die Bindung auf „Beliebiges Ereignis“ festgelegt ist.
* **** Treffertyp: Diese Dimension gibt an, ob ein Treffer im Vordergrund oder Hintergrund vorliegt.
