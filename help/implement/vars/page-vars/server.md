---
title: server
description: Füllen Sie die Dimension „Server“.
feature: Variables
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 77%

---

# server

Die `server`-Variable speichert normalerweise den Hostnamen Ihrer Website. Sie wird häufig in Report Suites verwendet, die Daten aus mehreren Domänen enthalten. Sie ist funktionell mit einer Prop identisch.

## Server mit dem Web SDK

Server ist [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=de) unter dem XDM-Feld `web.webPageDetails.server`.

## Server, der die Adobe Analytics-Erweiterung verwendet

Sie können „server“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
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
