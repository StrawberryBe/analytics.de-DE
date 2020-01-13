---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.cookieDomainPeriods

Die Variable bestimmt, in welcher Domäne die [!DNL Analytics]-Cookies `s_cc` und `s_sq` abgelegt sind, indem sie bestimmt, wie viele Punkte sich in der Domäne der Seiten-URL befinden. Diese Variable wird auch von Plug-ins verwendet, um die richtige Domäne zum Setzen der Plug-in-Cookies zu bestimmen.

Der Standardwert für *`cookieDomainPeriods`* ist „2“. Das ist der Wert, der verwendet wird, wenn *`cookieDomainPeriods`* weggelassen wird. Bei Verwendung der Domäne `www.mysite.com` sollte *`cookieDomainPeriods`* „2“ sein. Für `www.mysite.co.jp` sollte *`cookieDomainPeriods`* „3“ sein.

Wenn *`cookieDomainPeriods`* den Wert „2“ hat, die Domäne jedoch drei Punkte enthält, versucht die JavaScript-Datei, Cookies im Domänensuffix zu setzen.

Wenn Sie beispielsweise *`cookieDomainPeriods`* auf „2“ für die Domäne `www.mysite.co.jp` einstellen, werden die Cookies `s_cc` und `s_sq` für die Domäne `co.jp` erstellt. Da `co.jp` eine ungültige Domäne ist, werden diese Cookies von fast allen Browsern zurückgewiesen. Dadurch gehen Daten zur Zuordnung von Besucherklicks verloren, und im Bericht [!UICONTROL Besucherprofil] &gt; [!UICONTROL Technologie] &gt; [!UICONTROL Cookies] steht dann, dass fast 100 % der Besucher Cookies abgelehnt haben.

Wenn *`cookieDomainPeriods`* auf „3“ eingestellt ist, die Domäne jedoch nur zwei Punkte enthält, setzt die JavaScript-Datei Cookies in der Subdomäne der Site. Wenn Sie beispielsweise *`cookieDomainPeriods`* auf „3“ für die Domäne `www2.mysite.com` einstellen, werden die Cookies `s_cc` und `s_sq`Cookies für die Domäne `www2.mysite.com` erstellt. Wenn ein Besucher in eine andere Subdomäne der Site wechselt (z. B. `www4.mysite.com`), können alle mit `www2.mysite.com` gesetzten Cookies nicht mehr gelesen werden.

> [!NOTE] Fügen Sie keine zusätzlichen Subdomänen als Teil von *`cookieDomainPeriods`* hinzu. Zum Beispiel wäre `store.toys.mysite.com` immer noch *`cookieDomainPeriods`* auf „2“ gesetzt. Bei dieser Variablendefinition werden die Cookies korrekt in der Stammdomäne [!DNL mysite.com] gesetzt. Wenn *`cookieDomainPeriods`* in diesem Beispiel auf „3“ eingestellt wird, würden Cookies in der Domäne [!DNL toys.mysite.com] gesetzt, was die gleichen Folgen wie das Beispiel zuvor hätte.

Siehe auch [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | CDP | Betrifft mehrere Berichte und steuert, wie die Besucherkennung gespeichert und verarbeitet wird. | „2“ |

>[!NOTE]
>
>Einige Cloud-Computing-Dienste gelten als Domänen oberster Ebene, auf denen das Erstellen von Cookies nicht zulässig ist. (Beispiel: `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com` usw.) Bei einer Implementierung mithilfe dieser Dienste können Sie von der Analytics-Datenschutzeinstellung betroffen sein, die Benutzer entfernt, die alle Cookies blockiert haben, wenn Sie keine eigene Domäne eingerichtet haben (z. B. beim Testen Ihrer Implementierung). In diesem Fall wird jeder Treffer, bei dem das System feststellt, dass Cookies deaktiviert, nicht funktionsfähig oder nicht für den Zugriff verfügbar sind, deaktiviert und somit vom Reporting ausgeschlossen.

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

* Wenn Sie feststellen, dass Daten über die Zuordnung von Besucherklicks fehlen oder dass laut dem unter [!UICONTROL Traffic] &gt; [!UICONTROL Technologie] &gt; [!UICONTROL Cookies] verfügbaren Bericht ein großer Prozentsatz von Besuchern Cookies abgelehnt hat, prüfen Sie, ob *`cookieDomainPeriods`* korrekt ist.

* Wenn *`cookieDomainPeriods`* höher als die Anzahl der Abschnitte in der Domäne ist, werden Cookies in der gesamten Domäne gesetzt. Dies kann zu Datenverlusten führen, wenn Besucher zwischen Subdomänen wechseln.
* Die Variable *`cookieDomainPeriods`* wurde bei nicht mehr unterstützten Implementierungen zum Festlegen des Besucher-ID-Cookie vor *`trackingServer`* festgelegt. Obwohl diese Implementierung nur im veralteten Code vorkommt, besteht bei fehlender korrekter Definition von *`cookieDomainPeriods`* in diesem Fall die Gefahr eines Datenverlusts.
