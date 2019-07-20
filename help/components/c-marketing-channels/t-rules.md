---
description: Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.
seo-description: Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.
seo-title: Einrichten von Marketingkanal-Verarbeitungsregeln
solution: Analytics
subtopic: Marketingkanäle
title: Einrichten von Marketingkanal-Verarbeitungsregeln
topic: Reports and Analytics
uuid: 0 e 47634 f -3 c 69-46 db -8 af 4-8 d 0 b 3 d 15 f 7 a 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

Dieser Vorgang verwendet eine E-Mail-Regel als Beispiel. Es wird davon ausgegangen, dass Sie Ihrer Kanalliste auf der Seite „Marketingkanal-Manager“ einen E-Mail-Kanal hinzugefügt haben.

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [!UICONTROL Marketingkanäle: Automatisches Setup] angezeigt.

   Siehe [Ausführen des automatischen Setups](/help/components/c-marketing-channels/c-channel-autosetup.md).

1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Marketing Channels]** &gt; **[!UICONTROL Marketing Channel Processing Rules]**.

   ![Schritt Ergebnis](assets/marketing_channel_rules.png)

1. Wählen Sie im Menü **Neuen Regelsatz hinzufügen:** die Option **[!UICONTROL E-Mail]**.

   Hier wählen Sie keinen Kanal sondern eine Vorlage aus, die die Regel mit einigen der erforderlichen Parameter füllt.

   ![Schritt Ergebnis](assets/example_email.png)

   Verwenden Sie zur Regelkonfiguration die Boolesche Logik (if/then (wenn/dann) Aussagen). In einer E-Mail-Kanalregel geben Sie z. B. die Einstellungen oder Informationen ein, die in der folgenden Regelaussage hervorgehoben sind:

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   In this example, *`<value>`* is the query string parameter that you use for your email campaign, such as *`eml`*.
1. To continue creating rules, click **[!UICONTROL Add Rule]**.
1. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
1. Klicken Sie auf **[!UICONTROL Speichern.]**

>[!MORE_LIKE_THIS]
>
>* [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/c-faq.md)

