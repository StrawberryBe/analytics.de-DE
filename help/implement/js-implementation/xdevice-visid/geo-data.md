---
description: Geo-Segmentdaten werden auf Grundlage des ersten Treffers des Besuches vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird.
keywords: Analytics Implementation
solution: Analytics
title: Geo-Segmentdaten
topic: Developer and implementation
uuid: 8449bf11-c367-4698-a73e-f6cb59f8c945
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Geo-Segmentdaten

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud Device Co-op-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Geo-Segmentdaten werden auf Grundlage des ersten Treffers des Besuches vermerkt und bei einem einzelnen Besuch nicht geändert, wobei es keine Rolle spielt, welches Gerät verwendet wird.

Wenn ein Kunde von seinem privaten Computer aus auf Ihre Website zugreift und dann innerhalb von 30 Minuten noch einmal von seinem Laptop aus Ihre Website besucht, bleiben die Geo-Segmentdaten unverändert. Wenn Sie VISTA einsetzen, um eine eVar mit Geo-Segmentdaten aufzufüllen, erfolgt dies auf der Grundlage der IP-Adresse in jedem Treffer. Das kann dazu führen, dass mehrere Geo-Segmentdatenwerte vorhanden sind, wenn sich die IP-Adresse beim gleichen Besuch ändert.
