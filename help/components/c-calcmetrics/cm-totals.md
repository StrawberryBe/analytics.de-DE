---
title: Berechnete Metriken insgesamt
description: Erfahren Sie, wie sich die Summen berechneter Metriken in Analytics-Tools unterscheiden.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Berechnete Metriken insgesamt

Die Anzeige der Gesamtwerte für berechnete Metriken unterscheidet sich zwischen [!DNL Reports & Analytics] und [!DNL Analysis Workspace]. In diesem Abschnitt werden die Unterschiede erläutert.

## Summen berechneter Metriken in [!DNL Reports & Analytics]

Wenn Sie Berichte in anzeigen, [!DNL Reports & Analytics]werden berechnete Metriken immer `n/a` unter der Gesamtsumme angezeigt. Da alle berechneten Metriken benutzerdefiniert sind, ergibt diese Summe in vielen Fällen keinen Sinn. Siehe folgendes Beispiel:

Ihre Organisation hat die berechnete Metrik `orders` `visits` / erstellt, um den Prozentsatz der Besuche zu ermitteln, die etwas auf Ihrer Site gekauft haben. Wenn Sie diese Metrik in einen Produktbericht eingefügt haben, werden mehrere Produkte einer einzigen Bestellung zugeordnet. Und mehrere Produkte werden einem einzelnen Besuch zugeordnet. Wenn in diesem Bericht eine berechnete Metriksumme enthalten ist, ergeben sich folgende Fragen:

| Frage | Antwort |
|---|---|
| Ist es sinnvoll, die Zeilenelemente zusammenzufassen? | Dies ist nicht der Fall, da mehrere Produkte in einer Bestellung enthalten sein können und mehrere Produkte in einem Besuch enthalten sein können. Wenn die Zeileneinträge aggregiert würden, entsprächen die Gesamtbestellungen und Gesamtbesuche nicht den tatsächlichen Gesamtbestellungen und Gesamtbesuchen. |
| Ist es sinnvoll, Gesamtbestellungen und Gesamtbesuche zu tätigen? | Dies ist nicht der Fall, da die Summe nicht mit der Summe der einzelnen Zeileneinträge übereinstimmt. Darüber hinaus werden Gesamtbestellungen und Gesamtbesuche separat berechnet. |

Da es keine logische und konkrete Methode gibt, um zu bestimmen, ob eine berechnete Metrik in der Berichterstellung sinnvoll ist, wird der Metrikgesamtwert vollständig ausgelassen. Wenn Sie eine Gesamtsumme erhalten möchten, führen Sie einen der folgenden Schritte aus:

* Erstellen Sie eine berechnete Metrik, die die Gesamtversionen der Metriken enthält, die Sie einbeziehen möchten.
* Erstellen Sie einen Datenextrahierungsbericht, der eingeplant werden kann.
* Create a data request within [!DNL ReportBuilder].
* Verwendung [!DNL Analysis Workspace] (siehe unten).

## Summen berechneter Metriken in [!DNL Analysis Workspace]

Wenn Sie Daten im Arbeitsbereich für Analysen anzeigen, werden die Summen für berechnete Metriken in den meisten Fällen angezeigt. In einigen Fällen ist eine Gesamtsumme nicht möglich, z. B. wenn die Zeilen des Berichts ein gemischtes Format aufweisen (z. B. Dezimalzahl und Währung).

Wenn Summen angezeigt werden, werden sie häufig serverseitig berechnet, was bedeutet, dass die Gesamtsumme Metriken wie Besuche oder Besucher dedupliziert. Unter bestimmten Umständen werden berechnete Metriken clientseitig generiert, indem sie in Tabellenzeilen zusammengefasst werden. Das bedeutet, dass die Summe keine Metriken wie Besuche oder Besucher dedupliziert. Dies geschieht:

* Wenn [statische Zeilen](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) in Freiform-Tabellen verwendet werden und die Option "Als Summe der aktuellen Zeilen **** anzeigen"aktiviert ist (Standard).
* In der [Donut-Visualisierung](/help/analyze/analysis-workspace/visualizations/donut.md), sodass Zahlen bis zu 100%.
