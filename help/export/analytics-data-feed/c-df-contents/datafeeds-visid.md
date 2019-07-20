---
description: 'null '
keywords: Datenfeed; job; Besucher; Experience Cloud ID; analytics visitor id; identifizieren
seo-description: 'null '
seo-title: Besucher identifizieren
solution: Analytics
title: Besucher identifizieren
topic: Reports and Analytics
uuid: 2490 b 67 e-a 333-422 d -82 fa-cb 0670 ef 2 e 0 c
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Besucher identifizieren

Analytics bietet verschiedene Mechanismen, mit deren Hilfe Besucher identifiziert werden können (aufgelistet in [Identifizieren von Besuchern](../../../export/analytics-data-feed/c-df-contents/datafeeds-visid.md#concept_BE966BABA7D0475BB706BC6676B8FA11)). Regardless of the method used to identify a visitor, in data feeds the final visitor ID used by Analytics is split across the `post_visid_high` and `post_visid_low` columns, even when using the Identity Service.

**Gehen Sie wie folgt vor, um Unique Visitor zu identifizieren:**

1. Exclude all rows where `exclude_hit > 0`.
1. Exclude all rows with `hit_source = 5,7,8,9`. Bei 5, 8, und 9 handelt es sich um Zusammenfassungszeilen, die mithilfe der Datenquellen hochgeladen werden. 7 steht für Transaktions-ID-Datenquellen-Uploads, die nicht beim Zählen der Besuche und Besucher enthalten sein sollten. Siehe [Trefferquellensuche](../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42)
1. Combine `post_visid_high` with `post_visid_low`. All hits across all dates that contain this combination of `post_visid_high` and `post_visid_low` can be considered as coming from same visitor.

Wenn Sie ermitteln möchten, welcher Mechanismus zur Ermittlung des Besucher-ID-Werts verwendet wurde (zum Beispiel zur Berechnung der Cookie-Annahme), enthält `post_visid_type` einen Suchschlüssel, der die verwendete ID-Methode anzeigt. Die Suchschlüssel sind gemeinsam mit den Besucher-ID-Mechanismen in der [Tabelle unten](../../../export/analytics-data-feed/c-df-contents/datafeeds-visid.md#table_D267D36451F643D1BB68AF6FEAA6AD1A) aufgeführt.

## Experience Cloud ID {#section_1628ED37D31E4B0EB75632E397A06B29}

Die Experience Cloud ID wird in der separaten Spalte `mcvisid` genannt. Da diese ID in ihrer eigenen Spalte berichtet wird, kann unklar sein, ob Analytics diese oder eine andere ID verwendet, um den Besucher zu identifizieren.

If the Experience Cloud ID was used to identify the visitor, the ID will be contained in the `post_visid_high` and `post_visid_low` columns and the `post_visid_type` will be set to 5. When calculating metrics, you should use the value from the `post_visid_high` and `post_visid_low` columns since these columns will always contain the final visitor ID.

>[!TIP]
>
> When using the Adobe Analytics visitor ID as a key for other systems, always use `post_visid_high` and `post_visid_low`. Diese Felder sind die einzigen Besucher-ID-Felder, bei denen garantiert jede Zeile des Datenfeeds einen Wert enthält.

## Analytics-Besucher-IDs {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Es gibt verschiedene Wege, Besucher in Analytics zu identifizieren (sie sind in der folgenden Tabelle in der präferierten Reihenfolge aufgelistet):

| Verwendete Reihenfolge | Abfrageparameter (Erfassungsmethode) | Spaltenwert post_visid_type | Vorhanden, wenn |
|---|---|---|---|
| ![](assets/step1_icon.png) | [vid (s.visitorID)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_custom) | 0 | s.visitorID eingestellt wird. |
| ![](assets/step2_icon.png) | [aid (s_vi cookie)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_analytics) | 3 | der Besucher über bestehendes s_vi-Cookie verfügt, bevor Sie den Besucher-ID-Dienst bereitgestellt haben, oder wenn Sie eine [Schonfrist](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_grace_period) für die Besucher-ID konfiguriert haben. |
| ![](assets/step3_icon.png) | [mid (AMCV_ Cookie, festgelegt vom Identitätsdienst)](https://marketing.adobe.com/resources/help/en_US/mcvid/) | 5 | der Browser des Besuchers Cookies (Erstanbieter) akzeptiert und der Identitätsdienst bereitgestellt wird. |
| ![](assets/step4_icon.png) | [fid (Fallback-Cookie auf H.25.3 oder neuer bzw. AppMeasurement für JavaScript)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_fallback) | 4 | der Browser des Besuchers Cookies (intern) akzeptiert. |
| ![](assets/step5_icon.png) | [HTTP Mobilfunk-Teilnehmer-Kopfzeile](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_mobile) | 2 | das Gerät als Mobilgerät erkannt wird. |
| ![](assets/step6_icon.png) | [IP-Adresse, Benutzeragent, Gateway-IP-Adresse](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_fallback) | 1 | der Browser des Besuchers keine Cookies akzeptiert. |

In vielen Szenarien sehen Sie möglicherweise 2 oder 3 verschiedene IDs für einen Aufruf, Analytics verwendet jedoch die erste vorhandene ID aus dieser Liste als offizielle Besucher-ID und teilt den Wert auf die Spalten `post_visid_high` und `post_visid_low` auf. Wenn Sie beispielsweise eine benutzerspezifische Besucher-ID festlegen (die im vid-Abfrageparameter enthalten ist), wird diese ID bevorzugt vor anderen IDs verwendet, die möglicherweise für denselben Treffer vorliegen.
