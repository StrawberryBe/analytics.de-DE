---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d52e4d41ac0fc6ce6db04e491fc33bac2284f040
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 42%

---

# Aktuelle Adobe Analytics-Versionshinweise (Februar 2024)

**Letzte Aktualisierung**: Samstag, 16. Februar 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 14. Februar 2024 bis zum 11. März 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Activity Map für Web SDK ohne zusätzliche Kosten** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. Durch diese Verbesserung werden einige Linkereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung von AppMeasurement. |  | Donnerstag, 6. März 2024 |
| **Anhebung der standardmäßigen Schwellenwerte für niedrigen Traffic** | In **Mitte April 2024** beginnt Adobe mit der Erhöhung der standardmäßigen Report Suite-Schwellenwerte für niedrigen Traffic wie folgt: ![niedrige Traffic-Schwellenwerte](assets/thresholds.png) Dies wirkt sich nur auf Variablen aus, die derzeit unter den neuen Schwellenwerten liegen. Diese Änderungen werden schrittweise vorgenommen, und wir erwarten, dass die Arbeit durch die **Ende Mai**. Wenn diese Erhöhungen eingeführt werden, werden Sie möglicherweise Änderungen bei Variablen mit hoher Kardinalität bemerken:<ul><li>Es können mehr Dimensionswerte für die Berichterstellung verfügbar sein.</li><li>Segmente und berechnete Metriken können weitere Daten enthalten.</li><li>Virtual Report Suites, die auf Segmenten basieren, können mehr Daten enthalten.</li></ul> | Mitte April 2024 | Ende Mai 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden folgende Klassifizierungsprobleme behoben: AN-319515; AN-337559; AN-338149; AN-338702; AN-338769; AN-338891; AN-339 AN-339649; AN-339668; AN-339669; AN-339776; AN-339822; AN-340017; AN-34020 2; AN-340476;
* Es wurden die folgenden Probleme mit dem Classifications Rule Builder behoben: AN-338385; AN-338399; AN-338592; AN-338810; AN-338893; AN-339431; 9894; AN-339933; AN-340201; AN-340309;
* Die folgenden A4T-Probleme wurden behoben: AN-334830; AN-336194; AN-338309; AN-338650;
* Es wurde ein Problem mit der folgenden Datenerfassung behoben: AN-339323
* Fehlerkorrektur - Die folgenden Data Warehouse-Probleme wurden behoben: AN-335542; AN-331425; AN-337215; AN-338445; AN-338651; AN-3394 61; AN-340066; AN-340207; AN-340460
* Fehlerkorrektur - Die folgenden Daten-Feeds funktionieren jetzt einwandfrei: AN-335952; AN-338653; AN-339508; AN-339681; AN-340418
* Die folgenden Data Sources-Probleme wurden behoben: AN-338648
* Die folgenden Analysis Workspace-Probleme wurden behoben: AN-326509; AN-336186; AN-336190; AN-336309; AN-337922; AN-338094; AN-38333 23; AN-338556; AN-339600; AN-340445

### Weitere behobene Fehler in Analytics

AN-328239; AN-332908; AN-335449; AN-335517; AN-336075; AN-336100; AN-336128; AN 338088; AN-338270; AN-338393; AN-338494; AN-339326; AN-339742; AN-33983; AN-3 40419;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| Adobe-API-Objektmitgliederergänzungen | 17. Januar 2024 | Adobe kann vorhandenen API-Objekten jederzeit und ohne Vorankündigung oder Änderungen der Versionierung optionale Anforderungs- und Antwortmitglieder (Name/Wert-Paare) hinzufügen. Adobe empfiehlt, in der API-Dokumentation jedes Drittanbieter-Tools, das Sie in unsere APIs integrieren, nachzuschlagen, damit solche Ergänzungen bei der Verarbeitung ignoriert werden, wenn sie nicht verstanden werden. Bei ordnungsgemäßer Implementierung handelt es sich bei diesen Ergänzungen um grundlegende Änderungen für Ihre Implementierung. Adobe entfernt keine Parameter und fügt keine erforderlichen Parameter hinzu, ohne zuvor durch Versionshinweise eine Standardbenachrichtigung bereitzustellen. |
| `getPageLoadTime`-Plug-in veraltet | 10. Januar 2024 | Dieses Plug-in wird nicht mehr unterstützt. Der Code verwendet die Methode „performance.timing“, die (laut MDN) [veraltet](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming) ist. Die Arbeit an einem aktualisierten Plug-in hat begonnen. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.25.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2023](/help/release-notes/2023.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
