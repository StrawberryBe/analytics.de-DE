---
description: Mit dem Generator für berechnete Metriken kann jeder Benutzer eine Beitragsmetrik erstellen.
seo-description: Mit dem Generator für berechnete Metriken kann jeder Benutzer eine Beitragsmetrik erstellen.
seo-title: Beitragsmetrik
title: Beitragsmetrik
uuid: 7cb191be-bc4e-46ef-8a20-ccba5355e253
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# Beitragsmetrik

Hier ein einfacher Anwendungsfall: Sie sind Inhaltsbesitzer und möchten sehen, welche Seiten zu Besuchen beigetragen haben (d.h. an Besuchen teilgenommen haben), die eine Bestellung enthielten. So geht’s:

> [!NOTE] Früher mussten Sie dies über die Admin Tools tun. Sie können Teilnahmemetriken nach wie vor in der Admin Tools aktivieren, jedoch lediglich für die benutzerdefinierten Ereignisse 1–100.

Im Folgenden wird ein einfacher Anwendungsfall beschrieben: Als Inhaber von Inhalt möchten Sie sehen, welche Seiten bei Besuchen beteiligt waren, die zu E-Mail-Anmeldungen geführt haben. So geht’s:

1. Erstellen Sie eine neue Metrik im Generator für berechnete Metriken.
1. Ziehen Sie das Erfolgsereignis "Bestellungen"in die Arbeitsfläche "Definition".
1. Ändern Sie das [Zuordnungsmodell](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) dieses Ereignisses in **[!UICONTROL Teilnahme]** unter dem **[!UICONTROL Einstellungswerkzeug]** . Wählen Sie **[!UICONTROL Besuchs]** -Lookback. Die Definition sollte etwa so aussehen:

   ![](assets/participation.png)

1. Speichern Sie die Metrik.
1. Verwenden Sie die berechnete Metrik in einem **[!UICONTROL Seitenbericht]** .

   ![](assets/participation-pages.png)

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei.

