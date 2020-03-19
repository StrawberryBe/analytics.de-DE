---
title: pageName
description: Der Name der Seite auf Ihrer Site.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# pageName

Die `pageName` Variable speichert normalerweise den Namen einer bestimmten Seite. Es ist hilfreich festzustellen, welche einzelnen Seiten bevorzugt werden. Diese Variable füllt die Dimension &quot;Seitenname&quot;.

> [!NOTE] Diese Dimension wird immer aus Linktracking-Aufrufen entfernt. Wenn Sie den Seitennamen sehen möchten, auf dem ein Link verfolgt wurde, sollten Sie diese Variable in eine eVar kopieren.

Wenn diese Variable bei einem gegebenen Seitenverfolgungsaufruf nicht definiert ist, wird stattdessen die [`pageURL`](pageurl.md) Variable verwendet.

## Seitenname beim Start der Adobe Experience Platform

Sie können den Seitennamen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Page name] section.

Sie können den Seitennamen auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.pageName in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.pageName` Variable ist eine Zeichenfolge, die normalerweise den Namen der Seite enthält. Er hat einen Maximalwert von 100 Byte. längere Werte werden abgeschnitten. Diese Kürzung umfasst Instanzen, in denen die Variable zurückfällt, `pageURL` wenn sie leer ist.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
