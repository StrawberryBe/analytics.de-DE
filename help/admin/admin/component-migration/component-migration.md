---
description: Erläutert die Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics.
title: Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics
feature: Admin Tools
exl-id: 49c7e47a-464b-4465-9b30-d77f886ca6dc
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 5%

---

# Migrieren von Komponenten und Projekten von Adobe Analytics zum Customer Journey Analytics

Adobe Analytics-Admins können Adobe Analytics-Projekte und die zugehörigen Komponenten zu Customer Journey Analytics migrieren.

Der Migrationsvorgang umfasst:

* Neuerstellung von Adobe Analytics-Projekten in Customer Journey Analytics.

* Zuordnung von Dimensionen und Metriken aus Adobe Analytics-Report Suites zu Dimensionen und Metriken in Customer Journey Analytics-Datenansichten.

  Einige Dimensionen und Metriken werden automatisch zugeordnet. Für andere müssen Sie im Rahmen des Migrationsprozesses manuell zuordnen. Segmente werden ebenfalls migriert, müssen jedoch im Rahmen des Migrationsprozesses nicht zugeordnet werden.

  Alle migrierten Komponenten werden nach Abschluss der Migration in der Migrationszusammenfassung angezeigt.

## Vorbereitung auf eine Migration

Bevor Sie Projekte zum Customer Journey Analytics migrieren, erfahren Sie mehr über die Migration von Projekten in der [Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics](/help/admin/admin/component-migration/prepare-component-migration.md).

## Migrieren von Adobe Analytics-Projekten auf Customer Journey Analytics

>[!IMPORTANT]
>
>Bevor Sie, wie in diesem Abschnitt beschrieben, Projekte auf das Customer Journey Analytics migrieren, erfahren Sie mehr über das Migrieren von Projekten im [Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics](/help/admin/admin/component-migration/prepare-component-migration.md).
>
>Alle Dimensionen oder Metriken, die Sie zuordnen, sind dauerhaft, sowohl für dieses Projekt als auch für alle zukünftigen Projekte, die in Ihrer gesamten IMS-Organisation migriert werden. Alle Zuordnungen, die Sie vornehmen, können nach Abschluss der Migration nicht mehr geändert werden.

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Admin**] und dann [!UICONTROL **Alle Admins**] aus.

1. under [!UICONTROL **Datenkonfiguration und -erfassung**] auswählen [!UICONTROL **Komponentenmigration**].

