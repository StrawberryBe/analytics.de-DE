---
title: pageName
description: Der Name der Seite auf Ihrer Website.
exl-id: 24ac40a9-f0e7-4534-abf2-2397f5fe16c2
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '236'
ht-degree: 100%

---

# pageName

Die `pageName`-Variable speichert normalerweise den Namen einer bestimmten Seite. Es ist hilfreich, zu bestimmen, welche einzelnen Seiten am beliebtesten sind. Diese Variable befüllt die Dimension [Seite](/help/components/dimensions/page.md).

Wenn diese Variable bei einem gegebenen Seiten-Tracking-Aufruf nicht definiert ist, wird stattdessen die [`pageURL`](pageurl.md)-Variable verwendet.

>[!NOTE]
>
>Datenerfassungs-Server von Adobe entfernen diese Dimension aus allen [Linktracking](/help/implement/vars/functions/tl-method.md)-Bildanforderungen. Wenn diese Dimension bei Linktracking-Treffern angezeigt werden soll, kopieren Sie sie in eine [eVar](evar.md).

## Seitenname bei Verwendung von Tags in Adobe Experience Platform

Sie können den Seitennamen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Seitenname].

Sie können den Seitennamen auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.pageName in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.pageName`-Variable ist eine Zeichenfolge, die normalerweise den Namen der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten. Diese Kürzung umfasst Fälle, in denen auf `pageURL` zurückgegriffen wird, wenn diese Variable leer ist.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
