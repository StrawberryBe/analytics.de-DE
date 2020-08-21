---
description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
keywords: Dynamic Tag Management;rule;create rule;new rule;javascript/third party tags;set up actions for condition;add new script;non-sequential javascript;sequential javascript;non-sequential html
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Aktionen einrichten, die von der Bedingung ausgelöst werden
uuid: 2e892f0b-7261-41ee-b849-6e3054a38de0
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '231'
ht-degree: 100%

---


# Aktionen einrichten, die von der Bedingung ausgelöst werden

Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.

Nachdem Sie die Bedingung eingerichtet haben, müssen Sie die Aktionen einrichten, die von der Bedingung ausgelöst werden sollen. Zu diesen Aktionen zählen beispielsweise [!DNL Analytics]-Ereignisse, Drittanbieter-Tags oder benutzerdefinierte Skripte. Im folgenden Beispiel wird beschrieben, wie Sie Skripte oder Drittanbieter-Tags einrichten.

Neben integrierten Tools wie [!DNL Adobe Analytics] und Google Analytics kann das Dynamic Tag Management jede Art von JavaScript auslösen oder HTML in Ihre Website einfügen – in ausgewählten Seiten oder in spezifischen Szenarios.

Jede Regel kann beliebig viele Skripte auslösen oder HTML-Codes einfügen.

>[!NOTE]
>
>Da DTM es Ihnen ermöglicht, benutzerdefinierten Code in Ihre Seite aufzunehmen, müssen Sie darauf achten, keine Sicherheitslücken durch seitenübergreifende Skripterstellung (XSS) zu erzeugen (weitere Informationen finden Sie im [OWASP-Leitfaden](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS))). Bei der Verwendung von Datenelementen in Skripten muss besonders vorsichtig vorgegangen werden. Gehen Sie stets davon aus, dass Datenelementwerte von nicht vertrauenswürdigen Quellen übermittelt werden könnten.

**So richten Sie Aktionen ein, die von der Bedingung ausgelöst werden**

1. Klicken Sie auf **[!UICONTROL JavaScript/Drittanbieter-Tags]**, um Ihrer Regel ein neues Skript hinzuzufügen.

   ![](assets/scripts-actions.png)

1. Klicken Sie auf **[!UICONTROL Neues Skript hinzufügen]**.

   ![](assets/scripts-actions2.png)

1. Benennen Sie das Skript.
1. Geben Sie an, wie das Skript ausgelöst werden soll, und fügen Sie den gewünschten Inhalt in den Textbereich ein. ![](assets/scripts-actions3.png)

1. Klicken Sie auf **[!UICONTROL Code speichern]**. Das Skript wird der Warteschlange für die Regel hinzugefügt. ![](assets/scripts-actions4.png)

