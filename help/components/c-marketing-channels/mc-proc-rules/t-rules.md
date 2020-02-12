---
title: Einrichten von Marketingkanal-Verarbeitungsregeln
description: Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.
translation-type: tm+mt
source-git-commit: ea4d9e6c9396032fe323de594cb43eecbf97aa15

---


# Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

Dieser Vorgang verwendet eine E-Mail-Regel als Beispiel. Es wird davon ausgegangen, dass Sie Ihrer Kanalliste auf der Seite „Marketingkanal-Manager“ einen E-Mail-Kanal hinzugefügt haben.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Report Suite auswählen.

   If your report suite does not have channels defined, the [!UICONTROL Marketing Channels: Auto Setup] page displays.

   See [Run the Automatic Setup](/help/components/c-marketing-channels/getting-started/c-channel-autosetup.md).

1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.

   ![Schritt Ergebnis](assets/marketing_channel_rules.png)

1. Wählen Sie im **[!UICONTROL Add New Rule Set]** Menü die Option **[!UICONTROL Email]**.

   Hier wählen Sie keinen Kanal sondern eine Vorlage aus, die die Regel mit einigen der erforderlichen Parameter füllt.

   ![Schritt Ergebnis](assets/example_email.png)

   Verwenden Sie zur Regelkonfiguration die Boolesche Logik (if/then (wenn/dann) Aussagen). In einer E-Mail-Kanalregel geben Sie z. B. die Einstellungen oder Informationen ein, die in der folgenden Regelaussage hervorgehoben sind:

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   In diesem Beispiel ist *`<value>`* der Abfragezeichenfolgenparameter, den Sie für Ihre E-Mail-Kampagne verwenden, wie z. B. *`eml`*.
1. Um weitere Regeln zu erstellen, klicken Sie auf **[!UICONTROL Add Rule]**.
1. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
1. Klicken Sie auf **[!UICONTROL Save.]**

>[!MORELIKETHIS]
>
>* [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/mc-faq/c-faq.md)

