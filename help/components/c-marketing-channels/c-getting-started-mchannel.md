---
title: Erste Schritte mit Marketingkanälen
description: Erfahren Sie mehr zum Arbeitsablauf für Marketingkanäle, zur automatischen Einrichtung und zum Anwenden der Report Suite-Vorlageneinstellungen auf mehrere Report Suites.
translation-type: tm+mt
source-git-commit: 21f4b9df688776f7a1db96f76e258031ae3abb3d

---


# Erste Schritte mit Marketingkanälen

Marketingkanäle werden häufig dazu verwendet, einen Einblick darin zu erhalten, wie Besucher auf Ihre Site gelenkt werden. Sie können basierend auf den Kanälen, die Sie nachverfolgen möchten, und darauf, wie Sie diese nachverfolgen möchten, eigene Marketingkanal-Verarbeitungsregeln anpassen.

Marketingkanäle kreisen um First- und Last-Touch-Metriken, die Komponenten von standardmäßigen Konversionsmetriken sind.

## Arbeitsablauf der Marketingkanäle

![](assets/step1_icon.png) Definieren jedes Kanals auf Grundlage Ihrer Geschäftsanforderungen.

Das Definieren der von Ihnen verwendeten Kanäle ist eine der wichtigsten Komponenten der Marketingkanäle. Das Definieren der Kanäle kann die Zusammenarbeit mehrerer Einzelpersonen in Ihrer Organisation erfordern. Im Folgenden finden Sie einige zu berücksichtigende Fragen:

* Nutzen Sie eine gebührenpflichtige Suche?
* Nutzen Sie E-Mail-Kampagnen? Nutzen Sie mehrere E-Mail-Kampagnen, die Sie getrennt nachverfolgen möchten?
* Haben Sie Affiliates, die den Datenverkehr an Ihre Website weiterleiten? Sind Affiliates vorhanden, die Sie einzeln nachverfolgen möchten?
* Sind externe Kampagnen vorhanden, für die eine getrennte Nachverfolgung vorteilhaft wäre?
* Möchten Sie alle Websites mit sozialen Netzwerken zusammenfassen, oder gibt es soziale Netzwerke, die Sie einzeln nachverfolgen möchten?
* Sind andere Kanäle vorhanden, die möglicherweise die Konversion beeinflussen, die Sie nachverfolgen möchten?

Eine Liste mit empfohlenen Kanälen finden Sie unter [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/c-faq.md). Erstellen Sie eine Liste der Kanäle, die Sie nutzen möchten, um die Aktivierung und Definierung beim Erstellen von Kanälen zu vereinfachen.

![](assets/step2_icon.png) Fügen Sie Marketingkanäle auf der [!UICONTROL Marketing Channel Manager] Seite hinzu.

After defining what channels to track, you enable them in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

Wichtige Voraussetzungen und grundlegende Informationen finden Sie unter [Kanäle und Regeln](/help/components/c-marketing-channels/c-channels.md).

Informationen zum Verfahren finden Sie unter [Hinzufügen von Marketing-Kanälen](/help/components/c-marketing-channels/c-channels.md).

>[!NOTE]
>
>Wenn Marketing-Kanäle noch nicht konfiguriert wurden, wird das [automatische Setup](/help/components/c-marketing-channels/c-getting-started-mchannel.md) angezeigt. Dieses Setup stellt mehrere vorkonfigurierte Kanäle bereit, die Sie anpassen können. Adobe empfiehlt, dass Sie diese Regeln als Vorlage verwenden. Wenn Sie jedoch bereits über zuverlässige Kanaldefinitionen verfügen, können Sie das automatische Setup überspringen.

![](assets/step3_icon.png) Konfigurieren oder verfeinern Sie die Regeln der einzelnen Kanäle auf der [!UICONTROL Marketing Channel Processing Rules] Seite.

After you create channels on the [!UICONTROL Marketing Channel Manager] page, you configure the rules so that channels can retrieve and report data.

See [Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md).

Wenn Kanäle im automatischen Setup erstellt wurden, werden die Regeln in diesen Kanälen definiert. Sie können sie an Ihre Bedürfnisse anpassen.

## Automatische Einrichtung für Marketingkanäle {#run-auto-setup}

Der Marketing-Kanal-Bericht bietet zum Einstieg eine einmalige Setup-Seite. Hier finden Sie eine Vielzahl an Marketing-Kanälen, die Sie zur Nachverfolgung nutzen können. Wenn Sie mit der Erstellung von Kanälen und Regeln vertraut sind, können Sie dieses Setup überspringen. Adobe empfiehlt jedoch, dass Sie den Assistent zur Erstellung der Kanäle nutzen. Durch das automatische Setup sehen Sie, wie Regeln erstellt werden. Darüber hinaus haben Sie die Möglichkeit, diese individuell anzupassen. Sie können die vordefinierten Kanäle jederzeit deaktivieren oder löschen.

So führen Sie das automatische Setup für Marketingkanäle aus.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. On the [!UICONTROL Report Suite Manager], select a report suite.
1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   ![Schritt Ergebnis](assets/wizard.png)

   >[!NOTE]
   >
   >The [!UICONTROL Marketing Channels: Auto Setup] page displays automatically when you access channel configuration applications in Admin Tools. (Weitere Informationen finden Sie unter [Marketing-Kanal-Manager](/help/components/c-marketing-channels/c-channels.md).) Die Seite wird nicht angezeigt, wenn Ihre Report Suite einen oder mehrere Marketingkanäle enthält. Sie können nur dann erneut auf die Seite zugreifen, wenn Sie eine andere Report Suite ohne Marketingkanäle auswählen.

1. Stellen Sie sicher, dass die gewünschten Kanäle ausgewählt sind.

   When selected, **[!UICONTROL Email]**, **[!UICONTROL Display]**, and **[!UICONTROL Affiliate]** are required fields.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites

So verwenden Sie eine Master-Report Suite als Vorlage, um Ihre Marketingkanalkonfiguration zu testen. Diese Vorlage kann zur Zeitersparnis in einer Massenaktualisierung für eine oder mehrere Produktions-Report Suites übernommen werden. Diese Aufgabe muss separat für Kanäle und Regelsätze erfolgen.

> [!NOTE] Übernehmen Sie zunächst die Kanäle aus einer Vorlage, bevor Sie Regelsätze einsetzen. Bei diesem Ablauf müssen die Kanäle für alle Report Suites identisch sein.

1. Stellen Sie sicher, dass der Marketingkanalbericht für die gewünschten Report Suites aktiviert wurde. Dieser Schritt wird von Ihrem Kundenbetreuer durchgeführt.
1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie auf der Seite **[!UICONTROL Report Suite Manager]** die Vorlagen-Report Suite sowie eine oder mehrere Ziel-Report Suites aus.
1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.
1. On the **[!UICONTROL Select Master Report Suites]** page, select a template report suite.
1. Klicken Sie auf **[!UICONTROL Save All]**.
1. Übernehmen von Regeln aus einer Vorlage für mehrere Report Suites:
   1. Return to the [!UICONTROL Report Suite Manager] page.
   1. Wählen Sie auf der Seite Report Suite-Manager die Vorlagen-Report Suite sowie eine oder mehrere Ziel-Report Suites aus.
   1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.
   1. Klicken Sie auf **[!UICONTROL Save]**. Wenn die Schaltfläche „Speichern“ deaktiviert ist, aktivieren Sie sie, indem Sie eine der Regeln erweitern.

