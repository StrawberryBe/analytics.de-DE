---
title: t
description: Senden Sie einen Seitenansichts-Tracking-Aufruf an Adobe.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 100%

---


# t()

Die `t()`-Methode ist eine wichtige Kernkomponente von Adobe Analytics. Sie nimmt alle auf der Seite definierten Analytics-Variablen, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungs-Server.

Betrachten Sie beispielsweise den folgenden JavaScript-Code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension item";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Beim Ausführen der `t()`-Methode werden alle definierten Analytics-Variablen verwendet und eine URL auf der Grundlage dieser Variablen formuliert. Einige Analytics-Variablen bestimmen die URL des Bildes, während andere Variablen die Parameterwerte der Abfragezeichenfolge bestimmen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe empfängt die Bildanforderung und analysiert dann die Parameter für Anforderungsheader, URL und Abfragezeichenfolge. Datenerfassungs-Server geben dann ein transparentes 1x1-Pixel-Bild zurück, das unsichtbar auf Ihrer Website angezeigt wird.

## Seitenansichts-Tracking-Aufruf in Adobe Experience Platform Launch

Launch verfügt über einen speziellen Speicherort, um einen Seitenansichts-Tracking-Aufruf festzulegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie [!UICONTROL Aktionstyp] auf „Beacon senden“.
6. Klicken Sie auf die Optionsschaltfläche `s.t()`.

## s.t()-Methode in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Rufen Sie die `s.t()`-Methode auf, wenn Sie einen Tracking-Aufruf an Adobe senden möchten.

```js
s.t();
```

Optional können Sie ein Objekt als Argument verwenden, um Variablenwerte zu überschreiben. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md).

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In früheren Versionen von AppMeasurement wurden mehrere Code-Zeilen verwendet, um diese Funktion aufzurufen. Der zusätzliche Code enthielt historisch gesehen Workarounds für verschiedene Browser. Die Standardisierung und Best Practices in modernen Browsern erfordern diesen Code-Block nicht mehr. Jetzt wird nur noch der `s.t()`-Methodenaufruf benötigt.
