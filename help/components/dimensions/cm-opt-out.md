---
title: Einwilligungsmanagement Opt-out
description: Ermitteln Sie, von welchen Datenschutzeinstellungen ein Besucher abgemeldet hat.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 5%

---

# Einwilligungsmanagement Opt-out

Die Dimension &quot;Opt-out aus der Einverständnisverwaltung&quot;zeigt an, welche Datenschutzeinstellungen ein Besucher ausdrücklich abgelehnt hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für die Datenschutz-Opt-out anzuzeigen.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']` wenn auf `1`. Wenn `cm.ssf` gleich `0` oder leer ist, hat diese Variable keine Auswirkung.
* `contextData.['opt.dmp']` wenn auf `N`. Wenn `opt.dmp` gleich `Y`, die [Einverständnisverwaltung Opt-in](cm-opt-in.md) -Dimension wird stattdessen ausgefüllt.
* `contextData.['opt.sell']` wenn auf `N`. Wenn `opt.sell` gleich `Y`, die [Einverständnisverwaltung Opt-in](cm-opt-in.md) -Dimension wird stattdessen ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimension-Elementen gehören die folgenden drei Werte:

* **`SSF`**: Der Besucher hat sich abgemeldet von [Serverseitige Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md). Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `cm.ssf` gleich `1`. Siehe [Datenschutz - Übersicht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html) im Benutzerhandbuch für Audience Manager finden Sie weitere Informationen. Der Treffer wird nicht an Adobe Audience Manager weitergeleitet.
* **`DMP`**: Der Besucher hat sich gegen die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `N`. Ähnlich wie `SSF`, wird der Treffer nicht an Adobe Audience Manager weitergeleitet.
* **`SELL`**: Der Besucher widersprach der Freigabe oder dem Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `N`.
