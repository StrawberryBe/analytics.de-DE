---
description: Ermittelt, wie sich verschiedene Werbe-Trackingcodes auf die unterschiedlichen Konversionsereignisse auf Ihrer Site auswirken. Mit diesem Bericht können Sie feststellen, welche speziellen Kampagnen bei verschiedenen Erfolgsereignissen bessere Ergebnisse erzielen, oder wie Kampagnen die Aktionen auf Ihrer Site unterstützen oder behindern. Sie können z. B. ermitteln, welche Kampagnen den meisten Umsatz generieren.
title: Trackingcodes
topic: Reports
uuid: c893d592-10fd-4b40-84b3-8c8949a67b25
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Trackingcodes

Ermittelt, wie sich verschiedene Werbe-Trackingcodes auf die unterschiedlichen Konversionsereignisse auf Ihrer Site auswirken. Mit diesem Bericht können Sie feststellen, welche speziellen Kampagnen bei verschiedenen Erfolgsereignissen bessere Ergebnisse erzielen, oder wie Kampagnen die Aktionen auf Ihrer Site unterstützen oder behindern. Sie können z. B. ermitteln, welche Kampagnen den meisten Umsatz generieren.

**Allgemeine Eigenschaften**

* Dieser Bericht referenziert Daten direkt in [s.campaign](/help/implement/vars/page-vars/campaign.md)
* Die Variable, auf der dieser Bericht basiert, ist eine  [Konversionsvariable](/help/admin/admin/conversion-var-admin/conversion-var-admin.md). Das heißt, sie kann über die Seitenansicht hinaus bestehen und innerhalb des angegebenen Ablaufzeitraums Metriken zugeordnet werden.
* Umsatz ist die Standardmetrik des Berichts. You can change this default value in the [!UICONTROL Report Suite Manager] in [!UICONTROL Admin Tools]. ( **[!UICONTROL Edit Settings]** > **[!UICONTROL Individual Report Settings]** > **[!UICONTROL Default Metrics]**.)

* Der Bericht kann sowohl als Trendansicht als auch als Rangansicht angezeigt werden.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* The [!UICONTROL Campaigns] and [!UICONTROL Creative Elements] reports are classifications based on this report, and are automatically created with each report suite.

* Sie können SAINT-Classifications zum Umbenennen und Konsolidieren von Zeileneinträgen in dem Bericht verwenden.
* Sie können diesen Bericht durch die folgenden Berichte aufschlüsseln (je nach Unternehmens- und Report Suite-Einstellungen):

   * Zeit pro Besuch
   * Seiten- und Sitebereichsberichte mit allen zugehörigen Classifications
   * Klicktiefe, Entrypages und Ursprüngliche Entrypages
   * Die meisten Berichte zu Traffic-Quellen
   * Besuchnummer und Kundenloyalität
   * Viele Berichte zu Besucherprofil und Technologie, jedoch ohne Geosegmentation
   * Alle benutzerspezifischen Konversion-Ereignisse

* In diesem Bericht können die folgenden Metriken verwendet werden (je nach Unternehmens- und Report Suite-Einstellungen):

   * Clickthroughs: Anzahl der Definitionen der Variable *`s.campaign`*
   * Alle E-Commerce-Standardmetriken: Umsatz, Bestellungen, Einheiten, Warenkorb, Warenkorbansichten, Checkouts, Zusätze zum Warenkorb, Entnahmen aus Warenkorb.
   * Alle benutzerspezifischen Ereignisse: Ereignisse 1-80 und Ereignisse 81-100 bei H22-Code oder höher.
   * Besuche und Besucher: Die Verfügbarkeit hängt von der Organisation und der Report Suite ab. Nähere Informationen erhalten Sie von Ihrem Kundenbetreuer.

**Reports &amp; Analytics – Eigenschaften**

* Klicken Sie auf **[!UICONTROL Conversion]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Tracking Code]** , um nach diesem Bericht zu suchen, es sei denn, das Menü wurde angepasst.

* Dieser Bericht kann auch nach allen [Listenvariablen](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/list-var-admin.html) aufgeschlüsselt werden.
* Verfügbare Metriken: Seitenansichten, Besuche und Unique Visitor.
* Dieser Bericht kann Segmente verwenden.

**Eigenschaften von Ad Hoc Analysis**

* Zusätzlich zu den meisten vordefinierten Konversionsvariablen können Sie den Bericht zum Trackingcode nach allen anderen Berichten der Berichterstellungsoberfläche aufschlüsseln.
* Zusätzlich zu E-Commerce- und benutzerspezifischen Ereignissen können Sie alle Konversions- und Traffic-Metriken sowie unterschiedliche Zuordnungen für die Konversionsmetriken nutzen.
* Dieser Bericht kann erweiterte Segmente verwenden.

