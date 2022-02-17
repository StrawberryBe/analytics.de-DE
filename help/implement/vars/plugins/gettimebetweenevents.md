---
title: getTimeBetweenEvents
description: Messen Sie den Zeitraum zwischen zwei Ereignissen.
feature: Variables
exl-id: 15887796-4fe4-4b3a-9a65-a4672c5ecb34
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 100%

---

# Adobe-Plug-in: getTimeBetweenEvents

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getTimeBetweenEvents`-Plug-in können Sie die Zeitspanne zwischen zwei beliebigen Analytics-Ereignissen, einschließlich Warenkorb- und benutzerspezifischen Ereignissen, verfolgen. Es ist nützlich, um die Zeit zu verfolgen, die ein Checkout-Prozess oder ein anderer Prozess, den Sie messen möchten, benötigt. Dieses Plug-in ist nicht erforderlich, wenn Sie keine Konversionsprozesse haben, bei denen Sie messen möchten, wie lange sie dauern.

## Installieren des Plug-ins mithilfe von Tags in Adobe Experience Platform

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getTimeBetweenEvents initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/* Adobe Consulting Plugin: getTimeBetweenEvents v3.0 (AppMeasurement highly recommended) */
function getTimeBetweenEvents(ste,rt,stp,res,cn,etd,fmt,bml,rte){var v=ste,B=rt,x=stp,C=res,k=cn,m=etd,E=fmt,F=bml,p=rte;if("-v"===v)return{plugin:"getTimeBetweenEvents",version:"3.0"};var q=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof q&&(q.contextData.getTimeBetweenEvents="3.0",window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var n=window.location.hostname,f=window.location.hostname.split(".").length-1;if(n&&!/^[0-9.]+$/.test(n)){f=2<f?f:2;var l=n.lastIndexOf(".");if(0<=l){for(;0<=l&&1<f;)l=n.lastIndexOf(".",l-1),f--;l=0<l?n.substring(l):n}}g=l;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}},window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""},window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var f="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,f="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,f="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,f="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,f="seconds",d=isNaN(d)?.2:b/d);f=Math.round(c*d/b)/d+" "+f;0===f.indexOf("1 ")&&(f=f.substring(0,f.length-1));return f}},window.inList=window.inList||function(c,b,d,e){if("string"!==typeof b)return!1;if("string"===typeof c)c=c.split(d||",");else if("object"!==typeof c)return!1;d=0;for(a=c.length;d<a;d++)if(1==e&&b===c[d]||b.toLowerCase()===c[d].toLowerCase())return!0;return!1},"string"===typeof v&&"undefined"!==typeof B&&"string"===typeof x&&"undefined"!==typeof C)){k=k?k:"s_tbe";m=isNaN(m)?1:Number(m);var r=!1,t=!1,y=v.split(","),z=x.split(",");p=p?p.split(","):[];for(var u=window.cookieRead(k),w,D=new Date,A=D.getTime(),h=new Date,e=0;e<p.length;++e)if(window.inList(q.events,p[e])){h.setDate(h.getDate()-1);window.cookieWrite(k,"",h);return}h.setTime(h.getTime()+864E5*m);for(e=0;e<y.length&&!r&&(r=window.inList(q.events,y[e]),!0!==r);++e);for(e=0;e<z.length&&!t&&(t=window.inList(q.events,z[e]),!0!==t);++e);1===y.length&&1===z.length&&v===x&&r&&t?(u&&(w=(A-u)/1E3),window.cookieWrite(k,A,m?h:0)):(!r||1!=B&&u||window.cookieWrite(k,A,m?h:0),t&&u&&(w=(D.getTime()-u)/1E3,!0===C&&(h.setDate(h.getDate()-1),window.cookieWrite(k,"",h))));return w?window.formatTime(w,E,F):""}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeBetweenEvents`-Funktion verwendet die folgenden Argumente:

