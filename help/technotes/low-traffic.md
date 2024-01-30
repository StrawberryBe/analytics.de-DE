---
description: Wenn ein Bericht viele eindeutige Werte aufweist, verwendet Adobe das Dimensionselement "Geringer Datenverkehr", um die Berichtsleistung zu verbessern.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: d3a959d128f4740fd98ff40e5b92a3ea983d3c05
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 31%

---

# Wert „Geringer Datenverkehr“ in Adobe Analytics

Wenn ein Bericht zahlreiche eindeutige Werte aufweist, kann mit Adobe nun sichergestellt werden, dass die wichtigsten Werte in Ihrem Bericht auftauchen. Eindeutige Variablenwerte, die über einen bestimmten Schwellenwert hinweg gesammelt werden (siehe unten), werden unter einem Dimensionselement mit der Bezeichnung **[!UICONTROL Geringer Traffic]**.

## So funktioniert [!UICONTROL Geringer Datenverkehr]

* Adobe Analytics verwendet zwei Schwellenwerte, um zu bestimmen, welche eindeutigen Werte jeden Monat in Berichten angezeigt werden: A **[!UICONTROL niedrige Schwelle]** und **[!UICONTROL hoher Schwellenwert]**. Diese Schwellen können von Zeit zu Zeit durch Adobe angepasst werden. Die aktuellen Schwellenwerte sind:
   * **[!UICONTROL Niedriger Schwellenwert]**: > 500.000 einmalige Werte im Monat.
   * **[!UICONTROL Hoher Schwellenwert]**: > 1.000.000 einmalige Werte im Monat.
* Die Berichterstellung ist nicht betroffen, wenn die Variable in einem bestimmten Monat den unteren Schwellenwert nicht erreicht.
* Wenn eine Variable den unteren Schwellenwert erreicht, werden die Daten unter zusammengefasst [!UICONTROL Geringer Traffic]. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten enthalten ist, wird er wie gewohnt hinzugefügt.
   * Wenn ein Wert noch nicht in Berichten enthalten ist, wird er zunächst im [!UICONTROL Geringer Traffic] Dimensionselement.
   * Wenn ein Wert, der unter [!UICONTROL Geringer Traffic] einen Traffic-Zustrom erhält (typischerweise Instanzen in den zweistelligen Stellen an einem einzelnen Tag), wird er als eigenes Dimensionselement erkannt. Vor Erreichen der Schwelle gesammelte Instanzen bleiben unter [!UICONTROL Geringer Traffic]. Der genaue Zeitpunkt, zu dem das Dimensionselement in Berichten angezeigt wird, weist viele Abhängigkeiten auf, z. B. die Anzahl der Server, die Daten für die Report Suite verarbeiten, und die Zeitspanne zwischen den einzelnen Dimensionselementinstanzen.
* Erreicht eine Variable den hohen Schwellenwert, wird eine aggressivere Filterung angewendet. Eindeutige Werte erfordern Instanzen in den dreistelligen Stellen an einem Tag, bevor sie als eigenes Dimensionselement erkannt werden.

Diese Logik ermöglicht es Adobe, die Berichterstellungsfunktionen zu optimieren, während es Ihrem Unternehmen weiterhin ermöglicht, über wichtige Dimensionselemente zu berichten, die später im Monat erfasst wurden. Wenn Ihr Unternehmen beispielsweise eine Site mit Millionen von Artikeln betreibt und gegen Ende des Monats ein neuer Artikel beliebt wird (nachdem er beide einmaligen Schwellenwerte überschritten hat), können Sie die Leistung dieses Artikels dennoch analysieren, ohne dass der Artikel erfasst wird unter [!UICONTROL Geringer Traffic]. Diese Logik ist nicht dazu gedacht, alles aufzuheben, das eine bestimmte Anzahl von Seitenansichten pro Tag oder Monat erhält.

>[!NOTE]
>Die [Seite](../components/dimensions/page.md) -Dimension verwendet mehrere Backend-Spalten, die alle auf eindeutige Schwellenwerte angerechnet werden, darunter `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url`, und `click_context`. Diese Backend-Spalten können [!UICONTROL Geringer Traffic] -Logik angewendet werden, bevor die Anzahl der eindeutigen Seitendimensionen in Workspace den unteren Schwellenwert erreicht.

Beachten Sie, dass die oben beschriebene Logik für niedrigen Traffic am besten mit Variablen funktioniert, die Dimensionselemente enthalten, die im Laufe des Monats mehrmals auftreten. Wenn die Dimensionselemente einer Variablen bei jedem Treffer nahezu oder vollständig eindeutig sind, erreicht die Variable schnell den unteren Schwellenwert, und alle neuen Dimensionselemente für den Monat werden in der Gruppe mit geringem Traffic landen.

## Ändern der Schwellenwerte für eindeutige Werte

Die Schwellenwerte können manchmal pro Variable geändert werden. Wenden Sie sich an die Adobe-Kundenunterstützung oder Ihr Adobe-Account-Team, um diese Änderung anzufordern. Das Ausmaß, in dem die Schwellenwerte erhöht werden können, hängt von mehreren Faktoren ab, und Adobe kann möglicherweise nicht in der Lage sein, Schwellenerhöhungen in allen Fällen zu berücksichtigen. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert erhöhen möchten
* Sowohl den ersten als auch den zweiten gewünschten Schwellenwert

Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen ein gutes Urteilsvermögen anzuwenden. Erhöhen Sie nur die individuellen Grenzwerte für Variablen, die für die Reporting-Anforderungen Ihres Unternehmens von entscheidender Bedeutung sind.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Wenden Sie sich an die Adobe-Kundenunterstützung , wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## „Geringer Datenverkehr“ mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **Data Warehouse:** Die Anzahl der eindeutigen Werte in Data-Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht das Reporting beliebig vieler eindeutiger Werte.
   * In einigen eingeschränkten Szenarien können weiterhin „Geringer Datenverkehr“-Werte angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl eindeutiger Werte enthalten, werden unter „Geringer Datenverkehr“ erfasste Werte nicht berücksichtigt.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Classification unter „Geringer Datenverkehr“ fällt, wird der Wert nicht klassifiziert.
   * Klassifizierungswerte für geringen Traffic, die über den Importer bezogen wurden, können in Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * Klassifizierungswerte für geringen Traffic, die über den Regelaufbau erhalten wurden, *können nicht* in Data Warehouse angezeigt werden. <!-- AN-122872 -->
