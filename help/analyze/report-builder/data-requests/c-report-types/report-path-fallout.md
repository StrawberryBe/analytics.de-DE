---
description: Beschreibt, wie Report Builder Pfad- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports & Analytics unterscheidet.
title: Pfad- und Pfad-Fallout-Berichte in Report Builder
feature: Report Builder
role: User, Admin
exl-id: 211b0e76-2895-401d-a5a5-73e459a486e2
source-git-commit: d218d07ec16e981d7e148092b91fbbd5711e840f
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 88%

---

# Pfad- und Pfad-Fallout-Berichte in Report Builder

Beschreibt, wie Report Builder Pfad- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports &amp; Analytics unterscheidet.

| Pfadberichtname in Reports &amp; Analytics (Pfade > Dimension >) | Unterstützt in Report Builder? |
|--- |--- |
| Nächste/Vorherige  Dimension „Fluss“ | Ist nicht als eigenständiger Bericht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Nächste/Vorherige  Dimension | Ist nicht als eigenständiger Bericht verfügbar. Kann mit einem Pfadbericht und mithilfe eines Filters reproduziert werden. |
| Fallout | Als eigenständiger Bericht unterstützt und bereitgestellt (Pfade > Dimension > Dimension Fallout). |
| Vollständige Pfade | Nicht unterstützt. |
| PathFinder | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe eines Filters reproduziert werden. |
| Pfadlänge | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Dimensionszusammenfassung | Ist nicht als eigenständiger Bericht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse > Neuladungen | Ist nicht als eigenständiger Bericht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik „Neuladungen“ reproduziert werden. |
| Seitenanalyse > Dimension „Tiefe“ | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Besuchszeit pro Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege > Entrypages | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Einstiegs-Site“ reproduziert werden. |
| Einstiege und Ausstiege > Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege > Einzelseitenbesuche | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege > Dimension „Ausstieg“ | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Ausstiegs-Site“ reproduziert werden. |
