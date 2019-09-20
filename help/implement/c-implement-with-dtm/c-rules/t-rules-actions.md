---
description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
keywords: Dynamisches Tag-Management;Regel;Regel erstellen;Neue Regel;JavaScript/Drittanbieter-Tags;Einrichten von Aktionen für Bedingung;Hinzufügen von neuem Skript;Nicht sequenzielles Javascript;sequenzielles Javascript;Nicht sequenzielles HTML
seo-description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
seo-title: Aktionen einrichten, die von der Bedingung ausgelöst werden
solution: Experience Cloud, Analytics, Target, Dynamisches Tag-Management
title: Aktionen einrichten, die von der Bedingung ausgelöst werden
uuid: 2e892f0b-7261-41ee-b849-6e3054a38de0
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Aktionen einrichten, die von der Bedingung ausgelöst werden

Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.

Nachdem Sie die Bedingung eingerichtet haben, müssen Sie die Aktionen einrichten, die von der Bedingung ausgelöst werden sollen. These actions can include [!DNL Analytics] events, third-party tags, and custom scripts. Im folgenden Beispiel wird beschrieben, wie Sie Skripte oder Drittanbieter-Tags einrichten.

Neben integrierten Tools wie [!DNL Adobe Analytics] und Google Analytics kann das Dynamic Tag Management jede Art von JavaScript auslösen oder HTML in Ihre Website einfügen – in ausgewählten Seiten oder in spezifischen Szenarios.

Jede Regel kann beliebig viele Skripte auslösen oder HTML-Codes einfügen.

>[!NOTE]
>
>Because DTM allows you to inject custom code into your page, please take care not to create cross-site scripting (XSS) vulnerabilities (see [OWASP’s guide](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)) for more info). Bei der Verwendung von Datenelementen in Skripten muss besonders vorsichtig vorgegangen werden. Gehen Sie stets davon aus, dass Datenelementwerte von nicht vertrauenswürdigen Quellen übermittelt werden könnten.

**So richten Sie Aktionen ein, die von der Bedingung ausgelöst werden**

1. Click **[!UICONTROL JavaScript / Third Party Tags]** to add a new script to your rule.

   ![](assets/scripts-actions.png)

1. Klicken Sie auf **[!UICONTROL Neues Skript hinzufügen]**.

   ![](assets/scripts-actions2.png)

1. Benennen Sie das Skript.
1. Geben Sie an, wie das Skript ausgelöst werden soll, und fügen Sie den gewünschten Inhalt in den Textbereich ein. ![](assets/scripts-actions3.png)

1. Click **[!UICONTROL Save Code]**, and the script will be added to the queue for the rule. ![](assets/scripts-actions4.png)

