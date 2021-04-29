---
title: Analysieren von Marketing-Kanälen
description: Erfahren Sie, wie Sie die Dimensionen von Marketing-Kanäle in Workspace verwenden.
exl-id: 7030e41a-4e92-45c7-9725-66a3ef019313
translation-type: tm+mt
source-git-commit: 7202a49dda7c3ef4f4b535476d3cf637b9e9f7f6
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 81%

---

# Analysieren von Marketing-Kanälen

>[!NOTE]
>
>Um die Effektivität von Marketing-Kanälen für Attribution IQ und Customer Journey Analytics zu maximieren, haben wir einige [überarbeitete Best Practices](/help/components/c-marketing-channels/mchannel-best-practices.md) veröffentlicht.

Sie möchten wahrscheinlich wissen, welcher Ihrer Marketing-Kanäle der effektivste ist und bei wem, damit Sie Ihre Bemühungen gezielter ausrichten und eine bessere Rendite aus Ihrem Marketing-Budget erzielen können. Die Dimensionen und Metriken der Marketing-Kanäle in Workspace sind eines der Tools in Adobe Analytics, mit dem Sie den Einfluss verschiedener Kanäle auf Ihre Bestellungen, Umsätze usw. verfolgen. und nützliche Einblicke in die Kanäle gewinnen können. Hier sind die Dimensionen und Metriken, die Sie in Bezug auf Marketing-Kanäle verwenden können:

![](assets/mc-dims.png)

| Dimension/Metrik | Definition |
| --- | --- |
| Marketing-Kanal | Dies ist die empfohlene Dimension für Marketing-Kanäle. Attribution IQ-Modelle können zur Laufzeit darauf angewendet werden. Diese Dimension verhält sich identisch mit den Dimensionen des Letztkontakt-Kanals, ist jedoch anders gekennzeichnet, um Verwirrung bei der Verwendung mit einem anderen Attributionsmodell zu vermeiden. |
| Letztkontakt-Kanal | Veraltete Dimension mit vorab angewendetem und unveränderlichem Letztkontakt-Attributionsmodell. |
| Erstkontakt-Kanal | Veraltete Dimension mit vorab angewendetem und unveränderlichem Erstkontakt-Attributionsmodell. |
| Marketing-Kanalinstanzen | Diese Metrik misst, wie oft ein Marketing-Kanal in einer Bildanforderung definiert wurde, einschließlich standardmäßiger Seitenansichten und benutzerspezifischer Link-Aufrufe. Enthält keine persistenten Werte. |
| Neue Interaktionen | Diese Metrik ähnelt Instanzen, wird jedoch nur inkrementiert, wenn in einer Bildanforderung First Touch-Marketing-Kanal definiert wird. |

## Basisanalyse

Diese Freiform-Tabelle zeigt die Metriken „Online-Bestellungen“, „Online-Umsatz“ und „Konversionsrate“ für jeden Marketing-Kanal an:

![](assets/mc-viz1.png)

Hier sehen Sie die Online-Bestellungen und den Online-Umsatz der einzelnen Marketing-Kanäle in einem Ringdiagramm:

![](assets/mc-viz2.png)

Dieses Liniendiagramm zeigt die Trends bei Online-Bestellungen für verschiedene Kanäle im Zeitverlauf:

![](assets/mc-viz3.png)

## Erweiterte Analyse

„Details des Marketing-Kanals“ taucht tiefer in die einzelnen Kanal ein, um Ihnen bestimmte Kampagnen, Platzierungen usw. zu zeigen. Sie können jeden Marketing-Kanal in Details unterteilen:

![](assets/mc-viz4.png)

## Anwenden von Attributionsmodellen

Sie können [Attribution IQ](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/panels/attribution.html) verwenden, um verschiedene Attributionsmodelle sofort anzuwenden:

![](assets/mc-viz5.png)

Beachten Sie, dass dieselbe Metrik (Online-Bestellungen) unterschiedliche Ergebnisse generiert, wenn Sie verschiedene Attributionsmodelle anwenden.

## Tab-übergreifende Marketing-Analyse

Mithilfe des veralteten First Touch-Kanals und des Last Touch-Kanals erhalten Sie eine hilfreiche Ansicht zu den Interaktionen der Kanal:

![](assets/mc-viz6.png)

In diesem Video erfahren Sie mehr über tabulatorübergreifende Marketing-Analyse: [Verwenden der tabulatorübergreifenden Analyse, um die grundlegende Marketing-Zuordnung in Analysis Workspace zu untersuchen](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/attribution-iq/using-cross-tab-analysis-to-explore-basic-marketing-attribution-in-analysis-workspace.html).
