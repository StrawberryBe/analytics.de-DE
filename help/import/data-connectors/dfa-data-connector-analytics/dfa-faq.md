---
description: Häufig gestellte Fragen zum DFA-Datenanschluss.
keywords: DFA
title: Häufig gestellte Fragen
topic: Data Connectors
uuid: 59d187e9-1ec1-4cf3-8831-b981f87c9372
translation-type: tm+mt
source-git-commit: 6669f678c1327b6af4a5b67c8033a9b7d8c9dbcf
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 97%

---


# Häufig gestellte Fragen {#frequently-asked-questions}

## Warum werden meine Anmeldedaten vom Data Connectors-Assistenten nicht akzeptiert? {#section-f019b3de18774df3954af7881aa564fa}

Wenn Sie überprüft haben, dass die Anmeldedaten gültig sind, stellen Sie sicher, dass der für die Integration bereitgestellte Benutzername für den API-Zugriff aktiviert ist. Der Data Connectors-Assistent verwendet die DFA-API zur Validierung der Anmeldedaten sowie zum Aktivieren und Deaktivieren der Adobe-spezifischen Einstellungen in der DFA-API. Der API-Zugriff ist eine Funktion, die ein Administrator in der DFA-Oberfläche aktivieren muss. Stellen Sie als Nächstes sicher, dass Sie Zugriff auf die im Assistenten ausgewählte Advertiser- oder Floodlight-Konfigurations-ID haben.

## Warum werden mir keine Daten aus den nächtlich hochgeladenen Metriken (DFA-Impressionen, DFA-Klicks usw.) angezeigt?   {#section-465fd22ae6b447ffb6baf20b57daa433}

Bei Version 1.5 der Integration kann das daran liegen, dass Ihre Integration noch keiner Client-Site-ID zugewiesen wurde. Für den nächtlichen Austausch sowie zum Abfragen von Daten vom DFA-Anzeigenserver ist eine Client-Site-ID (CSID) erforderlich. Es kann ab dem Datum der Integration bis zu drei Tage dauern, bis CSIDs mit Google ausgetauscht werden. Sobald die CSID bei Google eingegangen ist, erhalten Sie unter der E-Mail-Adresse der Integration die neue CSID sowie den aktuellen JavaScript-Code.

Wenn Sie die Einrichtungs-E-Mail nach drei Tagen nicht erhalten haben und keine Metriken gesendet werden, liegt das Problem wahrscheinlich darin, dass die CSID bereits einer anderen Integration zugewiesen ist. Bei Google werden CSID und Report Suite eins zu eins zugeordnet; wenn für eine Integration in einer Report Suite also dieselbe Advertiser-ID wie für eine andere Integration in einer anderen Report Suite verwendet wird, wird nur der ersten eine CSID zugeordnet. Um die Zuordnung einer CSID zu einer Report Suite oder Advertiser-ID zu ändern, müssen Sie einen Fall bei der Google-Hilfe erstellen.

Beispiel: Es gibt eine Integration in Report Suite A mit der Advertiser-ID Z, der eine CSID zugeordnet wird. Später wird eine weitere Integration in Report Suite B mit der Advertiser-ID Z eingerichtet und dieser neuen Integration wird die CSID NICHT erneut zugeordnet. Dazu ist die Erstellung eines Falls bei Google erforderlich. Ein anderes Beispiel wäre eine Integration in Report Suite A mit der Advertiser-ID Z, später wird eine weitere Integration in Report Suite A mit der Advertiser-ID Z eingerichtet. Es werden nur Daten zur Integration an die erste Integration gesendet. Allerdings kann die erste Integration in diesem Fall deaktiviert werden, woraufhin Daten an die zweite Integration gesendet werden.

>[!NOTE]
>
>Bei Version 2.0 der Integration werden keine CSIDs verwendet. Daher ist diese Übertragung von CSIDs nicht erforderlich.

