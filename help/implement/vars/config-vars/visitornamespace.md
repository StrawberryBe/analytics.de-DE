---
title: visitorNameSpace
description: Eingestellte Variable, die die Cookie-Domäne bestimmt hatte.
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '217'
ht-degree: 100%

---

# visitorNamespace

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie stattdessen [`trackingServer`](trackingserver.md).

In früheren Versionen von Adobe Analytics verwendete AppMeasurement die `visitorNameSpace`-Variable zur Bestimmung der Unterdomäne von `2o7.net`, in der Besuchercookies gespeichert werden. Durch die zunehmenden Datenschutzpraktiken in modernen Browsern werden die Cookies von Drittanbietern weniger zuverlässig. Mit der Einführung der Variablen `trackingServer` und [`trackingServerSecure`](trackingserversecure.md) wird `visitorNameSpace` nicht mehr benötigt.

>[!TIP]
>
>Adobe empfiehlt die Verwendung von Erstanbieter-Cookies auf Ihrer Website. Erstanbieter-Cookies verwenden diese Variable nicht.

## Besucher-Namespace bei Verwendung von Tags in Adobe Experience Platform

[!UICONTROL Besucher-Namespace] ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Besucher-Namespace] angezeigt wird.

Adobe empfiehlt, dieses Feld nicht zu verwenden. Verwenden Sie stattdessen `trackingServer` und `trackingServerSecure`.

## s.visitorNamespace in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.visitorNamespace`-Variable ist eine Zeichenfolge, die einen eindeutigen Wert pro Organisation enthält. Alte AppMeasurement-Bibliotheken enthielten diesen eindeutigen Wert automatisch, wenn sie von früheren Versionen von Adobe Analytics heruntergeladen wurden. Aktuelle AppMeasurement-Bibliotheken verwenden diese Variable nur, wenn `trackingServer` und `trackingServerSecure` gesetzt sind.

Wenn Ihre Organisation diese Variable noch benötigt, wählen Sie einen Wert, der Ihre Organisation repräsentiert. Sie können diesen Wert in einem [Lösungsdesigndokument](../../prepare/solution-design.md) speichern.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
