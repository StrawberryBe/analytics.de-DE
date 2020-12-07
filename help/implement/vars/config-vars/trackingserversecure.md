---
title: trackingServerSecure
description: Stellen Sie fest, an welcher Position auf HTTPS-Seiten Bildanforderungen gesendet werden.
translation-type: tm+mt
source-git-commit: dfe2b09b2ee287219d18099c51b6fbd7c86bab21
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 96%

---


# trackingServerSecure

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServerSecure`-Variable bestimmt die Position, an der eine Bildanforderung über HTTPS gesendet wird. Außerdem wird festgelegt, an welcher Stelle die Cookies von Besuchern gespeichert werden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!IMPORTANT]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Unique Visitor-Anzahl kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## SSL-Tracking-Server in Adobe Experience Platform Launch

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL SSL-Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in der [`trackingServer`](trackingserver.md)-Variablen verwendet.

## s.trackingServerSecure in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.trackingServerSecure`-Variable ist eine Zeichenfolge, die die Stelle enthält, an die Bildanforderungen gesendet werden sollen. Es handelt sich dabei fast immer um eine Unterdomäne Ihrer Website. Moderne Datenschutzpraktiken in Browsern machen Cookies von Drittanbietern häufig unzuverlässig. Wenn diese Variable leer ist, wird der Wert in der `s.trackingServer`-Variablen verwendet.

Der Wert für diese Variable ist fast immer eine Erstanbieter-Domäne, z. B. `data.example.com`. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.html) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domäne und Unterdomäne. Beispiel:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME records usually point to a subdomain on `data.adobedc.net`, `sc.adobedc.net` or `2o7.net`.
