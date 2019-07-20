---
description: Schritte, die Sie durchführen können, um die Verwendung von Datenquellen vorzubereiten.
seo-description: Schritte, die Sie durchführen können, um die Verwendung von Datenquellen vorzubereiten.
seo-title: Vorbereiten der Verwendung von Datenquellen
solution: Analytics
subtopic: Datenquellen
title: Vorbereiten der Verwendung von Datenquellen
topic: Entwickler und Implementierung
uuid: 876 ea 069-574 b -4 e 23-93 b 7-e 3828 bfd 90 f 5
translation-type: tm+mt
source-git-commit: 887f48d2ea5f21b7db95a1a8f716f7da9cf43662

---


# Vorbereitung der Verwendung von Data Sources

Schritte, die Sie durchführen können, um die Verwendung von Datenquellen vorzubereiten.

* [Identifizieren und Benennen der Metriken](../../import/c-data-sources/datasrc-preparing.md#section_0D1DA6D7768E4C4CB6E9A2F4639C0135)
* [Identifizieren von Datendimensionen](../../import/c-data-sources/datasrc-preparing.md#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A)
* [Kampagnen-Trackingcode](../../import/c-data-sources/datasrc-preparing.md#section_468222796FF449ABAA90D88EB3264CB1)
* [Transaktions-ID](../../import/c-data-sources/datasrc-preparing.md#section_D9513C1204B7496C9B738C5B12CCCFC7)
* [Identifizieren eines gültigen Datumsbereichs für Datenquelle-Daten](../../import/c-data-sources/datasrc-preparing.md#section_03AAB1291BDC4403BDC50905A78FDB71)

## Identifizieren und Benennen der Metriken {#section_0D1DA6D7768E4C4CB6E9A2F4639C0135}

It is important to understand the metrics or measurements that are contained in your data sources, such as *`Off-line Sales Revenue by Product`*, *`Returns by Product`*, or *`Ad Impressions by Campaign`*. Dies sind die Namen, die Sie mit Berichtsmetriken (Ereignisse, Props und eVars) verbinden können.

Nachdem Sie die entsprechenden Metrik-zu-Ereignis-Zuordnungen für die Data Sources-Daten bestimmt haben, benennen Sie die Ereignisse mit beschreibenden Namen für die zugeordnete Data Sources-Metrik um.

Siehe [Erfolgsereignisse](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=success_event) in der Hilfe der Admin Tools.

>[!NOTE]
>
>Adobe empfiehlt dringend, neue, leere Ereignisse mit Datenquellen-Daten zu verwenden. In seltenen Fällen kann es sinnvoll sein, ein bereits vorhandenes Ereignis zu verwenden.

## Identifizieren von Datendimensionen {#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A}

Identifizieren und erfassen Sie Daten (Berichte), die Sie zum Aufschlüsseln der über Data Sources importierten Metriken verwenden möchten. Diese Daten werden auch als *`data dimensions`*.

Wenn beispielsweise eine Data Sources-Metrik Anzeigenimpressionen misst, ist Ihre Datendimension wahrscheinlich der Kampagnen-Trackingcode. Wenn Sie die Offline-Verkäufe messen, möchten Sie u. U. den Produktcode (oder die SKU) als Datendimension verwenden.

Sie können für eine Metrik mehrere Datendimensionen definieren, aber jede Metrik muss über einen entsprechenden Wert oder eine Kombination aus Werten für jede zugeordnete Datendimension verfügen. Wenn Sie zum Beispiel eine Offline-Verkaufsmetrik importieren und sie *`Product`* und *`Partner`* Datendimensionen muss die Offline-Verkaufsmetrik für jede Kombination von Produkt und Partner relevant sein (z. B. Gesamtumsatz).

>[!NOTE]
>
>Es ist möglich, Gesamtmetriken zu importieren, die nicht nach einer Datendimension aufgeschlüsselt werden können.

Wenn Sie die zu verwendende Datendimension mit einer Datenquelle definiert haben, integrieren Sie die Dimensionsdaten in Marketingberichte, indem Sie sie einer Variablen zuordnen. Verwenden Sie entweder Standardberichte (z. B. Produkt, Trackingcode, Keyword) oder Konversion-Traffic-Variablen (eVars).

Wenn Sie eVars verwenden, können Sie entweder vorhandene eVars oder neue eVars als Datendimensionen verwenden. Stellen Sie nach Auswahl einer eVar für den Empfang einer Datendimension aus Data Sources sicher, dass Sie sie ordnungsgemäß benennen.

Siehe [Erfolgsereignisse](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=success_event) in der Hilfe zu Analytics.

## Kampagnen-Trackingcode {#section_468222796FF449ABAA90D88EB3264CB1}

Sie können nicht nur Erfolgsereignisse, sondern optional auch zugeordnete eVar-Werte importieren. Wenn Sie die Online-Aktivität mit einem Kampagnen-Trackingcode verfolgen und Kampagnen-Trackingcodes für die Offline-Metriken haben, können Sie die Metriken mit Kampagnen-Trackingcodes importieren. Auf diese Weise können Sie Online- und Offline-Metriken in Kampagnenberichten anzeigen.

Wenn Sie Data Sources-Metriken ohne zugeordneten eVar-Wert importieren, können die Datenquelle-Metriken nicht nach eVars aufgeschlüsselt angezeigt werden. Stattdessen werden ausschließlich Gesamtmetriken angezeigt.

## Transaktions-ID {#section_D9513C1204B7496C9B738C5B12CCCFC7}

Mit einer Transaktions-ID wird ein Online-Ereignis mit einem Offline-Ereignis verbunden.

## Identifizieren eines gültigen Datumsbereichs für Datenquelle-Daten {#section_03AAB1291BDC4403BDC50905A78FDB71}

Nachdem Sie die Data Sources-Metriken (benutzerspezifische Ereignisse) und Datendimensionen (eVars) definiert haben, müssen Sie den Datumsbereich der Datenquelle-Daten überprüfen, die Sie importieren möchten. Sie können keine Data Sources-Daten importieren, die außerhalb des Bereichs der vorliegenden Berichtsdaten liegen.

Sie können beispielsweise keine Datenquelle-Daten aus einem Zeitraum vor der Implementierung der Online-Datenverfolgung importieren. Data Sources-Daten sollten in Tage unterteilt werden.
