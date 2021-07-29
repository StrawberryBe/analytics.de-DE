---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 83%

---

# pageType

Die `pageType`-Variable ist eine Markierung, mit der Sie Fehlerseiten (wie z. B. 404-Fehler) auf Ihrer Website angeben können. Wenn diese Variable die Zeichenfolge `errorPage` enthält, wird die Dimension „Seiten nicht gefunden“ gefüllt.

>[!IMPORTANT]
>
>Legen Sie diese Variable nicht auf Seiten ohne Fehler fest.

## Seitentyp mit Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.pageType in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die `s.pageType`-Variable ist eine Zeichenfolge, bei der der `errorPage`-Wert der einzige gültige Wert ist. Setzen Sie diese Variable auf diesen Wert auf jeder Fehlerseite Ihrer Website, z. B. auf 404-Seiten.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Verwenden Sie eine eVar, um den Fehler-Code zu erfassen, damit Sie weitere Informationen zu spezifischen Fehlern erhalten, auf die Besucher Ihrer Website stoßen.
