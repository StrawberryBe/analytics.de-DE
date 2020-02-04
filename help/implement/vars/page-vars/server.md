---
title: server
description: Füllen Sie die Dimension "Server".
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# server

Die `server` Variable speichert normalerweise den Hostnamen Ihrer Site. Es wird häufig in Report Suites verwendet, die Daten aus mehreren Domänen enthalten. Es ist funktionell mit einer Eigenschaftsvariable identisch.

## Server in Adobe Experience Platform Launch

Sie können den Server entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Server] .

Sie können für den Server einen beliebigen Zeichenfolgenwert oder ein Datenelement festlegen.

## s.server in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.server` Variable ist eine Zeichenfolge, die normalerweise den Hostnamen Ihrer Site enthält. Er hat einen Maximalwert von 100 Byte. längere Werte werden abgeschnitten.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
