---
description: 'null '
seo-description: 'null '
seo-title: Sammelnummer und Sammeländerung
title: Sammelnummer und Sammeländerung
uuid: 177 c 1 b 89-6 d 98-473 d -8447-6 b 4 cdc 479565
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sammelnummer und Sammeländerung

## Visualisierung für Zusammenfassungsnummer

* Wenn keine Zelle ausgewählt ist, wird die gesamte Spalte ausgewählt.
* Wenn eine einzelne Zelle ausgewählt ist, wird die Zusammenfassung für diese Zelle angezeigt.
* Wenn mehr als eine Zelle ausgewählt ist, wird die zuerst ausgewählte Zelle angezeigt.
* Wenn die Spalte ausgewählt ist, wird der erste Zellenwert in der Spalte verwendet.

![](assets/summary-number.png)

## Visualisierung der Zusammenfassungsänderung

* Wenn keine Zelle ausgewählt ist, werden die ersten beiden Zellenwerte in der Spalte verglichen.
* Wenn eine Zelle ausgewählt ist, wird 0 angezeigt, weil der Zellenwert mit sich selbst verglichen wird.
* Wenn zwei Zellen ausgewählt sind, wird die erste ausgewählte Zelle als Numerator und die zweite als Denominator verwendet.
* Wenn mehr als zwei Zellen ausgewählt sind, werden nur die ersten beiden Zellen für den Vergleich berücksichtigt.
* Wenn ein Zellbereich ausgewählt ist, wird die erste Zelle mit den letzten im Bereich ausgewählten Zellen verglichen.
* Wenn die Spalte ausgewählt ist, wird der erste Wert mit sich selbst verglichen, sodass eine Änderung von 0 angezeigt wird.
* Die grüne bzw. rote Farbgebung der Zusammenfassungsänderung kann durch Folgendes bestimmt werden:

   * [Polarität benutzerspezifischer Ereignisse](https://marketing.adobe.com/resources/help/en_US/reference/success_event.html).
   * Option [Aufwärts-Trend anzeigen als](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_build_metrics.html) einer berechneten Metrik.

## Summary Change settings {#section_2581AC0107634FB4990AB8347E5897AA}

Klicken Sie auf das Zahnrad-Symbol neben der Visualisierung, um die Einstellungen für die Zusammenfassung zu konfigurieren:

| Einstellung | Definition |
|--- |--- |
| Prozentsatz | Verwenden Sie Prozentsätze und keine Rohdaten. |
| Legende eingeblendet | Zeigt die verwendeten Metriken. |
| Optionen für Zusammenfassungsnummer: Wert abkürzen | Sie können zwischen 0 und 3 Dezimalstellen für verkürzte Werte auswählen. |
| Optionen für Zusammenfassungsänderung: prozentualen Unterschied anzeigen | Zeigt den prozentualen Unterschied zwischen den beiden Zahlen. |
| Optionen für Zusammenfassungsänderung: tatsächlichen Unterschied anzeigen | Zeigt den tatsächlichen Unterschied zwischen den beiden Zahlen. |