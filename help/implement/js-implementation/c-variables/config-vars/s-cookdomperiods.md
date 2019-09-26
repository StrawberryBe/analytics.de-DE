---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.cookieDomainPeriods

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set by determining the number of periods in the domain of the page URL. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen.

The default value for  is "2". *`cookieDomainPeriods`* This is the value that is used if *`cookieDomainPeriods`* is omitted. For example, using the domain ,  should be "2". `www.mysite.com`*`cookieDomainPeriods`* For ,  should be "3".`www.mysite.co.jp`*`cookieDomainPeriods`*

If *`cookieDomainPeriods`* is set to "2" but the domain contains three periods, the JavaScript file attempts to set cookies on the domain suffix.

For example, if setting  to "2" on the domain , the  and  cookies are created on the domain . *`cookieDomainPeriods`*`www.mysite.co.jp``s_cc``s_sq``co.jp` Da `co.jp` eine ungültige Domäne ist, werden diese Cookies von fast allen Browsern zurückgewiesen. Dadurch gehen Daten zur Zuordnung von Besucherklicks verloren, und im Bericht [!UICONTROL Besucherprofil] &gt; [!UICONTROL Technologie] &gt; [!UICONTROL Cookies] steht dann, dass fast 100 % der Besucher Cookies abgelehnt haben.

Wenn *`cookieDomainPeriods`* auf 3 eingestellt ist, die Domäne jedoch nur zwei Punkte enthält, setzt die JavaScript-Datei Cookies in der Subdomäne der Site. For example, if setting  to "3" on the domain , the  and  cookies are created on the domain . *`cookieDomainPeriods`*`www2.mysite.com``s_cc``s_sq``www2.mysite.com` When a visitor goes to another subdomain of your site (such as `www4.mysite.com`), all cookies set with `www2.mysite.com` cannot be read.

>[!NOTE]
>
>Do not include additional subdomains as part of *`cookieDomainPeriods`*. For example,  would still have  set to "2". `store.toys.mysite.com`*`cookieDomainPeriods`* Bei dieser Variablendefinition werden die Cookies korrekt in der Stammdomäne [!DNL mysite.com] gesetzt. Setting *`cookieDomainPeriods`* to "3" in this example would set cookies on the domain [!DNL toys.mysite.com], which has the same implications as the prior example.

Siehe auch [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | CDP | Betrifft mehrere Berichte und steuert, wie die Besucherkennung gespeichert und verarbeitet wird. | 2 |

>[!NOTE]
>
>Einige Cloud-Computing-Dienste werden als Domänen der obersten Ebene betrachtet, die das Schreiben von Cookies nicht zulassen. (Beispiel: `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com`usw.) Bei einer Implementierung mithilfe dieser Dienste können Sie von der Analytics-Datenschutzeinstellung betroffen sein, die Benutzer entfernt, die alle Cookies blockiert haben, wenn Sie keine eigene Domäne eingerichtet haben (z. B. beim Testen Ihrer Implementierung). In diesem Fall wird jeder Treffer, bei dem das System feststellt, dass Cookies deaktiviert, nicht funktionsfähig oder nicht für den Zugriff verfügbar sind, deaktiviert und somit vom Reporting ausgeschlossen.

## Beispiele

Manuelles Festlegen der Variablen:

```js
s.cookieDomainPeriods = "3";
```

Verschiedene Beispiele zum dynamischen Festlegen der Variablen, wenn eine JavaScript-Hauptdatei beide Typen hostet:

```js
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```

```js
s.cookieDomainPeriods = "2"; 
var d=window.location.hostname; 
if(d.indexOf(".co.uk") > 0 || d.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

```js
s.cookieDomainPeriods = "2"; 
if(window.location.indexOf(".co.jp") > 0 || window.location.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

## Probleme, Fragen und Tipps

* Wenn Sie feststellen, dass Daten über die Zuordnung von Besucherklicks fehlen oder dass laut dem unter [!UICONTROL Datenverkehr] &gt; [!UICONTROL Technologie] &gt; [!UICONTROL Cookies] verfügbaren Bericht ein großer Prozentsatz von Besuchern Cookies abgelehnt hat, prüfen Sie, ob *`cookieDomainPeriods`* korrekt festgelegt ist.

* If *`cookieDomainPeriods`* is higher than the number of sections in the domain, cookies will be set with the full domain. Dies kann zu Datenverlusten führen, wenn Besucher zwischen Subdomänen wechseln.
* Die Variable wurde bei nicht mehr unterstützten Implementierungen verwendet, bevor der Besucher-ID-Cookie festgelegt *`cookieDomainPeriods`* *`trackingServer`* wurde. Obwohl diese Implementierung nur im veralteten Code vorkommt, besteht bei fehlender korrekter Definition *`cookieDomainPeriods`* in diesem Fall die Gefahr eines Datenverlusts.