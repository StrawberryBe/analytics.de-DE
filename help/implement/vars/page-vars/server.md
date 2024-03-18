---
title: server
description: Füllen Sie die Dimension „Server“.
feature: Variables
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 74%

---

# server

Die `server`-Variable speichert normalerweise den Hostnamen Ihrer Website. Sie wird häufig in Report Suites verwendet, die Daten aus mehreren Domänen enthalten. Sie ist funktionell mit einer Prop identisch.

## Server mit dem Web SDK

Der Server ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.server`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.server`

## Server, der die Adobe Analytics-Erweiterung verwendet

Sie können „server“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Server].

Sie können „server“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.server in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.server`-Variable ist eine Zeichenfolge, die normalerweise den Hostnamen Ihrer Website enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
