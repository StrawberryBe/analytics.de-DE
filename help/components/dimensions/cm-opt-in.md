---
title: Einverständnisverwaltungs-Opt-in
description: Ermitteln Sie, zu welchen Datenschutzeinstellungen sich ein Besucher bzw. eine Besucherin angemeldet hat.
exl-id: b2768180-b763-41fb-8cba-665fac047e29
feature: Dimensions
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 91%

---

# Einverständnisverwaltungs-Opt-in

Das &quot;Opt-in der Einwilligungsverwaltung&quot; [Dimension](overview.md) zeigt an, welche Datenschutzeinstellungen ein Besucher aktiviert hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für ein Datenschutz-Opt-in anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['opt.dmp']`, wenn auf `Y` gesetzt. Wenn `opt.dmp` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.
* `contextData.['opt.sell']`, wenn auf `Y` gesetzt. Wenn `opt.sell` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimensionselementen gehören die folgenden zwei Werte:

* **`DMP`**: Der Besucher bzw. die Besucherin hat sich für die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `Y` ist.
* **`SELL`**: Der Besucher bzw. die Besucherin akzeptierte die Freigabe oder den Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `Y` ist.
