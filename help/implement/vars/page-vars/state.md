---
title: Land
description: Füllen Sie den Bericht "Besucherstatus"in Reports & Analysen aus.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# state

> [!IMPORTANT] Diese Variable wird eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Verwenden Sie stattdessen die Dimension &quot;US-Bundesstaaten&quot;, die AppMeasurement automatisch basierend auf dem Standort des Besuchers erfasst.

In früheren Versionen von Adobe Analytics wurde die `state` Variable verwendet, wenn Besucher Versandinformationen auf Einzelhandels-Sites ausfüllten. Es ist funktionell identisch mit einer Prop, aber nicht in Analysis Workspace verfügbar.

## Status beim Starten der Adobe Experience Platform

Sie können den Status entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Status] .

Sie können den Status auf einen beliebigen Zeichenfolgenwert oder ein Datenelement festlegen.

## s.state in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.state` Variable ist eine Zeichenfolge, die normalerweise das Bundesland oder den Bundesstaat des Besuchers enthält. Vollständige Statusnamen oder Zweibuchstaben-Codes sind gültig. Er hat einen Maximalwert von 50 Byte. längere Werte werden abgeschnitten. Der Standardwert ist eine leere Zeichenfolge.

```js
s.state = "Utah";
```
