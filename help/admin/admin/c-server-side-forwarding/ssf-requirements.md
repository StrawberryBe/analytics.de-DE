---
description: Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.
seo-description: Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.
seo-title: Anforderungen an die serverseitige Weiterleitung
solution: Audience Manager
title: Anforderungen an die serverseitige Weiterleitung
uuid: e52c9292-b2ed-4782-9594-c813e4f894e1
translation-type: tm+mt
source-git-commit: bc46011a48aa18e33ba6f1912223857f5a664f35

---


# Anforderungen an die serverseitige Weiterleitung

Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.

## Lösungsanforderungen

Die serverseitige Weiterleitung funktioniert mit [Analytics](https://www.adobe.com/data-analytics-cloud/analytics.html) und [Audience Manager](https://www.adobe.com/data-analytics-cloud/audience-manager.html) und/oder [Zielgruppen](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).

## Dienstanforderungen

Die serverseitige Weiterleitung erfordert den [Identitätsdienst](https://marketing.adobe.com/resources/help/en_US/mcvid/). Der Identitätsdienst stellt eine universelle ID bereit, die Site-Besucher in allen Lösungen der Experience Cloud identifiziert. Sie müssen den ID-Dienst implementieren, bevor die serverseitige Weiterleitung funktioniert.

## Codeversionen

Für die serverseitige Weiterleitung ist Version 1.5 (oder höher) der nachstehend aufgeführten Codebibliotheken erforderlich. Als bewährte Methode wird empfohlen, anstelle der erforderlichen Mindestanforderungen die neuesten Versionen zu verwenden.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### Bestimmen der Version der Codebibliothek

Jedes Tool zur Überwachung der HTTP-Anfragen von einem Browser kann die Versionsnummer für den AppMeasurement- und Besucher-API-Code anzeigen. The `AppMeasurement_Module_AudienceManagement.js` does not contain or return a version ID. In den folgenden Beispielen wird veranschaulicht, wie die Versions-IDs für `AppMeasurement.js`- und `VisitorAPI.js`-Code aussehen.

* `AppMeasurement.js`: Der [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html) gibt die AppMeasurement-Version wie folgt zurück: `Version of Code | JS-1.5.1`. In anderen Tools wird möglicherweise eine andere Kennzeichnung verwendet, der Wert folgt jedoch immer dem Muster `JS-X.X.X`, wobei `X` einer Versionsnummer entspricht.
* `VisitorAPI.js`: Suchen Sie nach dem `d_visid_ver` Parameter. It will show you the Visitor ID service like this: `d_visid_ver: 1.5.5`. Besucher-API-Code, der älter als Version 1.5.2 ist, enthält keine Versionsnummer. Sie verwenden wahrscheinlich eine ältere Codebibliothek (und müssen ein Upgrade durchführen), wenn die Überwachungsergebnisse keine Versionsnummer zurückgeben.
