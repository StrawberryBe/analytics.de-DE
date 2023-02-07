---
description: Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen.
title: Report Suite-Daten beschriften
feature: Data Governance
exl-id: d1bd833c-3fd4-4572-a5dc-d7bab8a79cb8
source-git-commit: f135138de15f3fc788e637128daeb064d0d453af
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 44%

---

# Report Suite-Daten beschriften

Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. Machen Sie sich zunächst mit der [Bezeichnungen und ihre Definitionen](/help/admin/c-data-governance/data-labeling/gdpr-labels.md).

>[!NOTE]
>
>Beachten Sie, dass die Beschriftung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein.

## Zuweisen oder Bearbeiten von Datenschutzbezeichnungen für Report Suites {#assign-edit}

**Beispiel**: Als Datenverantwortlicher planen Sie die Erfassung von E-Mail-Adressen und Cookie-IDs von betroffenen Personen, um deren Datenschutzanfragen zu verarbeiten. Diese Cookie-IDs werden in einer Adobe Analytics Report Suite gespeichert.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Data Governance]**.

   ![Datenschutzbezeichnungen](assets/privacy_rs_settings.png)

1. Wählen Sie eine Report Suite aus der **[!UICONTROL Report Suites]** Auswahl oben.

1. Wählen Sie links im Filterabschnitt aus, welche Variablengruppen Sie beschriften möchten. Sie können jeweils nur eine Gruppe von Variablen beschriften.

   * **Standardkomponenten** - Standardkomponenten sind vordefinierte Analytics-Dimensionen und -Metriken, die standardmäßig in einer Analytics-Implementierung erfasst werden.
   * **Konversionsvariablen** - Die Custom Insight-Konversionsvariable (oder -eVar) wird auf ausgewählten Webseiten Ihrer Site im Adoben-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Ein eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.
   * **Listenvariablen** - Listenvariablen sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.
   * **Traffic-Variablen** - Custom Insight-Traffic-Variablen (oder Eigenschaften) ermöglichen es Ihnen, benutzerdefinierte Daten mit bestimmten Traffic-bezogenen Ereignissen zu korrelieren. Die Eigenschaftsvariablen sind in den Implementierungscode auf jeder Seite der Website eingebunden.
   * **Erfolgsereignisse** - Erfolgsereignisse (auch Konversionsereignisse oder benutzerspezifische Ereignisse genannt) sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..
   * **Klassifizierungen** - Klassifizierungsaufschlüsselungen werden verwendet, um Analytics-Berichtsdaten verwandten Eigenschaften zuzuordnen. Classifications können für verschiedene Zwecke verwendet werden, werden jedoch meist zum Klassifizieren von Kampagnen-Trackingcodes (sowohl interne als auch externe) und Produkt-IDs verwendet.

1. Wählen Sie eine Variable aus, indem Sie das entsprechende Kontrollkästchen aktivieren, und klicken Sie dann auf **[!UICONTROL Datenschutzbezeichnungen bearbeiten]** auf der blauen Leiste, die unten auf dem Bildschirm angezeigt wird.

   ![Bearbeiten](assets/edit-label.png)

   In diesem Bildschirm werden die aktuell angewendeten Bezeichnungen angezeigt und Sie können zusätzliche Bezeichnungen anwenden. Je nach Komponente können Sie möglicherweise nicht alle Beschriftungen anwenden oder ändern.

   ![Angewandte Beschriftungen](assets/edit-labels2.png)

1. Nachdem Sie sämtliche Beschriftungen abgeschlossen haben, klicken Sie auf **[!UICONTROL Übernehmen]**.

