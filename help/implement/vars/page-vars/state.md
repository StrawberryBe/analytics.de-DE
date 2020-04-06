---
title: state
description: Füllen Sie den Bericht „Bundesstaat des Besuchers“ in Reports and Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# state

>[!IMPORTANT] Diese Variable wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Verwenden Sie stattdessen die Dimension „US-Bundesstaaten“, die AppMeasurement automatisch basierend auf dem Standort des Besuchers erfasst.

In früheren Versionen von Adobe Analytics wurde die `state`-Variable verwendet, wenn Besucher Versandinformationen auf Retail-Websites ausfüllten. Sie ist funktionell mit einer Prop identisch, aber nicht in Analysis Workspace verfügbar.

## state in Adobe Experience Platform Launch

Sie können „state“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL State] section.

Sie können „state“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.state in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.state`-Variable ist eine Zeichenfolge, die normalerweise das Bundesland oder den Bundesstaat des Besuchers enthält. Vollständige Namen oder Zweibuchstaben-Codes der Bundesstaaten sind gültig. Sie hat einen Maximalwert von 50 Byte. Längere Werte werden abgeschnitten. Der Standardwert ist eine leere Zeichenfolge.

```js
s.state = "Utah";
```
