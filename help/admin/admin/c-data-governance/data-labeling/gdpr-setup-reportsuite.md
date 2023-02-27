---
description: Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen.
title: Kennzeichnen von Report Suite-Daten
feature: Data Governance
exl-id: d1bd833c-3fd4-4572-a5dc-d7bab8a79cb8
source-git-commit: c774d05ca3b1f9f45ec118b0e7b8a839a03b87e3
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 95%

---

# Kennzeichnen von Report Suite-Daten

Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. Machen Sie sich hierzu zunächst mit den [Kennzeichnungen und ihren Definitionen vertraut](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md).

>[!NOTE]
>
>Beachten Sie, dass die Beschriftung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein.

## Zuweisen oder Bearbeiten von Report-Suite-Datenschutzkennzeichnungen {#assign-edit}

**Beispiel**: Als Datenverantwortlicher planen Sie die Erfassung von E-Mail-Adressen und Cookie-IDs von betroffenen Personen, um deren Datenschutzanfragen zu verarbeiten. Diese Cookie-IDs werden in einer Adobe Analytics Report Suite gespeichert.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Data Governance]**.

   ![Datenschutzkennzeichnung](assets/privacy_rs_settings.png)

1. Wählen Sie eine Report Suite aus der obigen **[!UICONTROL Report Suite]**-Auswahl.

1. Wählen Sie links im Filterabschnitt aus, welche Variablengruppen Sie kennzeichnen möchten. Sie können jeweils nur eine Gruppe von Variablen beschriften.

   * **Standardkomponenten** – Standardkomponenten sind native Analytics-Dimensionen und -Metriken, die standardmäßig bei einer Analytics-Implementierung erfasst werden.
   * **Konversionsvariablen** – die Custom-Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Web-Seiten Ihrer Site in den Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer bzw. der Benutzerin für einen bestimmten Zeitraum.
   * **Listenvariablen** – Listenvariablen sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.
   * **Traffic-Variablen** – Custom-Insight-Traffic-Variablen (oder Props) ermöglichen die Korrelation von benutzerdefinierten Daten mit spezifischen Traffic-bezogenen Ereignissen. Die Eigenschaftsvariablen sind in den Implementierungs-Code auf jeder Seite der Website eingebunden.
   * **Erfolgsereignisse** – Erfolgsereignisse (auch Konversionsereignisse oder benutzerdefinierte Ereignisse genannt) sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..
   * **Klassifizierungen** – Klassifizierungsaufschlüsselungen werden zur Zuordnung von Analytics-Berichtsdaten zu bestimmten Eigenschaften eingesetzt. Klassifizierungen können für zahlreiche Zwecke eingesetzt werden, werden jedoch meistens dazu verwendet, um Kampagnen-Trackingcodes (sowohl interne als auch externe) und Produkt-IDs zu klassifizieren.

1. Wählen Sie eine Variable aus, indem Sie das entsprechende Kontrollkästchen aktivieren, und klicken Sie dann auf **[!UICONTROL Datenschutzkennzeichnungen bearbeiten]** auf der blauen Leiste unten auf dem Bildschirm.

   ![Bearbeiten](assets/edit-label.png)

   In diesem Bildschirm werden die aktuell angewendeten Kennzeichnungen angezeigt und Sie können zusätzliche Kennzeichnungen anwenden. Je nach Komponente können Sie möglicherweise nicht alle Kennzeichnungen anwenden oder ändern.

   ![Angewandte Kennzeichnungen](assets/edit-labels2.png)

1. Nachdem Sie sämtliche Kennzeichnungen abgeschlossen haben, klicken Sie auf **[!UICONTROL Übernehmen]**.

