---
description: Wenn ein Bericht eine große Anzahl einzigartiger Werte aufweist, stellt Adobe eine Funktion bereit, um sicherzustellen, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden.
seo-description: Wenn ein Bericht eine große Anzahl einzigartiger Werte aufweist, stellt Adobe eine Funktion bereit, um sicherzustellen, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden.
seo-title: Wert geringer Traffic in Adobe Analytics
solution: Analytics
title: Wert geringer Traffic in Adobe Analytics
topic: Metriken
uuid: 56 f 723 f 8-94 e 8-478 f -8 ea 3-16 dad 21 dfa 1 f
translation-type: tm+mt
source-git-commit: 1fdd14497171dbf5850ec1b1d873a06931d58435

---


# Wert geringer Traffic in Adobe Analytics

Wenn ein Bericht eine große Anzahl einzigartiger Werte aufweist, stellt Adobe eine Funktion bereit, um sicherzustellen, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden. Unique variable values collected after approximately 500,000 existing values are listed under a line item titled **(Low-Traffic)**.

## Funktionsweise geringer Traffic

* Die Berichterstellung ist nicht betroffen, wenn die Variable in einem bestimmten Monat 500.000 einzigartige Werte nicht erreicht.
* Wenn eine Variable diesen ersten Schwellenwert von 500.000 erreicht, werden die Daten unter geringer Traffic zusammengefasst. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn bereits ein Wert in Berichten vorhanden ist, fügen Sie diesen Wert wie gewohnt hinzu.
   * Wenn sich ein Wert noch nicht in der Berichterstellung befindet, prüfen Sie, ob dieser Wert heute über etwa etwa zehn Mal angesehen wurde. Falls ja, fügen Sie diesen Wert zu Berichten hinzu. Wenn sie nicht mehr als etwa zehn Mal gezählt wurde, lassen Sie sie unter geringer Traffic.
* Wenn eine Report Suite mehr als 1.000.000 einzigartige Werte erreicht, wird eine aggressive Filterung angewendet:
   * Wenn bereits ein Wert in Berichten vorhanden ist, fügen Sie diesen Wert wie gewohnt hinzu.
   * Wenn sich ein Wert noch nicht in der Berichterstellung befindet, prüfen Sie, ob dieser Wert heute über etwa ca. ca. 100 Mal angesehen wurde. Falls ja, fügen Sie den Wert zu Berichten hinzu. Wenn dies nicht der Fall ist, lassen Sie sie unter geringer Traffic.

> [!NOTE] Wenn ein Variablenwert ausreichend Traffic empfängt, um den Behälter für den niedrigen Traffic zu verlassen, werden die ersten erfassten Werte nicht in den entsprechenden Zeileneintrag verschoben. Diese ersten 10 bis 100 Instanzen bleiben unter geringer Traffic.

## Ändern von Schwellenwertschwellenwerten

Die Schwellenwerte liegen standardmäßig bei 500.000 und einer Million individuellen Werten. Diese Beschränkungen können pro Variable geändert werden. Wenden Sie sich an den Kundenbetreuer Ihrer Organisation, um diese Änderung anzufordern. Berücksichtigen Sie beim Anfordern einer Änderung Folgendes:

* Die Report Suite-ID
* Die Variable, die Sie erhöhen möchten, soll den Schwellenwert für
* Sowohl der erste als auch der zweite Schwellenwert

Diese Änderung kann Mehrkosten haben und hängt von Vertrag ab. Änderungen an Schwellenwerten können sich auch auf die Berichtleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung individueller Werte in einer Variablen gute Entscheidungen zu treffen.

Niedrige Traffic-Schwellenwerte sind in der Analytics-Benutzeroberfläche nicht sichtbar. Wenden Sie sich an einen unterstützten Benutzer in Ihrem Unternehmen, wenn Sie weitere Informationen zu vorhandenen Schwellenwerten wünschen.

## Geringer Traffic mit Komponenten und anderen Funktionen

Bei unterschiedlichen Funktionen werden niedrige Traffic-Werte unterschiedlich behandelt.

* **Data Warehouse:** Die Anzahl eindeutiger Werte in Data Warehouse-Berichten ist nicht beschränkt. Die eindeutige Architektur ermöglicht die Berichterstellung über eine beliebige Anzahl einzigartiger Werte.
   * In einigen eingeschränkten Szenarien können Werte geringer Traffic weiterhin angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-evars und Marketingkanaldetails.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl einzigartiger Werte enthalten, werden die unter niedrigem Traffic erfassten Werte nicht berücksichtigt.
* **Klassifizierungen:** Klassifizierungsberichte unterliegen ebenfalls eindeutigen Beschränkungen. Wenn der Wert für die übergeordnete Variable einer Klassifizierung unter geringer Traffic enthalten ist, wird der Wert nicht klassifiziert.
   * Wenn Sie Werte klassifizieren, bevor sie in Daten angezeigt werden, werden diese Werte für den eindeutigen Schwellenwert in diesem Monat gezählt.
