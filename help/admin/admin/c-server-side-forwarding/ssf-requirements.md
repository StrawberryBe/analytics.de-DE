---
description: Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.
solution: Audience Manager
title: Anforderungen an die serverseitige Weiterleitung
uuid: e52c9292-b2ed-4782-9594-c813e4f894e1
translation-type: ht
source-git-commit: 327fdfd6a6d6bfe1c7bae9825fc8812b5ac7d095
workflow-type: ht
source-wordcount: '321'
ht-degree: 100%

---


# Anforderungen an die serverseitige Weiterleitung

Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.

## Lösungsanforderungen

Die serverseitige Weiterleitung funktioniert mit [Analytics](https://www.adobe.com/de/data-analytics-cloud/analytics.html) und [Audience Manager](https://www.adobe.com/de/analytics/audience-manager.html) und/oder [Zielgruppen](https://docs.adobe.com/content/help/de-DE/core-services/interface/audiences/audience-library.html).

## Dienstanforderungen

Die serverseitige Weiterleitung erfordert den [Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html). Identity Service bietet eine universelle ID zum Identifizieren der Site-Besucher über alle Experience Cloud-Lösungen hinweg. Sie müssen den ID-Dienst implementieren, bevor die serverseitige Weiterleitung funktioniert.

## Codeversionen

Für die serverseitige Weiterleitung ist Version 1.5 (oder höher) der nachstehend aufgeführten Codebibliotheken erforderlich. Als Best Practice wird empfohlen, anstelle der erforderlichen Mindestanforderungen die neuesten Versionen zu verwenden.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### Bestimmen der Version der Codebibliothek

Jedes Tool, das die von einem Browser ausgelösten HTTP-Anfragen überwacht. kann die Versionsnummer für den AppMeasurement und Visitor API-Code anzeigen. `AppMeasurement_Module_AudienceManagement.js` enthält keine Versions-ID und gibt keine Versions-ID zurück. In den folgenden Beispielen wird veranschaulicht, wie die Versions-IDs für `AppMeasurement.js`- und `VisitorAPI.js`-Code aussehen.

* `AppMeasurement.js`: Der [Adobe Debugger](https://docs.adobe.com/content/help/de-DE/analytics/implementation/validate/debugger.html) gibt die AppMeasurement-Version wie folgt zurück: `Version of Code | JS-1.5.1`. In anderen Tools wird möglicherweise eine andere Kennzeichnung verwendet, der Wert folgt jedoch immer dem Muster `JS-X.X.X`, wobei `X` einer Versionsnummer entspricht.
* `VisitorAPI.js`: Suchen Sie nach dem Parameter `d_visid_ver`. Er gibt den Besucher-ID-Dienst wie folgt an: `d_visid_ver: 1.5.5`. Besucher-API-Code, der älter als Version 1.5.2 ist, enthält keine Versionsnummer. Sie verwenden wahrscheinlich eine ältere Codebibliothek (und müssen ein Upgrade durchführen), wenn die Überwachungsergebnisse keine Versionsnummer zurückgeben.
