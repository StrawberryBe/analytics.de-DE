---
description: Erstellen Sie ein Adobe Analytics-Tool für die Implementierung mithilfe des Dynamic Tag Managements. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).
keywords: Dynamic Tag Management
seo-description: Erstellen Sie ein Adobe Analytics-Tool für die Implementierung mithilfe des Dynamic Tag Managements. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).
seo-title: Adobe Analytics manuell implementieren (alt)
solution: Experience Cloud, Analytics, Target, Dynamisches Tag-Management
title: Adobe Analytics manuell implementieren (alt)
uuid: d3ad2035-393d-4a77-81f6-e749ee717c09
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Adobe Analytics manuell implementieren (alt)

Create an Adobe Analytics tool for deployment using [!UICONTROL Dynamic Tag Management]. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).

Informationen zur automatischen Implementierungsverwaltung finden Sie unter [Adobe Analytics-Tool hinzufügen](../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8).

Wenn Sie eine manuelle Konfiguration auf automatisch umstellen möchten, bearbeiten Sie ein Tool und klicken Sie auf **[!UICONTROL Automatische Konfiguration aktivieren]**.

1. Laden Sie den Analytics-Messungscode herunter:
   1. In Analytics, click **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]**.
   1. Click **[!UICONTROL JavaScript (new)]** to download the code locally.
1. Im [!UICONTROL dynamischen Tag-Management][erstellen Sie eine Webeigenschaft](../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123).

   ![](assets/dtm-property.png)

   Nachdem Sie die Webeigenschaft erstellt haben, ist diese auf der Registerkarte [!UICONTROL Webeigenschaften] im [!UICONTROL Dashboard] zur Bearbeitung verfügbar. Es ist nicht erforderlich, die Webeigenschaft zu aktivieren..

1. Fügen Sie der Eigenschaft ein Analytics-Tool hinzu:
   1. On the **[!UICONTROL Web Properties]** tab, click the property.
   1. On the **[!UICONTROL Overview]** tab, click **[!UICONTROL Add a Tool]**.
   1. From the **[!UICONTROL Tool Type]** menu, select **[!UICONTROL Adobe Analytics]**.

      ![](assets/dtm-add-analytics-tool.png)

   1. Konfigurieren Sie die folgenden Felder:

      | Element | Beschreibung |
      |---|---|
      | Tool-Typ | Experience Cloud-Lösung, z. B. Analytics, Target, Social usw. |
      | Tool-Name | Der Werkzeugname. Dieser Name wird auf der Registerkarte [!UICONTROL Übersicht] unter [!UICONTROL Installierte Tools] angezeigt. |
      | Produktions-Konto-ID | Eine ID für Ihr Produktions-Konto zur Datensammlung. Das Dynamic Tag Management installiert automatisch das richtige Konto in der Produktions- und Staging-Umgebung. |
      | Staging-Konto-ID | Eine ID, die für Ihre Entwicklungs- oder Testumgebung verwendet wird. Mit dem Staging-Konto werden Ihre Testdaten von der Produktion getrennt gehalten. |

1. Klicken Sie auf **[!UICONTROL Tool erstellen]**.

   Auf der Registerkarte [!UICONTROL Übersicht] wird das installierte Tool angezeigt.

1. To configure the code, click **[!UICONTROL Settings]** ![](assets/settings_gear.png).

   Klicken Sie mindestens auf **[!UICONTROL Cookies]und konfigurieren Sie Ihren Tracking-Server und den SSL-Tracking-Server.**

1. Klicken Sie auf **[!UICONTROL Allgemein]** und [fügen Sie den Kern-AppMeasurement-Code](../../implement/c-implement-with-dtm/c-aa-tool/t-appmeasurement-code.md#task_068D72664B2743359A64ADB8692D3658)ein.
1. Definieren Sie eine [Seitenladeregel](../../implement/c-implement-with-dtm/c-rules/t-rules-create.md#task_B7FB5ED415AF430C952265AC2835C0DB) , um [!DNL Analytics]Daten zu erfassen.

   Sie können nun Regeln zum Sammeln von Analysedaten definieren. Möglicherweise möchten Sie zuerst einige Datenelemente definieren. Mithilfe von Datenelementen können Sie Daten aus der Seite extrahieren, die Sie verwenden können, um Ihre Regel zu konfigurieren. To get started, you can define a page load rule that does not have any conditions to collect [!DNL Analytics] data on each page.
1. [Fügen Sie auf der Registerkarte „Einbettung“ den Kopf- und Fußzeilencode hinzu.](../../implement/c-implement-with-dtm/c-headers-footers/t-header-footer-code.md#task_43C8DD699A514638B0620775C06423E5)

   Für die Staging-Umgebung können Sie die Standard-Hostingoption Amazon beibehalten. Sie können diese Option bei Bedarf vor der Implementierung in der Produktionsumgebung ändern.
1. (Optional) Click **[!UICONTROL Settings]** ![](assets/settings_gear.png) on the Options tab, and configure the Adobe Analytics code.

   >[!NOTE]
   >
   >The settings on the [!UICONTROL Adobe Analytics] page (General, Cookies, and so on) override settings in your `s_code`. Wenn diese Einstellungen in Ihrem `s_code` vorhanden sind, müssen sie an dieser Stelle nicht wiederholt werden.

