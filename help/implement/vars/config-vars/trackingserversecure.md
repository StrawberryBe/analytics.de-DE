---
title: trackingServerSecure
description: Stellen Sie fest, an welcher Position auf HTTPS-Seiten Bildanforderungen gesendet werden.
feature: Variables
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 61%

---

# trackingServerSecure

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServerSecure`-Variable bestimmt die Position, an der eine Bildanforderung über HTTPS gesendet wird. Außerdem wird festgelegt, an welcher Stelle die Cookies von Besuchern gespeichert werden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!WARNING]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Zahl der Unique Visitors kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## Edge-Domäne mit der Web SDK-Erweiterung

Das Web SDK verwendet [!UICONTROL Edge-Domäne] zur Verarbeitung von Tracking-Server und Secure Tracking Server. Sie können die gewünschte [!UICONTROL Edge-Domäne] Wert beim Konfigurieren der Web SDK-Erweiterung.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Erweiterungen] und klicken Sie auf die **[!UICONTROL Konfigurieren]** Schaltfläche unter [!UICONTROL Adobe Experience Platform Web SDK].
1. Festlegen der gewünschten **[!UICONTROL Edge-Domäne]** Textfeld.

Siehe [Konfigurieren der Adobe Experience Platform Web SDK-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) in der Web SDK-Dokumentation finden Sie weitere Informationen.

>[!TIP]
>
>Wenn Ihr Unternehmen von einer Implementierung der AppMeasurement- oder Analytics-Erweiterung zum Web SDK wechselt, kann dieses Feld denselben Wert verwenden, der in `trackingServerSecure` (oder `trackingServer`).

## Edge-Domäne, die das Web SDK manuell implementiert

SDK mit konfigurieren [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de). Das Feld ist eine Zeichenfolge, die die Domäne bestimmt, an die Daten gesendet werden sollen.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-Tracking-Server mit der Adobe Analytics-Erweiterung

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL SSL-Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in der [`trackingServer`](trackingserver.md)-Variablen verwendet.

## s.trackingServerSecure in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackingServerSecure`-Variable ist eine Zeichenfolge, die die Stelle enthält, an die Bildanforderungen gesendet werden sollen. Es handelt sich dabei fast immer um eine Unterdomäne Ihrer Website. Moderne Datenschutzpraktiken in Browsern machen Cookies von Drittanbietern häufig unzuverlässig. Wenn diese Variable leer ist, wird der Wert in der `s.trackingServer`-Variablen verwendet.

Der Wert für diese Variable ist fast immer eine Erstanbieter-Domäne, z. B. `data.example.com`. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domain und Unterdomäne. Beispiel:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-Einträge verweisen normalerweise auf eine Subdomain auf `data.adobedc.net`, `sc.adobedc.net` oder `2o7.net`.
