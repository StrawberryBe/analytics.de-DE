---
description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
keywords: Dynamisches Tag-Management; rule; create rule; new rule; javascript/drittanbieter-Tags; Aktionen für Bedingungen einrichten; neues Skript hinzufügen; non-sequenzielles javascript; sequenzielles javascript; nicht sequenzielles HTML
seo-description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
seo-title: Aktionen einrichten, die von der Bedingung ausgelöst werden
solution: Marketing Cloud, Analytics, Target, Dynamisches Tag-Management
title: Aktionen einrichten, die von der Bedingung ausgelöst werden
uuid: 2 e 892 f 0 b -7261-41 ee-b 849-6 e 3054 a 38 de 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

