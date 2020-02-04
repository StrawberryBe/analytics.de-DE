---
title: trackingServerSecure
description: Stellen Sie fest, wo Bildanforderungen auf HTTPS-Seiten gesendet werden.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackingServerSecure

Adobe erfasst Daten auf Ihrer Site, indem es eine vom Besucher erstellte Bildanforderung empfängt. Die `trackingServerSecure` Variable bestimmt den Ort, an dem eine Bildanforderung über HTTPS gesendet wird. Außerdem wird festgelegt, an welchem Ort die Cookies von Besuchern gespeichert werden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

> [!IMPORTANT] Wenn Sie diesen Wert ändern, sucht AppMeasurement an einem anderen Ort nach Cookies. Die Anzahl individueller Besucher kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besuchercookies an der neuen Position eingestellt werden.

## SSL-Tracking-Server beim Start der Adobe Experience Platform

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Allgemein] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Allgemein] &quot;, das das Feld &quot; [!UICONTROL SSL-Tracking-Server] &quot;anzeigt.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in der `trackingServer` Variablen verwendet.

## s.trackingServerSecure in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.trackingServerSecure` Variable ist eine Zeichenfolge, die den Speicherort zum Senden von Bildanforderungen enthält. Es ist fast immer eine Subdomäne Ihrer Site. Moderne Datenschutzpraktiken in Browsern machen Drittanbieter-Cookies in der Regel unzuverlässig. Wenn diese Variable leer ist, wird der Wert in der `s.trackingServer` Variablen verwendet.

Der Wert für diese Variable ist fast immer eine Erstanbieterdomäne, z. B. `data.example.com`. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung zunächst konfiguriert, definiert auch die verwendete Domäne und Subdomäne. Beispiel:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-Einträge verweisen normalerweise auf eine Subdomäne auf `ssl.d1.sc.omtrdc.net`.
