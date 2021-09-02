---
title: channel
description: Füllen Sie die Dimension „Website-Bereiche“.
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# channel

Die `channel`-Variable speichert normalerweise den Abschnitt der Website, auf dem sich eine bestimmte Seite befindet. Es ist hilfreich, zu bestimmen, welche Gruppen Ihrer Website am beliebtesten sind. Diese Variable füllt die Dimension „Website-Bereiche“.

## Kanal bei Verwendung von Tags in Adobe Experience Platform

Sie können „channel“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Kanal].

Sie können „channel“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.channel in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.channel`-Variable ist eine Zeichenfolge, die normalerweise den Website-Bereich der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten.

```js
s.channel = "Example site section";
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.channel = digitalData.page.category.primaryCategory;
```
