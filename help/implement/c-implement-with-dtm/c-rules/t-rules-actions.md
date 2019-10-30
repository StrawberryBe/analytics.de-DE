---
description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
keywords: Dynamic Tag Management;Regel;Regel erstellen;neue Regel;JavaScript-/Drittanbieter-Tags;Aktionen für Bedingung einrichten;Neues Skript hinzufügen;Nicht sequentielles JavaScript;Sequentielles JavaScript;Nicht sequentielles HTML
seo-description: Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.
seo-title: Aktionen einrichten, die von der Bedingung ausgelöst werden
solution: Experience Cloud, Analytics, Target, Dynamic Tag Management
title: Aktionen einrichten, die von der Bedingung ausgelöst werden
uuid: 2e892f0b-7261-41ee-b849-6e3054a38de0
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Aktionen einrichten, die von der Bedingung ausgelöst werden

Richten Sie Aktionen ein, die von der Bedingung ausgelöst werden sollen.

Nachdem Sie die Bedingung eingerichtet haben, müssen Sie die Aktionen einrichten, die von der Bedingung ausgelöst werden sollen. Zu diesen Aktionen zählen beispielsweise [!DNL Analytics]-Ereignisse, Drittanbieter-Tags oder benutzerdefinierte Skripte. Im folgenden Beispiel wird beschrieben, wie Sie Skripte oder Drittanbieter-Tags einrichten.

Neben integrierten Tools wie [!DNL Adobe Analytics] und Google Analytics kann das Dynamic Tag Management jede Art von JavaScript auslösen oder HTML in Ihre Website einfügen – in ausgewählten Seiten oder in spezifischen Szenarios.

Jede Regel kann beliebig viele Skripte auslösen oder HTML-Codes einfügen.

> [!NOTE] Da DTM es Ihnen ermöglicht, benutzerspezifischen Code in Ihre Seite einzufügen, sollten Sie darauf achten, keine Schwachstellen für seitenübergreifende Skripterstellung (XSS) zu erstellen (weitere Informationen finden Sie im [OWASP-Handbuch](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)) ). Bei der Verwendung von Datenelementen in Skripten muss besonders vorsichtig vorgegangen werden. Gehen Sie stets davon aus, dass Datenelementwerte von nicht vertrauenswürdigen Quellen übermittelt werden könnten.

**So richten Sie Aktionen ein, die von der Bedingung ausgelöst werden**

1. Klicken Sie auf **[!UICONTROL JavaScript/Drittanbieter-Tags]**, um Ihrer Regel ein neues Skript hinzuzufügen.

   ![](assets/scripts-actions.png)

1. Klicken Sie auf **[!UICONTROL Neues Skript hinzufügen]**.

   ![](assets/scripts-actions2.png)

1. Benennen Sie das Skript.
1. Geben Sie an, wie das Skript ausgelöst werden soll, und fügen Sie den gewünschten Inhalt in den Textbereich ein. ![](assets/scripts-actions3.png)

1. Klicken Sie auf **[!UICONTROL Code speichern]**. Das Skript wird der Warteschlange für die Regel hinzugefügt. ![](assets/scripts-actions4.png)

