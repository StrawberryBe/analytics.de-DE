---
title: state
description: Füllen Sie den Bericht „Bundesstaat des Besuchers“ in Reports and Analytics.
feature: Variables
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 93%

---

# state

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Verwenden Sie stattdessen die Dimension „US-Bundesstaaten“, die AppMeasurement automatisch basierend auf dem Standort des Besuchers erfasst.

In früheren Versionen von Adobe Analytics wurde die `state`-Variable verwendet, wenn Besucher Versandinformationen auf Retail-Websites ausfüllten. Sie ist funktionell mit einer Prop identisch, aber nicht in Analysis Workspace verfügbar.

## Status bei Verwendung der Adobe Analytics-Erweiterung

Sie können den Status entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Bundesstaat].

Sie können „state“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.state in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.state`-Variable ist eine Zeichenfolge, die normalerweise das Bundesland oder den Bundesstaat des Besuchers enthält. Vollständige Namen oder Zweibuchstaben-Codes der Bundesstaaten sind gültig. Sie hat einen Maximalwert von 50 Byte. Längere Werte werden abgeschnitten. Der Standardwert ist eine leere Zeichenfolge.

```js
s.state = "Utah";
```
