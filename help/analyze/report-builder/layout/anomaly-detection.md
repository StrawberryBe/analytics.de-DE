---
description: Die Anomalieerkennung verwendet statistische Modellierung, um automatisch unerwartete Trends in Ihren Daten zu finden. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. Wenn eine unerwartete Spitze oder ein unerwarteter Rückgang auftritt, werden Sie im Bericht vom System benachrichtigt.
title: Anomalieerkennung
topic: Report builder
uuid: 02da21b4-3394-471b-97b5-aa1bddf1f445
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Anomalieerkennung {#anomaly-detection}

Die Anomalieerkennung verwendet statistische Modellierung, um automatisch unerwartete Trends in Ihren Daten zu finden. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. Wenn eine unerwartete Spitze oder ein unerwarteter Rückgang auftritt, werden Sie im Bericht vom System benachrichtigt.

Beispiele für Anomalien, die Sie untersuchen könnten:

* Drastische Rückgänge im durchschnittlichen Bestellwert
* Spitzen in Bestellungen mit geringem Umsatz
* Spitzen oder Verwerfungen in Testregistrierungen
* Tropfen in Ansichten der Landingpage
* Gewürze in Video-Puffer-Ereignissen
* Spitzen in niedrigen Video-Bitraten

>[!NOTE] Die Anomalieerkennung ist nur verfügbar, wenn Sie als Granularität „Tag“ auswählen.

<p class="head"> <b>Metriken zur Anomalieerkennung</b> </p>

Die Anomalieerkennung fügt für jede ausgewählte Metrik neue Metrikwerte hinzu, darunter:

<table id="table_BF75FC874634498DB6632C12CBD8D533"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Untergrenze </td> 
   <td colname="col2"> <p>Untere Ebene des Prognoseintervalls. Werte unterhalb dieser Ebene werden als abweichend betrachtet. </p> <p>Stellt eine Konfidenz von 95 % dar, dass Werte über dieser Grenze liegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Erwartet </td> 
   <td colname="col2"> <p>Der prognostizierte Wert, der auf der Analyse der Daten basiert. Dieser Wert ist auch der mittlere Punkt zwischen der oberen und der unteren Grenze. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Obere Grenze </td> 
   <td colname="col2"> <p>Obere Ebene des Prognoseintervalls. Werte über dieser Grenze werden als abweichend betrachtet. </p> <p>Stellt eine Konfidenz von 95 % dar, dass Werte unter diesem Wert liegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

ReportBuilder wendet diese Werte auf ausgewählte Metriken an. Wenn Sie beispielsweise eine Metrik für Seitenansichten auswählen und die Anomalieerkennung anwenden, wird eine Metrik für die *`Page Views Lower Bound`* verwendet.

**Berechnung der Anomalieerkennung**

Die Anomalieerkennung verwendet einen Schulungszeitraum, um die Daten des Prognoseintervalls zu berechnen, zu lernen und Berichte darüber zu erstellen. Der Schulungszeitraum ist der historische Zeitraum, in dem ermittelt wird, was normal oder abweichend ist, und das Erlernte auf den Berichte anwendet. In Marketingberichten stehen Schulungszeiträume von 30, 60 und 90 zur Verfügung. In ReportBuilder sind 30 Tage verfügbar.

Der Schulungszeitraum entspricht nicht unbedingt dem ausgewählten Berichte. Ein Berichtsdiagramm zeigt den Datumsbereich an, den Sie im Kalender angeben.

Zur Berechnung der Daten wird der Tagesgesamtwert für jede Metrik mit dem Schulungszeitraum unter Verwendung der folgenden Algorithmen verglichen:

* Holt-Winters-Multiplikativ (Dreifache exponentielle Ausgleichung)
* Holt-Winters-Additiv (Dreifache exponentielle Ausgleichung)
* Trendkorrektur der Holts (exponentielle Ausgleichung der Dublette)

Jeder Algorithmus wird angewendet, um den Algorithmus mit der kleinsten Summe der quadratischen Fehler (SSE) zu bestimmen. Anschließend werden der mittlere absolute Prozentfehler (MAPE) und der aktuelle Standardfehler berechnet, um sicherzustellen, dass das Modell statistisch gültig ist.

Diese Algorithmen können erweitert werden, um Prognosen für Metriken in zukünftigen Zeiträumen bereitzustellen.

Da der Schulungszeitraum je nach Beginn des Berichte variiert, können die gemeldeten Daten für dasselbe Datum in zwei verschiedenen Zeiträumen unterschiedlich sein.

Wenn Sie z. B. einen Bericht für den 1. bis 14. Januar ausführen und dann einen Bericht für den 7. bis 21. Januar ausführen, werden in den beiden Berichten möglicherweise unterschiedliche Prognosedaten für dieselbe Metrik vom 7. bis 14. Januar angezeigt. Dies ist auf die unterschiedlichen Ausbildungszeiten zurückzuführen.

| Berichte | Schulungszeitraum |
|--- |--- |
| 1.-14. Januar | 27. November - 31. Dezember |
| 7.-21. Januar | 4. Dezember - 6. Januar |
