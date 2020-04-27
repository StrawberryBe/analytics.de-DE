---
description: Filter, die dimensionsspezifische Terme anwenden.
title: Spezifische Filter
topic: Report builder
uuid: b3a8187a-3d59-4da0-abca-e933664332e3
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Spezifische Filter

Filter, die dimensionsspezifische Terme anwenden.

Sie können dimensionsspezifische Filter setzen, indem Sie einen Filter erstellen, für den exakte Kriterien erfüllt werden müssen. Beispielsweise können Sie den folgenden Filtertyp erstellen: Seite unter [!DNL homepage.htm], [!DNL contact_us.html], [!DNL corporate_info.html].

**So erstellen Sie einen spezifischen Filter**

1. Erstellen oder bearbeiten Sie eine Anforderung und gehen Sie zum [!UICONTROL Request Wizard: Step 2]Bericht.

   ![Schritt Ergebnis](assets/dimension_filter.png)

1. On the [!UICONTROL Request Wizard: Step 2], click the link next to the dimension in the grid, then choose **[!UICONTROL Filter]**.

   ![Schritt Ergebnis](assets/choose_page_specific01.png)

1. Enable **[!UICONTROL Specific]**, then enable one of the following options:

   * **Aus Zellenbereich:** Hier können Sie Daten aus Zellen auswählen. Folgende Optionen stehen zur Auswahl:
   * **Alle Zellen im Bereich:** Hier können Sie jede Zelle für den Bereich zuordnen. Eine Textbeschreibung erläutert, wie viele Gruppen von Zellen Sie auswählen müssen. Um mehr als eine Gruppe von Zellen zuzuordnen, drücken Sie während der Auswahl die Strg-Taste. Wenn der Bereich, der zugeordnet werden muss, mehr als eine Zelle enthält, ist dies die einzige verfügbare Option.
   * **Erste Zelle im Bereich:** Sie müssen nur die Zelle in der linken oberen Ecke des Bereichs auswählen und dann eine Richtung für die Daten wählen. Falls die Anforderung über mehrere Zeiträume geht, müssen Sie außerdem die Richtung der Zeiträume auswählen und entscheiden, ob eine bestimmte Anzahl von Zellen zwischen Zeiträumen übersprungen werden soll.
   * **Aus Liste:** Ermöglicht die Auswahl von Daten aus einer Liste, der Sie Daten hinzufügen können.
1. If you enable **[!UICONTROL From List]**, select any available listed items or click **[!UICONTROL Add]**.

   When you click **[!UICONTROL Add]**, the [!UICONTROL Select From List] form displays a list of available dimension values for the current request date range, limited to the first 10,000 items. You can search across these items or click **[!UICONTROL More ...]**, which displays the [!UICONTROL Search Form], so that you can create a more detailed search for dimensions.
1. Klicken Sie auf der [!UICONTROL Select From List]Seite auf **[!UICONTROL OK]**.
1. On the [!UICONTROL Choose Page] form, save your Specific filter if you want, then click **[!UICONTROL OK]**.