1. Suchen Sie das Projekt, das Sie migrieren möchten. Sie können die Projektliste filtern, sortieren oder durchsuchen.

   Standardmäßig werden nur Projekte angezeigt, die für Sie freigegeben wurden. Um alle Projekte in Ihrer Organisation anzuzeigen, wählen Sie die **Filter** Symbol und dann erweitern [!UICONTROL **Sonstige Filter**] und wählen [!UICONTROL **Alle anzeigen**]. (Weitere Informationen zum Filtern, Sortieren und Durchsuchen der Projektliste finden Sie unter [Filtern, Sortieren und Durchsuchen der Projektliste](#filter-sort-and-search-the-list-of-projects).

1. Bewegen Sie den Mauszeiger über das Projekt, das Sie migrieren möchten, und wählen Sie dann die **Migrieren** icon ![Projekt migrieren](assets/migrate.svg).

   Oder

   Wählen Sie das Projekt aus, das Sie migrieren möchten, und wählen Sie dann [!UICONTROL **Zu Customer Journey Analytics migrieren**].

   Sie können jeweils nur ein Projekt zur Migration auswählen.

   Die [!UICONTROL **Migrieren des Projektnamens zu Customer Journey Analytics**] angezeigt.

   <!-- add screenshot -->

1. Im [!UICONTROL **Projektinhaber**] Geben Sie den Namen des Benutzers ein, den Sie als Projekteigentümer festlegen möchten, und wählen Sie ihn im Dropdown-Menü aus.

   Der von Ihnen angegebene Eigentümer hat vollständige Verwaltungsrechte für das Projekt.

1. Im [!UICONTROL **Zuordnungsschema für Report Suites**] wählen Sie eine Report Suite aus.

1. Im [!UICONTROL **Datenansicht**] Dropdown-Menü wählen Sie die Customer Journey Analytics-Datenansicht aus, in die das Projekt und die Komponenten migriert werden sollen.

1. Auswählen [!UICONTROL **Zuordnungsschema**].

1. Im [!UICONTROL **Zuordnungsschema**] -Abschnitt, erweitern Sie die [!UICONTROL **Dimensionen**] und [!UICONTROL **Metriken**] Abschnitte.

   Einige Dimensionen und Metriken in Adobe Analytics werden automatisch einer Dimension oder Metrik in Customer Journey Analytics zugeordnet. Andere müssen manuell zugeordnet werden.

   **Dimensionen und Metriken automatisch zuordnen**

   >[!NOTE]
   >
   >   Wenn Sie das WebSDK zur Aufnahme von Daten in Adobe Experience Platform verwendet haben, können Dimensionen und Metriken nicht automatisch zugeordnet werden. Weitere Informationen finden Sie unter [Voraussetzungen](/help/admin/admin/component-migration/prepare-component-migration.md#prerequisites) in [Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics](/help/admin/admin/component-migration/prepare-component-migration.md).

   Einige Dimensionen und Metriken in Adobe Analytics werden automatisch einer Dimension oder Metrik in Customer Journey Analytics zugeordnet. Sie können für diese Dimensionen und Metriken keine Zuordnungsentscheidungen treffen.

   Beispiel: die **Besuche** Metrik in Adobe Analytics automatisch mit der **Sitzungen** Metrik in Customer Journey Analytics.

   Sie können eine beliebige Dimension oder Metrik auswählen, um die zugehörigen IDs anzuzeigen.

   <!-- update screenshot after I can see the Status column -->

   ![Schema für die Projektmigration](assets/project-migration-schema.png)

   **Dimensionen und Metriken manuell zuordnen**

   Einige Dimensionen und Metriken in Adobe Analytics können nicht automatisch einer Dimension oder Metrik in Customer Journey Analytics zugeordnet werden.

   Wenn eine Dimension oder Metrik nicht automatisch zugeordnet werden kann, wird neben dem [!UICONTROL **Dimensionen**] oder [!UICONTROL **Metriken**] -Kopfzeile, die die Anzahl der Dimensionen oder Metriken angibt, die manuell zugeordnet werden müssen. In der Tabelle wird ein Warnsymbol angezeigt ![Warnsymbol](assets/schema-warning.png) wird neben jeder Dimension oder Metrik angezeigt, die manuell zugeordnet werden muss.

   Darüber hinaus wird die [!UICONTROL **Status**] Spalte sagt [!UICONTROL **Nicht zugeordnet**].

   <!-- update screenshot after I can see the Status column -->

   ![Manuelle Zuordnung des Migrationsschemas](assets/schema-manual-map.png)

1. Um Dimensionen und Metriken manuell zuzuordnen, wählen Sie eine Dimension oder Metrik aus, die ein Warnsymbol enthält ![Warnsymbol](assets/schema-warning.png), dann in der [!UICONTROL **Zugeordnete Customer Journey Analytics-Metrik**] (oder [!UICONTROL **Zugeordnete Customer Journey Analytics-Dimension**] -Feld, wenn Sie eine Dimension zuordnen), wählen Sie unter Customer Journey Analytics die Dimension oder Metrik aus, die Sie der ausgewählten Dimension oder Metrik zuordnen möchten.

   ![Zuordnungsdimensionen und -metriken](assets/schema-manual-map-drop-down.png)

   Nachdem eine Dimension oder Metrik zugeordnet wurde, wird das Warnsymbol ausgeblendet und die [!UICONTROL **Status**] Spaltenänderungen in [!UICONTROL **Zugeordnet**] mit einem grünen Punkt. (Status von [!UICONTROL **Zugeordnet**] mit einem grauen Punkt zeigt an, dass die Dimension oder Metrik während einer vorherigen Migration zugeordnet wurde. Alle vorherigen Zuordnungen können nicht aktualisiert werden.)

   Wiederholen Sie diesen Vorgang für jede Dimension oder Metrik, die das Warnsymbol enthält.

   Nachdem alle Dimensionen und Metriken in der Adobe Analytics Report Suite in der Customer Journey Analytics-Datenansicht einer Dimension oder Metrik zugeordnet sind, wird ein grünes Häkchen angezeigt ![Häkchen](assets/report-suite-check.png) wird neben dem Report Suite-Namen in der [!UICONTROL **Zuordnungsschema für Report Suites**] Abschnitt.

1. (Bedingt) Wenn das zu migrierende Projekt mehr als eine Report Suite enthält, wählen Sie eine andere Report Suite im [!UICONTROL **Zuordnungsschema für Report Suites**] und wiederholen Sie dann Schritt 6 bis Schritt 10. <!-- double-check that the step numbers are still correct -->

1. Auswählen [!UICONTROL **Migrieren**].

   >[!WARNING]
   >
   >   Nach Auswahl wird eine Warnmeldung auf dem Bildschirm angezeigt [!UICONTROL **Migrieren**]. Bevor Sie fortfahren, sollten Sie wissen, dass alle Dimensionen oder Metriken, die Sie zuordnen, dauerhaft sind, sowohl für dieses Projekt als auch für alle zukünftigen Projekte, die in Ihrer gesamten Organisation migriert werden. Wenn Sie fortfahren, können die von Ihnen erstellten Zuordnungen nicht geändert werden.

   Nach Abschluss der Migration wird die [!UICONTROL **Migrationsstatus**] bietet eine Zusammenfassung der migrierten Elemente.

   Wenn die Migration fehlschlägt, lesen Sie den Abschnitt [Fehlgeschlagene Migration wiederholen](#retry-a-failed-migration) unten für weitere Informationen.

## Fehlgeschlagene Migration wiederholen

Wenn eine Migration fehlschlägt, können Sie die Migration erneut versuchen.

Bevor Sie eine fehlgeschlagene Migration wiederholen, müssen Sie alle [nicht unterstützte Elemente](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html#understand-unsupported-elements-that-cause-errors) aus dem Projekt.

>[!NOTE]
>
>Wenn die Migration nach einem erneuten Versuch weiterhin fehlschlägt, wenden Sie sich mit der Projekt-ID an die Kundenunterstützung . Sie finden die Projekt-ID auf der Seite Migrationsstatus . <!-- when does this page display? How can they get there -->

So wiederholen Sie eine fehlgeschlagene Migration:

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Admin**] und dann [!UICONTROL **Alle Admins**] aus.

1. under [!UICONTROL **Datenkonfiguration und -erfassung**] auswählen [!UICONTROL **Komponentenmigration**].

1. Auswählen [!UICONTROL **Fehlgeschlagen**] im [!UICONTROL **Migrationsstatus**] neben dem Projekt, das Sie erneut versuchen möchten.

   ![Spalte mit Migrationsstatus](assets/migration-failed.png)

   Die [!UICONTROL **Migrationsstatus**] angezeigt.

   Diese Seite wird auch unmittelbar nach Abschluss der im Abschnitt beschriebenen Migrationsschritte angezeigt. [Migrieren von Adobe Analytics-Projekten auf Customer Journey Analytics](#migrate-adobe-analytics-projects-to-customer-journey-analytics) höher.

1. Auswählen [!UICONTROL **Migration wiederholen**].

## Filtern, Sortieren und Durchsuchen der Projektliste

Sie können die Liste der Projekte auf der Seite Komponentenmigration filtern, sortieren und durchsuchen.

### Filtern der Projektliste

Sie können nach folgenden Kriterien filtern:

| Filter | Beschreibung |
|---------|----------|
| [!UICONTROL **Status**] | Der Status der Migration: <ul><li>[!UICONTROL **Nicht gestartet**]</li><li>[!UICONTROL **Gestartet**]</li><li>[!UICONTROL **Abgeschlossen**]</li><li>[!UICONTROL **Fehlgeschlagen**]</li></ul>. |
| [!UICONTROL **Tags**] | Wählen Sie beliebige Tags in der Tag-Liste aus. Es werden nur Projekte angezeigt, auf die die ausgewählten Tags angewendet wurden. |
| [!UICONTROL **Report Suite**] | Wählen Sie eine beliebige Report Suite in der Liste der Report Suites aus. Es werden nur Projekte angezeigt, die die ausgewählten Report Suites verwenden. |
| [!UICONTROL **Eigentümer**] | Wählen Sie einen beliebigen Inhaber in der Liste der Inhaber aus. Es werden nur Projekte angezeigt, die den ausgewählten Benutzern gehören. |
| [!UICONTROL **Sonstige Filter**] | Die folgenden zusätzlichen Filter sind verfügbar: <ul><li>[!UICONTROL **Mine**]: Zeigt nur Projekte an, für die Sie als Inhaber festgelegt sind.</li><li>[!UICONTROL **Freigegeben für mich**]: Zeigt nur Projekte an, die für Sie freigegeben wurden.</li><li>[!UICONTROL **Favoriten**]: Zeigt nur Projekte an, die als Favorit markiert sind. (Sie können ein Projekt als Favoriten aus dem [Projekt-Landingpage](/help/analyze/landing.md).</li><li>[!UICONTROL **Monatlich**]</li><li>[!UICONTROL **Jährlich**]</li></ul> |

{style="table-layout:auto"}

### Liste der Projekte sortieren

Sie können die Projektliste nach einer beliebigen Spalte sortieren.

So sortieren Sie die Projektliste:

1. Wählen Sie die Spaltenüberschrift der Spalte aus, nach der Sie sortieren möchten.

1. (Optional) Wählen Sie dieselbe Spaltenüberschrift erneut aus, um die Sortierreihenfolge umzukehren.

### Suchen nach einem Projekt

Sie können die Liste der Projekte auf der Seite Komponentenmigration durchsuchen, um das Projekt zu finden, das Sie migrieren möchten.

1. Geben Sie im Suchfeld oben auf der Seite Komponentenmigration den Namen des Projekts ein, das Sie migrieren möchten.

1. Wählen Sie das Projekt aus, wenn es im Dropdown-Menü angezeigt wird.

<!-- is there going to be a way to customize the columns that are displayed? -->
