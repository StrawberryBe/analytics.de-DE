---
title: trackingServer
description: Stellen Sie fest, an welcher Position Bildanforderungen gesendet werden.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '415'
ht-degree: 100%

---


# trackingServer

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServer`-Variable bestimmt die Position, an der eine Bildanforderung gesendet wird. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!IMPORTANT]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Unique Visitor-Anzahl kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## Tracking-Server in Adobe Experience Platform Launch

„Tracking-Server“ ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig `[rsid].112.2o7.net`ausgewählt.

## s.trackingServer in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.trackingServer`-Variable ist eine Zeichenfolge, die die Stelle enthält, an die Daten gesendet werden sollen.

>[!TIP]
>
>Einige Implementierungen senden Daten an `2o7.net`. Dies ist zwar eine gültige Datenerfassungsdomäne, verwendet aber keine regionale Datenerfassung. Implementierungen mit `2o7.net` sehen etwas höhere Antwortzeiten für Bildanforderungen.

## Bestimmen des Werts für „trackingServer“

Der Wert dieser Variablen hängt davon ab, ob Sie Erstanbieter-Cookies oder Drittanbieter-Cookies verwenden. Adobe empfiehlt dringend, Erstanbieter-Cookies in Ihrer Implementierung zu verwenden.

### Erstanbieter-Cookies

Wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, ist es wahrscheinlich, dass jemand in Ihrem Unternehmen den Erstanbieter-Cookie-Prozess bereits abgeschlossen hat. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.html) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domäne und Unterdomäne. Beispiel:

```js
s.trackingServer = "data.example.com";
```

Normalerweise sind CNAME-Einträge bereits eingerichtet und verweisen auf `sc.omtrdc.net`. Die Domäne `2o7.net` ist auch ein gültiges CNAME-Ziel, das hauptsächlich in früheren Versionen von Adobe Analytics verwendet wird.

### Drittanbieter-Cookies

>[!TIP]
>
>Durch die zunehmenden Datenschutzpraktiken in modernen Browsern werden die Cookies von Drittanbietern weniger zuverlässig. Adobe empfiehlt, den Erstanbieter-Cookie-Workflow zu befolgen.

Wenn Sie eine Drittanbieter-Cookie-Implementierung verwenden, ist der Wert für `trackingServer` eine Unterdomäne von `sc.omtrdc.net`. Beispiel:

```js
s.trackingServer = "example.sc.omtrdc.net";
```

Wählen Sie eine für Ihre Organisation eindeutige Unterdomäne aus, die wahrscheinlich nicht von einer anderen Organisation ausgewählt wird, die Adobe Analytics verwendet. Stellen Sie sicher, dass alle Implementierungen in Ihrem Unternehmen denselben Tracking-Server verwenden. Es kann hilfreich sein, diese Informationen in einem [Lösungsdesigndokument](../../prepare/solution-design.md) zu verwalten.

>[!NOTE]
>
>Verwenden Sie keine Subdomänen, die tiefer als `example.sc.omtrdc.net` gehen. Zum Beispiel ist `custom.example.sc.omtrdc.net` kein gültiger Trackingserver.
