---
title: getTimeToComplete
description: Messen Sie die Zeit, die zum Ausführen einer Aufgabe benötigt wird.
translation-type: ht
source-git-commit: 37a3a44053260d9cdb2a3797e07f6d34592abc1f
workflow-type: ht
source-wordcount: '762'
ht-degree: 100%

---


# Adobe-Plug-in: getTimeToComplete

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getTimeToComplete`-Plug-in verfolgt die Zeit, die ein Benutzer zum Ausführen eines Prozesses auf einer Website benötigt. Die Zeiterfassung beginnt mit dem Aufruf der `start`-Aktion und endet mit dem Aufruf der `stop`-Aktion. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn es auf der Website einen Workflow gibt, der einige Zeit in Anspruch nimmt, und Sie wissen möchten, wie viel Zeit die Besucher benötigen, um ihn abzuschließen. Es ist nicht erforderlich, dieses Plug-in zu verwenden, wenn der Arbeitsablauf auf Ihrer Website eine kurze Zeitspanne (weniger als 3 Sekunden) in Anspruch nimmt, da die Granularität auf die volle Sekunde begrenzt ist.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getTimeToComplete initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeToComplete v4.0 */
function getTimeToComplete(sos,cn,exp,tp){var f=sos,m=cn,l=exp,e=tp;if("-v"===f)return{plugin:"getTimeToComplete",version:"4.0"};var k=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof k&&(k.contextData.getTimeToComplete="4.0");window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var h="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,h="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,h="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,h="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,h="seconds",d=isNaN(d)?.2:b/d);h=Math.round(c*d/b)/d+" "+h;0===h.indexOf("1 ")&&(h=h.substring(0,h.length-1));return h}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var e=window.location.hostname,h=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){h=2<h?h:2;var f=e.lastIndexOf(".");if(0<=f){for(;0<=f&&1<h;)f=e.lastIndexOf(".",f-1),h--;f=0<f?e.substring(f):e}}g=f;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var k=new Date;k.setTime(k.getTime()+6E4*d)}else k=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""};f=f?f.toLowerCase():"start";if("stop"===f||"start"===f){m=m?m:"s_gttc";e?e="d"===e?864E5:"h"===e?36E5:"s"===e?1E3:6E4:(l=30,e=6E4);l=isNaN(l)?30:l;l*=e;k=cookieRead(m);e=new Date;if("stop"===f&&k)return l=Math.round((e.getTime()-k)/1E3),cookieWrite(m,"",0),formatTime(l);"start"!==f||k?k&&Number(k)<e.getTime()+18E5&&cookieWrite(m,k,30):(f=String(e.getTime()),e.setTime(e.getTime()+l),cookieWrite(m,f,e))}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeToComplete`-Methode verwendet die folgenden Argumente:

* **`sos`** (optional, Zeichenfolge): Stellen Sie `"start"` ein, wenn Sie den Timer starten möchten. Stellen Sie `"stop"` ein, wenn Sie den Timer anhalten möchten. Die Standardeinstellung ist `"start"`.
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, in dem der Startzeit gespeichert werden soll. Die Standardeinstellung ist `"s_gttc"`.
* **`exp`** (optional, Ganzzahl): Die Anzahl der Tage, in denen das Cookie (und der Timer) abläuft. Die Standardeinstellung ist `0`, was das Ende der Browser-Sitzung darstellt.

Beim Aufrufen dieser Methode wird eine Zeichenfolge zurückgegeben, die die Anzahl der Tage, Stunden, Minuten und/oder Sekunden zwischen der `"start"`- und der `"stop"`-Aktion enthält.

## Beispielaufrufe

### Beispiel 1

Verwenden Sie diese Anrufe, um die Zeit zwischen dem Beginn des Checkout-Prozesses und dem Kauf zu bestimmen.

Starten Sie den Timer, wenn der Besucher den Checkout startet:

```js
if(s.events.indexOf("scCheckout") > -1) s.getTimeToComplete("start");
```

Beenden Sie den Timer, wenn der Besucher den Kauf tätigt, und setzen Sie prop1 auf den Zeitunterschied zwischen Stopp und Start:

```js
if(s.events.indexOf("purchase") > -1) s.prop1 = s.getTimeToComplete("stop");
```

s.prop1 erfasst die zum Abschluss des Kaufprozesses benötigte Zeit

### Beispiel 2

Wenn mehrere Timer gleichzeitig ausgeführt werden sollen (um verschiedene Prozesse zu messen), müssen Sie das cn-Cookie-Argument manuell festlegen.  Wenn Sie z. B. die Zeit messen möchten, die für den Abschluss eines Kaufs benötigt wird, würden Sie den folgenden Code festlegen ...

```javascript
if(s.inList(s.events, "scCheckout")) s.getTimeToComplete("start", "gttcpurchase");
if(s.inList(s.events, "purchase")) s.prop1 = s.getTimeToComplete("start", "gttcpurchase");
```

... aber wenn Sie auch (gleichzeitig) die Zeit messen wollten, die für das Ausfüllen eines Anmeldeformulars benötigt wird, würden Sie auch den folgenden Code ausführen:

```js
if(s.inList(s.events, "event1")) s.getTimeToComplete("start", "gttcregister", 7);
if(s.inList(s.events, "event2")) s.prop2 = s.getTimeToComplete("stop", "gttcregister", 7);
```

Im zweiten Beispiel soll event1 den Beginn eines Registrierungsprozesses erfassen, der – aus welchen Gründen auch immer – bis zu 7 Tagen dauern kann, und event2 soll den Abschluss der Registrierung erfassen.  s.prop2 erfasst die zum Abschluss des Registrierungsprozesses benötigte Zeit

## Versionsverlauf

### 4.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 3.1 (30. September 2019)

* Es wurde eine Logik hinzugefügt, die im ersten Argument entweder den Wert „start“ oder „stop“ erfordert.  Alle anderen übergebenen Werte verhindern die Ausführung des Plug-ins.
* `inList 2.0`-Plug-in auf `inList 2.1` aktualisiert.

### 3.0 (23. August 2018)

* `formatTime v1.0`-Plug-in auf `formatTime v1.1` aktualisiert.

### 3.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Geringfügige Fehlerbehebungen.

### 2.0 (21. Juni 2016)

* Die Abhängigkeit vom `p_fo`-Plug-in wurde beseitigt.
* Kompatibilität mit H-Code und AppMeasurement hinzugefügt.
* Konsolenprotokollierung hinzugefügt.
