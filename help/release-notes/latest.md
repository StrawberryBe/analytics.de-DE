---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: b38cdaaf79e22902c4a0fa0e9b782baba9cf0b26
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (Märzi 2024)

**Zuletzt aktualisiert**: 21. März 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 12. März 2024 bis April 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **AppMeasurement-Aktualisierung** | [AppMeasurement-Version v2.26.0](/help/implement/appmeasurement-updates.md) ist verfügbar. | | Dienstag, 4. März 2024 |
| **Auf der Landingpage „Projekte“ ist eine neue Spalte verfügbar** | Die Spalte **[!UICONTROL Zuletzt verwendet]** ist nun bei Ansicht der Registerkarte „Projekte“ auf der [Adobe Analytics-Landingpage](https://experienceleague.adobe.com/docs/analytics/analyze/landing.html?lang=de) verfügbar. <p>Mithilfe dieser Informationen können Sie feststellen, ob ein Projekt für Benutzerinnen und Benutzer in Ihrer Organisation nützlich ist, indem angezeigt wird, an welchem Datum und zu welcher Uhrzeit das Projekt zuletzt geöffnet wurde.</p> <p>Zuvor war die Spalte **[!UICONTROL Zuletzt verwendet]** nur im Manager für berechnete Metriken, im Segment-Manager und im Warnhinweis-Manager verfügbar.</p> |  | 13. März 2024 |
| **Analytics-Unterstützung für Einwilligungs-Flags, die von Google für DMA erforderlich sind** | Aufgrund neuer europäischer Datenschutzbestimmungen verlangt Google, dass die an Google gesendeten, in Europa erhobenen Daten angeben müssen, ob zwei spezifische Arten von Einwilligungen erteilt wurden. **Ab dem 6. März** akzeptiert Google keine Ereignisdaten mehr, die nicht angeben, dass die entsprechende Einwilligung erteilt wurde. Adobe Analytics bietet Unterstützung für die Erfassung dieser Daten über eine neue adConsent -Variable. Die neue Variable wird in der Liste [Benutzeroberfläche für Datenschutzberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md) angezeigt. Wenn Sie diese Funktion aktivieren möchten und bereits Datenschutzfunktion für die vorherigen Einwilligungsvariablen bereits aktiviert ist, müssen Sie die Datenschutzfunktion erneut aktivieren.<p>Die [Dimension „Einverständnis für Anzeigenplattform“](/help/components/dimensions/ad-consent.md) zeigt an, ob das Einverständnis zum Senden von Daten an Drittanbieter für Werbung wie Google eingeholt wird. |  | 13. März 2024 |
| **Die Verwendung von Report Builder ist in der Spalte „Verwendet in“ des Managers für berechnete Metriken und des Segment-Managers enthalten** | Beim Anzeigen der Spalte **Verwendet in** im Manager für berechnete Metriken oder im Segment-Manager stehen nun Nutzungsdaten für den Report Builder zur Verfügung.<p>Bisher waren Nutzungsdaten im Segment-Manager nur für Warnhinweise, Projekte, geplante Projekte und berechnete Metriken verfügbar, während Nutzungsdaten im Manager für berechnete Metriken nur für Warnhinweise, Projekte und geplante Projekte verfügbar waren.</p> |  | Juli |
| **Verwenden derselben Cloud-Konten für Daten-Feeds, Data Warehouse und Klassifizierungssätzen** | Von Ihnen erstellte Cloud-Konten und -Standorte können jetzt zum Exportieren von Daten (mit Daten-Feeds und Data Warehouse) und zum Importieren von Daten (mit Klassifizierungssätzen) verwendet werden.<p> **Änderungen beim Konfigurieren von Konten:** Benutzerinnen und Benutzer können Cloud-Import- und -Exportkonten konfigurieren und Cloud-Import- und -Exportspeicherorte konfigurieren, die für einen der folgenden Zwecke verwendet werden können:<ul><li>Importieren von Daten mit Klassifizierungssätzen</li><li>Exportieren von Daten mit Daten-Feeds</li><li>Exportieren von Daten mit Data Warehouse.</li></ul><p>**Änderungen bei der Verwaltung von Konten**: Benutzerinnen und Benutzer können die Seite „Standorte“ (unter Komponenten > Standorte) verwenden, um alle von ihnen erstellten Konten und Standorte anzuzeigen und zu verwalten, unabhängig davon, wo sie erstellt wurden. <p>Zuvor galt die Seite „Standorte“ nur für Konten, die zum Importieren von Daten mit Klassifizierungssätzen erstellt wurden.</p> | | April 2024 |
| **Verwaltung aller Speicherorte und Konten in der Organisation durch Admins** | Eine neue Option auf der Registerkarte „Speicherorte“ (auf der Seite „Komponenten“ > „Speicherorte“) ermöglicht es Admins, alle Speicherorte in der Organisation anzuzeigen und zu verwalten.<p>Eine neue Option auf der Registerkarte „Speicherort-Konten“ (auf der Seite „Komponenten“ > „Speicherorte“) ermöglicht es Admins, alle Konten in der Organisation anzuzeigen und zu verwalten.</p> <p>Bislang konnten Admins nur von ihnen selbst erstellte Speicherorte und Konten anzeigen und verwalten.</p> |  | April 2024 |
| **Activity Map verwendet weniger Server-Aufrufe für Web SDK** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. <p>Durch diese Verbesserung werden einige Link-Ereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung durch AppMeasurement.</p> |  | Donnerstag, 1. Mai 2024 |
| **Anhebung der standardmäßigen Schwellenwerte für geringeren Traffic** | **Mitte April 2024** beginnt Adobe mit der Erhöhung der standardmäßigen Report Suite-Schwellenwerte für geringen Traffic wie folgt: ![Schwellenwerte für geringen Traffic](assets/thresholds.png) Dies wirkt sich nur auf Variablen aus, die derzeit unter den neuen Schwellenwerten liegen. Diese Änderungen werden schrittweise vorgenommen und wir gehen davon aus, dass sie bis **Ende Mai** abgeschlossen sind. Wenn diese Erhöhungen eingeführt werden, werden Sie möglicherweise Änderungen bei Variablen mit hoher Kardinalität bemerken:<ul><li>Es können mehr Dimensionswerte für das Reporting verfügbar sein.</li><li>Segmente und berechnete Metriken können weitere Daten enthalten.</li><li>Virtual Report Suites, die auf Segmenten basieren, können mehr Daten enthalten.</li><li>Klassifizierungs-Exporte können mehr Daten enthalten.</li></ul> | | Mitte April 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden folgende Klassifizierungsprobleme behoben: AN-335632; AN-337559; AN-340164; AN-340370; AN-341089; AN-341211; AN-341284; AN-341469; AN-341481; AN-341760; AN-341778; AN-342144; AN-342258; AN-342338, AN-342400
* Es wurden die folgenden Probleme mit dem Classification Rule Builder behoben: AN-340921; AN-341269; AN-341292; AN-341467; AN-341666; AN-342145; AN-342329
* Es wurden die folgenden Probleme mit intelligenten Warnhinweisen behoben: AN-340736
* Es wurden die folgenden Probleme mit der Segmentierung behoben: AN-336242
* Es wurden die folgenden Probleme mit Data Warehouse behoben: AN-335354; AN-339446; AN-339774; AN-340221; AN-340599; AN-341277; AN-342009; AN-342088; AN-342592
* Es wurden die folgenden Probleme mit Daten-Feeds behoben: AN-335508; AN-340887; AN-341050; AN-341208; AN-341403; AN-341479; AN-341524; AN-341661; AN-342000; AN-342125; AN-342256; AN-342301; AN-342410; AN-342502; AN-342525
* Es wurden die folgenden Probleme mit Report Builder behoben: AN-340540
* Es wurden die folgenden Probleme mit Analysis Workspace behoben: AN-295889; AN-330981; AN-338818; AN-339730; AN-341114; AN-341520

### Weitere behobene Fehler in Analytics

AN-312198; AN-338009; AN-339549; AN-333970; AN-334790; AN-336461; AN-336572; AN-339549; AN-341119; AN-341246; AN-341268; AN-341272; AN-341475; AN-341547; AN-341558; AN-341680; AN-342017;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 20. März 2024 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, deren Freigabe für April oder Mai geplant ist, wird damit beginnen, eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durchzusetzen. Wenn „Besucherzuordnung aktivieren“ in der Report Suite aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Derzeit gibt es keine Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low`. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` einen `cust_visid` für einen Treffer hatte. |
| **Adobe-API-Objektmitgliederergänzungen** | 17. Januar 2024 | Adobe kann jederzeit ohne Ankündigung oder Versionsänderung optionale Anfrage- und Antwortmitglieder (Name/Wert-Paare) zu bestehenden API-Objekten hinzufügen. Adobe empfiehlt, in der API-Dokumentation jedes Drittanbieter-Tools, das Sie in unsere API integrieren, nachzuschlagen, damit solche Ergänzungen bei der Verarbeitung ignoriert werden, wenn sie nicht verstanden werden. Bei ordnungsgemäßer Implementierung stellen diese Ergänzungen keine einschneidenden Änderungen für Ihre Implementierung dar. Adobe entfernt keine Parameter und fügt keine erforderlichen Parameter hinzu, ohne zuvor durch Versionshinweise eine Standardbenachrichtigung bereitzustellen. |
| **`getPageLoadTime`-Plug-in veraltet** | 10. Januar 2024 | Dieses Plug-in wird nicht mehr unterstützt. Der Code verwendet die Methode „performance.timing“, die (laut MDN) [veraltet](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming) ist. Die Arbeit an einem aktualisierten Plug-in hat begonnen. |

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
