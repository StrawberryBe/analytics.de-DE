---
title: trackingServer
description: Stellen Sie fest, an welcher Position Bildanforderungen gesendet werden.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackingServer

Adobe erfasst Daten auf Ihrer Site, indem es eine vom Besucher erstellte Bildanforderung empfängt. Die `trackingServer` Variable bestimmt den Ort, an den eine Bildanforderung gesendet wird. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

> [!IMPORTANT] Wenn Sie diesen Wert ändern, sucht AppMeasurement an einem anderen Ort nach Cookies. Die Anzahl individueller Besucher kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besuchercookies an der neuen Position eingestellt werden.

## Tracking-Server beim Start der Adobe Experience Platform

Tracking Server ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Allgemein] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Allgemein] &quot;, das das Feld &quot; [!UICONTROL Tracking-Server] &quot;enthält.

Wenn dieses Feld leer gelassen wird, wird standardmäßig `[rsid].112.2o7.net`ausgewählt.

## s.trackingServer in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.trackingServer` Variable ist eine Zeichenfolge, die den Speicherort zum Senden von Daten enthält.

> [!TIP] Einige Implementierungen verweisen auf Daten `2o7.net`. Dies ist zwar eine gültige Datenerfassungsdomäne, verwendet aber keine regionale Datenerfassung. Implementierungen mit `2o7.net` einer etwas höheren Reaktionszeit auf Bildanforderungen.

## Den Wert für trackingServer bestimmen

Der Wert dieser Variablen hängt davon ab, ob Sie Erstanbieter-Cookies oder Drittanbieter-Cookies verwenden. Adobe empfiehlt dringend, Erstanbieter-Cookies in Ihrer Implementierung zu verwenden.

### Erstanbieter-Cookies

Wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, ist es wahrscheinlich, dass jemand in Ihrem Unternehmen den Erstanbieter-Cookie-Prozess bereits abgeschlossen hat. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung zunächst konfiguriert, definiert auch die verwendete Domäne und Subdomäne. Beispiel:

```js
s.trackingServer = "data.example.com";
```

Normalerweise sind CNAME-Einträge bereits eingerichtet und verweisen auf `sc.omtrdc.net`. Die Domäne `2o7.net` ist auch ein gültiges CNAME-Ziel, das hauptsächlich in früheren Versionen von Adobe Analytics verwendet wird.

### Drittanbieter-Cookies

> [!TIP] Durch die zunehmende Datenschutzpraxis in modernen Browsern wird die Zuverlässigkeit von Drittanbieter-Cookies eingeschränkt. Adobe empfiehlt, den Arbeitsablauf für Erstanbieter-Cookies zu befolgen.

Wenn Sie eine Drittanbieter-Cookie-Implementierung verwenden, `trackingServer` ist der Wert für eine Subdomäne von `sc.omtrdc.net`. Beispiel:

```js
s.trackingServer = "example.sc.omtrdc.net";
```

Wählen Sie eine Subdomäne, die für Ihr Unternehmen eindeutig ist und die wahrscheinlich nicht von einer anderen Organisation ausgewählt wird, die Adobe Analytics verwendet. Stellen Sie sicher, dass alle Implementierungen in Ihrem Unternehmen denselben Tracking-Server verwenden. Es kann hilfreich sein, diese Informationen in einem [Lösungsdesigndokument](../../prepare/solution-design.md)zu verwalten.
