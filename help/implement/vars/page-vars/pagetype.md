---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 8a6c639af7427a9975ccd061d059696d4611dff3
workflow-type: ht
source-wordcount: '208'
ht-degree: 100%

---

# pageType

Die `pageType`-Variable ist eine Markierung, mit der Sie Fehlerseiten (wie z. B. 404-Fehler) auf Ihrer Website angeben können. Wenn diese Variable die Zeichenfolge `errorPage` enthält, befüllt sie die [Dimension](/help/components/dimensions/pages-not-found.md) und [Metrik](/help/components/metrics/pages-not-found.md) „Seiten nicht gefunden“.

>[!IMPORTANT]
>
>Richten Sie diese Variable für Nicht-Fehler-Seiten ein.

## Seitentyp unter Verwendung des Web SDK

Die Seitentyp-Variable wird [für Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) im XDM-Feld `web.webPageDetails.isErrorPage` zugeordnet. Dieses XDM-Feld erfordert einen booleschen Wert. Setzen Sie ihn auf `true`, um die Seite als Fehlerseite zu kennzeichnen, oder auf `false`, wenn es sich nicht um eine Fehlerseite handelt. Adobe übersetzt den booleschen Wert automatisch in den String-Wert `errorPage`, wenn er an eine Analytics Report Suite gesendet wird.

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
