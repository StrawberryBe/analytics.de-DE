---
title: doPlugins
description: Konfigurieren Sie die Logik kurz bevor ein Treffer kompiliert und an Adobe gesendet wird.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# doPlugins

Die `doPlugins` Variable dient als &quot;letzter Aufruf&quot;, um Werte in Ihrer Implementierung festzulegen. Wenn [`usePlugins`](../config-vars/useplugins.md) diese Option aktiviert ist, wird sie automatisch ausgeführt, unmittelbar bevor Bildanforderungen jeglicher Art kompiliert und an Adobe gesendet werden, darunter:

* Alle Ansichten-([`t()`](t-method.md))
* Alle Link-Verfolgungsaufrufe ([`tl()`](tl-method.md)einschließlich automatischer Download-Links und Exitlinks)

Verwenden Sie die `doPlugins` Variable, um Plug-in-Code aufzurufen und endgültige Variablenwerte festzulegen, bevor eine Bildanforderung kompiliert und an Adobe gesendet wird.

## Plug-ins in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.doPlugins in AppMeasurement und benutzerdefinierter Code starten

Stellen Sie die `s.doPlugins` Variable auf eine Funktion ein, die den gewünschten Code enthält. Die Funktion wird automatisch ausgeführt, wenn Sie einen Verfolgungsaufruf ausführen.

```js
s.doPlugins = function() {/* Desired code */};
```

> [!NOTE] Legen Sie eine Funktion nur einmal in Ihrer Implementierung auf die `doPlugins` Variable fest. Wenn Sie die `doPlugins` Variable mehrmals festlegen, wird nur der neueste Code verwendet.

## Beispiele

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

> [!NOTE] Frühere Versionen von AppMeasurement hatten einen etwas anderen `doPlugins()` Code. Adobe empfiehlt die Verwendung des oben genannten Formats als Best Practice.
