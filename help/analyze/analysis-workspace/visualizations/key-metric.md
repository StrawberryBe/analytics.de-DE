---
description: Verwenden Sie die Visualisierung der Schlüsselmetrik-Zusammenfassung, um die Leistung der Kennzahlen über zwei Timelines hinweg zu vergleichen.
title: Zusammenfassung einer Schlüsselmetrik
feature: Visualizations
role: User, Admin
exl-id: c74e77ff-15d6-48f1-a845-85bdf3444c3a
source-git-commit: 1843989f77482152adeaee1f1c9e523d0c55dc21
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 100%

---

# Zusammenfassung einer Schlüsselmetrik

Mit der [!UICONTROL Zusammenfassung der Schlüsselmetrik] können Sie sehen, wie eine wichtige Metrik innerhalb eines einzigen Zeitrahmens trendet. Außerdem können Sie damit die Leistung von Metriken über zwei Zeitrahmen hinweg vergleichen. Sie bietet die Vorteile mehrerer Visualisierungen, die in einer Visualisierung kombiniert werden:

* **[!UICONTROL Linie]** Visualisierungen, die zeigen, wie die Metrik für die primären und Vergleichsdatumsbereiche trendet.

* **[!UICONTROL Zusammenfassende prozentuale Änderung]**, die die Zunahme oder Abnahme der Metrik zwischen dem primären und dem Vergleichsdatumsbereich anzeigt

* Aktueller Gesamtwert ([!UICONTROL **Summenzahl**]) für die Metrik

## Anwendungsbeispiele

Diese Visualisierung eignet sich für eine Vielzahl gängiger Anwendungsfälle, darunter:

* Ein Analyst, der versucht zu verstehen, wie die Entwicklung der Chancen in diesem Monat im Vergleich zum gleichen Zeitraum des letzten Jahres aussah.

* Ein Vermarkter, der untersucht, wie sich die Lead-Generierung für einen bestimmten Lead-Typ von diesem Monat zum letzten Monat verändert hat.

* Eine Führungskraft, die wissen möchte, wie sich die Buchungen in diesem Quartal im Vergleich zum letzten Quartal verändert haben.

## Konfigurieren der Zusammenfassung einer Schlüsselmetrik

1. Ziehen Sie die Visualisierung **[!UICONTROL Zusammenfassung einer Schlüsselmetrik]** aus dem Menü **[!UICONTROL Visualisierungen]** in der linken Leiste in ein Bedienfeld.

1. Konfigurieren Sie die Visualisierung, indem Sie eine Metrik, einen primären Datumsbereich, einen Vergleichsdatumsbereich und ein Segment (falls gewünscht) auswählen:

   ![](assets/key-metric-config.png)

   | Konfigurationseinstellungen | Definition |
   | --- | --- |
   | **[!UICONTROL Metrik]** | Wählen Sie die Metrik aus, die Sie überprüfen möchten. Alle Metriken werden unterstützt. |
   | **[!UICONTROL Primärer Datumsbereich]** | Der aktuelle Datumsbereich für die Freiformtabelle. |
   | **[!UICONTROL Vergleichsdatumsbereich]** | Der Datumsbereich, mit dem Sie den primären Datumsbereich vergleichen möchten. |
   | **[!UICONTROL Segment (optional)]** | Jedes Segment, an dem Sie für diese Zusammenfassung interessiert sind. |

   {style=&quot;table-layout:auto&quot;}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Ausgabe anzeigen

![](assets/key-metric-output.png)

Bitte beachten Sie:

* Der Kantengraph **[!UICONTROL Vorheriger Zeitraum]** (immer grau dargestellt) entspricht dem **[!UICONTROL Vergleichsdatumsbereich]** im Konfigurationsschritt.

* Wenn während der Konfiguration kein Vergleichsdatumsbereich angegeben ist, oder in den Visualisierungseinstellungen ausgeblendet wird, wird nur das Liniendiagramm für den primären Datumsbereich angezeigt. Die Änderung der Zusammenfassung wird ausgeblendet.

* Von hier aus können Sie mit dem Mauszeiger über die Liniendiagramme fahren, um die Statistiken für einzelne Tage zu sehen:

![](assets/key-metric-output2.png)

## Visualisierungseinstellungen

Die Zusammenfassung der Schlüsselmetriken bietet mehrere flexible Einstellungen, um eine bessere Berichterstellung und Kommunikation wichtiger Metriken zu ermöglichen. Die Einstellungen können über das Zahnradsymbol in der oberen rechten Ecke der Visualisierung aufgerufen werden.

![](assets/key-metric-settings.png)

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Prozentuale Veränderung betonen]** | Anzeige der Zusammenfassungsänderung in hervorgehobener fetter Schrift in der Mitte der Visualisierung |
| **[!UICONTROL Zahlenwert hervorheben]** | Anzeige der Zusammenfassungsanzahl in hervorgehobener fetter Schrift in der Mitte der Visualisierung |
| **[!UICONTROL Legende eingeblendet]** | Ein- oder Ausblenden der Legende am unteren Rand der Visualisierung |
| **[!UICONTROL Anmerkungen anzeigen]** | Von einem Administrator hinzugefügte Anmerkungen anzeigen oder ausblenden |
| **[!UICONTROL Sparklines anzeigen]** | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn sie ausgeblendet ist, wird die Legende so geändert, dass sie keinen visuellen Bezug mehr zu den Linien hat. |
| **[!UICONTROL Min. und Max. für Wortgrafiken anzeigen]** | Ein- und Ausblenden von Minimal- und Maximalwerten in Primär- und Vergleichsliniendiagrammen |
| **[!UICONTROL Vergleich anzeigen]** | Vergleichsdaten ein- oder ausblenden. Wenn diese Option ausgeblendet ist, werden sowohl das Vergleichszeilendiagramm als auch die Zusammenfassungsänderung der Objekte ausgeblendet. |
| **[!UICONTROL Gesamtanzahl anzeigen]** | Zusammenfassungsnummer anzeigen oder ausblenden |
| **[!UICONTROL Rohdifferenz anzeigen]** | Rohdifferenz zwischen dem Gesamtwert der Metrik im primären Datumsbereich und im sekundären Datumsbereich anzeigen oder ausblenden |
| **[!UICONTROL Wert kürzen]** | Abkürzen von Zahlenwerten zur Vereinfachung der kommunizierten Einblicke (z. B. 20.000 -> 20K) |

## Visualisierung bearbeiten

Nach dem Erstellen der Visualisierung können Sie die ursprüngliche Konfiguration noch bearbeiten.

1. Klicken Sie oben rechts in der Visualisierung auf das Stiftsymbol (neben dem Zahnradsymbol für Einstellungen).

   ![](assets/edit-icon.png)

   Sie gelangen nun zurück zur ursprünglichen Konfigurationsansicht.

1. Ändern Sie die Metrik, den primären Datumsbereich, den Vergleichsdatumsbereich oder das Segment nach Belieben.
