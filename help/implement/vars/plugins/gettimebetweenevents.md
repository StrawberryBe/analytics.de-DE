---
title: getTimeBetweenEvents
description: Messen Sie den Zeitraum zwischen zwei Ereignissen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getTimeBetweenEvents

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getTimeBetweenEvents` Plug-in können Sie die Zeitspanne zwischen zwei beliebigen Analytics-Ereignissen, einschließlich Warenkorb- und benutzerspezifischen Ereignissen, verfolgen. Es ist nützlich, wenn Sie verfolgen möchten, wie lange ein Kassengangprozess dauert, oder einen anderen Prozess, bei dem Sie die Zeit messen möchten. Dieses Plug-in ist nicht erforderlich, wenn Sie keine Konvertierungsprozesse haben, mit denen Sie messen möchten, wie lange sie dauern.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe Angebots ist eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Catalog] Schaltfläche
1. Installieren und Veröffentlichen der [!UICONTROL Common Analytics Plugins] Erweiterung
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Hinzufügen Sie eine Aktion mit der folgenden Konfiguration auf die oben stehende Regel:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialize getTimeBetweenEvents
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter der Adobe Analytics-Erweiterung.
1. Erweitern Sie das [!UICONTROL Configure tracking using custom code] Akkordeon, das die [!UICONTROL Open Editor] Schaltfläche einblendet.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

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

## Plug-In verwenden

Die `getTimeBetweenEvents` Methode verwendet die folgenden Argumente:

* **`ste`** (erforderlich, Zeichenfolge): Beginn Timer-Ereignis. Eine kommagetrennte Zeichenfolge aus Analytics-Ereignissen, die als &quot;Beginn des Timers&quot;bezeichnet wird.
* **`rt`** (erforderlich, Boolescher Wert): Option Timer neu starten. Legen Sie diese Einstellung fest, `true` wenn Sie den Timer jedes Mal neu starten möchten, wenn die `events` Variable ein Beginn-Timer-Ereignis enthält. Legen Sie diese Einstellung fest, `false` wenn der Timer nicht neu gestartet werden soll, wenn ein Beginn-Timer-Ereignis angezeigt wird.
* **`stp`** (erforderlich, Zeichenfolge): Stoppen Sie Timer-Ereignis. Eine kommagetrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer stoppt.
* **`res`** (erforderlich, Boolescher Wert): Option Timer zurücksetzen. Legen Sie diese Einstellung fest, `true` wenn Sie die Zeit seit dem Start des Timers aufzeichnen möchten UND setzen Sie den Timer nach dem Beenden zurück. Legen Sie diese Einstellung fest, `false` wenn Sie die Zeit aufzeichnen möchten, den Timer jedoch nicht beenden möchten. Bei Festlegung auf `false`wird der Timer weiter ausgeführt, nachdem die Variable &quot;Ereignisses&quot;ein stop-Ereignis aufgezeichnet hat.
   > [!TIP] Wenn Sie dieses Argument auf `false`setzen, empfiehlt es sich dringend, das unten stehende `rte` Argument festzulegen.
* **`cn`** (optional, Zeichenfolge): Der Cookie-Name, in dem die Uhrzeit des ersten Ereignisses gespeichert wird. Die Standardeinstellung ist `"s_tbe"`.
* **`etd`** (optional, integer): Die Ablaufzeit für das Cookie in Tagen. Mit `0` Ablauf am Ende der Browsersitzung festlegen. Wenn kein Wert festgelegt ist, wird standardmäßig 1 Tag verwendet.
* **`fmt`** (optional, Zeichenfolge): Das Format der Zeit, in der die Anzahl der Sekunden zurückgegeben wird (standardmäßig ohne)
   * `"s"` für Sekunden
   * `"m"` für Minuten
   * `"h"` für Stunden
   * `"d"` für Tage
   * Ist dies nicht der Fall, basiert das Format des Rückgabewerts auf den folgenden Regeln:
      * Alles, was weniger als eine Minute beträgt, wird auf die nächste 5-Sekunden-Benchmark gerundet. Beispiel: 10 Sekunden, 15 Sekunden
      * Alles zwischen einer Minute und einer Stunde wird auf den nächsten 1/2-Minuten-Benchmark gerundet. Beispiel: 30,5 Minuten, 31 Minuten
      * Alles, was zwischen einer Stunde und einem Tag liegt, wird auf den nächstgelegenen Referenzwert der Viertelstunde gerundet. Beispiel: 2,25 Stunden, 3,5 Stunden
      * Alles, was länger als ein Tag ist, wird auf die nächste Benchmark gerundet. Beispiel: 1 Tage, 3 Tage, 9 Tage
* **`bml`** (optional, Zahl): Die Länge des Rundungs-Referenzwerts entsprechend dem Format des `fmt` Arguments. Wenn das `fmt` Argument beispielsweise `"s"` und dieses Argument `2`lautet, wird der Rückgabewert auf den nächsten 2-Sekunden-Referenzwert gerundet. Wenn `fmt` das Argument `"m"` und dieses Argument `0.5`vorliegt, wird der Rückgabewert auf den nächstgelegenen Halbminutenwert gerundet.
* **`rte`** (optional, Zeichenfolge): Kommagetrennte Zeichenfolge aus Analytics-Ereignissen, die den Timer entfernen oder löschen. Die Standardeinstellung ist nichts.

Beim Aufrufen dieser Methode wird eine Ganzzahl zurückgegeben, die die Zeitdauer zwischen dem Beginn-Timer-Ereignis und dem Stopp-Timer-Ereignis im gewünschten Format darstellt.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");
```

