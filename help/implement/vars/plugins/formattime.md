---
title: formatTime
description: Konvertieren Sie eine Anzahl von Sekunden in das Äquivalent in Minuten, Stunden usw.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in:formatTime

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `formatTime` Plug-in können Sie eine beliebige Anzahl von Sekunden in Anspruch nehmen und sie in einem Zusammenfassungsformat darstellen, gerundet auf einen gewünschten Referenzwert. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie einen Zeitwert in Sekunden erfassen und ihn in ein Behälterformat (z. B. Minuten, Tage oder Wochen) konvertieren möchten. Dieses Plug-in ist nicht erforderlich, wenn Sie keine zweitbasierten Werte in ein zeitaufgerundetes Format aufnehmen möchten.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Fügen Sie der oben stehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialize formatTime
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
1. Erweitern Sie die [!UICONTROL Verfolgung mithilfe eines benutzerdefinierten Code] -Akkordeons, das die Schaltfläche zum [!UICONTROL Öffnen des Editors] anzeigt.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung `s_gi`). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `formatTime` Methode verwendet die folgenden Argumente:

* **`ns`**(erforderlich, ganze Zahl): Die Anzahl der Sekunden, die konvertiert oder formatiert werden sollen
* **`tf`**(optional, Zeichenfolge): Der Formattyp, in dem die Sekunden zurückgegeben werden; standardmäßig auf Sekunden
   * Legen Sie diese Einstellung auf `"d"` fest, wenn Sie die Zeit in Tagen wünschen (standardmäßig auf die nächste 1/4-Tage-Benchmark gerundet)
   * Legen Sie diese Einstellung auf `"h"` fest, wenn Sie die Zeit in Stunden wünschen (standardmäßig auf den nächsten 1/4-Stunden-Benchmark gerundet)
   * Legen Sie diese Einstellung auf `"m"` fest, wenn Sie die Zeit in Minuten benötigen (standardmäßig auf die nächste 1/2-Minuten-Benchmark gerundet)
   * Auf einstellen, `"s"` wenn Sie die Zeit in Sekunden wünschen (standardmäßig auf den nächsten 5-Sekunden-Referenzwert gerundet)
* **`bml`**(optional, Zahl): Die Länge der Rundungsbenchmarks. Standardeinstellung der im`tf`Argument aufgeführten Benchmarks

Die Methode gibt die Anzahl der Sekunden zurück, die mit der im `tf` Argument angegebenen Einheit formatiert wurden. Wenn das `tf` Argument nicht festgelegt ist:

* Alles, was weniger als eine Minute beträgt, wird auf die nächste 5-Sekunden-Benchmark gerundet.
* Alles zwischen einer Minute und einer Stunde wird auf die nächste 1/2-Minuten-Benchmark gerundet
* Alles, was zwischen einer Stunde und einem Tag liegt, wird auf die nächste viertelstündige Benchmark gerundet
* Alles, was länger als ein Tag ist, wird auf die nächste Benchmark gerundet

## Beispiele

### Beispiel 1

Der folgende Code...

```js
s.eVar1 = s.formatTime(38242);
```

 ...wird s.eVar1 auf &quot;10.5 Stunden&quot;eingestellt

Das übergebene Argument - 38242 Sekunden - entspricht 10 Stunden, 37 Minuten und 22 Sekunden.  Da das tf-Argument in diesem Aufruf nicht festgelegt ist und die Anzahl der Sekunden, die übergeben werden, zwischen einer Stunde und einem Tag liegt, gibt das Plug-In die Anzahl der Sekunden zurück, die in die nächste viertelstündige Benchmark umgewandelt werden.

### Beispiel 2

Der folgende Code...

```js
s.eVar1 = s.formatTime(38250);
```

 ...wird s.eVar1 auf &quot;10,75 Stunden&quot;gesetzt. Das übergebene Argument - 38250 Sekunden - entspricht 10 Stunden, 37 Minuten und 30 Sekunden.  Durch das Runden der Anzahl der Sekunden, die an die nächste viertelstündige Benchmark übergeben werden, wird der Endwert auf 10,75 Stunden festgelegt

### Beispiel 3

Der folgende Code...

```js
s.eVar1 = s.formatTime(38242, "m");
```

 ...wird s.eVar1 auf &quot;637,5 Minuten&quot;eingestellt

In diesem Fall zwingt das &quot;m&quot;-Argument das Plug-In, die Sekunden in die nächste ½-Minuten-Benchmark umzurechnen

### Beispiel 4

Der folgende Code...

```js
s.eVar1 = s.formatTime(38242, "m", 20);
```

 ...wird s.eVar1 auf &quot;640 Minuten&quot;eingestellt

Der tf-Argumentwert (&quot;m&quot;) zwingt das Plug-In, die Sekunden in Minuten umzurechnen, aber der bml-Argumentwert (20) zwingt das Plug-In auch, die Minutenkonvertierung auf die nächste 20-Minuten-Benchmark zu runden.

### Beispiel 5

Der folgende Code...

```js
s.eVar1 = s.formatTime(125, "s", 2);
```

 ...wird s.eVar1 auf &quot;126 Sekunden&quot;gesetzt, was der nächstgelegenen 2-Sekunden-Benchmark auf 125 Sekunden entspricht

### Beispiel 6

Der folgende Code...

```js
s.eVar1 = s.formatTime(125, "m", 3);
```

 ...wird s.eVar1 auf &quot;3 Minuten&quot;gesetzt, was der nächstgelegenen 3-Minuten-Benchmark auf 125 Sekunden entspricht

### Beispiel 7

Der folgende Code...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

 ...wird s.eVar1 auf &quot;2.4 Minuten&quot;gesetzt, was der nächstgelegenen 2/5-Minuten-Benchmark (z.B. .4 = 2/5) bis 145 Sekunden

## Versionsverlauf

### 1.1 (21. Mai 2018)

* Das `bml` Argument wurde hinzugefügt, um eine flexiblere Rundung zu ermöglichen

### 1.0 (15. April 2018)

* Erste Version.
