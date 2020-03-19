---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domäne Cookies gespeichert werden sollen, wenn die Domäne einen Punkt in ihrem Suffix hat.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# fpCookieDomainPeriods

Die `fpCookieDomainPeriods` Variable hilft AppMeasurement bei der Bestimmung, wo Analytics-Cookies gesetzt werden, indem sie aufruft, dass das Domänensuffix einen zusätzlichen Zeitraum enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Zeitraum im Domänensuffix aufzunehmen und Cookies am richtigen Ort einzustellen. Es erbt den Wert von [`cookieDomainPeriods`](cookiedomainperiods.md), ist jedoch nach wie vor eine Best Practice, wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden.

* Bei Domänen wie `example.com` oder `www.example.com`muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"`.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp`setzen Sie diese Variable auf `"3"`.

> [!IMPORTANT] Unterdomänen für diese Variable nicht berücksichtigen. Legen Sie beispielsweise nicht `fpCookieDomainPeriods` für die Beispiel-URL fest `store.toys.example.com`. AppMeasurement erkennt standardmäßig, dass Cookies auch auf URLs mit vielen Subdomänen gespeichert werden `example.com`sollen.

## Erstanbieter-Domänenabschnitte beim Start der Adobe Experience Platform

Bei der Konfiguration der Adobe Analytics-Erweiterung ist &quot;Erstanbieter-Domänenzeiträume&quot;ein Feld unter dem [!UICONTROL Cookies] Akkordeon.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Cookies] Akkordeon, das das [!UICONTROL First-party Domain Periods] Feld aufdeckt.

Stellen Sie dieses Feld `3` nur auf Domänen ein, die einen Punkt in ihrem Suffix enthalten. Andernfalls kann dieses Feld leer gelassen werden.

## s.fpCookieDomainPeriods in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `fpCookieDomainPeriods` Variable ist eine Zeichenfolge, die in der Regel nur für Domänen festgelegt ist, die einen Punkt in ihrem Suffix enthalten `"3"`. Der Standardwert ist `"2"`für die meisten Domänen geeignet.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
