---
description: 'null'
keywords: DFA
title: Häufig gestellte Fragen
topic: Data connectors
uuid: 59d187e9-1ec1-4cf3-8831-b981f87c9372
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Häufig gestellte Fragen {#frequently-asked-questions}

## Warum werden meine Anmeldedaten vom Data Connectors-Assistenten nicht akzeptiert? {#section-f019b3de18774df3954af7881aa564fa}

Wenn Sie sich vergewissert haben, dass die Anmeldeinformationen gültig sind, stellen Sie sicher, dass der für die Integration angegebene Benutzername für den API-Zugriff aktiviert ist. Der Data Connectors-Assistent verwendet die DFA-API zum Überprüfen der Anmeldedaten sowie zum Deaktivieren und Aktivieren der Adobe-spezifischen Einstellungen in der DFA-API. Der API-Zugriff ist eine Einstellung, die von einem Administrator in der DFA-Oberfläche aktiviert werden muss. Vergewissern Sie sich anschließend, dass Sie über die Berechtigung zum Zugriff auf die im Assistenten ausgewählte Advertiser-ID oder Floodlight-Konfigurations-ID verfügen.

## Warum werden mir keine Daten aus den nächtlich hochgeladenen Metriken (DFA-Impressionen, DFA-Klicks usw.) angezeigt?  {#section-465fd22ae6b447ffb6baf20b57daa433}

Wenn Sie Version 1.5 der Integration verwenden, kann dies daran liegen, dass Ihrer Integration noch keine Client-Site-ID zugewiesen wurde. Für den nächtlichen Austausch und die Anforderung von Daten vom DFA-Anzeigenserver ist eine Client-Site-ID (CSID) erforderlich. CSIDs können bis zu 3 Tage nach der Integration mit Google ausgetauscht werden. Sobald die CSID bei Google eingegangen ist, erhalten Sie unter der E-Mail-Adresse der Integration die neue CSID sowie den aktuellen JavaScript-Code.

Wenn die Einrichtungs-E-Mail länger als 3 Tage vergangen ist und keine Metriken gesendet werden, besteht das wahrscheinlichste Problem darin, dass die CSID bereits einer anderen Integration zugewiesen wurde. Google verwaltet eine Zuordnung von 1 zu 1 zwischen CSID und Report Suite, d. h., wenn eine Integration in einer Report Suite dieselbe Advertiser-ID wie eine andere Integration in einer anderen Report Suite verwendet, wird nur der ersten eine CS-ID zugewiesen. Um zu ändern, welcher Report Suite oder welcher Advertiser-ID eine CSID zugeordnet ist, muss ein Ticket mit Google Support geöffnet werden.

Beispiel: Es gibt eine Integration in Report Suite A mit der Advertiser-ID Z, der eine CSID zugewiesen wird. Wenn später eine andere Integration in Report Suite B mit Advertiser Z eingerichtet wird, wird diese neuere Integration NICHT erneut der CSID zugewiesen. Dies würde ein Google-Ticket erfordern. Beispiel einer Integration in Report Suite A, mit Advertiser-ID Z und später einer weiteren Integration in Report Suite A ist Advertiser Z eingerichtet. Nur die erste Integration erhält Daten für die Integration. In diesem Fall kann jedoch die erste Integration deaktiviert werden und die Daten fließen zur zweiten Integration.

>[!NOTE] Bei Version 2.0 der Integration werden keine CSIDs verwendet. Daher ist diese Übertragung von CSIDs nicht erforderlich.

## Ich verwende Version 2.0 der Integration und Kostenmetriken werden für meine DFA-Anzeigen nicht angezeigt. Woran kann das liegen?  {#section-805748111bbe4bbf918d6dbbb2641fff}

Kostenmetriken müssen sowohl auf der Google DFA-Seite aktiviert, in der DFA-Oberfläche bereitgestellt und im Data Connectors-Assistenten aktiviert werden. Als Erstes müssen Sie überprüfen, ob Sie ein Analytics-Ereignis für DFA-Medienkosten zugeordnet und einen Währungscode bereitgestellt haben. Wenn Sie das Media Cost-Ereignis zugeordnet haben und den Assistenten beenden und speichern, wird das DFA-Flag omnitureCostData in der DFA-API aktiviert. Dies signalisiert Google, dass die Metriken in der nächtlichen Datei gesendet werden sollen. Sie können über die DFA-Oberfläche prüfen, ob omnitureCostData aktiviert ist, indem Sie sich die Eigenschaften des integrierten Floodlights ansehen. Stellen Sie nach Überprüfung dieser beiden Stellen sicher, dass die Anzeigen, die Teil des integrierten Floodlights sind, Kostendaten und Kostenstrukturen angeben. Wenn Kostendaten nicht in der DFA-Oberfläche bereitgestellt werden, werden sie nicht in Analytics angezeigt.

## Warum werden bei bestimmten Anzeigen keine DFA-Impressionen oder Durchsichten angezeigt, Klicks und Clickthroughs aber schon?  {#section-39b2eeeefd7f43d1a373df0b987bacef}

Es gibt Anzeigen, die nur Klickdaten aufzeichnen, die als Klicktracker bezeichnet werden. Diese Art von Anzeigen gibt keine Daten zur letzten Impression zurück, wenn der Floodlight-Server abgefragt wird. Wenden Sie sich an Ihre DFA-Agentur oder Ihren Google Support-Mitarbeiter, um zu überprüfen, ob es sich bei einer bestimmten Anzeige um eine Clicktracker- oder eine Nur-Klick-Anzeige handelt.

## Warum gibt es keine Clickthroughs für Anzeigen mit DFA-Klicks? {#section-758c1f1fc5b54bfc9294dcdc71bbd96a}

Darauf kann es eine von vielen Antworten geben.

Vergewissern Sie sich zunächst, dass die Anzeige über eine Landingpage-URL verfügt, die (a) für dieselbe Report Suite mit Adobe-Code getaggt ist, in der die Diskrepanz auftritt, und (b) den Abfragestringparameter  *`clickThroughParam`* enthält.

Überprüfen Sie anschließend, ob Sie über eine funktionierende Integration verfügen. Führen Sie dazu die unter [Bestätigung einer erfolgreichen DFA-Integration](../dfa-data-connector-analytics/dfa-integration.md) beschriebenen Schritte durch. Wird mit dem Adobe-Treffer auf der Landingpage ein DFA-Trackingcode angezeigt, sollte dieser Clickthrough ebenfalls im DFA-Kampagnenbericht enthalten sein. Wenn Sie nicht sehen, dass die Report Suites übereinstimmen, vergewissern Sie sich, dass die *`s.account`*-Variable der Landingpage und die in „Reports &amp; Analysen“ angezeigte Report Suite übereinstimmen. Wenn diese übereinstimmen, suchen Sie im Bericht &quot;Ansicht durch eVar&quot;nach Trackingcodes, die wie DFA:XXX:XXX:XXX:llXXX:XXX:XXX:XXX:XXX:XXX aussehen.

Dies zeigt an, dass die DFA-VISTA-Regel die Rohdaten aus DFA nicht verarbeiten konnte. Dieses Problem kann behoben werden, indem Sie über Ihren Adobe-Kundenbetreuer ein Support-Ticket öffnen.

Können Sie das Problem mit keiner der oben aufgeführten Lösungen beheben, finden Sie unter  [Abgleich von Metrikdiskrepanzen](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) weitere Möglichkeiten.
