---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.fpCookieDomainPeriods

Die Variable „“ dient für Cookies, die von JavaScript gesetzt werden (s_sq, s_cc, Plug-ins) und von Erstanbietern stammen, selbst wenn Ihre Implementierung die Domänen 2o7.net oder omtrdc.net von Drittanbietern verwendet.

The *`fpCookieDomainPeriods`* variable should never be dynamically set . If you use *`cookieDomainPeriods`*, it is good practice to specify a value for *`fpCookieDomainPeriods`* as well. *`fpCookieDomainPeriods`* inherits the *`cookieDomainPeriods`* value. Note that *`fpCookieDomainPeriods`* does not affect the domain on which the visitor ID cookie is set, even if your implementation treats this as a first-party cookie.

The name " *`fpCookieDomainPeriods`*" refers to the number of periods (".") in der Domäne, wenn diese mit „www“. beginnt. For example, `www.mysite.com` contains two periods, while `www.mysite.co.jp` contains three periods. Another way to describe the variable is the number of sections in the main domain of the site (two for `mysite.com` and three for `mysite.co.jp`).

The  for JavaScript file uses the  variable to determine the domain with which to set first-party cookies other than the visitor ID (s_vi) cookie. [!DNL AppMeasurement]*`fpCookieDomainPeriods`* There are at least two cookies affected by this variable, including `s_sq` and `s_cc` (used for visitor click map and cookie checking respectively). Außerdem hat es auch Auswirkungen auf Cookies, die von Plug-ins verwendet werden (wie z. B. [!UICONTROL getValOnce]).

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

Die Variable *`cookieDomainPeriods`*-Variablen werden Zeichenfolgen erwartet (siehe unten):

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

–