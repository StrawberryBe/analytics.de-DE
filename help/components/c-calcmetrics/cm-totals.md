---
title: Berechnete Metriken insgesamt
seo-title: Berechnete Metriken insgesamt
description: Erfahren Sie, wie sich berechnete Metriken in den Analytics-Tools unterscheiden.
seo-description: Berechnung der Summen errechneter Metriken
translation-type: tm+mt
source-git-commit: 658925799c530b46ff7b56d5d0685af6d9fef1b8

---


# Berechnete Metriken insgesamt

Die Gesamtsumme der berechneten Metriken wird zwischen [!DNL Reports & Analytics] und [!DNL Analysis Workspace]geändert. In diesem Abschnitt werden die Unterschiede erläutert.

## Gesamtsummen errechneter Metriken in [!DNL Reports & Analytics]

Wenn Sie Berichte anzeigen, [!DNL Reports & Analytics]werden berechnete Metriken immer `n/a` unter der Gesamtsumme angezeigt. Da alle berechneten Metriken benutzerdefiniert sind, gibt es für diese Summe viele Fälle, in denen diese Summe nicht sinnvoll ist. Siehe folgendes Beispiel:

Ihr Unternehmen hat die berechnete Metrik `orders` erstellt/ `visits` um den Prozentsatz der Besuche zu ermitteln, die etwas auf Ihrer Site gekauft haben. Wenn Sie diese Metrik in einen Produktbericht gebracht haben, werden mehrere Produkte einer einzelnen Bestellung zugeordnet. Außerdem werden mehrere Produkte einem einzelnen Besuch zugeordnet. Wenn in diesem Bericht eine berechnete Metriksumme angegeben wurde, werden folgende Fragen gestellt:

| Frage | Antwort |
|---|---|
| Macht es Sinn, die Zeilenelemente zu summieren? | Dies ist nicht der Fall, da mehrere Produkte in einer einzigen Bestellung enthalten sein können und mehrere Produkte in einen einzelnen Besuch eingeschlossen werden können. Wenn die Zeilenelemente aggregiert wurden, stimmen Gesamtbestellungen und Gesamtbesuche nicht mit den tatsächlichen Bestellungen und den Gesamtbesuchen überein. |
| Ergeben die Gesamtbestellungen und die Gesamtzahl der Besuche Sinn? | Dies ist nicht der Fall, da die Summe nicht mit der Summe der einzelnen Zeileneinträge übereinstimmt. Darüber hinaus werden Gesamtbestellungen und Gesamtbesuche separat berechnet. |

Da es keine logische und konkrete Methode gibt, um festzustellen, ob eine berechnete Metrik in Berichten sinnvoll ist, wird die Metriksumme vollständig ausgelassen. Wenn Sie eine Gesamtsumme erhalten möchten, können Sie einen der folgenden Schritte ausführen:

* Erstellen Sie eine berechnete Metrik, die die Gesamtversionen der Metriken enthält, die Sie einbeziehen möchten.
* Erstellen Sie einen Datenextrahierungsbericht, der geplant werden kann.
* Create a data request within [!DNL ReportBuilder].
* Verwenden [!DNL Analysis Workspace] (siehe unten).

## Berechnete Metriksummen in [!DNL Analysis Workspace]

Wenn Sie Daten im Analysis Workspace anzeigen, werden die Summen der berechneten Metriken in den meisten Fällen angezeigt. In einigen Fällen ist eine Gesamtsumme nicht möglich, z. B. wenn die Zeilen des Berichts aus gemischten Formaten bestehen (z. B. Dezimal und Währung).

Wenn die Summen angezeigt werden, werden sie oft serverseitig berechnet. Dies bedeutet, dass die gesamten Metriken wie Besuche oder Besucher insgesamt dedupliziert werden. Unter bestimmten Umständen werden berechnete Metriken clientseitig generiert, indem sie über mehrere Zeilen der Tabelle summiert werden. Dies bedeutet, dass die Metriken nicht mit Metriken wie Besuche oder Besucher dedupliziert werden. Dies geschieht:

* Wenn [statische Zeilen](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) in Freiform-Tabellen verwendet werden und die **[!UICONTROL Option Als Summe der aktuellen Zeilen]** anzeigen (Standard) ausgewählt wird
* In der [Ringdiagrammdarstellung](/help/analyze/analysis-workspace/visualizations/donut.md), damit Zahlen bis zu 100% addieren.
