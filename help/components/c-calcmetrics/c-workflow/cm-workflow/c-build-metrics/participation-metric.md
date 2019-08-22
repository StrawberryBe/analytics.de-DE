---
description: Mit dem Generator für berechnete Metriken kann jeder Benutzer eine Beitragsmetrik erstellen.
seo-description: Mit dem Generator für berechnete Metriken kann jeder Benutzer eine Beitragsmetrik erstellen.
seo-title: Beitragsmetrik
title: Beitragsmetrik
uuid: 7 cb 191 be-bc 4 e -46 ef -8 a 20-ccba 5355 e 253
translation-type: tm+mt
source-git-commit: bc0adf08d2b68c314c38f0484addbff567147e88

---


# Beitragsmetrik

Hier ein einfacher Anwendungsfall: Sie sind Eigentümer des Inhalts und möchten sehen, welche Seiten zu Besuchen beigetragen haben (d. h. an Besuchen beteiligt waren), die eine Bestellung enthielten. So geht’s:

>[!NOTE]
>
>Dies mussten Sie über die Admin Tools tun. Sie können Teilnahmemetriken nach wie vor in der Admin Tools aktivieren, jedoch lediglich für die benutzerdefinierten Ereignisse 1–100.

Im Folgenden wird ein einfacher Anwendungsfall beschrieben: Als Inhaber von Inhalt möchten Sie sehen, welche Seiten bei Besuchen beteiligt waren, die zu E-Mail-Anmeldungen geführt haben. Gehen Sie wie folgt vor:

1. Erstellen Sie eine neue Metrik im Generator für berechnete Metriken.
1. Ziehen Sie das Erfolgsereignis "Bestellungen" in die Arbeitsfläche" Definition" .
1. Ändern Sie das [Zuordnungsmodell](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#concept_B7A1FCFEFA9D4C4883208ACE8C9C8E5E) dieses Ereignisses in **[!UICONTROL den Beitrag]** unter " **[!UICONTROL Einstellungen]** " . Wählen Sie **[!UICONTROL "Besuch-]** Lookback" . Die Definition sollte etwa so aussehen:

   ![](assets/participation.png)

1. Speichern Sie die Metrik.
1. Verwenden Sie die errechnete Metrik in einem **[!UICONTROL Seitenbericht]** .

   ![](assets/participation-pages.png)

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei.

