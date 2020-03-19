---
title: t
description: Senden Sie einen Verfolgungsaufruf für die Ansicht einer Seite an Adobe.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# t() 

Die `t()` Methode ist eine wichtige Kernkomponente von Adobe Analytics. Es nimmt alle auf der Seite definierten Analytics-Variablen auf, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungsserver.

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

Die Ausführung der `t()` Methode nimmt alle Analytics-Variablen in Anspruch und formuliert eine URL, die auf diesen Variablen basiert. Einige Analytics-Variablen bestimmen die URL des Bilds, während andere Abfragen Parameterwerte für die Zeichenfolge festlegen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe empfängt die Bildanforderung und analysiert dann die Parameter für den Anforderungsheader, die URL und die Abfrage. Datenerfassungsserver geben dann ein transparentes 1x1-Pixel-Bild zurück, das unsichtbar auf Ihrer Site angezeigt wird.

## Seitenverfolgungsaufruf bei der Ansicht in Adobe Experience Platform Launch

&quot;Launch&quot;verfügt über einen eigenen Standort, der einen Seitenverfolgungsaufruf für die Ansicht festlegt.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Actions]dem Symbol &quot;+&quot;auf
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und das [!UICONTROL Action Type] auf Beacon senden fest.
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