## Ich verwende Version 2.0 der Integration und ich sehe keine Kostenmetriken für meine DFA-Anzeigen. Woran kann das liegen?   {#section-805748111bbe4bbf918d6dbbb2641fff}

Kostenmetriken müssen sowohl bei Google-DFA und im Data Connectors-Assistenten aktiviert sein als auch über die DFA-Oberfläche bereitgestellt werden. Zuerst sollten Sie überprüfen, ob Sie DFA-Medienkosten ein Analytics-Ereignis zugewiesen und einen Währungscode angegeben haben. Wenn Sie das Medienkostenereignis zugeordnet sowie den Assistenten abgeschlossen und gespeichert haben, wird das DFA-omnitureCostData-Flag in der DFA-API aktiviert. Dadurch erhält Google die Information, dass die Metriken mit der nächtlichen Dateisendung übertragen werden sollen. Versichern Sie sich auch mithilfe der DFA-Oberfläche, dass omnitureCostData aktiviert ist, indem Sie sich die Eigenschaften im integrierten Floodlight ansehen. Überprüfen Sie abschließend, dass in den Anzeigen, die Teil des integrierten Floodlights sind, Kostendaten und -zusammensetzungen angegeben sind. Werden Kostendaten in der DFA-Oberfläche nicht bereitgestellt, erscheinen sie auch nicht in Analytics.

## Warum werden bei bestimmten Anzeigen keine DFA-Impressionen oder Durchsichten angezeigt, Klicks und Clickthroughs aber schon?   {#section-39b2eeeefd7f43d1a373df0b987bacef}

Manche Anzeigen erfassen nur Klickdaten und werden daher Klicktracker genannt. Bei diesen Anzeigen werden keine Daten zur letzten Impression bei Abfrage des Floodlight-Servers zurückgegeben. Sie können überprüfen, ob es sich bei einer Anzeige um einen Klicktracker oder eine reine Klickanzeige handelt, indem Sie sich an Ihre DFA-Agentur oder Ihren Ansprechpartner bei der Google-Hilfe wenden.

## Warum gibt es keine Clickthroughs für Anzeigen mit DFA-Klicks? {#section-758c1f1fc5b54bfc9294dcdc71bbd96a}

Auf diese Frage gibt es viele Antworten.

Vergewissern Sie sich zunächst, dass die Anzeige über eine Landingpage-URL verfügt, die (a) für dieselbe Report Suite mit Adobe-Code getaggt ist, in der die Diskrepanz auftritt, und (b) den Abfragestringparameter  *`clickThroughParam`* enthält.

Überprüfen Sie anschließend, ob Sie über eine funktionierende Integration verfügen. Führen Sie dazu die unter [Bestätigung einer erfolgreichen DFA-Integration](../dfa-data-connector-analytics/dfa-integration.md) beschriebenen Schritte durch. Wird mit dem Adobe-Treffer auf der Landingpage ein DFA-Trackingcode angezeigt, sollte dieser Clickthrough ebenfalls im DFA-Kampagnenbericht enthalten sein. Wenn Sie nicht sehen, dass die Report Suites übereinstimmen, vergewissern Sie sich, dass die *`s.account`*-Variable der Landingpage und die in „Reports &amp; Analysen“ angezeigte Report Suite übereinstimmen. Stimmen diese überein, suchen Sie nach Trackingcodes im Durchsichts-eVar-Bericht, die das Format DFA:XXX:XXX:XXX:llXXX:XXX:XXX:XXX:XXX aufweisen.

Diese geben an, dass die DFA-Rohdaten nicht durch die DFA-VISTA-Regel verarbeitet werden konnten. Dieses Problem kann durch Öffnen eines Support-Tickets über Ihren Kundenbetreuer behoben werden.

Können Sie das Problem mit keiner der oben aufgeführten Lösungen beheben, finden Sie unter  [Abgleich von Metrikdiskrepanzen](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) weitere Möglichkeiten.
