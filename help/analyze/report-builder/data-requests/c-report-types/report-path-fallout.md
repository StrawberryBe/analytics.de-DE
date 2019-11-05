---
description: Beschreibt, wie ReportBuilder Pfade- und Trichteranalyseberichte unterstützt und wie sich die Implementierung von Reports & Analysen unterscheidet.
seo-description: Beschreibt, wie ReportBuilder Pfade- und Trichteranalyseberichte unterstützt und wie sich die Implementierung von Reports & Analysen unterscheidet.
seo-title: Pfad- und Pfad-Fallout-Berichte in Report Builder
solution: Analytics
title: Pfad- und Pfad-Fallout-Berichte in Report Builder
topic: ReportBuilder
uuid: 9ca6cb97-8f31-46f6-977a-e81a89a176d1
translation-type: tm+mt
source-git-commit: bc46011a48aa18e33ba6f1912223857f5a664f35

---


# Pfad- und Pfad-Fallout-Berichte in Report Builder

Beschreibt, wie ReportBuilder Pfade- und Trichteranalyseberichte unterstützt und wie sich die Implementierung von Reports &amp; Analysen unterscheidet.

| Pfadberichtname in Reports &amp; Analysen (Pfade &gt; Dimension &gt;) | Unterstützt in ReportBuilder? |
|--- |--- |
| Nächste/Vorherige  Dimensionsfluss | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Nächste/Vorherige  Dimension | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Pfadbericht und mithilfe eines Filters reproduziert werden. |
| Fallout | Unterstützt und als eigenständiger Bericht bereitgestellt ( Pfade &gt; Dimension &gt; Dimension-Trichteranalyse). |
| Vollständige Pfade | Nicht unterstützt. |
| PathFinder | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines Filters reproduziert werden. |
| Path Length | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse &gt;  Dimensionszusammenfassung | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse &gt; Neuladungen | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik Neuladungen reproduziert werden. |
| Seitenanalyse &gt; Dimensionstiefe | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse &gt; Besuchszeit für Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege &gt; Entrypages | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters Einstiegssite reproduziert werden. |
| Einstiege und Ausstiege &gt; Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege &gt; Einzelseitenbesuche | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege &gt; Ausstiegsdimension | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters Ausstiegssite reproduziert werden. |
