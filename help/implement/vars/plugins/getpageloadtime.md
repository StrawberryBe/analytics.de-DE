---
title: getPageLoadTime
description: Verfolgen Sie die Ladezeit einer Seite.
translation-type: tm+mt
source-git-commit: b3c5fa41194d74725f48e12a546d8ce1c08b9b7d
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 98%

---


# Adobe-Plug-in: getPageLoadTime

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getPageLoadTime`-Plug-in verwendet das JavaScript-Performance-Objekt, mit dem Sie die Zeit messen können, die eine Seite zum vollständigen Laden benötigt. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie messen möchten, wie lange das Laden von Seiten dauert.

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
   * Aktionstyp: getPageLoadTime initialisieren
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
/* Adobe Consulting Plugin: getPageLoadTime v2.0 with performanceWriteFull, performanceWritePart, performanceCheck, and performanceRead helper functions (Requires AppMeasurement and the p_fo plugin) */
function getPageLoadTime(){function f(){function a(a,b){if(0<=a&&0<=b)return 6E4>a-b&&0<=a-b?parseFloat((a-b)/1E3).toFixed(2):60}var b=performance.timing;0<b.loadEventEnd&&(clearInterval(window.pi),""===window.cookieRead("s_plt")&&(window.cookieWrite("s_plt",a(b.loadEventEnd,b.navigationStart)),window.cookieWrite("s_pltp",window.pageName)));window.ptc=b.loadEventEnd}if(arguments&&"-v"===arguments[0])return{plugin:"getPageLoadTime",version:"2.0"};var c=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof c&&(c.contextData.getPageLoadTime="2.0");window.pageName="undefined"!==typeof c&&c.pageName||"";window.cookieWrite=window.cookieWrite||function(a,b,e){if("string"===typeof a){var c=window.location.hostname,h=window.location.hostname.split(".").length-1;if(c&&!/^[0-9.]+$/.test(c)){h=2<h?h:2;var d=c.lastIndexOf(".");if(0<=d){for(;0<=d&&1<h;)d=c.lastIndexOf(".",d-1),h--;d=0<d?c.substring(d):c}}g=d;b="undefined"!==typeof b?""+b:"";if(e||""===b)if(""===b&&(e=-60),"number"===typeof e){var k=new Date;k.setTime(k.getTime()+6E4*e)}else k=e;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(b)+"; path=/;"+(e?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(a)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,c=b.indexOf(" "+a+"="),f=0>c?c:b.indexOf(";",c);return(a=0>c?"":decodeURIComponent(b.substring(c+2+a.length,0>f?b.length:f)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};"undefined"!==typeof performance&&p_fo("performance")&&((c=performance,c.clearResourceTimings(),""!==window.cookieRead("s_plt")&&(0<c.timing.loadEventEnd&&clearInterval(window.pi),window._pltLoadTime=window.cookieRead("s_plt"),window._pltPreviousPage=window.cookieRead("s_pltp"),window.cookieWrite("s_plt",""),window.cookieWrite("s_pltp","")),0===c.timing.loadEventEnd)?window.pi=setInterval(function(){f()},250):0<c.timing.loadEventEnd&&(window.ptc?window.ptc===c.timing.loadEventEnd&&1===c.getEntries().length&&(window.pwp=setInterval(function(){var a=performance;0<a.getEntries().length&&(window.ppfe===a.getEntries().length?clearInterval(window.pwp):window.ppfe=a.getEntries().length);""===window.cookieRead("s_plt")&&(window.cookieWrite("s_plt",((a.getEntries()[a.getEntries().length-1].responseEnd-a.getEntries()[0].startTime)/1E3).toFixed(2)),window.cookieWrite("s_pltp",window.pageName))},500)):f()))};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPageLoadTime`-Methode verwendet keine Argumente. Wenn diese Methode aufgerufen wird, wird nichts zurückgegeben. Stattdessen werden die folgenden Variablen festgelegt:

* `s._pltPreviousPage`: Die vorherige Seite, damit Sie die Ladezeit mit der vorherigen Seite korrelieren können.
* `s._pltLoadTime`: Die Zeit in Sekunden, die das Laden der vorherigen Seite dauerte.

Das getPageLoadTime-Plug-in erstellt zwei Erstanbieter-Cookies:

* `s_plt`: Die Zeit in Sekunden, die das Laden der vorherigen Seite dauerte. Läuft am Ende der Browser-Sitzung ab.
* `s_pltp` Der Wert der `s.pageName`-Variablen, der in der vorherigen Adobe Analytics-Bildanforderung aufgezeichnet wurde. Läuft am Ende der Browser-Sitzung ab.

## Beispielaufrufe

### Beispiel 1

Das Ausführen des folgenden Codes ...

```js
if(s.pageName) s.getPageLoadTime();
if(s._pltPreviousPage)
{
  s.prop10 = s._pltLoadTime;
  s.prop11 = s._pltPreviousPage
  s.eVar10 = prop11;
  s.events = "event100=" + s._pltLoadTime;
}
```

... geschieht Folgendes:

* Das getPageLoadTime-Plug-in wird ausgeführt, wenn s.pageName gesetzt ist.
* s.prop10 wird auf die Ladezeit der vorherigen Seite gesetzt.
* s.prop11 und s.eVar10 werden auf den Namen der vorherigen Seite gesetzt (wie in s.pageName aufgezeichnet).
* event100 wird gesetzt. Dabei handelt es sich um ein benutzerdefiniertes numerisches Ereignis, das der Ladezeit der vorherigen Seite entspricht.   Wenn Sie in diesem Fall ein benutzerspezifisches Ereignis verwenden, können Sie die Gesamtdauer für alle Seitenladevorgänge der vorherigen Seite (von allen Besuchern/Besuchen) abrufen und somit eine berechnete Metrik verwenden, um die durchschnittliche Seitenladezeit für jede Seite zu ermitteln.

## Versionsverlauf

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (22. Mai 2018)

* Erste Version.
