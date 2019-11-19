---
description: Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren.
keywords: Analytics Implementation;eVar;conversion variable;eVar value;conversion;success event
solution: Analytics
title: Konversionsvariablen (eVars)
topic: Developer and implementation
uuid: 50071c1c-be00-4b3a-a7ee-5d129acf498b
translation-type: tm+mt
source-git-commit: edf88e40cae8b6886b04257f266666c13a37f88d

---


# Konversionsvariablen (eVars)

Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren.

eVars eignen sich am besten zur Messung von Ursache und Wirkung, z. B.:

* Welche internen Kampagnen haben den Umsatz beeinflusst?
* Welche Banneranzeigen haben letztlich zu einer Registrierung geführt?
* Wie viele interne Suchläufe wurden durchgeführt, bevor eine Bestellung aufgegeben wurde?

>[!IMPORTANT]
>
>Wenn Sie Analytics implementieren, müssen Sie wissen, welche und wie viele eVars Sie verwenden möchten. Außerdem sollten Sie mit der Konfiguration dieser eVars in der Admin Console vertraut sein. Detaillierte Informationen über eVars finden Sie unter [Konversionsvariablen (eVar)](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) in der Analytics-Hilfe und -Referenz.

Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.

Wenn eine eVar auf einen Wert für einen Besucher gesetzt wird, merkt Adobe sich automatisch diesen Wert, bis er abläuft. Jedes Erfolgsereignis, das beim Besucher während der eVar-Aktivität eintritt, wird für den eVar-Wert gezählt.

> [!NOTE] Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [Listenvariablen](/help/implement/js-implementation/page-variables/listvariable.md).

Weitere Informationen zu Variablen finden Sie unter:

* [Variablen für die Analytics-Implementierung und -Berichte](/help/implement/js-implementation/c-variables/sc-variables.md) in dieser Hilfe
* [Variablen – Verwendung in den Berichten](https://marketing.adobe.com/resources/help/en_US/reference/variable_definitions.html)
* [Seitenvariablen](/help/implement/js-implementation/page-variables/page-variables.md)
* [Kampagnenvariable](/help/implement/js-implementation/page-variables/campaign.md)
* [Variable „products“](/help/implement/js-implementation/page-variables/products.md)
* [Variable „products“](https://marketing.adobe.com/resources/help/en_US/mobile/android/products.html) in der Dokumentation zum mobilen SDK

