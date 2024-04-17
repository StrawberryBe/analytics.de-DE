---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 627a813d0d5595521d72f0cf832b3a1ceb7655f8
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 51%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2024)

**Letzte Aktualisierung**: Donnerstag, 17. April 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 17. April 2024 bis Mai. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Streaming-Medien: Senden von Roku-Daten an das Adobe Experience Platform-Edge Network** | Jetzt [Installieren von Media Analytics mit Experience Platform Edge](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge)können Sie das Adobe Experience Platform Roku-SDK verwenden, um Streaming-Medien-Daten an Adobe Experience Platform zu senden. |  | 12. April 2024 |
| **Verbesserter Workflow für die Web SDK-Migration** | Die Adobe Experience Platform-Datenerfassung ordnet jetzt automatisch viele Felder aus dem Datenobjekt direkt Adobe Analytics zu. Dieser verbesserte Workflow bietet die folgenden Vorteile:<ul><li>Dadurch kann Ihr Unternehmen zum Web SDK migrieren, ohne sich Gedanken über die Erstellung oder Einhaltung einer [!UICONTROL XDM-Schema]. Siehe [Zuordnung von Datenobjektvariablen](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/data-var-mapping) für weitere Informationen. (Weitere Links zur Dokumentation zu folgen)</li><li>Nach der Migration zum Web SDK ist Ihr Unternehmen besser in der Lage, von Adobe Analytics zu Customer Journey Analytics zu migrieren. Dies liegt daran, dass das Web SDK eine nahtlosere Migration zu Customer Journey Analytics ermöglicht.</li></ul> (Weitere Informationen zu diesen und anderen Migrationsoptionen werden in Kürze verfügbar sein.) |  | April 2024 |
| **Verbesserung der Berechtigungen für &quot;Nur Projekt&quot; [!UICONTROL Arbeitsbereich] Komponenten** | Wenn ein Benutzer (Benutzer A) zuvor ein Projekt für einen anderen Benutzer (Benutzer B) freigegeben und Benutzer B Bearbeitungszugriff auf das Projekt gewährt hat, konnte Benutzer B das Projekt bearbeiten. Benutzer B kann jedoch nicht [!UICONTROL Schnellsegmente] eingebettet in das Projekt. Diese Einschränkung wurde entfernt - Benutzer B kann bearbeiten [!UICONTROL Schnellsegmente] und anderen Projektkomponenten, die in das freigegebene Projekt eingebettet sind. |  | 17. April 2024 |
| **Verwenden Sie dieselben Cloud-Konten für [!UICONTROL Daten-Feeds], [!UICONTROL Data Warehouse], und [!UICONTROL Klassifizierungssätze]** | Von Ihnen erstellte Cloud-Konten und -Standorte können jetzt zum Exportieren von Daten verwendet werden (mit [!UICONTROL Daten-Feeds] und [!UICONTROL Data Warehouse]) und Importieren von Daten (mit [!UICONTROL Klassifizierungssätze]).<p> **Änderungen beim Konfigurieren von Konten:** Benutzer können [Konfigurieren von Cloud-Import- und -Exportkonten](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations) die für einen der folgenden Zwecke verwendet werden können:<ul><li>Importieren von Daten mit [!UICONTROL Klassifizierungssätze]</li><li>Exportieren von Daten mit [!UICONTROL Daten-Feeds]</li><li>Exportieren von Daten mit [!UICONTROL Data Warehouse].</li></ul><p>**Änderungen bei der Verwaltung von Konten**: Benutzer können die [Standorte](https://experienceleague.adobe.com/en/docs/analytics/components/locations/locations-manager) Seite (unter [!UICONTROL Komponenten] > Loc), um alle Konten und Standorte anzuzeigen und zu verwalten, die sie erstellen, unabhängig davon, wo sie erstellt wurden. <p>Zuvor wurde die Variable [!UICONTROL Standorte] Seite nur auf Konten angewendet, die zum Importieren von Daten mit [!UICONTROL Klassifizierungssätze].</p> | | 17. April 2024 |
| **Verwaltung aller Speicherorte und Konten in der Organisation durch Admins** | Eine neue Option auf der Registerkarte „Speicherorte“ (auf der Seite „Komponenten“ > „Speicherorte“) ermöglicht es Admins, alle Speicherorte in der Organisation anzuzeigen und zu verwalten.<p>Eine neue Option für [Standort](https://experienceleague.adobe.com/en/docs/analytics/components/locations/locations-manager) Registerkarte Konten (auf der Seite Komponenten > Standorte ) ermöglicht es Administratoren, alle Konten in der Organisation anzuzeigen und zu verwalten.</p> <p>Bislang konnten Admins nur von ihnen selbst erstellte Speicherorte und Konten anzeigen und verwalten.</p> |  | 17. April 2024 |
| **Anhebung der standardmäßigen Schwellenwerte für geringeren Traffic** | **Mitte April 2024** beginnt Adobe mit der Erhöhung der standardmäßigen Report Suite-Schwellenwerte für geringen Traffic wie folgt: ![Schwellenwerte für geringen Traffic](assets/thresholds.png) Dies wirkt sich nur auf Variablen aus, die derzeit unter den neuen Schwellenwerten liegen. Diese Änderungen werden schrittweise vorgenommen und wir gehen davon aus, dass sie bis **Ende Mai** abgeschlossen sind. Wenn diese Erhöhungen eingeführt werden, werden Sie möglicherweise Änderungen bei Variablen mit hoher Kardinalität bemerken:<ul><li>Es können mehr Dimensionswerte für das Reporting verfügbar sein.</li><li>Segmente und berechnete Metriken können weitere Daten enthalten.</li><li>Virtual Report Suites, die auf Segmenten basieren, können mehr Daten enthalten.</li><li>Klassifizierungs-Exporte können mehr Daten enthalten.</li></ul> | Mitte April 2024 | Samstag, 31. Mai 2024 |
| **Activity Map verwendet weniger Server-Aufrufe für Web SDK** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. <p>Durch diese Verbesserung werden einige Link-Ereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung durch AppMeasurement.</p> |  | Donnerstag, 1. Mai 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden folgende Klassifizierungsprobleme behoben: AN-343439; AN-343503; AN-343504; AN-343986; AN-344262; AN-344564; AN-3452 04; AN-345234
* Es wurden die folgenden Probleme mit dem Classifications Rule Builder behoben: AN-341488; AN-342501; AN-345751
* Es wurde das folgende Problem mit intelligenten Warnhinweisen behoben: AN-343466;
* Es wurden die folgenden Probleme mit der Segmentierung behoben: AN-342313
* Das folgende Data Warehouse-Problem wurde behoben: AN-344292
* Fehlerkorrektur - Die folgenden Datenfeeds funktionieren jetzt einwandfrei: AN-339545; AN-340092; AN-342124; AN-342862; AN-343737; AN-3445. 329; AN-344703; AN-344721; AN-344940; AN-345180; AN-345196; AN-345225; AN-3452 36; AN-345326; AN-345631; AN-345659
* Es wurde das folgende Data Sources-Problem behoben: AN-343541
* Die folgenden Analysis Workspace-Probleme wurden behoben: AN-336303; AN-336472; AN-338422; AN-338556; AN-339718; AN-340147; AN-3403 01; AN-340421; AN-340951; AN-341172; AN-342905; AN-342909; AN-343448; AN-34357 0; AN-344050; AN-344182; AN-344763; AN-344768;
* Es wurden folgende Analytics-Administratorprobleme behoben: AN-342519; AN-342523; AN-343623; AN-343882; AN-344237; AN-344829; AN-345 235;
* Die folgenden A4T-Probleme wurden behoben: AN-341619; AN-344402
* Das folgende Problem mit der mobilen App wurde behoben: AN-342010

### Weitere behobene Fehler in Analytics

AN-336099; AN-337474; AN-337993; AN-339718; AN-339901; AN-34014; AN-341356; AN 343021; AN-343102; AN-343353; AN-343416; AN-340014; AN-344037; AN-344525; AN-3 45737

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 20. März 2024 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, deren Freigabe für April oder Mai geplant ist, wird damit beginnen, eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durchzusetzen. Wenn „Besucherzuordnung aktivieren“ in der Report Suite aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Derzeit gibt es keine Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low`. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` einen `cust_visid` für einen Treffer hatte. |
| **Adobe-API-Objektmitgliederergänzungen** | 17. Januar 2024 | Adobe kann jederzeit ohne Ankündigung oder Versionsänderung optionale Anfrage- und Antwortmitglieder (Name/Wert-Paare) zu bestehenden API-Objekten hinzufügen. Adobe empfiehlt, in der API-Dokumentation jedes Drittanbieter-Tools, das Sie in unsere API integrieren, nachzuschlagen, damit solche Ergänzungen bei der Verarbeitung ignoriert werden, wenn sie nicht verstanden werden. Bei ordnungsgemäßer Implementierung stellen diese Ergänzungen keine einschneidenden Änderungen für Ihre Implementierung dar. Adobe entfernt keine Parameter und fügt keine erforderlichen Parameter hinzu, ohne zuvor durch Versionshinweise eine Standardbenachrichtigung bereitzustellen. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2023](/help/release-notes/2023.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
