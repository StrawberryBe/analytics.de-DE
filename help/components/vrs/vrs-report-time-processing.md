---
description: „Berichtszeitverarbeitung“ ist eine virtuelle Report Suite-Einstellung zur zerstörungsfreien, rückwirkenden Verarbeitung von Daten.
title: Berichtszeitverarbeitung
role: Admin
solution: Analytics
feature: VRS
exl-id: 3742b9d1-f1fb-4690-bd44-b4719ff9d9bc
source-git-commit: ec4edb257490d326ab8f8de51a4ab9412a2b4a28
workflow-type: tm+mt
source-wordcount: '1306'
ht-degree: 84%

---

# Berichtszeitverarbeitung

[!UICONTROL Berichtszeitverarbeitung] ist eine Virtual Report Suite-Einstellung, mit der Daten in Analysis Workspace zerstörungsfrei und rückwirkend verarbeitet werden können.

[!UICONTROL Berichtszeitverarbeitung] betrifft nur die Daten in der Virtual Report Suite und hat keinen Einfluss auf Daten oder die Datenerfassung in der zugrunde liegenden Report Suite. Der Unterschied zwischen [!UICONTROL Berichtszeitverarbeitung] und der herkömmlichen Analytics-Verarbeitung lässt sich am besten anhand des folgenden Diagramms veranschaulichen:

![Traditionelle Verarbeitungs-Pipeline](assets/google1.jpg)

Während der Datenverarbeitung in Analytics fließen die Daten durch die Datenerfassungspipeline und einen Vorverarbeitungsschritt, indem die Daten für die Berichterstellung vorbereitet werden. In diesem Schritt der Vorverarbeitung werden die Besuchsablauflogik und eVar-Persistenzlogik (unter anderem) auf die Daten angewendet, während sie erfasst werden. Der primäre Nachteil dieses Vorverarbeitungsmodells besteht darin, dass jegliche Konfiguration vorab erfolgen muss, noch bevor die Daten erfasst werden. Das heißt, dass die an den Vorverarbeitungseinstellungen vorgenommen Änderungen nur ab diesem Zeitpunkt und für neue Daten gelten. Dies ist problematisch, wenn defekte Daten eingehen oder wenn Einstellungen falsch konfiguriert wurden.

[!UICONTROL Berichtszeitverarbeitung] ist eine völlig andere Methode zur Verarbeitung von Analytics-Daten für die Berichterstellung. Anstatt vor dem Erfassen von Daten die Verarbeitungslogik vorab zu bestimmen, ignoriert Analytics die während des Vorverarbeitungsschritts festgelegten Daten und wendet diese Logik bei jeder Berichtsausführung an:

![Pipeline zur Berichtszeitverarbeitung](assets/google2.jpg)

Diese Verarbeitungsarchitektur ermöglicht weit flexiblere Berichterstellungsoptionen. Sie können beispielsweise den Timeout-Zeitraum für Besuche auf eine beliebige Zeitdauer ohne Zerstörung ändern, und diese Änderungen werden in Ihrer eVar-Persistenz und den Segmentbehältern für den gesamten Berichtszeitraum übernommen. Zudem können Sie eine beliebige Anzahl von Virtual Report Suites mit jeweils unterschiedlichen Optionen zu Berichtszeitverarbeitung generieren, die auf derselben zugrunde liegenden Report Suite basieren, ohne Daten in der zugrunde liegenden Report Suite zu ändern.

[!UICONTROL Berichtszeitverarbeitung] ermöglicht Analytics auch, zu verhindern, dass Hintergrundtreffer neue Besuche starten, und ermöglicht die [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html?lange=de) , um einen neuen Besuch zu starten, sobald ein App-Startereignis ausgelöst wird.

## Konfigurationsoptionen

Die folgenden Konfigurationsoptionen sind derzeit für Virtual Report Suites mit aktivierter Berichtszeitverarbeitung verfügbar:

