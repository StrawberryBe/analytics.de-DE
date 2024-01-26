---
title: usePlugins
description: Aktivieren oder deaktivieren Sie die doPlugins()-Funktion.
feature: Variables
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 34%

---

# usePlugins

Wenn `usePlugins` aktiviert ist, wird die [`doPlugins()`](../functions/doplugins.md)-Funktion kurz vor der AppMeasurement-Kompilierung ausgeführt und ein Treffer an Adobe gesendet. Aktivieren Sie diese Variable, wenn Sie die `doPlugins()`-Funktion verwenden.

## Verwenden Sie die `onBeforeEventSend` Callback mit dem Web SDK

Das Web SDK verfügt zwar nicht über einen booleschen Wert, der die Ausführung zusätzlicher Logik handhabt, bevor Daten an Adobe gesendet werden, können Sie die `onBeforeEventSend` Callback zur Änderung von Daten. Siehe [Globale Änderung von Ereignissen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in der Web SDK-Dokumentation finden Sie weitere Informationen.

## Verwenden von Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung mit der Bezeichnung &quot;Common Analytics Plugins&quot;, mit der Sie die meisten aufrufen können. [Plug-ins](../plugins/impl-plugins.md). Installieren Sie die Erweiterung und rufen Sie das gewünschte Plug-in in einer Regel auf.

Wenn das gewünschte Plug-in nicht in der Adobe-Erweiterung enthalten ist, verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.usePlugins in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.usePlugins`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `doPlugins()`-Funktion aufruft. Der Standardwert lautet `false`. Setzen Sie diese Variable auf `true`, wenn Sie die `doPlugins()`-Funktion in Ihrer Implementierung verwenden.

```js
s.usePlugins = true;
```
