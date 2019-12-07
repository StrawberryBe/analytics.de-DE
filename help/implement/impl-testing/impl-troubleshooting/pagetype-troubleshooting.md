---
description: Die Variable „pageType“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Korrektes Festlegen der Variable „PageType“
topic: Developer and implementation
uuid: eafaf58e-ba07-416f-89b9-694687cc4802
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

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
