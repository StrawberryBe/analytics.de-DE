---
title: getTimeBetweenEvents
description: Messen Sie den Zeitraum zwischen zwei Ereignissen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 100%

---


# Adobe-Plug-in: getTimeBetweenEvents

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getTimeBetweenEvents`-Plug-in können Sie die Zeitspanne zwischen zwei beliebigen Analytics-Ereignissen, einschließlich Warenkorb- und benutzerspezifischen Ereignissen, verfolgen. Es ist nützlich, um die Zeit zu verfolgen, die ein Checkout-Prozess oder ein anderer Prozess, den Sie messen möchten, benötigt. Dieses Plug-in ist nicht erforderlich, wenn Sie keine Konversionsprozesse haben, bei denen Sie messen möchten, wie lange sie dauern.

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
   * Aktionstyp: getTimeBetweenEvents initialisieren
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
/* Adobe Consulting Plugin: getTimeBetweenEvents v2.1 (Requires formatTime and inList plug-ins) */
s.getTimeBetweenEvents=function(ste,rt,stp,res,cn,etd,fmt,bml,rte){var s=this;if("string"===typeof ste&&"undefined"!==typeof rt&&"string"===typeof stp&&"undefined"!==typeof res){cn=cn?cn:"s_tbe";etd=isNaN(etd)?1:Number(etd);var f=!1,g=!1,n=!1, p=ste.split(","),q=stp.split(",");rte=rte?rte.split(","):[];for(var h=s.c_r(cn),k,v=new Date,r=v.getTime(),c=new Date,a=0; a<rte.length;++a)s.inList(s.events,rte[a])&&(n=!0);c.setTime(c.getTime()+864E5*etd);for(a=0;a<p.length&&!f&&(f=s.inList(s.events,p[a]),!0!==f);++a);for(a=0;a<q.length&&!g&&(g=s.inList(s.events,q[a]),!0!==g);++a);1===p.length&&1===q.length&&ste===stp&&f&&g?(h&&(k=(r-h)/1E3),s.c_w(cn,r,etd?c:0)):(!f||1!=rt&&h||s.c_w(cn,r,etd?c:0),g&&h&&(k=(v.getTime()-h)/1E3,!0===res&&(n=!0)));!0===n&&(c.setDate( c.getDate()-1),s.c_w(cn,"",c));return k?s.formatTime(k,fmt,bml):""}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeBetweenEvents`-Methode verwendet die folgenden Argumente:

* **`ste`** (erforderlich, Zeichenfolge): Start-Timer-Ereignisse. Eine durch Komma getrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer starten sollen.
* **`rt`** (erforderlich, boolesch): Option, den Timer erneut zu starten. Setzen Sie das Argument auf `true`, wenn Sie den Timer jedes Mal neu starten möchten, wenn die `events`-Variable ein Start-timer-Ereignis enthält. Setzen Sie das Argument auf `false`, wenn der Timer bei einem Start-Timer-Ereignis nicht neu gestartet werden soll.
* **`stp`** (erforderlich, Zeichenfolge): Stop-Timer-Ereignisse. Eine durch Komma getrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer stoppen sollen.
* **`res`** (erforderlich, boolesch): Option, den Timer zurückzusetzen. Setzen Sie das Argument auf `true`, wenn Sie die Zeit seit dem Start des Timers aufzeichnen UND den Timer nach dem Stoppen zurücksetzen möchten. Setzen Sie das Argument auf `false`, wenn Sie die Zeit aufzeichnen, den Timer jedoch nicht stoppen möchten. Wenn das Argument auf `false` gesetzt ist, läuft der Timer nach der Aufzeichnung eines Stopp-Ereignisses durch die Ereignisvariable weiter.
   > [!TIP] Wenn Sie dieses Argument auf `false` setzen, empfiehlt es sich dringend, das unten stehende `rte`-Argument festzulegen.
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

Beim Aufrufen dieser Methode wird eine Ganzzahl zurückgegeben, die die Zeit zwischen dem Start-Timer-Ereignis und dem Stop-Timer-Ereignis im gewünschten Format darstellt.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");
```

... ist so konfiguriert, dass er sich wie folgt verhält:

* Der Timer startet, wenn s.events event1 enthält
* Der Timer startet jedes Mal erneut, wenn s.events event1 enthält
* Der Timer stoppt, wenn s.events event2 enthält
* Der Timer wird jedes Mal, wenn s.events event2 enthält, zurückgesetzt (d. h. auf 0 Sekunden gehen)
* Der Timer wird auch dann zurückgesetzt, wenn s.events event3 enthält ODER wenn der Besucher seinen Browser schließt
* Wenn eine tatsächliche Zeit zwischen event1 und event2 aufgezeichnet wird, setzt das Plug-in eVar1 auf die Anzahl der Sekunden zwischen den beiden eingestellten Ereignissen, gerundet auf den nächsten 2-Sekunden-Benchmark (z. B. 0 Sekunden, 2 Sekunden, 4 Sekunden, 10 Sekunden, 184 Sekunden usw.)
* Wenn s.events event2 enthält, bevor ein Timer gestartet wurde, wird eVar1 nicht gesetzt.

### Beispiel 2

Der folgende Code ...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");
```

... ist so konfiguriert, dass er sich wie folgt verhält:

* Der Timer startet, wenn s.events event1 enthält
* Der Timer wird NICHT jedes Mal neu gestartet, wenn s.events event1 enthält. Der ursprüngliche Timer wird weiterhin ausgeführt
* Der Timer wird NICHT gestoppt, wenn s.events event2 enthält, aber das Plug-in zeichnet die Zeit auf, seitdem das ursprüngliche Ereignis event1 aufgezeichnet wurde
* Der Timer wird in einem Cookie mit dem Namen „s_20“ gespeichert
* Der Timer wird nur zurückgesetzt, wenn s.events event3 enthält ODER wenn 20 Tage seit dem Start des Timers vergangen sind
* Wenn eine Zeit zwischen (dem ursprünglichen) event1 und event2 aufgezeichnet wird, setzt das Plug-in eVar1 auf die Anzahl der Stunden zwischen den beiden Ereignissen, die auf den nächsten 1,5-Stunden-Benchmark gerundet werden (z. B. 0 Stunden, 1,5 Stunden, 3 Stunden, 7,5 Stunden, 478,5 Stunden usw.).

### Beispiel 3

Der folgende Code ...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true);
```

... erzielt ähnliche Ergebnisse wie im ersten Beispiel oben. Der Wert von eVar1 wird jedoch je nach der endgültigen Länge des Timers in Sekunden, Minuten, Stunden oder Tagen zurückgegeben.  Außerdem läuft der Timer 1 Tag nach der ersten Einstellung ab und nicht, wenn der Besucher seinen Browser schließt.

## Versionsverlauf

### 2.1 (26. Mai 2018)

* Unterstützt Änderungen an der neuen Version des `formatTime`-Plug-ins.

### 2.0 (6. April 2018)

* Vollständige Umformulierung/Neuanalyse des Plug-ins.
