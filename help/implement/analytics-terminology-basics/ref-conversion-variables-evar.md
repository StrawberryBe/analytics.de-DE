---
description: Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren.
keywords: Analytics-Implementierung; Evar; Konversionsvariable; Evar-Wert; conversion; Erfolgsereignis
seo-description: Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren.
seo-title: Konversionsvariablen (evars)
solution: Analytics
title: Konversionsvariablen (evars)
topic: Entwickler und Implementierung
uuid: 50071 c 1 c-be 00-4 b 3 a-a 7 ee -5 d 129 acf 498 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Konversionsvariablen (evars)

Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren.

eVars eignen sich am besten zur Messung von Ursache und Wirkung, z. B.:

* Welche internen Kampagnen haben den Umsatz beeinflusst?
* Welche Banneranzeigen haben letztlich zu einer Registrierung geführt?
* Wie viele interne Suchläufe wurden durchgeführt, bevor eine Bestellung aufgegeben wurde?

>[!IMPORTANT]
>
>Bei der Implementierung von Analytics ist es wichtig zu wissen, welche evars Sie verwenden und wie viele. Außerdem sollten Sie mit der Konfiguration dieser eVars in der Admin Console vertraut sein. Detaillierte Informationen über eVars finden Sie unter [Konversionsvariablen (eVar)](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) in der Analytics-Hilfe und -Referenz.

Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.

Wenn eine eVar auf einen Wert für einen Besucher gesetzt wird, merkt Adobe sich automatisch diesen Wert, bis er abläuft. Jedes Erfolgsereignis, das beim Besucher während der eVar-Aktivität eintritt, wird für den eVar-Wert gezählt.

>[!NOTE]
>
>In einer Bildanforderung kann nur ein einzelner Wert in einer evar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [](/help/implement/js-implementation/c-variables/page-variables.md)Listenvariablen.

Weitere Informationen zu Variablen finden Sie unter:

* [Variablen für die Analytics-Implementierung und -berichterstellung](../../implement/js-implementation/c-variables/sc-variables.md#concept_E10E43221A2740FAAF900B79CE1EC5FB) in dieser Hilfe
* [Variablen – Verwendung in den Berichten](https://marketing.adobe.com/resources/help/en_US/reference/variable_definitions.html)
* [Seitenvariablen](/help/implement/js-implementation/c-variables/page-variables.md)
* [Kampagnenvariable](/help/implement/js-implementation/c-variables/page-variables.md)
* [Variable „products“](/help/implement/js-implementation/c-variables/page-variables.md)
* [Variable „products“](https://marketing.adobe.com/resources/help/en_US/mobile/android/products.html) in der Dokumentation zum mobilen SDK

