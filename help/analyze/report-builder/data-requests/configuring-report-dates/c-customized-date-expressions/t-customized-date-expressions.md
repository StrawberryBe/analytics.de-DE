---
description: Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.
title: Benutzerdefinierte Datumsausdrücke – Übersicht
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: User, Admin
exl-id: b3bdc07e-5c2d-4be3-86c9-b4b7380be0f6
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 25%

---

# Benutzerdefinierte Datumsausdrücke

Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.

Wenn Sie Ausdrücke erstellen, lesen Sie einen Kalender , um die Anzahl der Wochen und Tage korrekt anzugeben. Excel bietet verschiedene integrierte Funktionen für die Berechnung von Tagen, Werktagen, Monaten und Jahren, die zwischen zwei Datumswerten liegen. Sie können diese Funktionen in Formeln verwenden, um andere Intervalle zu berechnen, etwa Wochen oder Quartale.

**So aktivieren Sie benutzerdefinierte Ausdrücke**

Das folgende Beispiel zeigt, wie ein benutzerdefinierter Ausdruck für **[!UICONTROL Rollierende Datumswerte]**.

1. Im [!UICONTROL Anforderungs-Assistent: Schritt 1], anstatt **[!UICONTROL Vordefinierte Datumswerte]** auswählen **[!UICONTROL Rollierende Datumswerte]**.

   ![Screenshot mit ausgewählten rollierenden Datumswerten.](assets/rolldates1.png)

1. Wechseln Sie zu Rollierend wöchentlich, monatlich, vierteljährlich oder jährlich. Beachten Sie, wie sich die folgenden Optionen ändern.
1. Klicken Sie für weitere Anpassungsoptionen auf **[!UICONTROL Erweiterte Optionen anzeigen]**.

   ![Screenshot, der die erweiterten Optionen anzeigen hervorhebt.](assets/rolldates2.png)

1. Wenn Sie beispielsweise die oben genannten Daten in &quot;Monatlich&quot;ändern, vom ersten Tag vor drei Monaten bis zum ersten Tag dieses Monats, werden die Datumsangaben in den vorherigen Optionen aktualisiert, um Folgendes widerzuspiegeln:

   ![Screenshot mit den rollierenden Daten vom ersten Tag vor drei Monaten bis zum ersten Tag dieses Monats.](assets/rolldatesfor3.png)

1. Aktivieren **[!UICONTROL Ausdruck anpassen]**. Durch Auswahl der Optionen unter **[!UICONTROL Rollierende Datumswerte]** können Sie die Syntax für benutzerdefinierte Datumsausdrücke leicht sehen.

   ![Screenshot mit ausgewähltem Ausdruck anpassen](assets/rolldatesfor5.png)

   Sie können Erweiterte Optionen verwenden, um benutzerdefinierte Datumsausdrücke zu kombinieren und zuzuordnen. Wenn Sie beispielsweise Daten vom ersten Jahr bis zum Ende des letzten vollständigen Monats anzeigen möchten, können Sie Folgendes eingeben: `From: cy` `To: cm-1d`. Im Assistenten werden diese Daten als 1.1.2020-1.31.2020 angezeigt.
