---
title: pageName
description: Der Name der Seite auf Ihrer Website.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '226'
ht-degree: 100%

---


# pageName

Die `pageName`-Variable speichert normalerweise den Namen einer bestimmten Seite. Es ist hilfreich, zu bestimmen, welche einzelnen Seiten am beliebtesten sind. Diese Variable füllt die Dimension „Seitenname“.

>[!NOTE]
>
>Diese Dimension wird immer aus Linktracking-Aufrufen entfernt. Wenn Sie den Seitennamen sehen möchten, auf dem ein Link verfolgt wurde, sollten Sie diese Variable in eine eVar kopieren.

Wenn diese Variable bei einem gegebenen Seiten-Tracking-Aufruf nicht definiert ist, wird stattdessen die [`pageURL`](pageurl.md)-Variable verwendet.

## Seitenname in Adobe Experience Platform Launch

Sie können den Seitennamen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Seitenname].

Sie können den Seitennamen auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.pageName in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.pageName`-Variable ist eine Zeichenfolge, die normalerweise den Namen der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten. Diese Kürzung umfasst Fälle, in denen auf `pageURL` zurückgegriffen wird, wenn diese Variable leer ist.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
