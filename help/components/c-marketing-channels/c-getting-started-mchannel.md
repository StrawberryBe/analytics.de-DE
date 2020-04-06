---
title: Erste Schritte mit Marketing-Kanälen
description: Erfahren Sie mehr zum Arbeitsablauf für Marketing-Kanal, zur automatischen Einrichtung und zum Anwenden der Report Suite-Vorlageneinstellungen auf mehrere Report Suites.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Erste Schritte mit Marketing-Kanälen

Marketing-Kanal werden häufig verwendet, um Einblicke darüber zu erhalten, wie Besucher auf Ihre Site gelangen. Sie können Ihre Verarbeitungsregeln für den Marketing Kanal je nach den zu verfolgenden Kanälen und der Art ihrer Verfolgung anpassen.

Marketingkanäle kreisen um First- und Last-Touch-Metriken, die Komponenten von standardmäßigen Konversionsmetriken sind.

## Arbeitsablauf für Marketing-Kanal

![](assets/step1_icon.png) Definieren jedes Kanals auf Grundlage Ihrer Geschäftsanforderungen.

Die Definition der von Ihnen verwendeten Kanal ist eine der wichtigsten Komponenten von Marketing-Kanälen. Die Definition der Kanal kann die Zusammenarbeit zwischen mehreren Personen in Ihrem Unternehmen erfordern. Im Folgenden sind einige zu berücksichtigende Fragen aufgeführt:

* Verwenden Sie eine gebührenpflichtige Suche?
* Verwenden Sie E-Mail-Kampagnen? Verwenden Sie mehrere E-Mail-Kampagnen, die Sie separat nachverfolgen möchten?
* Haben Sie Affiliates, die den Traffic zu Ihrer Site leiten? Gibt es Affiliates, die Sie einzeln verfolgen möchten?
* Gibt es externe Kampagnen, die bei der getrennten Verfolgung von Vorteil wären?
* Möchten Sie alle Social Networking-Sites Aggregat haben oder gibt es solche, die Sie einzeln verfolgen möchten?
* Gibt es andere Kanal, die sich auf die Konvertierung auswirken können, die Sie verfolgen möchten?

Eine Liste mit empfohlenen Kanälen finden Sie unter  [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/c-faq.md). Erstellen Sie eine Liste der Kanäle, die Sie nutzen möchten, um die Aktivierung und Definierung beim Erstellen von Kanälen zu vereinfachen.

![](assets/step2_icon.png) Hinzufügen Marketing-Kanal auf der [!UICONTROL Marketing Channel Manager] Seite.

After defining what channels to track, you enable them in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

Wichtige Voraussetzungen und grundlegende Informationen finden Sie unter [Kanäle und Regeln](/help/components/c-marketing-channels/c-channels.md).

Informationen zum Verfahren finden Sie unter [Hinzufügen von Marketing-Kanälen](/help/components/c-marketing-channels/c-channels.md).

>[!NOTE]
>
>Wenn Marketing-Kanäle noch nicht konfiguriert wurden, wird das [automatische Setup](/help/components/c-marketing-channels/c-getting-started-mchannel.md) angezeigt. Dieses Setup bietet mehrere vorkonfigurierte Kanal, die Sie anpassen können. Adobe empfiehlt, diese Regeln als Vorlage zu verwenden. Wenn Sie jedoch bereits über solide Kanal-Definitionen verfügen, können Sie die automatische Einrichtung überspringen.

![](assets/step3_icon.png) Konfigurieren oder verfeinern Sie die Regeln der einzelnen Kanal auf der [!UICONTROL Marketing Channel Processing Rules] Seite.

After you create channels on the [!UICONTROL Marketing Channel Manager] page, you configure the rules so that channels can retrieve and report data.

See [Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md).

Wenn Kanal im automatischen Setup erstellt wurden, werden die Regeln in diesen Kanälen definiert. Sie können sie an Ihre Bedürfnisse anpassen.

## Automatische Einrichtung für Marketing-Kanal {#run-auto-setup}

Der Marketing-Kanal-Bericht bietet zum Einstieg eine einmalige Setup-Seite. Hier finden Sie eine Vielzahl an Marketing-Kanälen, die Sie zur Nachverfolgung nutzen können. Wenn Sie mit der Erstellung von Kanälen und Regeln vertraut sind, können Sie dieses Setup überspringen. Adobe empfiehlt jedoch, dass Sie dem Assistenten gestatten, die Kanal für Sie zu erstellen. Mit dem automatischen Setup können Sie sehen, wie Regeln erstellt werden, oder sie für eigene Zwecke bearbeiten. Sie können die vordefinierten Kanal jederzeit deaktivieren oder löschen.

So führen Sie das automatische Setup für Marketingkanäle aus.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. On the [!UICONTROL Report Suite Manager], select a report suite.
1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   ![Schritt Ergebnis](assets/wizard.png)

   >[!NOTE]
   >
   >The [!UICONTROL Marketing Channels: Auto Setup] page displays automatically when you access channel configuration applications in Admin Tools. (Weitere Informationen finden Sie unter [Marketing-Kanal-Manager](/help/components/c-marketing-channels/c-channels.md).) Die Seite wird nicht angezeigt, wenn Ihre Report Suite einen oder mehrere Marketingkanäle enthält. Sie können nur dann erneut auf diese Seite zugreifen, wenn Sie eine andere Report Suite auswählen, die keine Marketing-Kanal enthält.

1. Stellen Sie sicher, dass die gewünschten Kanäle ausgewählt sind.

   When selected, **[!UICONTROL Email]**, **[!UICONTROL Display]**, and **[!UICONTROL Affiliate]** are required fields.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites

Verwenden einer Master-Report Suite als Vorlage zum Testen Ihrer Marketing Kanal-Konfiguration. Diese Vorlage kann zur Zeitersparnis in einer Massenaktualisierung für eine oder mehrere Produktions-Report Suites übernommen werden. Diese Aufgabe wird für Kanal und Regelsätze separat durchgeführt.

>[!NOTE] Übernehmen Sie zunächst die Kanäle aus einer Vorlage, bevor Sie Regelsätze einsetzen. Bei diesem Ablauf müssen die Kanäle für alle Report Suites identisch sein.

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

