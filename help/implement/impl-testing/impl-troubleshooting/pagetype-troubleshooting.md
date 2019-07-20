---
description: Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).
keywords: Analytics-Implementierung
seo-description: Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).
seo-title: Pagetype-Variable falsch festlegen
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Pagetype-Variable falsch festlegen
topic: Entwickler und Implementierung
uuid: bedroaf 58 e-ba 7-416 f -89 b 9-694687 cc 4802
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pagetype-Variable falsch festlegen

Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).

Ihr einziger möglicher Wert lautet „errorPage“.

```js
pageType="errorPage"
```

Auf einer 404-Fehlerseite sollte die Variable  *`pageName`* nicht gefüllt werden. The *`pageType`* variable should be set only on a designated 404 error page. Any page containing content should never have a value in the *`pageType`* variable. Bei Seiten, die über Inhalte verfügen, können Sie die Variable wie folgt festlegen:

```js
pageType=""
```

Die Variable sollte bei Seiten mit Inhalten am besten ganz gelöscht werden. So wird unnötige Verwirrung in Bezug auf den Zweck dieser Variablen vermieden.
