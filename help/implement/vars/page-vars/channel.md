---
title: channel
description: Füllen Sie die Dimension „Website-Bereiche“.
feature: Variables
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 76%

---

# channel

Die `channel`-Variable speichert normalerweise den Abschnitt der Website, auf dem sich eine bestimmte Seite befindet. Es ist hilfreich, zu bestimmen, welche Gruppen Ihrer Website am beliebtesten sind. Diese Variable füllt die Dimension „Website-Bereiche“.

## Kanal mit dem Web SDK

Der Kanal ist [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) unter dem XDM-Feld `web.webPageDetails.siteSection`.

## Kanal mit der Adobe Analytics-Erweiterung

Sie können „channel“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Kanal].

Sie können „channel“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.channel in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.channel`-Variable ist eine Zeichenfolge, die normalerweise den Website-Bereich der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten.

```js
s.channel = "Example site section";
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.channel = digitalData.page.category.primaryCategory;
```
