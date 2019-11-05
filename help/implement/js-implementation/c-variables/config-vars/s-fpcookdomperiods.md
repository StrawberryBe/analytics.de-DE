---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# s.fpCookieDomainPeriods

Die Variable „“ dient für Cookies, die von JavaScript gesetzt werden (s_sq, s_cc, Plug-ins) und von Erstanbietern stammen, selbst wenn Ihre Implementierung die Domänen 2o7.net oder omtrdc.net von Drittanbietern verwendet.

Die Variable *`fpCookieDomainPeriods`* sollte niemals dynamisch gesetzt werden. Bei Verwendung von *`cookieDomainPeriods`* empfiehlt es sich, auch einen Wert für *`fpCookieDomainPeriods`* anzugeben. *`fpCookieDomainPeriods`* erbt den Wert von *`cookieDomainPeriods`*. Beachten Sie, dass *`fpCookieDomainPeriods`* keine Auswirkungen auf die Domäne hat, in der das Besucher-ID-Cookie gesetzt wird, selbst wenn dieses Cookie in einer Implementierung als Erstanbieter-Cookie behandelt wird.

Der Name „*`fpCookieDomainPeriods`*“ bezieht sich auf die Anzahl der Punkte („.“) in der Domäne, wenn diese mit „www“. beginnt. So enthält zum Beispiel `www.mysite.com` zwei Punkte, während `www.mysite.co.jp` drei Punkte enthält. Eine andere Interpretationsmöglichkeit wäre, dass diese Variable angibt, in wie viele Abschnitte die Hauptdomäne der Site untergliedert ist (zwei bei `mysite.com` und drei bei `mysite.co.jp`).

Die [!DNL AppMeasurement] für JavaScript-Datei verwendet die Variable *`fpCookieDomainPeriods`*, um die Domäne zu bestimmen, mit der Erstanbieter-Cookies außer dem [!UICONTROL Besucher-ID]-Cookie (s_vi) gesetzt werden. There are at least two cookies affected by this variable, including `s_sq` and `s_cc` (used for visitor click map and cookie checking respectively). Außerdem hat es auch Auswirkungen auf Cookies, die von Plug-ins verwendet werden (wie z. B. [!UICONTROL getValOnce]).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | cookieDomainPeriods |

## Codebeispiel für das Festlegen von Cookiedomänenvariablen

```js
s.fpCookieDomainPeriods="2" 
var d=window.location.hostname 
if(d.indexOf('.co.uk')>-1||d.indexOf('.com.au')>-1) 
  s.fpCookieDomainPeriods="3" 
```

## Syntax und mögliche Werte

Bei der Variable *`cookieDomainPeriods`* werden Zeichenfolgen erwartet (siehe unten):

```js
s.fpCookieDomainPeriods="3"
```

## Beispiele

```js
s.fpCookieDomainPeriods="3"
```

```js
s.fpCookieDomainPeriods="2"
```

## Konfigurationseinstellungen

Keine
