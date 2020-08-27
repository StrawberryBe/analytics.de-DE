---
description: Verwenden Sie die Visualisierungen "Zusammenfassungsnummer"und "Ändern", um wichtige Datenpunkte in einem Projekt anzuzeigen.
title: Sammelnummer und Sammeländerung
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
translation-type: tm+mt
source-git-commit: 0a3c4a6839d0c6ee2d8a98394ed38c433ea811d1
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 52%

---


# Sammelnummer und Sammeländerung

## Visualisierung für Zusammenfassungsnummer {#summary-number}

Verwenden Sie die Visualisierung der Zusammenfassungsnummer, um eine große Zahl hervorzuheben, die für ein Projekt wichtig ist. Diese Visualisierung verhält sich wie folgt:

* Wenn keine Zelle ausgewählt ist, wird die gesamte Spalte ausgewählt.
* Wenn eine einzelne Zelle ausgewählt ist, wird die Zusammenfassung für diese Zelle angezeigt.
* Wenn mehr als eine Zelle ausgewählt ist, wird die zuerst ausgewählte Zelle angezeigt.
* Wenn die Spalte ausgewählt ist, wird der erste Zellenwert in der Spalte verwendet.

![](assets/summary-number.png)

Klicken Sie oben rechts auf den **Visualisierungseinstellungen** , um die Einstellungen für die Zusammenfassungsnummer zu konfigurieren:

| Einstellung | Definition |
|--- |--- |
| Prozentsatz | Zeigt Prozentwerte anstelle von Rohdaten an. |
| Legende sichtbar | Zeigt Informationen zur angezeigten Metrik an. |
| Wert abkürzen | Sie können Werte kürzen und bis zu 3 Dezimalstellen anzeigen. |
| Wert zusammenfassen nach | Wählen Sie aus, ob die Werte für &quot;max&quot;, &quot;min&quot;, &quot;mittel&quot;, &quot;median&quot;oder &quot;sum&quot;für eine Auswahl von Daten angezeigt werden sollen. |

## Visualisierung für Zusammenfassungsänderung:{#summary-change}

Verwenden Sie die Visualisierung der Zusammenfassungsänderung, um das Delta (Änderung) zwischen zwei Zahlen anzuzeigen. Die grün- und rote Farbe der Zusammenfassungsänderung kann über die [benutzerdefinierte Ereignis-Polarität](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/success-events/success-event.html) oder die Option &quot;Trend nach oben [anzeigen als](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) &quot;einer berechneten Metrik gesteuert werden.

Diese Visualisierung verhält sich wie folgt:

* Wenn keine Zelle ausgewählt ist, werden die ersten beiden Zellenwerte in der Spalte verglichen.
* Wenn eine Zelle ausgewählt ist, wird 0 angezeigt, weil der Zellenwert mit sich selbst verglichen wird.
* Wenn zwei Zellen ausgewählt sind, wird die erste ausgewählte Zelle als Numerator und die zweite als Denominator verwendet.
* Wenn mehr als zwei Zellen ausgewählt sind, werden nur die ersten beiden Zellen für den Vergleich berücksichtigt.
* Wenn ein Zellbereich ausgewählt ist, wird die erste Zelle mit den letzten im Bereich ausgewählten Zellen verglichen.
* Wenn die Spalte ausgewählt ist, wird der erste Wert mit sich selbst verglichen, sodass eine Änderung von 0 angezeigt wird.

![](assets/summary-change.png)

Klicken Sie oben rechts auf das **Visualisierungseinstellungen** , um die Einstellungen für die Zusammenfassungsänderung zu konfigurieren:

| Einstellung | Definition |
|--- |--- |
| Prozentsatz | Zeigt Prozentwerte anstelle von Rohdaten an. |
| Legende sichtbar | Zeigt Informationen zur angezeigten Metrik an. |
| Prozentsatzänderung anzeigen | Zeigt die prozentuale Änderung zwischen den 2 Zahlen an. |
| Rohdifferenz anzeigen | Zeigt den tatsächlichen Unterschied zwischen den beiden Zahlen. Mit dieser Option können Sie auch Werte kürzen und bis zu 3 Dezimalstellen anzeigen. |
