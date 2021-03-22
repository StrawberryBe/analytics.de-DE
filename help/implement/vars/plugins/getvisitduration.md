---
title: getVisitDuration
description: Verfolgen Sie, wie viel Zeit ein Besucher bisher auf der Website verbracht hat.
translation-type: tm+mt
source-git-commit: ca8e563118dcc74dfa718bd203db295faf4e9aa6
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 98%

---


# Adobe-Plug-in: getVisitDuration

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getVisitDuration`-Plug-in verfolgt die Zeit in Minuten, die der Besucher bis zu diesem Zeitpunkt auf der Website verbracht hat. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie die kumulative Zeit auf der Website bis zu diesem Zeitpunkt oder die für die Durchführung einer Aktivität benötigte Zeit verfolgen möchten. Dieses Plug-in verfolgt nicht die Zeitspanne zwischen Ereignissen. Wenn diese Funktion gewünscht wird, verwenden Sie das [`getTimeBetweenEvents`](gettimebetweenevents.md)-Plug-in.

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
   * Aktionstyp: getVisitDuration initialisieren
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
/* Adobe Consulting Plugin: getVisitDuration v2.1 */
function getVisitDuration(){if(arguments&&"-v"===arguments[0])return{plugin:"getVisitDuration",version:"2.1"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof d&&(d.contextData.getVisitDuration="2.1");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};d=(new Date).getTime();var k=cookieRead("s_dur"),a=0;if(isNaN(k)||18E5<d-k)k=d;a=d-k;cookieWrite("s_dur",k+"",30);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute":a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getVisitDuration`-Methode verwendet keine Argumente. Sie gibt einen der folgenden Werte zurück:

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (wobei `[x]` die Anzahl der Minuten ist, die seit der Landung des Besuchers auf der Website vergangen sind)

Dieses Plug-in erzeugt ein Erstanbieter-Cookie mit dem Namen `"s_dur"`, das die Anzahl der Millisekunden angibt, die seit der Landung des Besuchers auf der Website vergangen sind. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
s.eVar10 = s.getVisitDuration();
```

... stellt eVar10 immer auf die Anzahl der Minuten ein, die vergangen sind, seit der Besucher auf der Website gelandet ist.

### Beispiel 2

Der folgende Code ...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

... prüft mithilfe des InList-Plug-ins, ob die Ereignisvariable das Kaufereignis enthält.  Ist dies der Fall, wird eVar10 auf die Anzahl der Minuten zwischen dem Beginn des Besuchs und dem Kaufzeitpunkt des Besuchers eingestellt.

### Beispiel 3

Der folgende Code ...

```js
s.prop10 = s.getVisitDuration();
```

... stellt prop10 immer auf die Anzahl der Minuten ein, die vergangen sind, seit der Besucher auf der Website gelandet ist.  Dies ist nützlich, wenn bei prop10 die Pfadsetzung aktiviert ist.  Wenn Sie die Metrik „Ausstiege“ zum Bericht „prop10“ hinzufügen, wird ein granularer Streudiagramm-Bericht angezeigt, wie lange ein Besuch in Minuten gedauert hat, bevor ein Besucher die Website verlassen hat.

## Versionsverlauf

### 2.1 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.0 (2. Mai 2018)

* Zwischenversion (vollständige Neuanalyse/Umformulierung des Plug-ins).
