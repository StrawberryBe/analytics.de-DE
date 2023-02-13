---
title: Einverständnisverwaltungs-Opt-out
description: Ermitteln Sie, von welchen Datenschutzeinstellungen sich ein Besucher bzw. eine Besucherin abgemeldet hat.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: ht
source-wordcount: '254'
ht-degree: 100%

---

# Einverständnisverwaltungs-Opt-out

Die Dimension „Einverständnisverwaltungs-Opt-out“ gibt an, welche Datenschutzeinstellungen ein Besucher ausdrücklich abgelehnt hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für ein Datenschutz-Opt-out anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']`, wenn auf `1` gesetzt. Wenn `cm.ssf` gleich `0` oder leer ist, hat diese Variable keine Auswirkung.
* `contextData.['opt.dmp']`, wenn auf `N` gesetzt. Wenn `opt.dmp` gleich `Y` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-in](cm-opt-in.md) ausgefüllt.
* `contextData.['opt.sell']`, wenn auf `N` gesetzt. Wenn `opt.sell` gleich `Y` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-in](cm-opt-in.md) ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimensionselementen gehören die folgenden drei Werte:

* **`SSF`**: Der Besucher bzw. die Besucherin hat sich von der [Server-seitigen Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md) abgemeldet. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `cm.ssf` gleich `1` ist. Weitere Informationen finden Sie im Benutzerhandbuch für Audience Manager im Abschnitt [Datenschutz – Übersicht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html?lang=de). Der Treffer wird nicht an Adobe Audience Manager weitergeleitet.
* **`DMP`**: Der Besucher bzw. die Besucherin hat sich gegen die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `N` ist. Ähnlich wie `SSF`, der Treffer wird nicht an Adobe Audience Manager weitergeleitet.
* **`SELL`**: Der Besucher bzw. die Besucherin widersprach der Freigabe oder dem Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `N` ist.