...konfiguriert ist, sich wie folgt zu verhalten:

* Der Timer wird Beginn, wenn s.Ereignisses Ereignis1 enthält.
* Der Timer wird jedes Mal neu gestartet, wenn s.Ereignisses Ereignis1 enthält
* Der Timer wird beendet, wenn s.Ereignisses Ereignis2 enthält
* Der Timer wird jedes Mal, wenn s.Ereignisses Ereignis2 enthält, auf 0 Sekunden zurückgesetzt (d.h. auf 0 Sekunden gehen)
* Der Timer wird auch dann zurückgesetzt, wenn s.Ereignisses Ereignis3 enthält ODER wenn der Besucher seinen Browser schließt
* Wenn eine tatsächliche Zeit zwischen Ereignis1 und Ereignis2 aufgezeichnet wird, stellt das Plug-In eVar1 auf die Anzahl der Sekunden zwischen den beiden Ereignissen ein, die auf die nächste 2-Sekunden-Benchmark gerundet werden (z. B. 0 Sekunden, 2 Sekunden, 4 Sekunden, 10 Sekunden, 184 Sekunden usw.).
* Wenn s.Ereignisses Ereignis2 enthält, bevor ein Timer gestartet wurde, wird eVar1 überhaupt nicht eingestellt.

### Beispiel 2

Der folgende Code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");
```

...konfiguriert ist, sich wie folgt zu verhalten:

* Der Timer wird Beginn, wenn s.Ereignisses Ereignis1 enthält.
* Der Timer wird NICHT jedes Mal neu gestartet, wenn s.Ereignisses Ereignis1 enthält. Der ursprüngliche Timer wird weiterhin ausgeführt
* Der Timer wird NICHT angehalten, wenn s.Ereignisses Ereignis2 enthält. Das Plug-In zeichnet jedoch die Zeit seit der Aufzeichnung der ursprünglichen Einstellung Ereignis1 auf
* Der Timer wird in einem Cookie namens &quot;s_20&quot;gespeichert
* Der Timer wird nur zurückgesetzt, wenn s.Ereignisses Ereignis3 enthält ODER wenn 20 Tage seit dem Start des Timers vergangen sind
* Wenn ein Zeitraum zwischen (dem ursprünglichen) Ereignis1 und Ereignis2 aufgezeichnet wird, stellt das Plug-In eVar1 auf die Anzahl der Stunden zwischen den beiden eingestellten Ereignissen ein, gerundet auf den nächsten 1 1/2-Stunden-Benchmark (z. B. 0 Stunden, 1,5 Stunden, 3 Stunden, 7,5 Stunden, 478,5 Stunden usw.)

### Beispiel 3

Der folgende Code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true);
```

...werden ähnliche Ergebnisse wie im ersten Beispiel oben erzielt; Der Wert von eVar1 wird jedoch je nach der endgültigen Länge des Timers in Sekunden, Minuten, Stunden oder Tagen zurückgegeben.  Außerdem läuft der Timer 1 Tag nach der ersten Einstellung ab und nicht, wenn der Besucher seinen Browser schließt.

## Versionsverlauf

### 2.1 (26. Mai 2018)

* Hiermit werden Änderungen an der neuen Version des `formatTime` Plug-Ins unterstützt.

### 2.0 (6. April 2018)

* Umschreiben/Neuanalyse des Plug-Ins
