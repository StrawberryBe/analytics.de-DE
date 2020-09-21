---
title: campaign
description: Füllen Sie die Dimension „Trackingcode“.
translation-type: ht
source-git-commit: 7220b99268532adb2e425d52744dbc3efb615953
workflow-type: ht
source-wordcount: '191'
ht-degree: 100%

---


# campaign

Die `campaign`-Variable dient der Erfassung von Trackingcodes auf Ihrer Website. In früheren Versionen von Adobe Analytics gab es eine Sonderbehandlung, bei der sie als Aufschlüsselung in die meisten Dimensionen verwendet werden konnte. In der aktuellen Version von Adobe Analytics ist sie mit einer eVar identisch.

Diese Variable füllt die Dimension „Trackingcode“.

## campaign in Adobe Experience Platform Launch

Sie können „campaign“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Kampagne].

Sie können „campaign“ auf einen Wert oder einen Abfragezeichenfolgenparameter setzen.

## s.campaign in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.campaign`-Variable ist eine Zeichenfolge, die normalerweise einen Trackingcode enthält, der in Marketing-Maßnahmen verwendet wird. Die maximale Länge beträgt 255 Byte. Werte, die länger als 255 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
