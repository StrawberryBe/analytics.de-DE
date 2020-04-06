---
description: Schritte, die Sie durchführen können, um die Verwendung von Datenquellen vorzubereiten.
subtopic: Data sources
title: Vorbereiten auf die Verwendung von Data Sources
topic: Developer and implementation
uuid: 876ea069-574b-4e23-93b7-e3828bfd90f5
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Vorbereiten auf die Verwendung von Data Sources

Schritte, die Sie durchführen können, um die Verwendung von Datenquellen vorzubereiten.

* [Identifizieren und Benennen der Metriken ](/help/import/c-data-sources/datasrc-preparing.md#section_0D1DA6D7768E4C4CB6E9A2F4639C0135)
* [Identifizieren von Datendimensionen](/help/import/c-data-sources/datasrc-preparing.md#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A)
* [Kampagnen-Trackingcode](/help/import/c-data-sources/datasrc-preparing.md#section_468222796FF449ABAA90D88EB3264CB1)
* [Transaktions-ID](/help/import/c-data-sources/datasrc-preparing.md#section_D9513C1204B7496C9B738C5B12CCCFC7)
* [Identifizieren eines gültigen Datumsbereichs für Datenquelle-Daten ](/help/import/c-data-sources/datasrc-preparing.md#section_03AAB1291BDC4403BDC50905A78FDB71)

## Identifizieren und Benennen der Metriken  {#section_0D1DA6D7768E4C4CB6E9A2F4639C0135}

Sie müssen die Metriken oder Messungen verstehen, die in den Datenquellen enthalten sind, beispielsweise *`Off-line Sales Revenue by Product`*, *`Returns by Product`* oder *`Ad Impressions by Campaign`*. Dies sind die Namen, die Sie mit Berichtsmetriken (Ereignissen, Props und eVars) verknüpfen können.

Benennen Sie nach der Ermittlung der entsprechenden Metrik-zu-Ereignis-Zuordnungen für die Data Sources-Daten die Ereignis mit beschreibenden Namen um, die für die zugehörige Data Sources-Metrik geeignet sind.

Siehe [Erfolgserlebnisse](https://marketing.adobe.com/resources/help/de_DE/reference/success_event.html) in der Hilfe zu den Admin Tools.

>[!NOTE] Adobe empfiehlt dringend den Einsatz von neuen, leeren Ereignissen mit Data Sources-Daten. In seltenen Fällen kann es sinnvoll sein, ein bereits bestehendes Ereignis zu verwenden.

## Identifizieren von Datendimensionen {#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A}

Identifizieren und erfassen Sie die Daten (Berichte), die Sie zur Unterteilung der über Data Sources importierten Metriken verwenden möchten. Diese Daten werden auch als  *`data dimensions`*.

Wenn beispielsweise eine Data Sources-Metrik Anzeigenimpressionen misst, ist Ihre Datendimension wahrscheinlich der Kampagnen-Trackingcode. Wenn Sie Offline-Verkäufe messen, sollten Sie Produktcode (oder SKU) als Datendimension verwenden.

Sie können für eine Metrik mehrere Datendimensionen definieren, aber jede Metrik muss über einen entsprechenden Wert oder eine Kombination aus Werten für jede zugeordnete Datendimension verfügen. Wenn Sie zum Beispiel eine Offline-Verkaufsmetrik importieren und sie  *`Product`*- und *`Partner`*-Datendimensionen zuordnen, muss die Offline-Verkaufsmetrik für beide Kombinationen aus Produkt und Partner (z. B. Gesamtumsatz) relevant sein.

>[!NOTE] Sie können Gesamtmetriken importieren, die nicht mit einer Datendimension unterteilt werden können.

Nachdem Sie die Datendimensionen definiert haben, die mit einer Datenquelle verwendet werden sollen, integrieren Sie die Dimensionsdaten in die Marketing-Berichte, indem Sie sie einer Variablen zuordnen. Verwenden Sie entweder Standardberichte (z. B. Produkt, Rückverfolgungscode, Suchbegriff) oder Konversions-Traffic-Variablen (eVars).

Bei Verwendung von eVars können Sie entweder vorhandene eVars oder neue eVars als Datendimensionen verwenden. Nachdem Sie eine eVar ausgewählt haben, um eine Datendimension aus Data Sources zu erhalten, sollten Sie sicherstellen, dass Sie sie entsprechend benennen.

Siehe [Erfolgsereignisse](https://marketing.adobe.com/resources/help/de_DE/reference/success_event.html) in der Analytics-Hilfe.

## Kampagnen-Trackingcode {#section_468222796FF449ABAA90D88EB3264CB1}

Neben dem Import von Erfolgswerten können Sie optional auch zugehörige eVar-Ereignis importieren. Wenn Sie beispielsweise die Online-Aktivität mit einem Kampagne-Trackingcode verfolgen und Kampagnen-Trackingcodes für die Offlinemetriken haben, können Sie die Metriken mit Kampagne-Trackingcodes importieren. Dieser Ansatz ermöglicht die Ansicht von Online- und Offlinemetriken in Kampagnen-Berichten.

Wenn Sie keine Datenquellen-Metriken mit einem zugehörigen eVar-Wert importieren, können Sie keine Datenquellen-Metriken, aufgeschlüsselt nach eVars, Ansicht werden. Stattdessen können Sie nur Summenmetriken sehen.

## Transaktions-ID {#section_D9513C1204B7496C9B738C5B12CCCFC7}

Die Transaktions-ID wird verwendet, um ein Online-Ereignis mit einem Offline-Ereignis zu verbinden.

## Identifizieren eines gültigen Datumsbereichs für Datenquelle-Daten  {#section_03AAB1291BDC4403BDC50905A78FDB71}

Nachdem Sie die Datenquellen-Metriken (benutzerdefinierte Ereignis) und Datendimensionen (eVars) definiert haben, überprüfen Sie den Datumsbereich der Datenquellen-Daten, die Sie importieren möchten. Sie können keine Datenquellen importieren, die außerhalb des Bereichs der vorhandenen Berichte liegen.

Sie können beispielsweise keine Datenquellendaten aus einer Zeit importieren, in der Sie die Online-Datenverfolgung implementiert haben. Die Datenquellen-Daten sollten nach Tagen aufgeschlüsselt werden.
