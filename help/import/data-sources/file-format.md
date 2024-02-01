---
title: Dateiformat der Datenquelle
description: Ordnungsgemäßes Generieren einer Datei für die Verwendung in Datenquellen.
exl-id: 6632b970-e931-4272-a69b-c1130ad6475f
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 5%

---

# Dateiformat der Datenquelle

Datenquellendateien haben die folgenden Eigenschaften:

* Die Datei befindet sich in `.txt` Format.
* Kommentierte Zeilen beginnen mit &quot;`#`&#39; und sind optional.
* Die erste Zeile ohne Kommentar enthält die Header der Datei.
* Der erste Wert jeder Zeile ist das Datum, das das Format `MM/DD/YYYY` oder `MM/DD/YYYY/HH/mm/SS`.
* Die Werte in jeder Zeile, einschließlich der Kopfzeilen, sind tabulatorgetrennt.
* Jede Zeile muss mindestens eine Dimension und eine Metrik aufweisen.

## Kommentare

Jede Zeile, die mit &quot;`#`&quot; ist ein Kommentar. Beim Herunterladen einer Datenquellenvorlagendatei sind die ersten beiden Zeilen Kommentare.

* Der erste Kommentar gibt den Vorlagentyp an, den Sie für die Datenquelle konfiguriert haben, die Backend-Benutzer-ID, mit der die Datenquelle erstellt wurde, und die Datenquellen-ID.
* Der zweite Kommentar enthält Anzeigenamen für die einzelnen Header, die in der Vorlagendatei enthalten sind.

Alle Kommentarzeilen werden bei der Dateiverarbeitung von Adobe ignoriert, sodass Sie die Vorlagenkommentare entfernen oder Ihre eigenen in der Datei hinzufügen können. Nur vollständige Zeilen können kommentiert werden. Sie können einzelne Felder oder Zeilen nicht auskommentieren.

## Kopfzeilen

Beim Hochladen von Datenquellendateien sind Spaltenüberschriften erforderlich. Bei diesen Spaltenüberschriften wird nicht zwischen Groß- und Kleinschreibung unterschieden, es sind jedoch erforderliche Leerzeichen erforderlich (z. B. `eVar1` ist eine ungültige Kopfzeile, während `EVAR 1` ist gültig). Spaltenüberschriften gelten für alle Report Suites. Verwenden Sie die folgenden Tabellen, um sicherzustellen, dass jeder Header in Ihrer Datenquellendatei korrekt festgelegt ist.

>[!TIP]
>
>Sie können eine Datenquellendatei von Grund auf neu erstellen, wenn Sie die richtigen Header in Ihre Datenquellendatei aufnehmen. Die Anzahl der Header, die in einer Datei enthalten sein können, ist nicht beschränkt. Jede Zeile darf jedoch maximal 4096 Byte enthalten.

| Dimension | Datenquellenüberschrift |
| --- | --- |
| [Kategorie](/help/components/dimensions/category.md) | `Category` |
| [eVar1 - eVar250](/help/components/dimensions/evar.md) | `Evar 1` - `Evar 250` |
| [Marketingkanal](/help/components/dimensions/marketing-channel.md) | `Marketing Channel` |
| [Marketingkanaldetails](/help/components/dimensions/marketing-detail.md) | `Marketing Channel Detail` |
| [Produkt](/help/components/dimensions/product.md) | `Product` |
| [Trackingcode](/help/components/dimensions/tracking-code.md) | `Tracking Code` |
| [Transaktions-ID](/help/implement/vars/page-vars/transactionid.md) | `transactionID` |
| [Postleitzahl](/help/components/dimensions/zip-code.md) | `Zip` |

{style="table-layout:auto"}

Dimensionen und Metriken werden in dieselbe Kopfzeile verschoben.

| Metrik | Datenquellenüberschrift |
| --- | --- |
| [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md) | `Cart Adds` |
| [Entnahme aus Warenkorb](/help/components/metrics/cart-removals.md) | `Cart Removes` |
| [Warenkorbansicht](/help/components/metrics/cart-views.md) | `Cart Views` |
| [Warenkorb](/help/components/metrics/carts.md) | `Cart Opens` |
| [Checkouts](/help/components/metrics/checkouts.md) | `Checkouts` |
| [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) | `Event 1` - `Event 1000` |
| [Bestellungen](/help/components/metrics/orders.md) | `Orders` |
| [Umsatz](/help/components/metrics/revenue.md) | `Price` |
| [Einheiten](/help/components/metrics/units.md) | `Quantity` |

{style="table-layout:auto"}

Adobe unterstützt keine Datenquellen für andere Dimensionen oder Metriken. Wenn Variablen erforderlich sind, die über das in den obigen Tabellen aufgeführte hinausgehen, sollten Sie die Variable [Bulk-Dateneinfüge-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/) anstatt.

## Datum

Der erste Wert in jeder Zeile **must** das Datum. Das Datumsformat muss eines der folgenden Formate aufweisen:

* **`MM/DD/YY/HH/mm/SS`**
* **`MM/DD/YY`**

Wenn die Stunden/Minuten/Sekunden nicht angegeben werden, wird der Zeitstempel für diesen Tag automatisch auf 23 Uhr festgelegt.

Eine Datenquellendatei unterstützt bis zu 90 eindeutige Tage. Wenn Sie mehr als 90 eindeutige Tage in einen Upload einbeziehen möchten, teilen Sie Ihre Daten in mehrere Dateien auf.

## Dimension und Metrikdaten

Nachfolgende Werte nach dem Datum in jeder Zeile enthalten die Daten, die Sie hochladen möchten. Jede Zeile entspricht dem jeweiligen Zeitstempel. Stellen Sie sicher, dass in jeder Zeile dieselbe Anzahl von Registerkarten vorhanden ist. Die Spalten können in beliebiger Reihenfolge angeordnet werden. Stellen Sie sicher, dass die Daten in den einzelnen Zeilen mit den Kopfzeilen oben übereinstimmen. Die maximale Datenmenge, die eine Zeile enthalten kann, beträgt 4096 Byte.

Dimension-Daten dürfen keine Semikolons (`;`). Zeilen, die Semikolons enthalten, werden übersprungen.

## Nächste Schritte

[Datei-Upload](file-upload.md): Erfahren Sie, wie Sie eine Datenquellendatei zur Erfassung per Adobe hochladen.
