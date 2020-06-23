---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domäne Cookies speichern soll, wenn Ihre Domäne einen Punkt im Suffix hat.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# fpCookieDomainPeriods

Mithilfe der `fpCookieDomainPeriods`-Variablen kann AppMeasurement ermitteln, wo Analytics-Cookies gesetzt werden, indem darauf hingewiesen wird, dass das Domänensuffix einen zusätzlichen Punkt enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Punkt im Domänensuffix zu berücksichtigen und Cookies an der richtigen Stelle zu setzen. Sie erbt den Wert von [`cookieDomainPeriods`](cookiedomainperiods.md), ist jedoch nach wie vor eine Best Practice, wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden.

* Bei Domänen wie `example.com` oder `www.example.com` muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"` setzen.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.

>[!IMPORTANT] Berücksichtigen Sie für diese Variable keine Unterdomänen. Legen Sie beispielsweise nicht `fpCookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt standardmäßig, dass Cookies auf `example.com` gespeichert werden sollen. Das gilt auch für URLs mit vielen Unterdomänen.

## Erstanbieter-Domänenpunkte in Adobe Experience Platform Launch

„Erstanbieter-Domänenpunkte“ ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Erstanbieter-Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur bei Domänen, die einen Punkt im Suffix enthalten, auf `3`. Andernfalls kann dieses Feld leer gelassen werden.

## s.fpCookieDomainPeriods in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die Variable `fpCookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"` gesetzt wird, und zwar nur bei Domänen, die einen Punkt in ihrem Suffix enthalten. Der Standardwert ist `"2"`, der für die meisten Domänen geeignet ist.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
