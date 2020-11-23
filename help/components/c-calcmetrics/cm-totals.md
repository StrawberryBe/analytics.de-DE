---
title: Berechnete Metriken insgesamt
description: Erfahren Sie, wie sich die Summen berechneter Metriken in Analytics-Werkzeugen unterscheiden.
translation-type: tm+mt
source-git-commit: bbe2b96960fd5aa6df331a77fdf5b04a769b6e84
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 94%

---


# Berechnete Metriken insgesamt

Die Anzeige der berechneten Metriken insgesamt unterscheidet sich zwischen [!DNL Reports & Analytics] und [!DNL Analysis Workspace]. In diesem Abschnitt werden die Unterschiede erläutert.

## Berechnete Metriken insgesamt in [!DNL Reports & Analytics]

Wenn Sie Berichte in [!DNL Reports & Analytics] anzeigen, wird für berechnete Metriken immer `n/a` unter der Summe angezeigt. Da alle berechneten Metriken benutzerspezifisch sind, ergibt diese Summe in vielen Fällen keinen Sinn. Siehe folgendes Beispiel:

Ihre Organisation hat die berechnete Metrik `orders`/`visits` erstellt, um den Prozentsatz der Besuche zu ermitteln, bei denen etwas auf Ihrer Site gekauft wurde. Wenn Sie diese Metrik in einen Produktbericht eingefügt haben, werden mehrere Produkte einer einzigen Bestellung zugeordnet. Außerdem werden mehrere Produkte einem einzelnen Besuch zugeordnet. Wenn in diesem Bericht eine berechnete Metriksumme enthalten ist, ergeben sich folgende Fragen:

| Frage | Antwort |
|---|---|
| Ist es sinnvoll, die Zeileneinträge zu addieren? | Dies ist nicht der Fall, da mehrere Produkte in einer Bestellung enthalten sein können und mehrere Produkte in einem Besuch enthalten sein können. Wenn die Zeileneinträge aggregiert werden, entsprechen die Bestellungen insgesamt und Besuche insgesamt nicht den tatsächlichen Bestellungen insgesamt und Besuchen insgesamt. |
| Ist es sinnvoll, die Bestellungen gesamt und die Besuche gesamt zu verwenden? | Dies ist nicht der Fall, da die Summe nicht mit der Summe der einzelnen Zeileneinträge übereinstimmt. Darüber hinaus handelt es sich bei den Bestellungen insgesamt und Besuchen insgesamt um vollkommen separate berechnete Metriken. |

Da es keine logische und konkrete Methode gibt, um zu bestimmen, ob eine berechnete Metrik in der Berichterstellung Sinn macht, wird der Metrikgesamtwert vollständig ausgelassen. Wenn Sie eine Gesamtsumme erhalten möchten, führen Sie einen der folgenden Schritte aus:

* Erstellen Sie eine berechnete Metrik, die die Gesamtversionen der Metriken enthält, die Sie einbeziehen möchten.
* Erstellen Sie einen Datenextraktionsbericht, der geplant werden kann.
* Erstellen Sie eine Datenanforderung in [!DNL ReportBuilder].
* Verwenden Sie [!DNL Analysis Workspace] (siehe unten).

## Berechnete Metriken insgesamt in [!DNL Analysis Workspace]

Wenn Sie Daten in Analysis Workspace anzeigen, werden die berechneten Metriken insgesamt in den meisten Fällen angezeigt. In einigen Fällen ist die Bereitstellung einer Gesamtsumme nicht möglich, beispielsweise wenn die Zeilen des Berichts unterschiedliche Formate aufweisen (z. B. Dezimalzahl und Währung).

Wenn Summen angezeigt werden, werden sie häufig serverseitig berechnet, was bedeutet, dass die Summe Metriken wie Besuche oder Besucher dedupliziert. Unter bestimmten Umständen werden berechnete Metriken clientseitig generiert, indem sie über Tabellenzeilen hinweg summiert werden. Das bedeutet, dass die Summe keine Metriken wie Besuche oder Besucher dedupliziert. Dies geschieht:

* Wenn [statische Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) in Freiform-Tabellen verwendet werden und die Option **[!UICONTROL Als Summe der aktuellen Zeilen anzeigen]** aktiviert ist (Standard).
* In der [Donut-Visualisierung](/help/analyze/analysis-workspace/visualizations/donut.md), sodass die Summe der Zahlen 100 % ergibt.

Weitere Informationen zu den Gesamtsummen in Analysis Workspace finden Sie unter [Arbeitsbereichsummen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html?lang=en#static-row-total).

