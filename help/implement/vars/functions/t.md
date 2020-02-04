---
title: t
description: Senden Sie einen Seitenansichtsverfolgungsaufruf an Adobe.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# t

Die `t` Methode ist eine wichtige Kernkomponente von Adobe Analytics. Es nimmt alle auf der Seite definierten Analytics-Variablen auf, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungsserver.

Betrachten Sie beispielsweise den folgenden JavaScript-Code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension value";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Die Ausführung der `t` Methode nimmt alle Analytics-Variablen in Anspruch und formuliert eine URL, die auf diesen Variablen basiert. Einige Analytics-Variablen bestimmen die URL des Bildes, während andere Variablen die Parameterwerte der Abfragezeichenfolge bestimmen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe empfängt die Bildanforderung und analysiert dann die Parameter für Anforderungsheader, URL und Abfragezeichenfolge. Datenerfassungsserver geben dann ein transparentes 1x1-Pixel-Bild zurück, das unsichtbar auf Ihrer Site angezeigt wird.

## Seitenansichtsverfolgung beim Start der Adobe Experience Platform

&quot;Launch&quot;hat einen eigenen Standort, der einen Seitenansichtsverfolgungsaufruf einstellt.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter &quot; [!UICONTROL Aktionen]&quot;auf das Symbol &quot;+&quot;
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Beacon senden fest.
6. Click the `s.t()` radio button.

## s.t()-Methode in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Rufen Sie die `s.t()` Methode auf, wenn Sie einen Verfolgungsaufruf an Adobe senden möchten.

```js
s.t();
```

Optional können Sie ein Objekt als Argument verwenden, um Variablenwerte zu überschreiben. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md) .

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

> [!NOTE] In früheren Versionen von AppMeasurement wurden mehrere Codezeilen verwendet, um diese Funktion aufzurufen. Der zusätzliche Code wurde historisch für verschiedene Browser angepasst. Die Standardisierung und Best Practices in modernen Browsern erfordern diesen Codeblock nicht mehr. Jetzt `s.t()` ist nur der Methodenaufruf erforderlich.
