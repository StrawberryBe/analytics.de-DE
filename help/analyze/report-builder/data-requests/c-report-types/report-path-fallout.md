---
description: Beschreibt, wie Report Builder Pfadsetzungs- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports & Analytics unterscheidet.
title: Pfad- und Pfad-Fallout-Berichte in Report Builder
topic: Report builder
uuid: 9ca6cb97-8f31-46f6-977a-e81a89a176d1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
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
| Seitenübersicht > Analyse | Ist als eigenständiger Bericht nicht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse > Neuladungen | Ist als eigenständiger Bericht nicht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik „Neuladungen“ reproduziert werden. |
| Seitenanalyse > Dimension „Tiefe“ | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Besuchszeit pro Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege > Entrypages | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Einstiegs-Site“ reproduziert werden. |
| Einstiege und Ausstiege > Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege > Einzelseitenbesuche | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege > Dimension „Ausstieg“ | Ist als eigenständiger Bericht nicht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Ausstiegs-Site“ reproduziert werden. |
