---
title: kanal
description: Füllen Sie die Dimension "Sitebereiche".
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# kanal

Die `channel` Variable speichert normalerweise den Abschnitt der Site, auf dem sich eine bestimmte Seite befindet. Es ist hilfreich festzustellen, welche Gruppen Ihrer Site bevorzugt werden. Diese Variable füllt die Dimension &quot;Sitebereiche&quot;.

## Kanal in Adobe Experience Platform Launch

Sie können den Kanal entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Kanal] .

Sie können channel auf einen beliebigen Zeichenfolgenwert oder Datenelement einstellen.

## s.channel in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `s.channel` Variable ist eine Zeichenfolge, die normalerweise den Site-Abschnitt der Seite enthält. Er hat einen Maximalwert von 100 Byte. längere Werte werden abgeschnitten.

```js
s.channel = "Example site section";
```
