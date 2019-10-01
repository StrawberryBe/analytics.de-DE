---
description: Before activating this integration, review the following items against your deployments of Adobe Analytics® and your email software.
seo-description: Before activating this integration, review the following items against your deployments of Adobe Analytics® and your email software.
seo-title: Before You Activate This Integration
title: Before You Activate This Integration
uuid: fdc762bc-24e3-4c0a-904d-d4be2a4f3a20
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# Vor Aktivierung dieser Integration {#before-you-activate-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Punkte in Bezug auf Ihre Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.

Auf diese Weise wird sichergestellt, dass vor der Aktivierung geeignete Best Practices oder Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

## Adobe Analytics Requirements{#adobe-analytics-requirements}

Lesen Sie die folgenden Informationen zu dieser Data Connectors-Integration in Bezug auf Adobe Analytics:

* **** Report Suite-spezifisch:Beachten Sie, dass diese Integration spezifisch für Report Suites ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren, und dass die Report Suite Daten enthält.
* **** Verfügbare und konfigurierte Analytics-Variablen: Für diese Integration sind 10 benutzerspezifische Ereignisse und 1 benutzerspezifische eVar erforderlich. Siehe [Analytics-Integrationsvariablen](appfigures-before-activation.md#analytics-integration-variables).

* **** Report Suite, die mit Live-Daten initialisiert wurde: Wenn Sie eine brandneue Report Suite für diese Integration erstellen, müssen einige (mindestens einen Treffer) Daten über die Live-Verfolgung der AppFigures-Anforderungen empfangen worden sein. Wenn keine Live-Daten aufgezeichnet wurden, kann die Report Suite keine integrierten App Store-Daten empfangen.

* **** Vorhandene Integration mit dem App Store: Durch diese Integration werden Daten für 13 Monate zurückgegeben. Um Überschneidungen mit früheren App Store-Datenanbietern zu vermeiden, wenden Sie sich bitte an Ihren appFigures-Kundenbetreuer. Teilen Sie ihnen mit, wann Sie zuletzt Daten erhalten haben. appFigures passt den Zeitraum für die Rückfüllung entsprechend an.

## appFigures Requirements{#appfigures-requirements}

Überprüfen Sie die folgenden Informationen zu dieser Data Connectors-Integration in Bezug auf appFigures:

* **** Aktueller Kunde von appFigures: Für diese Integration müssen Sie sowohl Adobe als auch appFigures verwenden. Wenn Sie derzeit nicht Benutzer von appFigures Enterprise Plan sind, verfügen Sie nicht über die zum Abschluss des Integrationsassistenten erforderlichen Informationen. Weitere Informationen finden Sie unter appFigures im Internet.
* **** appFigures-Kontoschlüssel: Zum Aktivieren des appFigures Data Connector ist ein appFigures-Kontoschlüssel erforderlich. Dieser Kontoschlüssel kann im Abschnitt "Add-ons"generiert werden. Weitere Informationen finden Sie unter Integration [konfigurieren](../appfigures-overview/t-appfigures-integration.md) .

* **Datenabwicklung**: Download-, Verkaufs- und Ranginformationen werden jeden Tag für die letzten 7 Tage synchronisiert. Nach 7 Tagen werden die Daten als endgültig betrachtet und nicht mehr aktualisiert.

## Preise{#pricing}

Diese Data Connectors-Integration beinhaltet Preisaspekte, die Sie kennen müssen.

Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

### Hinweise zu Adobe-Preisen {#section-2d1c79c895a5479bad8fdd97961ba6a3}

Für eine aktive Integration fallen derzeit keine Gebühren an. Es kann jedoch vorkommen, dass der Serveraufruf aufgrund des Datenquellen-Imports leicht ansteigt.

### appFigures Pricing Considerations {#section-c6afad08c34b43e3a7a3637eea3328c3}

Für diese Integration fallen derzeit keine Gebühren an. Diese Integration steht derzeit nur Enterprise-Kunden zur Verfügung. Weitere Informationen [erhalten Sie bei appFigures](https://appfigures.com/support/contact) .

## Analytics Integration Variables{#analytics-integration-variables}

The data connectors integration for appFigures uses Analytics variables to track various appFigures metrics.

Die folgende Tabelle beschreibt die Analytics-Variablen, die für die appFigures-Integration automatisch aktiviert werden.

### Required Variables {#section-3ca8dc46bab0436cba0c9ef827c8356a}

>[!NOTE]
>
>This integration uses dedicated variables for app store data, so you do not need to assign custom commerce variables and events.

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| eVar | App Store Objekt-ID | Imported from appFigures. | Configure this eVar with Visit expiration, Most recent allocation, and basic subrelations. |
| event (numeric) | App Store-Downloads | Imported from appFigures. | Anzahl der mobilen Anwendungs-Downloads. |
| event (numeric) | App Store Purchases (in app) | Imported from appFigures. | The number of in-app purchases and subscriptions. |
| event (numeric) | App Store-Platzierung | Imported from appFigures. | Dient zur Definition der berechneten Metrik "Durchschnittliche appFigures". Not used directly. |
| event (numerisch) | App Store-Divisor-Platzierung | Aus appFigures importiert. | Dient zur Definition der berechneten Metrik "Durchschnittliche appFigures". Nicht direkt verwendet. |
| event (numerisch) | App Store-Bewertung | Aus appFigures importiert. | Dient zur Definition der berechneten Metrik "Durchschnittliche appFigures". Nicht direkt verwendet. |
| event (numerisch) | Divisor für App Store-Bewertung | Aus appFigures importiert. | Dient zur Definition der berechneten Metrik "Durchschnittliche appFigures". Nicht direkt verwendet. |
| event (Währung) | App Store-Umsatz (in App) | Aus appFigures importiert. | Die Höhe des In-App-Umsatzes abzüglich der Store-Gebühr. |
| event (Währung) | App Store-Umsatz (einmalig) | Aus appFigures importiert. | Gesamtumsatz aus App-Käufen minus Store-Gebühr. |
| event (Währung) | App Store-Lizenzgebühren (in App) | Aus appFigures importiert. | Nicht verwendet |
| event (Währung) | App Store-Lizenzgebühren (einmal) | Aus appFigures importiert. | Nicht verwendet |
