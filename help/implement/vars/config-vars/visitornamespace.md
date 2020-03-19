---
title: visitorNameSpace
description: Variable, die die Cookie-Domäne bestimmt hat, wurde entfernt.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# visitorNamespace

> [!IMPORTANT] Diese Variable wird eingestellt. Verwenden Sie [`trackingServer`](trackingserver.md) stattdessen.

In früheren Versionen von Adobe Analytics verwendete AppMeasurement die `visitorNameSpace` Variable, um die Subdomäne zu ermitteln, in der die Besucher-Cookies gespeichert werden `2o7.net` . Durch die zunehmende Datenschutzpraxis in modernen Browsern wird die Zuverlässigkeit von Drittanbieter-Cookies eingeschränkt. Mit der Einführung der `trackingServer` und [`trackingServerSecure`](trackingserversecure.md) Variablen, ist nicht mehr erforderlich `visitorNameSpace` .

> [!TIP] Adobe empfiehlt die Verwendung von Erstanbieter-Cookies auf Ihrer Site. Erstanbieter-Cookies verwenden diese Variable nicht.

## Besucher Namensraum beim Starten der Adobe Experience Platform

[!UICONTROL Visitor Namespace] ist ein Feld unter dem [!UICONTROL Cookies] Akkordeon, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Cookies] Akkordeon, das das [!UICONTROL Visitor Namespace] Feld aufdeckt.

Adobe empfiehlt, dieses Feld nicht zu verwenden. Verwenden Sie `trackingServer` und `trackingServerSecure` stattdessen.

## s.visitorNamespace in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.visitorNamespace` Variable ist eine Zeichenfolge, die einen eindeutigen Wert pro Organisation enthält. Alte AppMeasurement-Bibliotheken enthielten diesen eindeutigen Wert automatisch, wenn sie von früheren Versionen von Adobe Analytics heruntergeladen wurden. Die aktuellen AppMeasurement-Bibliotheken verwenden diese Variable nur, wenn sie eingestellt sind `trackingServer` und nicht eingestellt `trackingServerSecure` sind.

Wenn Ihre Organisation diese Variable noch benötigt, wählen Sie einen Wert aus, der für Ihr Unternehmen steht. Sie können diesen Wert in einem [Lösungsdesign-Dokument](../../prepare/solution-design.md)speichern.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
