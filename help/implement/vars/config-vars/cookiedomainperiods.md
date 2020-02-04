---
title: cookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domäne Cookies gespeichert werden sollen, wenn die Domäne einen Punkt in ihrem Suffix hat.
translation-type: tm+mt
source-git-commit: 04b97e93a95691132680d4da197dc62eb2b9fdd1

---


# cookieDomainPeriods

AppMeasurement bestimmt den Speicherort des Cookies, indem es sich das Suffix &quot;Domäne&quot;und &quot;Domäne&quot;ansieht. Für Domänen wie `example.com`die legt AppMeasurement Cookies am richtigen Ort fest. Für andere Domänen wie `example.co.uk`AppMeasurement kann es jedoch versehentlich passieren, dass Cookies aktiviert werden `co.uk`. Die meisten Browser lehnen Cookies ab, die in dieser ungültigen Domäne eingerichtet wurden, was Probleme mit der Besucheridentifizierung verursacht.

Die `cookieDomainPeriods` Variable hilft AppMeasurement bei der Bestimmung, wo Analytics-Cookies gesetzt werden, indem sie aufruft, dass das Domänensuffix einen zusätzlichen Zeitraum enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Zeitraum im Domänensuffix aufzunehmen und Cookies am richtigen Ort einzustellen.

* Bei Domänen wie `example.com` oder `www.example.com`muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"`.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp`setzen Sie diese Variable auf `"3"`.

> [!IMPORTANT] Unterdomänen für diese Variable nicht berücksichtigen. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL fest `store.toys.example.com`. AppMeasurement erkennt standardmäßig, dass Cookies auch auf URLs mit vielen Subdomänen gespeichert werden `example.com`sollen.

## Domänenzeiträume beim Starten der Adobe Experience Platform

&quot;Domain Periods&quot;ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Cookies] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Cookies] &quot;, das das Feld &quot; [!UICONTROL Domänenzeiträume] &quot;anzeigt.

Stellen Sie dieses Feld `3` nur auf Domänen ein, die einen Punkt in ihrem Suffix enthalten. Andernfalls kann dieses Feld leer gelassen werden.

## s.cookieDomainPeriods in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `cookieDomainPeriods` Variable ist eine Zeichenfolge, die in der Regel nur für Domänen festgelegt ist, die einen Punkt in ihrem Suffix enthalten `"3"`. Der Standardwert ist `"2"`für die meisten Domänen geeignet.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
