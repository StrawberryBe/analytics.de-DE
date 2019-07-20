---
description: Beschreibt, wie reportbuilder Pfadberichte und Trichteranalysen unterstützt und wie die Implementierung von Reports & Analysen abweicht.
seo-description: Beschreibt, wie reportbuilder Pfadberichte und Trichteranalysen unterstützt und wie die Implementierung von Reports & Analysen abweicht.
seo-title: Pfad- und Pfadfallout-Berichte in Reportbuilder
solution: Analytics
title: Pfad- und Pfadfallout-Berichte in Reportbuilder
topic: ReportBuilder
uuid: 9 ca 6 cb 97-8 f 31-46 f 6-977 a-e 81 a 89 a 176 d 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pfad- und Pfadfallout-Berichte in Reportbuilder

Beschreibt, wie reportbuilder Pfadberichte und Trichteranalysen unterstützt und wie die Implementierung von Reports &amp; Analysen abweicht.

| Pfadberichtsname in Reports &amp; Analysen (Pfade &gt; Dimension &gt;) | Unterstützt in ReportBuilder? |
|--- |--- |
| Nächste/Vorherige  Dimensionsfluss | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Nächste/Vorherige  Dimension | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Pfadbericht und mithilfe eines Filters reproduziert werden. |
| Trichteranalyse | Unterstützt und als eigenständiger Bericht bereitgestellt (Pfade &gt; Dimension &gt; Dimension Trichteranalyse). |
| Vollständige Pfade | Nicht unterstützt. |
| PathFinder | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines Filters reproduziert werden. |
| Pfadlänge | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse &gt;  Dimensionszusammenfassung | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse &gt; Neuladungen | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik Neuladungen reproduziert werden. |
| Seitenanalyse &gt; Dimensionstiefe | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse &gt; Besuchszeit für Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege &gt; Entrypages | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters Einstiegssite reproduziert werden. |
| Einstiege und Ausstiege &gt; Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege &gt; Einzelseitenbesuche | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege &gt; Ausstieg  Dimension | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters Ausstiegssite reproduziert werden. |