---
description: Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).
keywords: Analytics-Implementierung
seo-description: Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).
seo-title: Korrektes Festlegen der Variable „PageType“
solution: Analytics
subtopic: Fehlerbehebung
title: Korrektes Festlegen der Variable „PageType“
topic: Entwickler und Implementierung
uuid: eafaf58e-ba07-416f-89b9-694687cc4802
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Korrektes Festlegen der Variable „PageType“

Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).

Ihr einziger möglicher Wert lautet „errorPage“.

```js
pageType="errorPage"
```

Auf einer 404-Fehlerseite sollte die Variable *`pageName`* nicht gefüllt werden. Die Variable *`pageType`* sollte nur auf einer dafür vorgesehenen 404-Fehlerseite festgelegt werden. Bei Seiten, die über Inhalte verfügen, darf niemals ein Wert in der Variable *`pageType`* stehen. Bei Seiten, die über Inhalte verfügen, können Sie die Variable wie folgt festlegen:

```js
pageType=""
```

Die Variable sollte bei Seiten mit Inhalten am besten ganz gelöscht werden. So wird unnötige Verwirrung in Bezug auf den Zweck dieser Variablen vermieden.
