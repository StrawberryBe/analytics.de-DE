---
description: Beschreibt, wie Report Builder Pfadsetzungs- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports & Analytics unterscheidet.
title: Pfad- und Pfad-Fallout-Berichte in Report Builder
feature: Report Builder
role: User, Admin
exl-id: 211b0e76-2895-401d-a5a5-73e459a486e2
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 98%

---

# Pfad- und Pfad-Fallout-Berichte in Report Builder

Beschreibt, wie Report Builder Pfadsetzungs- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports &amp; Analytics unterscheidet.

| Pfadberichtname in Reports &amp; Analytics (Pfade > Dimension >) | Unterstützt in Report Builder? |
|--- |--- |
| Nächste/Vorherige  Dimension „Fluss“ | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Nächste/Vorherige  Dimension | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Pfadbericht und mithilfe eines Filters reproduziert werden. |
| Fallout | Als eigenständiger Bericht unterstützt und bereitgestellt (Pfade > Dimension > Dimension Fallout). |
| Vollständige Pfade | Nicht unterstützt. |
| PathFinder | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines Filters reproduziert werden. |
| Pfadlänge | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Dimensionszusammenfassung | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse > Neuladungen | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik „Neuladungen“ reproduziert werden. |
| Seitenanalyse > Dimension „Tiefe“ | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Besuchszeit pro Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege > Entrypages | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Einstiegs-Site“ reproduziert werden. |
| Einstiege und Ausstiege > Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege > Einzelseitenbesuche | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege > Dimension „Ausstieg“ | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Ausstiegs-Site“ reproduziert werden. |
