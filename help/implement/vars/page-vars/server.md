---
title: server
description: Füllen Sie die Dimension „Server“.
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '159'
ht-degree: 100%

---

# server

Die `server`-Variable speichert normalerweise den Hostnamen Ihrer Website. Sie wird häufig in Report Suites verwendet, die Daten aus mehreren Domänen enthalten. Sie ist funktionell mit einer Prop identisch.

## Server in Adobe Experience Platform Launch

Sie können „server“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Server].

Sie können „server“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.server in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.server`-Variable ist eine Zeichenfolge, die normalerweise den Hostnamen Ihrer Website enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
