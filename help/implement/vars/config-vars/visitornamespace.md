---
title: visitorNameSpace
description: Variable, die die Cookie-Domäne bestimmt hat, wurde entfernt.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# visitorNamespace

> [!IMPORTANT] Diese Variable wird eingestellt. Verwenden Sie `trackingServer` stattdessen.

In früheren Versionen von Adobe Analytics verwendete AppMeasurement die `visitorNameSpace` Variable zur Bestimmung der Subdomäne, in der `2o7.net` Besuchercookies gespeichert wurden.  Durch die zunehmende Datenschutzpraxis in modernen Browsern wird die Zuverlässigkeit von Drittanbieter-Cookies eingeschränkt. Mit der Einführung der `trackingServer` und `trackingServerSecure` Variablen, ist nicht mehr erforderlich `visitorNameSpace` .

> [!TIP] Adobe empfiehlt die Verwendung von Erstanbieter-Cookies auf Ihrer Site. Erstanbieter-Cookies verwenden diese Variable nicht.

## Besucher-Namespace beim Starten der Adobe Experience Platform

[!UICONTROL Visitor Namespace] ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Cookies] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Cookies] &quot;, das das Feld &quot; [!UICONTROL Besucher-Namespace] &quot;anzeigt.

Adobe empfiehlt, dieses Feld nicht zu verwenden. Verwenden Sie `trackingServer` und `trackingServerSecure` stattdessen.

## s.visitorNamespace in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.visitorNamespace` Variable ist eine Zeichenfolge, die einen eindeutigen Wert pro Organisation enthält. Alte AppMeasurement-Bibliotheken enthielten diesen eindeutigen Wert automatisch, wenn sie von früheren Versionen von Adobe Analytics heruntergeladen wurden. Die aktuellen AppMeasurement-Bibliotheken verwenden diese Variable nur, wenn sie eingestellt sind `trackingServer` und nicht eingestellt `trackingServerSecure` .

Wenn Ihre Organisation diese Variable noch benötigt, wählen Sie einen Wert, der für Ihr Unternehmen steht. Sie können diesen Wert in einem [Lösungsdesigndokument](../../prepare/solution-design.md)speichern.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
