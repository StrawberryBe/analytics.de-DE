---
description: Report Builder 5.2 unterstützt vereinheitlichte berechnete Adobe Analytics-Metriken. Neben anderen Innovationen verfügen alle berechneten Metriken jetzt über eine globale ID – sie sind nicht mehr auf eine einzige Report Suite beschränkt.
title: Berechnete Metriken
uuid: c9814894-cda6-40ff-8ec4-3ab2c1908ebc
translation-type: tm+mt
source-git-commit: 96ddfa863fae6044131e27a6d1cddd62d50223eb

---


# Berechnete Metriken

Report Builder 5.2 unterstützt vereinheitlichte berechnete Adobe Analytics-Metriken. Neben anderen Innovationen verfügen alle berechneten Metriken jetzt über eine globale ID – sie sind nicht mehr auf eine einzige Report Suite beschränkt.

>[!NOTE] Vorhandene Arbeitsmappen können auf Anforderungen mit alten Metrik-IDs verweisen. Wenn Sie Report Builder 5.2 verwenden, werden diese alten Metrik-IDs in die neue globale ID konvertiert. Wenn Sie diese Arbeitsmappe für einen Benutzer von Report Builder v5.1 oder älter freigeben, kann dieser Benutzer die berechneten Metriken nicht anzeigen.

Weitere Informationen zum Erstellen und Verwalten von berechneten Metriken mit dem neuen Generator und Manager für berechnete Metriken finden Sie im Handbuch für [berechnete Metriken](https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics) .

In Schritt 2 des Anforderungs-Assistenten können Sie berechnete Metriken filtern und anwenden.

## Berechnete Metriken filtern {#section_376E986D3E684999A7CDB08E53854159}

**Filtern** Sie berechnete Metriken, indem Sie auf das Filtersymbol klicken:  ![](assets/segment_filter.png)

. Das Dialogfeld &quot;Erweiterte Filter&quot;enthält sowohl standardmäßige als auch berechnete Metriken.

Zu den verfügbaren Filtern gehören:

![](assets/advanced_filters.png)

| Filtername | Beschreibung |
|---|---|
| Tags | Ermöglicht das Filtern nach berechneten Metriken mit bestimmten Tags. Beachten Sie, dass Tag-Filter den Operator AND verwenden. Wenn Sie zwei Tags aktivieren, werden im rechten Bereich Metriken angezeigt, die mit **beiden** Tags versehen wurden. |
| Report Suites | Wenn Sie im Generator für berechnete Metriken in [!DNL Reports & Analytics] den Filter „Nur *Name der Report Suite*“ anwenden und dann in [!DNL Report Builder] den erweiterten Filter anzeigen, zeigt der erweiterte Filter nur die berechneten Metriken für die ausgewählte Report Suite an. |
| Eigentümer | Filtert Metriken nach Inhaber. Beachten Sie, dass Filter des Inhabers den Operator OR verwenden. Wenn Sie zwei Inhaber aktivieren, werden im rechten Bereich Metriken angezeigt, die **beiden** Inhabern gehören. |
| Weitere Filter > Genehmigt | Zeigt alle offiziell genehmigten Metriken an. |
| Weitere Filter > Favoriten | Zeigt alle Metriken an, die Sie als Favoriten markiert haben. |
| Weitere Filter > Meine | Zeigt alle Metriken an, deren Inhaber Sie sind. |
| Weitere Filter > Für mich freigegeben | Zeigt alle Metriken an, die andere für Sie freigegeben haben. |

## Berechnete Metriken anwenden {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Nachdem Sie die Filter ausgewählt haben, klicken Sie auf **[!UICONTROL Apply]** , um sie auf Ihre Anforderung anzuwenden. Die ausgewählten Metriken werden jetzt dem Berichtslayout hinzugefügt.

![](assets/filtering_for_metric.png)

