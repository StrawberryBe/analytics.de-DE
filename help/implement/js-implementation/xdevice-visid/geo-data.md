---
description: Geo-Segmentdaten werden auf Grundlage des ersten Treffers des Besuches vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird.
keywords: Analytics-Implementierung
seo-description: Geo-Segmentdaten werden auf Grundlage des ersten Treffers des Besuches vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird.
seo-title: Geo-Segmentdaten
solution: Analytics
title: Geo-Segmentdaten
topic: Entwickler und Implementierung
uuid: 8449 bf 11-c 367-4698-a 73 e-f 6 cb 59 f 8 c 945
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Geo-Segmentdaten

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Geo-Segmentdaten werden auf Grundlage des ersten Treffers des Besuches vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird.

Wenn ein Kunde von seinem privaten Computer aus auf Ihre Website zugreift und dann innerhalb von 30 Minuten noch einmal von seinem Laptop aus Ihre Website besucht, bleiben die Geo-Segmentdaten unverändert. Wenn Sie VISTA verwenden, um eine evar mit Geo-Segmentdaten auszufüllen, basiert diese auf der IP-Adresse in jedem Treffer. Dies kann zu mehreren Datensegmentwerten für Geo-Segmente führen, wenn sich die IP-Adresse für denselben Besuch ändert.
