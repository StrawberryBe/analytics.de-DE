---
title: pageName
description: Der Name der Seite auf Ihrer Website.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# pageName

Die `pageName`-Variable speichert normalerweise den Namen einer bestimmten Seite. Es ist hilfreich, zu bestimmen, welche einzelnen Seiten am beliebtesten sind. Diese Variable füllt die Dimension „Seitenname“.

>[!NOTE] Diese Dimension wird immer aus Linktracking-Aufrufen entfernt. Wenn Sie den Seitennamen sehen möchten, auf dem ein Link verfolgt wurde, sollten Sie diese Variable in eine eVar kopieren.

Wenn diese Variable bei einem gegebenen Seiten-Tracking-Aufruf nicht definiert ist, wird stattdessen die [`pageURL`](pageurl.md)-Variable verwendet.

## Seitenname in Adobe Experience Platform Launch

Sie können den Seitennamen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Page name] section.

Sie können den Seitennamen auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.pageName in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.pageName`-Variable ist eine Zeichenfolge, die normalerweise den Namen der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten. Diese Kürzung umfasst Fälle, in denen auf `pageURL` zurückgegriffen wird, wenn diese Variable leer ist.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
