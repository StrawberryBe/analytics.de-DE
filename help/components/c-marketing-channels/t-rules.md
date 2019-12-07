---
description: Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.
subtopic: Marketing channels
title: Einrichten von Marketingkanal-Verarbeitungsregeln
topic: Reports and analytics
uuid: 0e47634f-3c69-46db-8af4-8d0b3d15f7a8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

Dieser Vorgang verwendet eine E-Mail-Regel als Beispiel. Es wird davon ausgegangen, dass Sie Ihrer Kanalliste auf der Seite „Marketingkanal-Manager“ einen E-Mail-Kanal hinzugefügt haben.

1. Klicken Sie auf **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Report Suite auswählen.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [!UICONTROL Marketingkanäle: Automatisches Setup] angezeigt.

   Siehe [Ausführen des automatischen Setups](/help/components/c-marketing-channels/c-channel-autosetup.md).

1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Marketing-Kanäle]** &gt; **[!UICONTROL Verarbeitungsregeln für Marketing-Kanäle]**.

   ![Schritt Ergebnis](assets/marketing_channel_rules.png)

1. Wählen Sie im Menü **[!UICONTROL Neuen Regelsatz hinzufügen:]** die Option **[!UICONTROL E-Mail]**.

   Hier wählen Sie keinen Kanal sondern eine Vorlage aus, die die Regel mit einigen der erforderlichen Parameter füllt.

   ![Schritt Ergebnis](assets/example_email.png)

   Verwenden Sie zur Regelkonfiguration die Boolesche Logik (if/then (wenn/dann) Aussagen). In einer E-Mail-Kanalregel geben Sie z. B. die Einstellungen oder Informationen ein, die in der folgenden Regelaussage hervorgehoben sind:

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   In diesem Beispiel ist *`<value>`* der Abfragezeichenfolgenparameter, den Sie für Ihre E-Mail-Kampagne verwenden, wie z. B. *`eml`*.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**, um die Regelerstellung fortzusetzen.
1. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
1. Klicken Sie auf **[!UICONTROL Speichern.]**

>[!MORELIKETHIS]
>
>* [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/c-faq.md)

