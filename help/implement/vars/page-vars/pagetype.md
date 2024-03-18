---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 75%

---

# pageType

Die `pageType`-Variable ist eine Markierung, mit der Sie Fehlerseiten (wie z. B. 404-Fehler) auf Ihrer Website angeben können. Wenn diese Variable die Zeichenfolge `errorPage` enthält, befüllt sie die [Dimension](/help/components/dimensions/pages-not-found.md) und [Metrik](/help/components/metrics/pages-not-found.md) „Seiten nicht gefunden“.

>[!IMPORTANT]
>
>Richten Sie diese Variable für Nicht-Fehler-Seiten ein.

## Seitentyp unter Verwendung des Web SDK

Der Kanal wird den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.isErrorPage` - Dieses XDM-Feld ist ein boolescher Wert. Setzen Sie es auf `true` , um sie als Fehlerseite zu kennzeichnen, oder `false` , wenn es keine Fehlerseite ist.
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageType` - dieses Datenobjektfeld eine Zeichenfolge ist, setzen Sie es auf `"errorPage"` , um sie als solche zu kennzeichnen.

## Seitentyp unter Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.pageType in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.pageType`-Variable ist eine Zeichenfolge, bei der der `errorPage`-Wert der einzige gültige Wert ist. Setzen Sie diese Variable auf diesen Wert auf jeder Fehlerseite Ihrer Website, z. B. auf 404-Seiten.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Verwenden Sie eine eVar, um den Fehler-Code zu erfassen, damit Sie weitere Informationen zu spezifischen Fehlern erhalten, auf die Besucher Ihrer Website stoßen.