* **`ste`** (erforderlich, Zeichenfolge): Start-Timer-Ereignisse. Eine durch Komma getrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer starten sollen.
* **`rt`** (erforderlich, boolesch): Option, den Timer erneut zu starten. Setzen Sie das Argument auf `true`, wenn Sie den Timer jedes Mal neu starten möchten, wenn die `events`-Variable ein Start-timer-Ereignis enthält. Setzen Sie das Argument auf `false`, wenn der Timer bei einem Start-Timer-Ereignis nicht neu gestartet werden soll.
* **`stp`** (erforderlich, Zeichenfolge): Stop-Timer-Ereignisse. Eine durch Komma getrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer stoppen sollen.
* **`res`** (erforderlich, boolesch): Option, den Timer zurückzusetzen. Setzen Sie das Argument auf `true`, wenn Sie die Zeit seit dem Start des Timers aufzeichnen UND den Timer nach dem Stoppen zurücksetzen möchten. Setzen Sie das Argument auf `false`, wenn Sie die Zeit aufzeichnen, den Timer jedoch nicht stoppen möchten. Wenn das Argument auf `false` gesetzt ist, läuft der Timer nach der Aufzeichnung eines Stopp-Ereignisses durch die Ereignisvariable weiter.

   >[!TIP]
   >
   >Wenn Sie dieses Argument auf `false` setzen, empfiehlt es sich dringend, das unten stehende `rte`-Argument festzulegen.
* **`cn`** (optional, Zeichenfolge): Der Cookie-Name, in dem die Zeit des ersten Ereignisses gespeichert wird. Die Standardeinstellung ist `"s_tbe"`.
* **`etd`** (optional, Ganzzahl): Die Ablaufzeit für das Cookie in Tagen. Setzen Sie das Argument auf `0`, damit das Cookie am Ende der Browser-Sitzung abläuft. Wenn kein Wert festgelegt ist, wird standardmäßig 1 Tag verwendet.
* **`fmt`** (optional, Zeichenfolge): Das Format der Zeit, in der die Anzahl der Sekunden zurückgegeben wird (standardmäßig leer)
   * `"s"` für Sekunden
   * `"m"` für Minuten
   * `"h"` für Stunden
   * `"d"` für Tage
   * Wenn das Argument nicht gesetzt ist, basiert das Format des Rückgabewerts auf den folgenden Regeln:
      * Alles unter einer Minute wird auf den nächstliegenden 5-Sekunden-Benchmark gerundet. Beispiele: 10 Sekunden, 15 Sekunden
      * Alles zwischen einer Minute und einer Stunde wird auf den nächsten 1/2-Minuten-Benchmark gerundet. Beispiele: 30,5 Minuten, 31 Minuten
      * Alles zwischen einer Stunde und einem wird auf den nächsten viertelstündigen Benchmark gerundet. Beispiel: 2,25 Stunden, 3,5 Stunden
      * Alles, was länger als ein Tag ist, wird auf den nächsten Tages-Benchmark gerundet. Beispiel: 1 Tag, 3 Tage, 9 Tage
* **`bml`** (optional, Zahl): Die Länge des Rundungs-Benchmarks entsprechend dem Format des `fmt`-Arguments. Wenn das `fmt`-Argument beispielsweise `"s"` ist und dieses Argument `2` lautet, wird der Rückgabewert auf den nächsten 2-Sekunden-Benchmark gerundet. Wenn das `fmt`-Argument `"m"` ist und dieses Argument `0.5` lautet, wird der Rückgabewert auf den nächsten Halbminuten-Benchmark gerundet.
* **`rte`** (optional, Zeichenfolge): Durch Komma getrennte Zeichenfolge von Analytics-Ereignissen, die den Timer entfernen oder löschen. Die Standardeinstellung ist leer.

Beim Aufrufen dieser Funktion wird eine Ganzzahl zurückgegeben, die die Zeit zwischen dem Start-Timer-Ereignis und dem Stop-Timer-Ereignis im gewünschten Format darstellt.

## Beispielaufrufe

```js
// The timer starts or restarts when the events variable contains event1
// The timer stops and resets when the events variable contains event2
// The timer resets when the events variable contains event3 or the visitor closes their browser
// Sets eVar1 to the number of seconds between event1 and event2, rounded to the nearest 2-second benchmark
s.eVar1 = getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");

// The timer starts when the events variable contains event1. It does NOT restart with subsequent hits that also contain event1
// The timer records a "lap" when the events variable contains event2. It does not stop the timer.
// The timer resets when the events variable contains event3 or if more than 20 days pass since the timer started
// The timer is stored in a cookie labeled "s_20"
// Sets eVar4 to the number of hours between event1 and event2, rounded to the nearest 90-minute benchmark
s.eVar4 = getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");

// Similar to the above timer in eVar4, except the return value is returned in seconds/minutes/hours/days depending on the timer length.
// The timer expires after 1 day.
s.eVar4 = getTimeBetweenEvents("event1", true, "event2", true);
```

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.1 (26. Mai 2018)

* Unterstützt Änderungen an der neuen Version des `formatTime`-Plug-ins.

### 2.0 (6. April 2018)

* Vollständige Umformulierung/Neuanalyse des Plug-ins.
