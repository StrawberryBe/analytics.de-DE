---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domain Cookies speichern soll, wenn Ihre Domain einen Punkt im Suffix hat.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 43%

---


# cookieDomainPeriods

AppMeasurement ermittelt den Cookie-Speicherort anhand der Domain und des Domänensuffix. Bei Domänen wie `example.com` setzt AppMeasurement Cookies an der richtigen Stelle. Für andere Domänen wie `example.co.uk` kann AppMeasurement jedoch fälschlicherweise Cookies auf `co.uk` setzen. Die meisten Browser lehnen Cookies ab, die in dieser ungültigen Domain eingerichtet wurden, was Probleme mit der Besucheridentifizierung verursacht.

Mithilfe der `cookieDomainPeriods`-Variablen kann AppMeasurement ermitteln, wo Analytics-Cookies gesetzt werden, indem darauf hingewiesen wird, dass das Domänensuffix einen zusätzlichen Punkt enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Punkt im Domänensuffix zu berücksichtigen und Cookies an der richtigen Stelle zu setzen.

* Bei Domänen wie `example.com` oder `www.example.com` muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"` setzen.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.


>[!IMPORTANT]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt standardmäßig, dass Cookies auf `example.com` gespeichert werden sollen. Das gilt auch für URLs mit vielen Unterdomänen.


## Cookie-Domänenpunkte, Drittanbieter-Cookies und Legacy-Besucheridentifizierung

Nur wenn Sie die alte Adobe Analytics-Besucheridentifizierung (anstelle des empfohlenen Experience Cloud Identity-Diensts) verwenden, wird die implizite oder explizite Konfiguration von `cookieDomainPeriods` kann sich auf die Identifizierung von Besuchern auswirken, je nachdem, ob Drittanbieter-Cookies blockiert werden oder nicht.

Die folgende Tabelle zeigt vier mögliche Szenarien.

| Szenario | `cookieDomainPeriods` Konfiguration ist ... | Drittanbieter-Cookies werden blockiert? | Ergebnis bei Verwendung des alten Adobe Analytics-Besucheridentifizierungsdienstes |
|:---:|---|---|---|
| 1 | <span style="color:green">Richtig</span> | Nein | Besucher werden mit einer `s_vi` -Cookie, Server-seitig festlegen. |
| 2 | <span style="color:green">Richtig</span> | Ja | Besucher werden mit einem Fallback identifiziert `s_fid` -Cookie, Client-seitig festlegen (Erstanbieterseitendomäne). |
| 3 | <span style="color:red">Falsch</span> | Nein | Besucher werden anhand einer Kombination aus Benutzeragent und IP-Adresse mit einer Ausweich-ID identifiziert. <br/>AppMeasurement ist gezwungen, Cookies als Drittanbieter-Cookies zu setzen.<br/> Die `s_vi` -Cookie wird möglicherweise gesetzt, wenn `cookieDomainPeriods` nicht ordnungsgemäß übertragen wurde. |
| 4 | <span style="color:red">Falsch</span> | Ja | Besucher werden anhand einer Kombination aus Benutzeragent und IP-Adresse mit einer Ausweich-ID identifiziert.<br/>AppMeasurement ist gezwungen, Cookies als Drittanbieter-Cookies zu setzen, die blockiert werden, sodass keine Cookies gesetzt werden. |

>[!CAUTION]
>
>Möglicherweise haben Sie versehentlich konfiguriert `cookieDomainPeriods` <span style="color:red">falsch</span> (wobei der Standardwert `"2"`) bei Verwendung von Domänen wie `example.co.uk`. Diese implizite falsche Konfiguration führt dazu, dass Sie Besucher nach Szenario 3 oder 4 identifizieren.
>
>AppMeasurement-Version 2.26.x oder höher konfiguriert `cookieDomainPeriods` automatisch mit dem richtigen Wert, sodass nur Szenarien 1 oder 2 möglich sind. Wenn Sie ein Update auf AppMeasurement-Version 2.26.x oder höher durchführen, während Sie derzeit Besucher falsch identifizieren (Szenario 3 oder 4), hat das Update erhebliche Auswirkungen.
>
>* Besucher-IDs werden zurückgesetzt und Besucher werden als neue Besucher angezeigt. Es gibt keine Möglichkeit, neue Aktivitäten mit der vorherigen Besucher-ID zu verknüpfen.
>* Cookies werden gesetzt (z. B. für Linktracking oder Activity Map, z. B.`s_sq` -Cookie), was zu plötzlichen Unterschieden in der Berichterstellung führt.
>
>Beim korrekten Konfigurieren `cookieDomainPeriods` verbessert die AppMeasurement- und Analytics-Funktionalität. Es wird empfohlen zu prüfen, ob Sie von den Änderungen betroffen sind, die sich aus der Aktualisierung Ihrer AppMeasurement-Bibliothek ergeben.
>
> Siehe [Cookies in Analytics](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=de) für weitere Informationen zu den von AppMeasurement verwendeten Cookies.

## Cookie-Domänenpunkte mit dem Web SDK

Das Web SDK kann die richtige Cookie-Speicherdomäne ohne diese Variable ermitteln.

## Cookie-Domänenpunkte mit der Adobe Analytics-Erweiterung

Domain-Punkte ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur bei Domänen, die einen Punkt im Suffix enthalten, auf `3`. Andernfalls kann dieses Feld leer gelassen werden.

## Cookie-Domänenpunkte in der Code-AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `cookieDomainPeriods` in der JavaScript-Bibliothek von AppMeasurement oder im Editor für benutzerdefinierten Code der Analytics-Erweiterung.

Die Variable `cookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"` gesetzt wird, und zwar nur bei Domänen, die einen Punkt in ihrem Suffix enthalten. Der Standardwert ist `"2"`, der für die meisten Domänen geeignet ist.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
