---
title: Dynamische und statische Dimensionswerte
description: Interaktion mit dynamischen und statischen Dimensionswerten in Tabellen.
translation-type: tm+mt
source-git-commit: c21f16148bd8d23f8ba912662827bc636dda6ebc
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 2%

---


# Werte für dynamische und statische Dimensionen in Freiform-Tabellen

In Freiform-Tabellen können die Zeilen und Spalten verschiedene Komponentenwerte enthalten. Diese Werte können dynamisch (zeitabhängig) oder statisch (nicht zeitabhängig) sein, je nach Analyse, die Sie erstellen möchten.

## Dynamische Dimensionswerte

Dynamische Dimensionswerte ändern sich mit der Zeit und hängen von der in der Freiformtabelle sortierten Metrik ab. Dynamische Dimensionswerte werden bevorzugt, wenn Sie die obersten Elemente für einen bestimmten Zeitraum analysieren möchten.

Wenn Sie eine Dimension in eine Freiformtabelle ablegen, werden dynamische Zeilen zurückgegeben. Sie stellen die obersten Elemente dar, die der Dimension für eine bestimmte Metrik und einen bestimmten Zeitraum entsprechen. Sie können eine Dimension auch in Freiform-Tabellenspalten ablegen und die Dimension wird automatisch in die fünf wichtigsten Dimensionswerte erweitert.

Wenn Sie beispielsweise die Dimension &quot;Browsertyp&quot;in die Tabelle ziehen, werden die oberen Browsertyp-Dimensionswerte (z. B. Microsoft, Apple, Google usw.) dynamisch zu den Tabellenzeilen zurückkehren. Wenn sie in eine Spalte abgelegt werden, werden die obersten 5 Browsertyp-Dimensionswerte dynamisch zurückgegeben.

Dynamische Dimensionswerte haben die Option &quot;Zeilenfilter&quot;. Die Symbole &quot;Sperren&quot;und &quot;X&quot;sind **nicht** vorhanden.

## Statische Dimensionswerte

Statische Dimensionswerte ändern sich nicht mit der Zeit. Es handelt sich dabei um feste Komponenten, die immer in einer Freiform-Tabelle zurückgegeben werden. Statische Dimensionswerte werden bevorzugt, wenn Sie immer dasselbe Element analysieren möchten, unabhängig davon, ob es sich um bestimmte Kampagnen oder bestimmte Wochentage handelt.

Jedes Mal, wenn Sie bestimmte Komponentenwerte (Dimension, Metrik, Segment, Datumsbereich) manuell in eine Tabelle eingeben, ist das Ergebnis eine statische Liste von Zeilen oder Spalten. Statische Dimensionswerte können auch erstellt werden, wenn Sie Folgendes auswählen:

* Klicken Sie in den Zeilen mit der rechten Maustaste > Nur ausgewählte Zeilen [!UICONTROL anzeigen]
* Klicken Sie in Spalten mit der rechten Maustaste > Element statisch [!UICONTROL machen]

Wenn Sie beispielsweise über bestimmte Browsertyp-Elemente wie Microsoft und Apple ziehen, werden diese beiden Elemente immer in die Tabelle gezogen.

Statische Dimensionswerte haben **nicht** die Option zum Zeilenfilter. Stattdessen sind für jedes Element Sperren- und X-Symbole vorhanden. Klicken Sie auf das X-Symbol, um diesen Dimensionswert aus der Tabelle zu entfernen.

## Gemischte Dimensionswerte

Dimensionswerte aus verschiedenen Dimensionen können derselben Tabelle hinzugefügt werden. In diesen Fällen steht in der Kopfzeile der Zeile &quot;Gemischte Dimensionen&quot;. Diese Dimensionswerte sind statisch. Fügen Sie beispielsweise bestimmte Dimensionswerte aus der Dimension &quot;Browsertyp&quot;und andere Dimensionswerte aus der Dimension &quot;Browser&quot;hinzu.

## Freiformsummen

Dynamische und statische Zeilen verhalten sich in der Freiformsumme unterschiedlich. Standardmäßig:

* Dynamische Zeilen werden serverseitige und dekorative Metriken wie Besuche oder Besucher summiert
* Statische Zeilen werden clientseitig zusammengefasst und entfernen **keine** Metriken.

[Erfahren Sie mehr über die Gesamtoptionen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/workspace-totals.html) von Workspace für dynamische und statische Zeilen.
