---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# pageType

Die `pageType` Variable ist ein Flag, mit dem Sie Fehlerseiten auf Ihrer Site angeben können, z. B. 404-Fehler. Wenn diese Variable die Zeichenfolge enthält, `errorPage`wird die Dimension &quot;Seiten nicht gefunden&quot;gefüllt.

> [!IMPORTANT] Legen Sie diese Variable nicht auf Seiten ohne Fehler fest.

## Seitentyp beim Starten der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.pageType in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.pageType` Variable ist eine Zeichenfolge, bei der der Wert der einzige gültige Wert `errorPage` ist. Setzen Sie diese Variable auf diesen Wert auf jeder Fehlerseite Ihrer Site, z. B. auf 404 Seiten.

```js
s.pageType = "errorPage";
```

> [!TIP] Verwenden Sie eine eVar, um den Fehlercode zu erfassen, damit Sie weitere Informationen zu spezifischen Fehlern erhalten, auf die Besucher Ihrer Site stoßen.
