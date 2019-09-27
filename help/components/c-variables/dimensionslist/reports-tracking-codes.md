---
description: Ermittelt, wie sich verschiedene Werbe-Trackingcodes auf die unterschiedlichen Konversionsereignisse auf Ihrer Site auswirken. Mit diesem Bericht können Sie feststellen, welche speziellen Kampagnen bei verschiedenen Erfolgsereignissen bessere Ergebnisse erzielen, oder wie Kampagnen die Aktionen auf Ihrer Site unterstützen oder behindern. Sie können z. B. ermitteln, welche Kampagnen den meisten Umsatz generieren.
seo-description: Ermittelt, wie sich verschiedene Werbe-Trackingcodes auf die unterschiedlichen Konversionsereignisse auf Ihrer Site auswirken. Mit diesem Bericht können Sie feststellen, welche speziellen Kampagnen bei verschiedenen Erfolgsereignissen bessere Ergebnisse erzielen, oder wie Kampagnen die Aktionen auf Ihrer Site unterstützen oder behindern. Sie können z. B. ermitteln, welche Kampagnen den meisten Umsatz generieren.
seo-title: Trackingcodes
solution: Analytics
title: Trackingcodes
topic: Berichte
uuid: c893d592-10fd-4b40-84b3-8c8949a67b25
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Trackingcodes

Ermittelt, wie sich verschiedene Werbe-Trackingcodes auf die unterschiedlichen Konversionsereignisse auf Ihrer Site auswirken. Mit diesem Bericht können Sie feststellen, welche speziellen Kampagnen bei verschiedenen Erfolgsereignissen bessere Ergebnisse erzielen, oder wie Kampagnen die Aktionen auf Ihrer Site unterstützen oder behindern. Sie können z. B. ermitteln, welche Kampagnen den meisten Umsatz generieren.

**Allgemeine Eigenschaften**

* Dieser Bericht listet Daten direkt aus der auf Ihrer Website implementierten Variablen [„s.campaign“](/help/implement/js-implementation/c-variables/page-variables.md) auf.
* Die Variable, auf der dieser Bericht basiert, ist eine [Konversionsvariable](/help/admin/admin/conversion-var-admin/conversion-var-admin.md). Das heißt, sie kann über die Seitenansicht hinaus bestehen und innerhalb des angegebenen Ablaufzeitraums Metriken zugeordnet werden.
* Umsatz ist die Standardmetrik des Berichts. Sie können diesen Standardwert im [!UICONTROL Report Suite Manager] in den [!UICONTROL Admin Tools] ändern. ( **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Individual Report Settings]** &gt; **[!UICONTROL Default Metrics]**.)

* Der Bericht kann sowohl als Trendansicht als auch als Rangansicht angezeigt werden.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Die Berichte [!UICONTROL „Kampagnen“] und [!UICONTROL „Kreativelemente“] sind auf diesem Bericht basierende Classifications und werden automatisch mit jeder Report Suite erstellt.

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

   * Click-throughs: the number of times the *`s.campaign`* variable is defined
   * Alle E-Commerce-Standardmetriken: Umsatz, Bestellungen, Einheiten, Warenkorb, Warenkorbansichten, Checkouts, Zusätze zum Warenkorb, Entnahmen aus Warenkorb.
   * Alle benutzerspezifischen Ereignisse: Ereignisse 1-80 und Ereignisse 81-100 bei H22-Code oder höher.
   * Besuche und Besucher: Die Verfügbarkeit hängt von der Organisation und der Report Suite ab. Nähere Informationen erhalten Sie von Ihrem Kundenbetreuer.

**Reports &amp; Analytics – Eigenschaften**

* Click **[!UICONTROL Conversion]** &gt; **[!UICONTROL Campaigns]** &gt; **[!UICONTROL Tracking Code]** to locate this report, unless the menu is customized.

* Dieser Bericht kann auch nach allen [Listenvariablen](https://marketing.adobe.com/resources/help/en_US/sc/implement/list_var.html) aufgeschlüsselt werden.
* Verfügbare Metriken: Seitenansichten, Besuche und Unique Visitor.
* Dieser Bericht kann Segmente verwenden.

** Ad-hoc-Analysen-Eigenschaften**

* Zusätzlich zu den meisten vordefinierten Konversionsvariablen können Sie den Bericht zum Trackingcode nach allen anderen Berichten der Berichterstellungsoberfläche aufschlüsseln.
* Zusätzlich zu E-Commerce- und benutzerspezifischen Ereignissen können Sie alle Konversions- und Traffic-Metriken sowie unterschiedliche Zuordnungen für die Konversionsmetriken nutzen.
* Dieser Bericht kann erweiterte Segmente verwenden.

