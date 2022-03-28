---
description: Wenn ein Bericht eine große Anzahl eindeutiger Werte aufweist, verwendet Adobe das Dimensionselement "Geringer Datenverkehr", um die Berichtsleistung zu verbessern.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: e087c50784a99eb4e664021b243ad38c3b95e538
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 49%

---

# Wert „Geringer Datenverkehr“ in Adobe Analytics

Wenn ein Bericht zahlreiche eindeutige Werte aufweist, kann mit Adobe nun sichergestellt werden, dass die wichtigsten Werte in Ihrem Bericht auftauchen. Eindeutige Variablenwerte, die nach etwa 500.000 vorhandenen Werten gesammelt wurden, werden unter einem Dimensionselement mit der Bezeichnung aufgeführt **[!UICONTROL Geringer Traffic]**.

## So funktioniert [!UICONTROL Geringer Datenverkehr]

* Das Reporting ist nicht betroffen, wenn die Variable in einem bestimmten Monat nicht 500.000 eindeutige Werte erreicht.
* Wenn eine Variable 500.000 eindeutige Werte erreicht, werden die Daten unter [!UICONTROL Geringer Traffic]. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten enthalten ist, wird er wie gewohnt hinzugefügt.
   * Wenn ein Wert noch nicht in Berichten enthalten ist, wird er zunächst im [!UICONTROL Geringer Traffic] Dimensionselement.
   * Wenn ein Wert, der unter [!UICONTROL Geringer Traffic] in diesem Monat irgendwo in zweistelligen Ziffern angezeigt wird, wird es als eigenes Dimensionselement erkannt. Vor Erreichen der Schwelle gesammelte Instanzen bleiben unter [!UICONTROL Geringer Traffic]. Der genaue Schwellenwert weist viele Abhängigkeiten auf, z. B. die Anzahl der Server, die Daten für die Report Suite verarbeiten, und die Zeit zwischen den einzelnen Dimensionselementinstanzen.
* Wenn eine Report Suite mehr als 1.000.000 eindeutige Werte erreicht, wird eine aggressivere Filterung angewendet. Eindeutige Werte erfordern Instanzen in den dreistelligen Ziffern, bevor sie als eigenes Dimensionselement erkannt werden.

Diese Logik ermöglicht es der Adobe, die Berichterstellungsfunktionen zu optimieren und gleichzeitig Ihrem Unternehmen die Möglichkeit zu geben, über wichtige Dimensionselemente zu berichten, die später im Monat erfasst wurden. Ihre Organisation betreibt beispielsweise eine Site mit Millionen von Artikeln und ein neuer Artikel wurde gegen Ende des Monats beliebt (nachdem beide individuelle Schwellenwerte überschritten wurden). Sie können die Leistung dieses Artikels weiterhin analysieren, ohne dass er unter [!UICONTROL Geringer Traffic]. Beachten Sie, dass diese Logik nicht dazu gedacht ist, alles aufzuheben, das eine bestimmte Anzahl von Seitenansichten pro Tag oder Monat erhält.

>[!NOTE]
>Die [Seite](../components/dimensions/page.md) -Dimension verwendet mehrere Backend-Spalten, die alle auf eindeutige Schwellenwerte angerechnet werden, darunter `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`und `click_context`. Diese Backend-Spalten können [!UICONTROL Geringer Traffic] -Logik angewendet werden, bevor die Anzahl der eindeutigen Seitendimensionen in Workspace 500.000 erreicht.

## Ändern der Schwellenwerte für eindeutige Werte

Die Schwellenwerte liegen standardmäßig bei 500.000 und einer Million eindeutigen Werten. Diese Beschränkungen können variablenweise geändert werden. Wenden Sie sich an die Kundenunterstützung von Adobe oder den Kundenbetreuer Ihres Unternehmens, um diese Änderung anzufordern. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert erhöhen möchten
* Sowohl den ersten als auch den zweiten gewünschten Schwellenwert

Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen achtsam vorzugehen. Erhöhen Sie nur die individuellen Grenzwerte für Variablen, die für die Reporting-Anforderungen Ihres Unternehmens von entscheidender Bedeutung sind.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Wenden Sie sich an die Kundenunterstützung von Adobe , wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## „Geringer Datenverkehr“ mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **Data Warehouse:** Die Anzahl der eindeutigen Werte in Data-Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht das Reporting beliebig vieler eindeutiger Werte.
   * In einigen eingeschränkten Szenarien können weiterhin „Geringer Datenverkehr“-Werte angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl eindeutiger Werte enthalten, werden unter „Geringer Datenverkehr“ erfasste Werte nicht berücksichtigt.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Classification unter „Geringer Datenverkehr“ fällt, wird der Wert nicht klassifiziert.
   * Klassifizierungswerte für geringen Traffic, die über den Importer bezogen wurden, können in Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * Klassifizierungswerte für geringen Traffic, die über den Regelaufbau erhalten wurden, *können nicht* in Data Warehouse angezeigt werden. <!-- AN-122872 -->
