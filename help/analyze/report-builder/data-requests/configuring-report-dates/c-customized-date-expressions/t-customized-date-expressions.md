---
description: Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.
title: Benutzerdefinierte Datumsausdrücke – Übersicht
topic: Report builder
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
translation-type: tm+mt
source-git-commit: 2a6031cde69014859d6c3f943220c4da499a3191

---


# Benutzerdefinierte Datumsausdrücke – Übersicht

Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.

Es wird empfohlen, beim Erstellen von Ausdrucken auf einen bestimmten Kalender zu verweisen, damit die Anzahl der Wochen und Tage richtig angegeben wird. Excel bietet verschiedene integrierte Funktionen für die Berechnung von Tagen, Werktagen, Monaten und Jahren, die zwischen zwei Datumswerten liegen. Sie können diese Funktionen in Formeln verwenden, um andere Intervalle zu berechnen, etwa Wochen oder Quartale.

**So aktivieren Sie benutzerdefinierte Ausdrücke**

1. Wählen Sie [!UICONTROL Request Wizard: Step 1]statt &quot;Vordefinierte Datumswerte&quot; **[!UICONTROL Rolling Dates]**. Beachten Sie, wie sich die Optionen unten ändern.

   ![](assets/rolldates1.png)

1. Wechseln Sie zu Rollierend wöchentlich, monatlich, vierteljährlich oder jährlich.
1. Klicken Sie für weitere Anpassungsoptionen auf **[!UICONTROL Show Advanced Options]**. Durch Auswahl der Optionen im oberen Bereich können Sie die Syntax für benutzerdefinierte Datumsausdrücke leicht erkennen.

   ![](assets/rolldates2.png)

1. Aktivieren **[!UICONTROL Customize Expression]**. Durch Auswahl der Optionen unter **[!UICONTROL Rolling Dates]** können Sie die Syntax für benutzerdefinierte Datumsausdrücke leicht erkennen.

   ![](assets/rolldates5.png)

   Sie können erweiterte Optionen verwenden, um benutzerdefinierte Datumsausdrücke zu kombinieren und zuzuordnen. Wenn Sie z. B. Daten vom ersten Jahr bis zum Ende des letzten vollen Monats anzeigen möchten, können sie Folgendes schreiben:Von: cy To: cm-1d. Sie können sehen, dass im Assistenten diese Daten als 1/1/2020-1/31/2020 bestätigt werden.

   Wenn Sie beispielsweise die oben genannten Daten in &quot;Monatlich rollierend&quot;vom ersten Tag vor drei Monaten bis zum ersten Tag dieses Monats ändern, werden die Daten in den erweiterten Optionen entsprechend aktualisiert:

   ![](assets/rolldates5.png)

