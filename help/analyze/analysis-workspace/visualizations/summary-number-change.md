---
description: 'null'
title: Sammelnummer und Sammeländerung
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Sammelnummer und Sammeländerung

## Visualisierung für Zusammenfassungsnummer

* Wenn keine Zelle ausgewählt ist, wird die gesamte Spalte ausgewählt.
* Wenn eine einzelne Zelle ausgewählt ist, wird die Zusammenfassung für diese Zelle angezeigt.
* Wenn mehr als eine Zelle ausgewählt ist, wird die zuerst ausgewählte Zelle angezeigt.
* Wenn die Spalte ausgewählt ist, wird der erste Zellenwert in der Spalte verwendet.

![](assets/summary-number.png)

## Visualisierung für Zusammenfassungsänderung:

* Wenn keine Zelle ausgewählt ist, werden die ersten beiden Zellenwerte in der Spalte verglichen.
* Wenn eine Zelle ausgewählt ist, wird 0 angezeigt, weil der Zellenwert mit sich selbst verglichen wird.
* Wenn zwei Zellen ausgewählt sind, wird die erste ausgewählte Zelle als Numerator und die zweite als Denominator verwendet.
* Wenn mehr als zwei Zellen ausgewählt sind, werden nur die ersten beiden Zellen für den Vergleich berücksichtigt.
* Wenn ein Zellbereich ausgewählt ist, wird die erste Zelle mit den letzten im Bereich ausgewählten Zellen verglichen.
* Wenn die Spalte ausgewählt ist, wird der erste Wert mit sich selbst verglichen, sodass eine Änderung von 0 angezeigt wird.
* Die grüne bzw. rote Farbgebung der Zusammenfassungsänderung kann durch Folgendes bestimmt werden:
   * [Polarität benutzerspezifischer Ereignisse](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/success-events/success-event.html).
   * Option [Aufwärts-Trend anzeigen als](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) einer berechneten Metrik.

## Einstellungen zur Zusammenfassungsänderung {#section_2581AC0107634FB4990AB8347E5897AA}

Klicken Sie auf das Zahnrad-Symbol neben der Visualisierung, um die Einstellungen für die Zusammenfassung zu konfigurieren:

| Einstellung | Definition |
|--- |--- |
| Prozentsatz | Verwenden Sie Prozentsätze und keine Rohdaten. |
| Legende eingeblendet | Zeigt die verwendeten Metriken. |
| Optionen für Zusammenfassungsnummer: Wert abkürzen | Sie können zwischen 0 und 3 Dezimalstellen für verkürzte Werte auswählen. |
| Optionen für Zusammenfassungsänderung: prozentualen Unterschied anzeigen | Zeigt den prozentualen Unterschied zwischen den beiden Zahlen. |
| Optionen für Zusammenfassungsänderung: tatsächlichen Unterschied anzeigen | Zeigt den tatsächlichen Unterschied zwischen den beiden Zahlen. |
