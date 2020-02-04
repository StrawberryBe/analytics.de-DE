---
title: Kampagne
description: Füllen Sie die Dimension "Rückverfolgungscode".
translation-type: tm+mt
source-git-commit: c5a60bc9756af2742740dbc6a26a081f55ee3235

---


# Kampagne

Die `campaign` Variable dient der Erfassung von Rückverfolgungscodes auf Ihrer Site. In früheren Versionen von Adobe Analytics gab es eine spezielle Behandlung, bei der es als Aufschlüsselung in die meisten Dimensionen verwendet werden konnte. In der aktuellen Version von Adobe Analytics ist es mit einer eVar identisch.

Diese Variable füllt die Dimension &quot;Rückverfolgungscode&quot;.

## Kampagne in Adobe Experience Platform Launch

Sie können die Kampagne entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Kampagne] .

Sie können campaign auf einen Wert oder einen Abfragezeichenfolgenparameter setzen.

## s.campaign in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.campaign` Variable ist eine Zeichenfolge, die normalerweise einen Rückverfolgungscode enthält, der in Marketingbemühungen verwendet wird. Seine maximale Länge beträgt 255 Byte; Werte, die länger als 100 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
