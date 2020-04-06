---
description: Mit dem Generator für berechnete Metriken kann jeder eine Beitragsmetrik erstellen.
title: Beitragsmetrik
uuid: 7cb191be-bc4e-46ef-8a20-ccba5355e253
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Beitragsmetrik

Im Folgenden wird ein einfacher Anwendungsfall beschrieben: Als Inhaber von Inhalt möchten Sie sehen, welche Seiten bei Besuchen beteiligt waren, die zu einer Bestellung geführt haben. So geht’s:

>[!NOTE] Bisher mussten Sie hierzu die Admin Tools verwenden. Sie können Beitragsmetriken weiterhin in den Admin Tools aktivieren, jedoch nur für benutzerdefinierte Ereignis 1 - 100.

Im Folgenden wird ein einfacher Anwendungsfall beschrieben: Als Inhaber von Inhalt möchten Sie sehen, welche Seiten bei Besuchen beteiligt waren, die zu E-Mail-Anmeldungen geführt haben. So geht’s:

1. Erstellen Sie eine neue Metrik im Generator für berechnete Metriken.
1. Ziehen Sie das Erfolgsereignis „Bestellungen“ in die Arbeitsfläche „Definition“.
1. Change the [attribution model](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) of that event to **[!UICONTROL Participation]** under the **[!UICONTROL Settings]** gear. Wählen Sie **[!UICONTROL Visit]** Lookback. Die Definition sollte in etwa wie folgt aussehen:

   ![](assets/participation.png)

1. Speichern Sie die Metrik.
1. Use the calculated metric in a **[!UICONTROL Pages]** report.

   ![](assets/participation-pages.png)

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei.

