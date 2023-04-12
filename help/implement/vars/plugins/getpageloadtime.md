---
title: getPageLoadTime
description: Verfolgen Sie die Ladezeit einer Seite.
feature: Variables
exl-id: 9bf0e26b-f1af-48a6-900a-712f7e588d37
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 88%

---

# Adobe-Plug-in: getPageLoadTime

{{plug-in}}

Das `getPageLoadTime`-Plug-in verwendet das JavaScript-Performance-Objekt, mit dem Sie die Zeit messen können, die eine Seite zum vollständigen Laden benötigt. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie messen möchten, wie lange das Laden von Seiten dauert.

>HINWEIS/WARNUNG: Wenn Sie dieses Plug-in von einer früheren Version aktualisieren, müssen Sie höchstwahrscheinlich auch den Code ändern, der diese Funktion aufruft. Überprüfen Sie Ihre Implementierung und testen Sie sie gründlich, bevor Sie sie in der Produktion bereitstellen.

## Installieren des Plug-ins mit der Web SDK- oder Web SDK-Erweiterung

Dieses Plug-in wird noch nicht für die Verwendung im Web SDK unterstützt.

## Installieren des Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die am häufigsten verwendeten Plug-ins mit Adobe Analytics verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getPageLoadTime initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung &quot;Common Analytics Plugins&quot;nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPageLoadTime v3.0 */
!function(){let e=globalThis.window||this;e.getPageLoadTime=function(t){let i=function(){if(e.s_c_il){for(let t in e.s_c_il)if("s_c"===e.s_c_il[t]._c)return e.s_c_il[t]}}();function n(){var i=performance.timing;i.loadEventEnd>0&&(clearInterval(e.pi),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",function e(t,i){if(t>=0&&i>=0)return t-i<6e4&&t-i>=0?parseFloat((t-i)/1e3).toFixed(2):60}(i.loadEventEnd,i.navigationStart)+","+t)),e.ptc=i.loadEventEnd}if(i&&(i.contextData.getPageLoadTime="3.1"),t=t||i&&i.pageName||document.location.href,e.cookieWrite=e.cookieWrite||function(t,i,n){if("string"==typeof t){if(g=function(){var t=e.location.hostname,i=e.location.hostname.split(".").length-1;if(t&&!/^[0-9.]+$/.test(t)){i=2<i?i:2;var n=t.lastIndexOf(".");if(0<=n){for(;0<=n&&1<i;)n=t.lastIndexOf(".",n-1),i--;n=0<n?t.substring(n):t}}return n}(),i=void 0!==i?""+i:"",n||""===i){if(""===i&&(n=-60),"number"==typeof n){var o=new Date;o.setTime(o.getTime()+6e4*n)}else o=n}return!!t&&(document.cookie=encodeURIComponent(t)+"="+encodeURIComponent(i)+"; path=/;"+(n?" expires="+o.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!=typeof cookieRead)&&cookieRead(t)===i}},e.cookieRead=e.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var t=" "+document.cookie,i=t.indexOf(" "+e+"="),n=0>i?i:t.indexOf(";",i);return(e=0>i?"":decodeURIComponent(t.substring(i+2+e.length,0>n?t.length:n)))?e:""},e.p_fo=e.p_fo||function(t){return e.__fo||(e.__fo={}),!e.__fo[t]&&(e.__fo[t]={},!0)},performance&&e.p_fo("performance")){var o=performance;o.clearResourceTimings(),""!==e.cookieRead("s_plt")&&(o.timing.loadEventEnd>0&&clearInterval(e.pi),this._pltLoadTime=e.cookieRead("s_plt").split(",")[0],this._pltPreviousPage=e.cookieRead("s_plt").split(",")[1],e.cookieWrite("s_plt","")),0===o.timing.loadEventEnd?e.pi=setInterval(function(){n()},250):o.timing.loadEventEnd>0&&(e.ptc?e.ptc===o.timing.loadEventEnd&&1===o.getEntries().length&&(e.pwp=setInterval(function(){var i;(i=performance).getEntries().length>0&&(e.ppfe===i.getEntries().length?clearInterval(e.pwp):e.ppfe=i.getEntries().length),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",((i.getEntries()[i.getEntries().length-1].responseEnd-i.getEntries()[0].startTime)/1e3).toFixed(2)+","+t)},500)):n())}},e.getPageLoadTime.getVersion=function(){return{plugin:"getPageLoadTime",version:"3.0"}}}();
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPercentPageViewed`-Funktion verwendet die folgenden Argumente:

* **`pv`** (optional, Zeichenfolge): Die Dimension, mit der die Seitenladezeit korreliert werden soll. Dieser Wert sollte gleich einem Wert sein, der die Seite selbst identifiziert. Ist er nicht festgelegt, wird für dieses Argument standardmäßig die Variable „pageName“ von Adobe AppMeasurement verwendet (d. h. s.pageName) oder die URL, wenn s.pageName nicht festgelegt ist.

Der Aufruf dieser Funktion gibt nichts zurück. Stattdessen werden die folgenden Variablen festgelegt:

* `window._pltPreviousPage`: Der Wert der vorherigen Seite (d. h., was an das pv-Argument übergeben wurde)
* `window._pltLoadTime`: Die Zeit in Sekunden, die das Laden der vorherigen Seite dauerte.

Das getPageLoadTime-Plug-in erstellt ein First-Party-Cookie:

* `s_plt`: Die Zeit in Sekunden, die das Laden der vorherigen Seite dauerte.  Enthält auch den Wert dessen, was an das pv-Argument übergeben wurde. Läuft am Ende der Browser-Sitzung ab.

## Beispiel

```js
// 1. Run the getPageLoadTime function if the pageName variable is set
// 2. Set prop10 to the load time of the previous page
// 3. Set eVar10 to the name of the previous page
// 4. Set event100 to the load time (in seconds) of the previous page. A numeric event is required to capture this value.
// You can then use event100 in calculated metrics to obtain the average page load time per page.
if(s.pageName) getPageLoadTime();
if(window._pltPreviousPage)
{
  s.prop10 = window._pltLoadTime;
  s.eVar10 = window._pltPreviousPage
  s.events = "event100=" + window._pltLoadTime;
}
```

## Versionsverlauf

### 3.0 (6. Dezember 2022)

* Komplette Neuerstellung des Plug-ins, um es lösungsunabhängig zu machen.  Es ist jetzt beispielsweise mit dem AEP Web SDK kompatibel.
* Erstellt die Variablen `_pltPreviousPage` und `_pltLoadTime` im Fensterobjekt (anstatt im Objekt AppMeasurement s )
* Das Cookie s_pltp ist nicht mehr nötig. Alles wird jetzt im Cookie s_plt gespeichert.
* Enthält die Funktion getVersion, die bei der Fehlerbehebung hilft

### 2.0.1 (26. März 2021)

* Es wurde ein Problem behoben, bei dem das Plug-in Werte für das s-Objekt nicht korrekt setzte.

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (22. Mai 2018)

* Erste Version.
