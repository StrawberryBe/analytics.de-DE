---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domain Cookies speichern soll, wenn Ihre Domain einen Punkt im Suffix hat.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '291'
ht-degree: 100%

---

# cookieDomainPeriods

AppMeasurement ermittelt den Cookie-Speicherort anhand der Domain und des Domänensuffix. Bei Domänen wie `example.com` setzt AppMeasurement Cookies an der richtigen Stelle. Für andere Domänen wie `example.co.uk` kann AppMeasurement jedoch fälschlicherweise Cookies auf `co.uk` setzen. Die meisten Browser lehnen Cookies ab, die in dieser ungültigen Domain eingerichtet wurden, was Probleme mit der Besucheridentifizierung verursacht.

Mithilfe der `cookieDomainPeriods`-Variablen kann AppMeasurement ermitteln, wo Analytics-Cookies gesetzt werden, indem darauf hingewiesen wird, dass das Domänensuffix einen zusätzlichen Punkt enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Punkt im Domänensuffix zu berücksichtigen und Cookies an der richtigen Stelle zu setzen.

* Bei Domänen wie `example.com` oder `www.example.com` muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"` setzen.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.

>[!IMPORTANT]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt standardmäßig, dass Cookies auf `example.com` gespeichert werden sollen. Das gilt auch für URLs mit vielen Unterdomänen.

## Punkte in Domain-Namen bei Verwendung von Tags in Adobe Experience Platform

Domain-Punkte ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur bei Domänen, die einen Punkt im Suffix enthalten, auf `3`. Andernfalls kann dieses Feld leer gelassen werden.

## s.cookieDomainPeriods in AppMeasurement und im benutzerdefinierten Code-Editor

Die Variable `cookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"` gesetzt wird, und zwar nur bei Domänen, die einen Punkt in ihrem Suffix enthalten. Der Standardwert ist `"2"`, der für die meisten Domänen geeignet ist.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
