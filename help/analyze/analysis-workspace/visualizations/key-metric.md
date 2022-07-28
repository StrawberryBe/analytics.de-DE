---
description: Verwenden Sie die Visualisierung der Schlüsselmetrik-Zusammenfassung, um die Metrikleistung über zwei Zeitleisten hinweg zu vergleichen.
title: Zusammenfassung einer Schlüsselmetrik
feature: Visualizations
role: User, Admin
source-git-commit: a126f51c82cf7b23f4e03134c2d870d216dadc47
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 6%

---


# Zusammenfassung einer Schlüsselmetrik

>[!NOTE]
>
>Diese Funktion wird derzeit [eingeschränkt getestet](/help/release-notes/releases.md).

Mit der Visualisierung der Schlüsselmetrik-Zusammenfassung können Sie sehen, wie eine wichtige Metrik innerhalb eines einzigen Zeitrahmens in die Trends eingeht. Außerdem können Sie damit die Leistung von Metriken über zwei Zeitrahmen hinweg vergleichen. Sie bietet die Vorteile mehrerer Visualisierungen, die in einer Visualisierung kombiniert werden:

* **[!UICONTROL Linie]** Visualisierungen, die zeigen, wie die Metrik Trends für die primären und Vergleichsdatumsbereiche darstellt

* **[!UICONTROL Prozentänderung der Zusammenfassung]** , der die Metrikerhöhung oder -verringerung zwischen den primären und den Vergleichsdatumsbereichen anzeigt.

* Aktueller Gesamtwert ([!UICONTROL **Zusammenfassungsnummer**]) für die Metrik

## Anwendungsbeispiele

Diese Visualisierung behandelt eine Vielzahl gängiger Anwendungsfälle, darunter:

* Ein Analytiker versuchte zu verstehen, wie die Schaffung von Chancen in diesem Monat im Vergleich zum gleichen Zeitrahmen im letzten Jahr aussah.

* Ein Marketer, der untersucht, wie sich die Lead-Generierung für einen bestimmten Lead-Typ von diesem Monat zum letzten Monat verändert hat.

* Ein Geschäftsführer möchte verstehen, wie sich neue Buchungen von diesem Quartal zum letzten Quartal änderten.

## Konfigurieren der Zusammenfassung der Schlüsselmetriken

1. Ziehen Sie die **[!UICONTROL Zusammenfassung der Schlüsselmetriken]** Visualisierung aus der **[!UICONTROL Visualisierungen]** in der linken Leiste in ein Bedienfeld.

1. Konfigurieren Sie die Visualisierung, indem Sie eine Metrik, einen primären Datumsbereich, einen Vergleichsdatumsbereich und ein Segment auswählen (falls gewünscht):

   ![](assets/key-metric-config.png)

   | Konfigurationseinstellungen | Definition |
   | --- | --- |
   | **[!UICONTROL Metrik]** | Wählen Sie die Metrik aus, die Sie untersuchen möchten. Alle Metriken werden unterstützt. |
   | **[!UICONTROL Primärer Datumsbereich]** | Der aktuelle Datumsbereich für die Freiformtabelle. |
   | **[!UICONTROL Vergleichsdatumsbereich]** | Der Datumsbereich, mit dem Sie den primären Datumsbereich vergleichen möchten. |
   | **[!UICONTROL Segment (optional)]** | Jedes Segment, an dem Sie für diese Zusammenfassung interessiert sind. |

   {style=&quot;table-layout:auto&quot;}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Ausgabe anzeigen

![](assets/key-metric-output.png)

Bitte beachten Sie:

* Die **[!UICONTROL Vorheriger Zeitraum]** Kantengraph (immer grau dargestellt) entspricht dem **[!UICONTROL Vergleichsdatumsbereich]** im Konfigurationsschritt.

* Wenn ein Vergleichsdatumsbereich während der Konfiguration nicht ausgewählt oder in den Visualisierungseinstellungen ausgeblendet wird (siehe Einstellungen unten), wird nur das Liniendiagramm für den primären Datumsbereich angezeigt. Die Zusammenfassungsänderung wird ausgeblendet.

* Von hier aus können Sie mit dem Mauszeiger über die Liniendiagramme fahren, um die Statistiken für einzelne Tage anzuzeigen:

![](assets/key-metric-output2.png)

## Visualisierungseinstellungen

Die Zusammenfassung der Schlüsselmetriken bietet mehrere flexible Einstellungen, um eine bessere Berichterstellung und Kommunikation wichtiger Metriken zu ermöglichen. Die Einstellungen können über das Zahnradsymbol in der oberen rechten Ecke der Visualisierung aufgerufen werden.

![](assets/key-metric-settings.png)

| Einstellung | Beschreibung |
| --- | --- |
| Prozentuale Veränderung hervorheben | Änderung der Zusammenfassung im markanten fett gedruckten Typ in der Mitte der Visualisierung anzeigen |
| Wert der Hervorhebung | Zusammenfassungsnummer in markanter Fettschrift in der Mitte der Visualisierung anzeigen |
| Legende sichtbar | Legende unten in der Visualisierung ein- oder ausblenden |
| Anmerkungen anzeigen | Anzeigen oder Ausblenden von Anmerkungen, die von einem Administrator hinzugefügt wurden |
| Sparklines anzeigen | Zeigen Sie Liniendiagramme am unteren Rand des Diagramms an oder blenden Sie sie aus. Wenn die Legende ausgeblendet wird, wird sie nicht mehr visuell auf die Zeilen verweisen |
| Min. und Max. für Wortgrafiken anzeigen | Mindest- und Höchstwerte in Primär- und Vergleichsliniendiagrammen ein- oder ausblenden |
| Vergleich anzeigen | Vergleichsdaten ein- oder ausblenden. Wenn diese Option ausgeblendet ist, werden sowohl das Vergleichszeilendiagramm als auch die Zusammenfassungsänderung der Objekte ausgeblendet. |
| Gesamtanzahl anzeigen | Zusammenfassungsnummer anzeigen oder ausblenden |
| Rohdifferenz anzeigen | Rohdifferenz zwischen dem Gesamtwert der Metrik im primären Datumsbereich und im sekundären Datumsbereich anzeigen oder ausblenden |
| Wert abkürzen | Abkürzung für Zahlenwerte zur Vereinfachung kommunizierter Einblicke (z. B. 20.000 -> 20.000) |

## Visualisierung bearbeiten

Nach dem Erstellen der Visualisierung können Sie die ursprüngliche Konfiguration weiterhin bearbeiten.

1. Klicken Sie oben rechts in der Visualisierung auf das Stiftsymbol (neben dem Zahnradsymbol für Einstellungen).

   ![](assets/edit-icon.png)

   Sie werden nun zur ursprünglichen Konfigurationsansicht zurückgeführt.

1. Ändern Sie die Metrik, den primären Datumsbereich, den Vergleichsdatumsbereich oder das Segment wie gewünscht.
