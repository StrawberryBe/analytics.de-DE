---
description: Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.
seo-description: Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.
seo-title: Anforderungen für die serverseitige Weiterleitung
solution: Audience Manager
title: Anforderungen für die serverseitige Weiterleitung
uuid: e 52 c 9292-b 2 ed -4782-9594-c 813 e 4 f 894 e 1
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Anforderungen für die serverseitige Weiterleitung

Sie müssen diese Anforderungen bezüglich Experience Cloud-Lösung, -Service und -Code erfüllen, um die serverseitige Weiterleitung implementieren zu können. Diese Anforderungen beinhalten auch Anweisungen für die Überprüfung von Codeversionen und dazu, wo Sie die neuesten Codebibliotheken erhalten.

## Lösungsanforderungen

Die serverseitige Weiterleitung funktioniert mit [Analytics](https://www.adobe.com/data-analytics-cloud/analytics.html) und [Audience Manager](https://www.adobe.com/data-analytics-cloud/audience-manager.html) und/oder [Zielgruppen](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).

## Dienstanforderungen

Server-side forwarding requires the [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/). Der Identitätsdienst stellt eine universelle ID bereit, die Site-Besucher über alle Lösungen in der Experience Cloud hinweg identifiziert. Sie müssen den ID-Dienst implementieren, bevor die serverseitige Weiterleitung funktioniert.

## Codeversionen

Für die serverseitige Weiterleitung ist Version 1.5 (oder höher) der nachstehend aufgeführten Codebibliotheken erforderlich. Als bewährte Methode wird empfohlen, anstelle der erforderlichen Mindestanforderungen die neuesten Versionen zu verwenden.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### Bestimmen der Version der Codebibliothek

Jedes Tool zur Überwachung der HTTP-Anfragen von einem Browser kann die Versionsnummer für den AppMeasurement- und Besucher-API-Code anzeigen. The `AppMeasurement_Module_AudienceManagement.js` does not contain or return a version ID. In den folgenden Beispielen wird veranschaulicht, wie die Versions-IDs für `AppMeasurement.js`- und `VisitorAPI.js`-Code aussehen.

* `AppMeasurement.js`: Der [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html) gibt die appmeasurement-Version wie folgt zurück: `Version of Code | JS-1.5.1`. In anderen Tools wird möglicherweise eine andere Kennzeichnung verwendet, der Wert folgt jedoch immer dem Muster `JS-X.X.X`, wobei `X` einer Versionsnummer entspricht.
* `VisitorAPI.js`: Suchen Sie nach dem `d_visid_ver` Parameter. It will show you the Visitor ID service like this: `d_visid_ver: 1.5.5`. Besucher-API-Code, der älter als Version 1.5.2 ist, enthält keine Versionsnummer. Sie verwenden wahrscheinlich eine ältere Codebibliothek (und müssen ein Upgrade durchführen), wenn die Überwachungsergebnisse keine Versionsnummer zurückgeben.