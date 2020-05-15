---
description: Erläutert die neue Strategie für die kontinuierliche Funktionserweiterung in Adobe Analytics
title: Versionshinweise zu Adobe Analytics-Funktionen
translation-type: tm+mt
source-git-commit: dcca8559c9e730c9e04981d69068786878062561
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 4%

---


# Versionshinweise zu Adobe Analytics-Funktionen

Bisher wurden Adobe Analytics-Funktionen nach einem festen monatlichen Zeitplan veröffentlicht. Seit April 2020 ist Adobe Analytics in ein kontinuierliches Versand-Modell umgestiegen, das eine skalierbarere, stufenweise Einführung von Funktionen ermöglicht.

## Versionsstrategie

[!UICONTROL Analyse Workspace] nutzt Funktions-Flags (auch als &quot;Umschalter&quot;bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass vor der Vollversion ein kontrollierter Skalierungstest durchgeführt werden kann. Diese Versionsstrategie umfasst die folgenden Phasen:

* **Release to Production (RTP)**: Der Code wird für die Produktion freigegeben, wobei die Sichtbarkeit der Funktionen in Analyse Workspace deaktiviert ist. **Hinweis**: Bei RTP ist die Funktion möglicherweise in der 2.0 Analytics-API verfügbar.

* **Eingeschränkte Tests**: Eine schrittweise Veröffentlichung beginnt mit Tests durch interne Adobe-Benutzer. Die Verfügbarkeit der Version wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Die schrittweise Einführung erfolgt auf der Ebene der Experience Cloud-Organisation, sodass alle Benutzer mit Berechtigung in einem Unternehmen dasselbe Erlebnis erhalten.

* **Allgemeine Verfügbarkeit (GA)**: Die Funktion steht 100 % der Unternehmen mit der Berechtigung Experience Cloud zur Verfügung, und die Version der Funktionen ist abgeschlossen.

Bei jeder Funktionsversion kann die Zeitschiene von RTP bis GA variieren. Ziel ist es, die Releases kurz zu halten, sodass innerhalb von 2 Monaten nach Release Beginn (RTP) eine Funktion GA ist.

## Vorteile

Die gestaffelten Versionen ermöglichen es Adobe, den Softwarebereitstellungsprozess zu skalieren und sicherzustellen, dass die Funktionen vor der allgemeinen Verfügbarkeit vollständig gehärtet werden. Außerdem können Funktionen sofort nach Verfügbarkeit veröffentlicht werden, anstatt ein festes monatliches Versionsfenster einzuhalten.

## Häufig gestellte Fragen (FAQ)

| Frage | Antwort |
|---|---|
| Kann ich einen frühzeitigen Zugriff auf eine Funktion anfordern? | Nein. Der frühzeitige Zugang wird nicht gewährt.<br>Wenn Sie frühe Analytics-Konzepte testen möchten, empfehlen wir Ihnen, [Adobe Analytics Labs](https://docs.adobe.com/content/help/de-DE/analytics/analyze/tech-previews/overview.html) zu testen, um Rückmeldungen zu unseren branchenführenden Innovationen zu erhalten. |
| Hat diese Versionsstrategie Auswirkungen auf meinen Zugriff auf Funktionen? | Nein. Sobald eine Funktion GA erreicht hat, haben Sie Zugriff auf die Funktion, wenn sie in Ihrem Analytics-Paket enthalten ist.<br>Details zu Ihrem Analytics-Paket finden Sie unter [!UICONTROL Admin] > Einstellungen für die [!UICONTROL Firma] > Zugriffsebenen für [Funktionen](https://docs.adobe.com/content/help/en/analytics/admin/company-settings/feature-access-levels.html). |