---
description: Wenn ein Bericht eine große Anzahl eindeutiger Werte aufweist, kann mit Adobe nun sichergestellt werden, dass die wichtigsten Werte in Ihrem Bericht auftauchen.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: 'Metriken  '
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
translation-type: tm+mt
source-git-commit: 482dcc04b7d68c6a555d318d8493c309e5899ae1
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 79%

---

# Wert „Geringer Datenverkehr“ in Adobe Analytics

Wenn ein Bericht viele eindeutige Werte enthält, stellt Adobe eine Funktion bereit, mit der sichergestellt wird, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden. Eindeutige Variablenwerte, die nach etwa 500.000 vorhandenen Werten gesammelt wurden, werden unter einem Zeileneintrag mit dem Titel **(Geringer Datenverkehr)** aufgeführt.

## So funktioniert „Geringer Datenverkehr“

* Das Reporting ist nicht betroffen, wenn die Variable in einem bestimmten Monat nicht 500.000 eindeutige Werte erreicht.
* Wenn eine Variable diesen ersten Schwellenwert von 500.000 erreicht, werden die Daten unter „Geringer Datenverkehr“ erfasst. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten enthalten ist, wird er wie gewohnt hinzugefügt.
   * Wenn sich ein Wert noch nicht in Berichte befindet, sind die Schwellenwerte für die Anzahl der angezeigten Werte von Backend-Konfigurationen abhängig. Sie stellen keine genaue &quot;10&quot;- oder &quot;100&quot;-Darstellung dar.
* Wenn eine Report Suite mehr als 1.000.000 eindeutige Werte erreicht, wird eine aggressivere Filterung angewendet:
   * Wenn ein Wert bereits in Berichten enthalten ist, wird er wie gewohnt hinzugefügt.
   * Wenn sich ein Wert noch nicht in Berichte befindet, sind die Schwellenwerte für die Anzahl der angezeigten Werte von Backend-Konfigurationen abhängig. Sie stellen keine genaue &quot;10&quot;- oder &quot;100&quot;-Darstellung dar.

>[!NOTE]
>
>Wenn ein Variablenwert ausreichend Traffic erhält, um die Gruppe „Niedriger Datenverkehr“ zu verlassen, werden die ersten erfassten Werte nicht zu dem entsprechenden Zeilenelement verschoben. Diese ersten 10 bis 100 Instanzen werden weiterhin unter „Geringer Datenverkehr“ aufgeführt.

## Ändern der Schwellenwerte für eindeutige Werte

Die Schwellenwerte liegen standardmäßig bei 500.000 und einer Million eindeutigen Werten. Diese Beschränkungen können variablenweise geändert werden. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um diese Änderung anzufordern. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert erhöhen möchten
* Sowohl den ersten als auch den zweiten gewünschten Schwellenwert

Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen achtsam vorzugehen.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Bitten Sie einen unterstützten Anwender Ihres Unternehmens, sich an die Adobe-Kundenunterstützung zu wenden, wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## „Geringer Datenverkehr“ mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **Data Warehouse:** Die Anzahl der eindeutigen Werte in Data-Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht das Reporting beliebig vieler eindeutiger Werte.
   * In einigen eingeschränkten Szenarien können weiterhin „Geringer Datenverkehr“-Werte angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl eindeutiger Werte enthalten, werden unter „Geringer Datenverkehr“ erfasste Werte nicht berücksichtigt.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Classification unter „Geringer Datenverkehr“ fällt, wird der Wert nicht klassifiziert.
   * Klassifizierungswerte mit geringem Traffic, die über den Importeur bezogen werden, können in der Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * Classification-Werte mit geringem Traffic, die über den Rule Builder *erhalten wurden, können nicht in der Data Warehouse angezeigt werden. <!-- AN-122872 -->*
