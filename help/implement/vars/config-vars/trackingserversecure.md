---
title: trackingServerSecure
description: Stellen Sie fest, an welcher Position auf HTTPS-Seiten Bildanforderungen gesendet werden.
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# trackingServerSecure

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServerSecure`-Variable bestimmt die Position, an der eine Bildanforderung über HTTPS gesendet wird. Außerdem wird festgelegt, an welcher Stelle die Cookies von Besuchern gespeichert werden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!IMPORTANT]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Zahl der Unique Visitors kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## SSL-Tracking-Server bei Verwendung von Tags in Adobe Experience Platform

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL SSL-Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in der [`trackingServer`](trackingserver.md)-Variablen verwendet.

## s.trackingServerSecure in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.trackingServerSecure`-Variable ist eine Zeichenfolge, die die Stelle enthält, an die Bildanforderungen gesendet werden sollen. Es handelt sich dabei fast immer um eine Unterdomäne Ihrer Website. Moderne Datenschutzpraktiken in Browsern machen Cookies von Drittanbietern häufig unzuverlässig. Wenn diese Variable leer ist, wird der Wert in der `s.trackingServer`-Variablen verwendet.

Der Wert für diese Variable ist fast immer eine Erstanbieter-Domäne, z. B. `data.example.com`. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domäne und Unterdomäne. Beispiel:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-Einträge verweisen normalerweise auf eine Subdomain auf `data.adobedc.net`, `sc.adobedc.net` oder `2o7.net`.
