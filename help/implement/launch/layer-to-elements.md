---
description: 'null'
title: Datenschichtobjekte Datenelementen zuordnen
uuid: null
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Datenschichtobjekte Datenelementen zuordnen


Nachdem Sie eine Datenschicht [für Ihre Implementierung](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html) erstellt haben, können Sie Objekte darin [Datenelementen in Launch](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html#create-a-data-element)zuordnen. Datenelemente sind Bausteine für Ihre Datenzuordnung, die auf unterschiedliche Weise genutzt werden können. Sie können Datenelemente verwenden, um Daten über Adobe-Plattformlösungen hinweg zu erfassen, zu organisieren und bereitzustellen, einschließlich Ihrer Analytics-Berichte.

So ordnen Sie Datenschichtobjekte zu Datenelementen starten zu:

1. Klicken Sie in Start auf den Namen der Eigenschaft, der Sie das Datenelement hinzufügen möchten. Wenn Sie noch keine Eigenschaft eingerichtet haben, lesen Sie die Anweisungen zum [Erstellen einer Starteigenschaft](https://docs.adobe.com/content/help/en/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch.html).

2. Click **Data Elements** and then click **Create New Data Element**.

   ![Datenelement erstellen](assets/createelement.png)


3. Geben Sie einen Namen für Ihr Datenelement ein. Dieser Name sollte eine einfache Beschriftung sein, die einer JavaScript-Variablen in Ihrer Datenschicht entspricht, die Sie verfolgen möchten.

4. Wählen Sie als Erweiterung &quot; **Core&quot;aus.** Diese Erweiterung umfasst alle Variablen, die Sie benötigen.

5. For **Data Element Type**, select **JavaScript Variable**. Geben Sie den Namen der **JavaScript-Variablen** in das entsprechende Feld ein. Dies sollte mit dem exakten Namen des Objekts in Ihrer JavaScript-Datenschicht übereinstimmen.

6. Geben Sie als **Standardwert** einen Wert ein, den Sie standardmäßig festlegen möchten, oder lassen Sie ihn gegebenenfalls leer.

7. Gemäß Ihren Vorgehensweisen können Sie die Optionen auswählen, um Kleinbuchstaben zu erzwingen und sauberen Text zu erzwingen (Start wird mit einem herkömmlichen Abstand ausgeführt).

8. Geben Sie die Dauer an, für die Startspeicher-Werte für das neue Datenelement verwendet werden sollen.

9. Klicken Sie auf **Speichern**.

Das folgende Beispiel zeigt ein Datenelement &quot;Seitenname&quot;in Launch, das für die JavaScript-Variable ``pageName`` in der Datenschicht erstellt wurde:

![Element angeben](assets/new_element.png)


Wenn Ihre Datenschichtobjekte Datenelementen zugeordnet sind, können Sie diese zum Füllen von Analytics-Variablen nutzen. Weitere Informationen finden Sie unter [Zuordnen von Datenelementen zu Analytics-Variablen](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html).
