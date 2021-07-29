---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domäne Cookies speichern soll, wenn Ihre Domäne einen Punkt im Suffix hat.
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 92%

---

# cookieDomainPeriods

AppMeasurement ermittelt den Cookie-Speicherort anhand der Domäne und des Domänensuffix. Bei Domänen wie `example.com` setzt AppMeasurement Cookies an der richtigen Stelle. Für andere Domänen wie `example.co.uk` kann AppMeasurement jedoch fälschlicherweise Cookies auf `co.uk` setzen. Die meisten Browser lehnen Cookies ab, die in dieser ungültigen Domäne eingerichtet wurden, was Probleme mit der Besucheridentifizierung verursacht.

Mithilfe der `cookieDomainPeriods`-Variablen kann AppMeasurement ermitteln, wo Analytics-Cookies gesetzt werden, indem darauf hingewiesen wird, dass das Domänensuffix einen zusätzlichen Punkt enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Punkt im Domänensuffix zu berücksichtigen und Cookies an der richtigen Stelle zu setzen.

* Bei Domänen wie `example.com` oder `www.example.com` muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"` setzen.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.

>[!IMPORTANT]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt standardmäßig, dass Cookies auf `example.com` gespeichert werden sollen. Das gilt auch für URLs mit vielen Unterdomänen.

## Domänenpunkte mit Tags in Adobe Experience Platform

Domänenpunkte ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur bei Domänen, die einen Punkt im Suffix enthalten, auf `3`. Andernfalls kann dieses Feld leer gelassen werden.

## s.cookieDomainPeriods in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die Variable `cookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"` gesetzt wird, und zwar nur bei Domänen, die einen Punkt in ihrem Suffix enthalten. Der Standardwert ist `"2"`, der für die meisten Domänen geeignet ist.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
