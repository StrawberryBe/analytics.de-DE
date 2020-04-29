---
description: Einstiege geben an, wie oft ein Wert als erster Wert bei einem Besuch erfasst wird. Einstiege können nur einmal pro Besuch auftreten. Wenn die Variable nicht definiert ist, dann ist dies jedoch nicht zwingend der erste Hit.
title: Einträge
topic: Metrics
uuid: c4608b66-b70c-4e98-b7c6-9be5fbe4ec9c
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Einträge

&quot;Einträge&quot;gibt an, wie oft ein bestimmter Wert als erster Wert bei einem Besuch erfasst wird. Einstiege können nur einmal pro Besuch auftreten. Wenn die Variable nicht definiert ist, dann ist dies jedoch nicht zwingend der erste Hit.

In Analysis Workspace wurde im März 2020 die Weise geändert, wie der Wert „Keine“ in Bezug auf Einstiege/Ausstiege verwendet wird.  Da Sie jetzt &quot;Nones&quot;in Analyse Workspace aktivieren und deaktivieren können, wird &quot;Keine&quot;nach dem Ein- oder Ausstieg angewendet, während sie (bei &quot;evars&quot;) zuvor angewendet wurde.  Nehmen wir beispielsweise an, der erste Treffer eines Besuchs hat keinen Wert für z. B. eVar21, der zweite Treffer jedoch nicht. In Reports &amp; Analytics wird als Wert für den Einstieg „Nicht angegeben“ angezeigt, aber in Analysis Workspace wird dieser Wert beim zweiten Treffer angezeigt.

Entrypages werden pro Besuch aufgeschlüsselt, d. h., sie werden für alle Hits für einen Besuch beibehalten. Weitere Informationen finden Sie unter [Aufschlüsselung und Segmentierungscontainer](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-overview.html).
