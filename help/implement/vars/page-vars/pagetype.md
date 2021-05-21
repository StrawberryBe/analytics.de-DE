---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '135'
ht-degree: 100%

---

# pageType

Die `pageType`-Variable ist eine Markierung, mit der Sie Fehlerseiten (wie z. B. 404-Fehler) auf Ihrer Website angeben können. Wenn diese Variable die Zeichenfolge `errorPage` enthält, wird die Dimension „Seiten nicht gefunden“ gefüllt.

>[!IMPORTANT]
>
>Legen Sie diese Variable nicht auf Seiten ohne Fehler fest.

## Seitentyp in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.pageType in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.pageType`-Variable ist eine Zeichenfolge, bei der der `errorPage`-Wert der einzige gültige Wert ist. Setzen Sie diese Variable auf diesen Wert auf jeder Fehlerseite Ihrer Website, z. B. auf 404-Seiten.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Verwenden Sie eine eVar, um den Fehler-Code zu erfassen, damit Sie weitere Informationen zu spezifischen Fehlern erhalten, auf die Besucher Ihrer Website stoßen.
