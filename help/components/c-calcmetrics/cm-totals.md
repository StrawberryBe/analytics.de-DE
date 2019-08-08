---
title: Gesamtsummen für berechnete Metriken
seo-title: Gesamtsummen für berechnete Metriken
description: Erfahren Sie, wie sich berechnete Metriken in den Analytics-Tools unterscheiden.
seo-description: Berechnung der Summen errechneter Metriken
translation-type: tm+mt
source-git-commit: 774975605de502b66279888d8dd8ef58989a40de

---


# Gesamtsummen für berechnete Metriken

Die Gesamtsumme der berechneten Metriken wird zwischen [DNL Reports &amp; Analysen] und [DNL Analysis Workspace angezeigt]. In diesem Abschnitt werden die Unterschiede erläutert.

## Gesamtsummen errechneter Metriken in [!DNL Reports & Analytics]

Wenn Sie Berichte anzeigen, [!DNL Reports & Analytics]werden berechnete Metriken immer `n/a` unter der Gesamtsumme angezeigt. Da alle berechneten Metriken benutzerdefiniert sind, gibt es für diese Summe viele Fälle, in denen diese Summe nicht sinnvoll ist. Siehe folgendes Beispiel:

Ihr Unternehmen hat die [Bestellungen] / [Besuche] errechneter Metriken erstellt, um den Prozentsatz der Besuche zu ermitteln, die etwas auf Ihrer Site gekauft haben. Wenn Sie diese Metrik in einen Produktbericht gebracht haben, werden mehrere Produkte einer einzelnen Bestellung zugeordnet. Außerdem werden mehrere Produkte einem einzelnen Besuch zugeordnet. Wenn in diesem Bericht eine berechnete Metriksumme angegeben wurde, werden folgende Fragen gestellt:

| Frage | Antwort |
|---|---|
| Macht es Sinn, die Zeilenelemente zu summieren? | Dies ist nicht der Fall, da mehrere Produkte in einer einzigen Bestellung enthalten sein können und mehrere Produkte in einen einzelnen Besuch eingeschlossen werden können. Wenn die Zeilenelemente aggregiert wurden, stimmen Gesamtbestellungen und Gesamtbesuche nicht mit den tatsächlichen Bestellungen und den Gesamtbesuchen überein. |
| Ergeben die Gesamtbestellungen und die Gesamtzahl der Besuche Sinn? | Dies ist nicht der Fall, da die Summe nicht mit der Summe der einzelnen Zeileneinträge übereinstimmt. Darüber hinaus werden Gesamtbestellungen und Gesamtbesuche separat berechnet. |

Da es keine logische und konkrete Methode gibt, um festzustellen, ob eine berechnete Metrik in Berichten sinnvoll ist, wird die Metriksumme vollständig ausgelassen. Wenn Sie eine Gesamtsumme erhalten möchten, können Sie einen der folgenden Schritte ausführen:

* Erstellen Sie eine berechnete Metrik, die die Gesamtversionen der Metriken enthält, die Sie einbeziehen möchten.
* Erstellen Sie einen Datenextrahierungsbericht, der geplant werden kann.
* Erstellen Sie eine Datenanforderung in reportbuilder.
* Verwenden Sie den Analysis Workspace (siehe unten).

## Berechnete Metriksummen in [!DNL Analysis Workspace]

In Analysis Workspace werden berechnete Metriken unter bestimmten Umständen summiert, um eine Gesamtsumme anzuzeigen:

* Wenn [statische Zeilen](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) vorhanden sind und die [!UICONTROL Gesamtzahlen addiert werden, indem die Werte in jeder Spalte] (Standard) addiert werden, wird die Option "Standard" ausgewählt.
* [In der Ringdiagrammdarstellung.](/help/analyze/analysis-workspace/visualizations/donut.md)
* In der [Visualisierung der Zusammenfassungsänderung](/help/analyze/analysis-workspace/visualizations/summary-number-change.md).
