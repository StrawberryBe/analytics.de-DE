---
description: '[!DNL Activity Map] verfolgt Links mit einem stabileren Algorithmus, der '
seo-description: '[!DNL Activity Map] verfolgt Links mit einem stabileren Algorithmus, der '
seo-title: Zuverlässiges Linktracking
solution: Analytics
title: Zuverlässiges Linktracking
topic: Activity Map
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
translation-type: tm+mt
source-git-commit: ae18932eda59c059e2aa635cc30f233b88840031

---


# Zuverlässiges Linktracking

[!DNL Activity Map] verfolgt Links mit einem stabileren Algorithmus, der:

* Verfolgung von Seitenregionen, um zu verhindern, dass der gleiche Link auf unterschiedlichen Geräten verwechselt wird, da sich der Link an verschiedenen Positionen auf der Seite befindet,
* Eindeutigkeit von Links, d. h. unterschiedliche Links können nicht aufgrund von Problemen mit der Link-ID oder verschiedenen Browsermarken für ein und denselben Link gehalten werden.

For more on link tracking in [!DNL Activity Map], go [here](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md).

## Wie kann [!DNL Activity Map] die Linktracking PII-Daten erfassen? {#section_AEE57510D17B4C21A7D49D32D21D67B9}

> [!CAUTION] Durch Aktivierung der [!DNL Activity Map] Verfolgung erfassen Sie möglicherweise personenbezogene Daten (PII). Diese Daten können allein oder mit anderen Informationen verwendet werden, um eine einzelne Person zu identifizieren, zu kontaktieren oder zu finden oder um eine Einzelperson im Kontext zu identifizieren.

Here are some known cases where PII data might be collected using [!DNL Activity Map] Tracking:

* `Mailto` Links. Ein Mailto-Link ist ein HTML-Linktyp, der den standardmäßigen E-Mail-Client auf dem Computer für das Senden einer E-Mail aktiviert.
* `User ID` Links, die in der Kopf- und Fußzeile einer Website angezeigt werden, sobald sich der Benutzer angemeldet hat.
* Für Kreditinstitute wird möglicherweise die Kontonummer als ein Link angezeigt. Wenn darauf geklickt wird, wird der Linktext erfasst.
* Auf Websites für das Gesundheitswesen werden PII-Daten ebenfalls als Links angezeigt. Durch Klicken auf diese Links wird der Linktext erfasst. Dadurch werden die PII-Daten gesammelt.
