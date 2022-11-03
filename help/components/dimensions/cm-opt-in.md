---
title: Einwilligungsmanagement Opt-in
description: Ermitteln Sie, welche Datenschutzeinstellungen ein Besucher aktiviert hat.
source-git-commit: 49b2c144fea5786564ccb6dc70adead3bc669596
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# Einwilligungsmanagement Opt-in

Die Dimension &quot;Opt-in der Einverständnisverwaltung&quot;zeigt an, welche Datenschutzeinstellungen ein Besucher aktiviert hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für die Datenschutzaktivierung anzuzeigen.

## Diese Dimension mit Daten füllen

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['opt.dmp']` wenn auf `Y`. Wenn `opt.dmp` gleich `N`, die [Einverständnisverwaltung Opt-out](cm-opt-out.md) -Dimension wird stattdessen ausgefüllt.
* `contextData.['opt.sell']` wenn auf `Y`. Wenn `opt.sell` gleich `N`, die [Einverständnisverwaltung Opt-out](cm-opt-out.md) -Dimension wird stattdessen ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimension-Elementen gehören die beiden folgenden Werte:

* **`DMP`**: Der Besucher hat sich für die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `Y`.
* **`SELL`**: Der Besucher hat sich für die Freigabe oder den Verkauf der Daten an Dritte entschieden. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `Y`.
