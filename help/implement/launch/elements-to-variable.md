---
description: 'null'
title: Zuordnen von Datenelementen zu Analytics-Variablen
uuid: null
translation-type: tm+mt
source-git-commit: bb9648f4886ac26c77d89f850f7a68d40a9b4ffc

---


# Startdatenelemente Analytics-Variablen zuordnen


Nachdem Sie Ihre Datenschichtobjekte [den Datenelementen](https://docs.adobe.com/content/help/en/analytics/implementation/layer-to-elements.md)zum Start zugeordnet haben, können Sie Datenelemente [Analytics-Variablen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/overview.html)zuordnen.

So ordnen Sie Startdatenelemente Analytics-Variablen zu:

1. Weisen Sie das Datenelement gegebenenfalls einer globalen Variablen zu. Einige Datenelemente wie *Seitenname* gelten für jede Seite einer Eigenschaft. In solchen Fällen können Sie die Variable global festlegen, indem Sie folgende Schritte ausführen:

2. Blättern Sie unter &quot;Start&quot;nach unten und klicken Sie auf **Erweiterungs-Katalog**.

   ![Erweiterungskatalog](assets/extensions.png)

3. Klicken Sie unter Analytics auf **Konfigurieren** .

   ![Analytics-Erweiterung](assets/configure.png)


4. Wählen Sie unter **eVars** in **globalen Variablen** die eVar aus, die Sie eingerichtet [](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) haben, um mit der Variablen verknüpft zu werden. Wählen Sie &quot; **Als** festlegen&quot;und klicken Sie auf das Fass-Symbol im Feld ganz rechts, um das Datenelement anzugeben.

   ![eVar angeben](assets/evars.png)

5. Wählen Sie im Popupfenster &quot;Datenelement **auswählen** &quot;das Datenelement aus, das Sie auf die Variable anwenden möchten.

6. Klicken Sie auf **Speichern**.


Wenn das Datenelement nicht mit einer globalen Variablen verknüpft ist, können Sie auch einfach eine Regel [](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules.html) erstellen, die die Datenelemente Props oder evars zuweist.