* **[!UICONTROL Maximale Wartezeit für Besuch]:** Mit dieser Einstellung wird die Dauer der Inaktivität eines Unique Visitor definiert, bevor automatisch ein neuer Besuch gestartet wird. Die Standardeinstellung lautet 30 Minuten. Wenn Sie beispielsweise das Besuchstimeout auf 15 Minuten festlegen, wird für jede Sequenz mit erfassten Treffern eine neue Besuchsgruppierung erstellt, die nach 15 Minuten Inaktivität separiert ist. Diese Einstellung beeinflusst nicht nur Ihre Besuchszahlen, sondern auch die Art und Weise der Evaluierung von Besuchssegmentcontainern und die Besuchsablauflogik für eVars, die bei einem Besuch ablaufen. Durch eine Verringerung des Besuchstimeouts erhöht sich wahrscheinlich die Gesamtzahl der Besuche in der Berichterstellung, während eine Erhöhung des Besuchstimeouts wahrscheinlich zu einer Reduzierung der Gesamtbesuche in der Berichterstellung führt.
* **[!UICONTROL Besuchseinstellungen für Mobile Apps]:** Für Report Suites mit Daten, die von Mobile Apps über die [Adobe Mobile SDKs](https://experienceleague.adobe.com/docs/mobile.html) generiert wurden, sind zusätzliche Besuchseinstellungen verfügbar. Diese Einstellungen sind nicht destruktiv und betreffen nur Treffer, die über die Mobile SDKs erfasst wurden. Sie haben keinen Einfluss auf Daten, die außerhalb der Mobile SDKs erfasst wurden.
* **[!UICONTROL Starten neuer Besuche durch Hintergrundtreffer verhindern]:** Hintergrundtreffer werden von den Mobile SDKs erfasst, wenn sich die Mobile App in einem Hintergrundzustand befindet.
* **[!UICONTROL Bei jedem Anwendungsstart einen neuen Besuch starten]:** Zusätzlich zur maximalen Wartezeit für Besuche können Sie immer dann den Beginn eines Besuchs erzwingen, wenn von den Mobile SDKs ein Startereignis einer Mobile App aufgezeichnet wurde. Die Inaktivitätsdauer ist dabei unerheblich. Diese Einstellung hat einen Einfluss auf die Besuchsmetrik und den Besuchssegment-Container sowie die Besuchsgültigkeitslogik für eVars.
* **[!UICONTROL Neuen Besuch mit Ereignis starten]:** Eine neue Sitzung beginnt dann, wenn ein Ereignis ausgelöst wird – unabhängig davon, ob bei einer Sitzung eine Zeitüberschreitung aufgetreten ist oder nicht. Zur neuen Sitzung gehört auch das Ereignis, das sie ausgelöst hat. Zudem können Sie mehrere Ereignisse nutzen, um eine Sitzung zu starten, und eine neue Sitzung wird dann begonnen, wenn beliebige dieser Ereignisse in den Daten auftreten. Diese Einstellung wirkt sich auf Ihre Besuchszählung, den Besuchssegmentierungs-Container sowie die Besuchsablauflogik von eVars aus.

Im Folgenden finden Sie ein Video zum Starten eines neuen Besuchs mit einem Ereignis:

>[!VIDEO](https://video.tv.adobe.com/v/23129/?quality=12)

## Einschränkungen bei der Berichtszeitverarbeitung

Die Berichtszeitverarbeitung unterstützt nicht alle Metriken und Dimensionen, die in der herkömmlichen Analytics-Berichterstellung verfügbar sind. Auf Virtual Report Suites mit Berichtszeitverarbeitung können Sie nur über Analysis Workspace zugreifen, nicht aber über [!UICONTROL Reports &amp; Analytics], Data Warehouse, Report Builder, Daten-Feeds oder der Reporting-API.

Zudem werden bei „Berichtszeitverarbeitung“ nur Daten verarbeitet, die aus dem Datumsbereich der Berichterstellung stammen (nachfolgend als „Datumsfenster“ bezeichnet). Demnach bleiben auf „laufen nie ab“ festgelegte eVar-Werte für einen Besucher vor dem Datumsbereich der Berichterstellung in den Berichterstellungsfenstern nicht erhalten, und sie erscheinen nicht in Berichten. Das heißt auch, dass Kundenloyalitätsmessungen ausschließlich auf den im Berichterstellungsdatumsbereich vorhandenen Daten und nicht auf dem gesamten Verlauf vor dem Berichterstellungsdatumsbereich basieren.

Die folgenden Dimensionen und Metriken werden bei der Berichtszeitverarbeitung nicht unterstützt:

* **Analytics for Target**
* **Analytics für Advertising Cloud-Dimensionen/-Metriken**
* **Zähler-eVars**
* **Tage bis Erstkauf**
* **Tage seit letztem Kauf**
* **Tage seit dem letzten Besuch**
* **Ursprüngliche Entrypage**
* **eVars für die lineare Zuordnung**
* **Listen-Vars**
* **Marketing-Kanal-Dimensionen**
* **Ursprüngliche Referrer-Domäne**
* **Rückkehrhäufigkeit**
* **Einzelzugriff**
* **Transaktions-ID-Datenquellen**
* **Besuchnummer**

## Betroffene Dimensionen und Metriken

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
* **Dimensionen mit (geringem Traffic) oder &quot;Individuelle Werte überschritten&quot;:** Der Zeileneintrag (geringer Traffic) wird bei der Verwendung der Berichtszeitverarbeitung etwas anders bestimmt und entspricht nicht garantiert dem, was bei der Berichterstellung für die zugrunde liegende Report Suite beobachtet wird. Zeileneinträge von Dimensionen, die nicht Teil von &quot;Geringer Datenverkehr&quot;sind, stellen nicht garantiert 100 % der Daten für diesen Zeileneintrag dar. Je höher die Anzahl eindeutiger Werte in einer Dimension ist, desto größer können diese Unterschiede sein.
