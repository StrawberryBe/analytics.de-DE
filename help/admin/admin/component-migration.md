---
description: Erläutert die Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics.
title: Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics
feature: Admin Tools
source-git-commit: 8a9c3b4d6c7a59582a6fd8bdc5464c2dbed3ad1b
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 5%

---

# Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics

Adobe Analytics-Administratoren können Adobe Analytics-Komponenten und -Projekte auf Customer Journey Analytics migrieren.

Der Migrationsprozess umfasst:

* Erstellen Sie Adobe Analytics-Projekte im Customer Journey Analytics neu.

* Abgleichen von Dimensionen und Metriken aus Adobe Analytics-Report Suites mit Dimensionen und Metriken in Customer Journey Analytics-Datenansichten.

  Einige Dimensionen und Metriken werden automatisch abgeglichen. Bei anderen müssen Sie im Rahmen des Migrationsprozesses manuell eine Übereinstimmung finden.

## Voraussetzungen

Bevor Ihre Projekte und die zugehörigen Dimensionen und Metriken migriert werden können, müssen Sie zunächst:

* Verwenden Sie den Analytics-Quell-Connector, um Adobe Analytics-Report Suite-Daten im Customer Journey Analytics anzuzeigen. Gehen Sie dazu folgendermaßen vor:

   * [Report Suites für die Aufnahme in Adobe Experience Platform und Customer Journey Analytics einrichten](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

   * [Daten erfassen und verwenden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html?lang=de)

* Stellen Sie sicher, dass Benutzer in Customer Journey Analytics für die Datenansichten bereitgestellt werden, in denen Daten abgeglichen werden.

  Weitere Informationen finden Sie unter [Customer Journey Analytics-Berechtigungen in der Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) in [Zugriffskontrolle auf Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  Die Registerkarte Berechtigungen ist Teil jedes Produktprofils in Admin Console. Benutzende können zu bestimmten Produktprofilen hinzugefügt werden. Anschließend werden Rechte für bestimmte Datenansichten zugewiesen und festgelegt, welche Berechtigungen die Benutzenden in einem Produktprofil haben.

## Erstellen eines Migrationsplans als Organisation

Da alle Komponenten, die für eine bestimmte Projektmigration abgestimmt sind, für zukünftige Projektmigrationen für die gesamte Organisation gelten, ist es wichtig, dass Ihr Unternehmen alle Projektmigrationen im Voraus plant.

Sie sollten als Organisation entscheiden, welche Dimensionen und Metriken mit welchen übereinstimmen, um zu verhindern, dass einzelne Administratoren zum Zeitpunkt der Migration eines Projekts Entscheidungen in einem Silo treffen.

## Migrieren von Adobe Analytics-Projekten auf Customer Journey Analytics

>[!IMPORTANT]
>
>Bevor Sie, wie in diesem Abschnitt beschrieben, Projekte auf das Customer Journey Analytics migrieren, erfahren Sie mehr über das Migrieren von Projekten im [Migration planen](#plan-the-migration) Abschnitt weiter oben.
>
>Alle Dimensionen oder Metriken, die Sie zuordnen, sind dauerhaft, sowohl für dieses Projekt als auch für alle zukünftigen Projekte, die in Ihrer gesamten Organisation migriert werden. Wenn Sie fortfahren, können die von Ihnen erstellten Übereinstimmungen nicht geändert werden.



1. Wählen Sie in Adobe Analytics die [!UICONTROL **Admin**] Registerkarte und wählen Sie [!UICONTROL **Alle Administratoren**].

1. under [!UICONTROL **Datenkonfiguration und -erfassung**] auswählen [!UICONTROL **Komponentenmigration**].

1. (Bedingt) Um das Projekt, das Sie migrieren möchten, schnell zu finden, können Sie entweder:

   * Filtern Sie die Projektliste durch Auswahl des Symbols Filter .

     Sie können nach folgenden Kriterien filtern:

      * Status

      * Tags

      * Report Suite

      * Inhaber

      * Sonstige Filter

   * Verwenden Sie das Suchfeld, um nach dem Projekt zu suchen, das Sie migrieren möchten.

1. Bewegen Sie den Mauszeiger über das Projekt, das Sie migrieren möchten, und wählen Sie dann die **Migrieren** icon ![Projekt migrieren](assets/migrate.svg).

   Oder

   Wählen Sie das Projekt aus, das Sie migrieren möchten, und wählen Sie dann [!UICONTROL **Zu Customer Journey Analytics migrieren**].

   Sie können jeweils nur ein Projekt zur Migration auswählen.

   Die [!UICONTROL **Migrieren des Projektnamens zu Customer Journey Analytics**] angezeigt.

   <!-- add screenshot -->

1. Im [!UICONTROL **Projektinhaber**] Geben Sie den Namen des Benutzers ein, den Sie als Projekteigentümer festlegen möchten, und wählen Sie ihn im Dropdown-Menü aus.

   Der von Ihnen angegebene Eigentümer hat vollständige Verwaltungsrechte für das Projekt.

1. Im [!UICONTROL **Schema für Report Suites abgleichen**] wählen Sie eine Report Suite aus.

1. Im [!UICONTROL **Datenansicht**] Dropdown-Menü wählen Sie die Customer Journey Analytics-Datenansicht aus, in die das Projekt und die Komponenten migriert werden sollen.

1. Auswählen [!UICONTROL **Schema abgleichen**].

1. Im [!UICONTROL **Schema abgleichen**] -Abschnitt, erweitern Sie die [!UICONTROL **Dimensionen**] und [!UICONTROL **Metriken**] Abschnitte.

   Einige Dimensionen und Metriken in Adobe Analytics werden automatisch mit einer Dimension oder Metrik in Customer Journey Analytics abgeglichen. Andere müssen manuell abgeglichen werden.

   **Automatisch übereinstimmende Dimensionen und Metriken**

   Einige Dimensionen und Metriken in Adobe Analytics werden automatisch mit einer Dimension oder Metrik in Customer Journey Analytics abgeglichen. Sie können für diese Dimensionen und Metriken keine übereinstimmenden Entscheidungen treffen.

   Beispiel: die **Besuche** Metrik in Adobe Analytics automatisch mit der **Sitzungen** Metrik in Customer Journey Analytics.

   Sie können eine beliebige Dimension oder Metrik auswählen, um die zugehörigen IDs anzuzeigen.

   <!-- update screenshot after I can see the Status column -->

   ![Schema für die Projektmigration](assets/project-migration-schema.png)

   **Dimensionen und Metriken manuell abgleichen**

   Andere Dimensionen und Metriken in Adobe Analytics können nicht automatisch mit einer Dimension oder Metrik in Customer Journey Analytics abgeglichen werden.

   Wenn eine Dimension oder Metrik nicht automatisch zugeordnet werden kann, wird neben dem [!UICONTROL **Dimensionen**] oder [!UICONTROL **Metriken**] -Kopfzeile, die die Anzahl der Dimensionen oder Metriken angibt, die manuell abgeglichen werden müssen. In der Tabelle wird ein Warnsymbol angezeigt ![Warnsymbol](assets/schema-warning.png) wird neben jeder Dimension oder Metrik angezeigt, die manuell abgeglichen werden muss.

   <!-- update screenshot after I can see the Status column -->

   ![Manuelle Zuordnung des Migrationsschemas](assets/schema-manual-map.png)

1. Um Dimensionen und Metriken manuell zuzuordnen, wählen Sie eine Dimension oder Metrik aus, die ein Warnsymbol enthält ![Warnsymbol](assets/schema-warning.png), dann in der [!UICONTROL **Übereinstimmende Customer Journey Analytics-Metrik**] (oder [!UICONTROL **Abgleichen der Customer Journey Analytics-Dimension**] -Feld, wenn Sie eine Dimension zuordnen), wählen Sie unter Customer Journey Analytics die Dimension oder Metrik aus, die Sie mit der ausgewählten Dimension oder Metrik abgleichen möchten.

   ![Übereinstimmungsdimensionen und -metriken](assets/schema-manual-map-drop-down.png)

   Wiederholen Sie diesen Vorgang für jede Dimension oder Metrik, die das Warnsymbol enthält.

   Nachdem alle Dimensionen und Metriken in der Adobe Analytics Report Suite mit einer Dimension oder Metrik in der Customer Journey Analytics-Datenansicht übereinstimmen, wird ein grünes Häkchen angezeigt ![Häkchen](assets/report-suite-check.png) wird neben dem Report Suite-Namen in der [!UICONTROL **Schema für Report Suites abgleichen**] Abschnitt.

1. (Bedingt) Wenn das zu migrierende Projekt mehr als eine Report Suite enthält, wählen Sie eine andere Report Suite im [!UICONTROL **Schema für Report Suites abgleichen**] und wiederholen Sie dann Schritt 6 bis Schritt 10. <!-- double-check that the step numbers are still correct -->

1. Auswählen [!UICONTROL **Migrieren**].

   >[!WARNING]
   >
   >   Nach Auswahl wird eine Warnmeldung auf dem Bildschirm angezeigt [!UICONTROL **Migrieren**]. Bevor Sie fortfahren, sollten Sie wissen, dass alle Dimensionen oder Metriken, die Sie zuordnen, dauerhaft sind, sowohl für dieses Projekt als auch für alle zukünftigen Projekte, die in Ihrer gesamten Organisation migriert werden. Wenn Sie fortfahren, können die von Ihnen erstellten Übereinstimmungen nicht geändert werden.
