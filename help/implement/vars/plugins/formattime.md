---
title: formatTime
description: Konvertieren Sie eine Anzahl von Sekunden in das Äquivalent in Minuten, Stunden usw.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-Plug-in: formatTime

>[!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `formatTime`-Plug-in können Sie eine beliebige Anzahl von Sekunden in einem Zusammenfassungsformat darstellen, gerundet auf einen gewünschten Benchmark-Wert. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie einen Zeitwert in Sekunden in ein Zusammenfassungsformat (z. B. Minuten, Tage oder Wochen) konvertieren möchten. Dieses Plug-in ist nicht erforderlich, wenn Sie die sekundenbasierten Werte nicht in ein zeitgerundetes Format umwandeln wollen.

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
   * Aktionstyp: formatTime initialisieren
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
/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `formatTime`-Methode verwendet die folgenden Argumente:

* **`ns`** (erforderlich, Ganzzahl): Die Anzahl der Sekunden, die konvertiert oder formatiert werden sollen
* **`tf`** (optional, Zeichenfolge): Der Formattyp, in dem die Sekunden zurückgegeben werden; standardmäßig auf Sekunden gesetzt
   * Legen Sie diese Einstellung auf `"d"` fest, wenn Sie die Zeit in Tagen wünschen (standardmäßig auf den nächsten 1/4-Tage-Benchmark gerundet)
   * Legen Sie diese Einstellung auf `"h"` fest, wenn Sie die Zeit in Stunden wünschen (standardmäßig auf den nächsten 1/4-Stunden-Benchmark gerundet)
   * Legen Sie diese Einstellung auf `"m"` fest, wenn Sie die Zeit in Minuten wünschen (standardmäßig auf den nächsten 1/2-Minuten-Benchmark gerundet)
   * Legen Sie diese Einstellung auf `"s"` fest, wenn Sie die Zeit in Sekunden wünschen (standardmäßig auf den nächsten 5-Sekunden-Benchmark gerundet)
* **`bml`** (optional, Zahl): Die Länge der Rundungs-Benchmarks. Standardmäßig auf die im `tf`-Argument aufgeführten Benchmarks gesetzt

Die Methode gibt die Anzahl der Sekunden zurück, die mit der im `tf`-Argument angegebenen Einheit formatiert wurden. Wenn das `tf`-Argument nicht festgelegt ist:

* Alles unter einer Minute wird auf den nächstliegenden 5-Sekunden-Benchmark gerundet
* Alles zwischen einer Minute und einer Stunde wird auf den nächsten 1/2-Minuten-Benchmark gerundet
* Alles zwischen einer Stunde und einem wird auf den nächsten viertelstündigen Benchmark gerundet
* Alles, was länger als ein Tag ist, wird auf den nächsten Tages-Benchmark gerundet

## Beispiele

### Beispiel 1

Der folgende Code ...

```js
s.eVar1 = s.formatTime(38242);
```

... setzt s.eVar1 auf „10,5 Stunden“

Das übergebene Argument - 38242 Sekunden - entspricht 10 Stunden, 37 Minuten und 22 Sekunden.  Da das tf-Argument in diesem Aufruf nicht festgelegt ist und die Anzahl der Sekunden, die übergeben werden, zwischen einer Stunde und einem Tag liegt, gibt das Plug-in die Anzahl der Sekunden zurück, die auf den nächsten viertelstündigen Benchmark umgewandelt wurde.

### Beispiel 2

Der folgende Code ...

```js
s.eVar1 = s.formatTime(38250);
```

... setzt s.eVar1 auf „10,75 Stunden“
Das übergebene Argument - 38250 Sekunden - entspricht 10 Stunden, 37 Minuten und 30 Sekunden.  Durch das Runden der Anzahl der übergebenen Sekunden auf den nächsten viertelstündigen Benchmark wird in diesem Fall der Endwert auf 10,75 Stunden festgelegt

### Beispiel 3

Der folgende Code ...

```js
s.eVar1 = s.formatTime(38242, "m");
```

... setzt s.eVar1 auf „637,5 Minuten“

In diesem Fall zwingt das „m“-Argument das Plug-in, die Sekunden in den nächsten ½-Minuten-Benchmark umzurechnen

### Beispiel 4

Der folgende Code ...

```js
s.eVar1 = s.formatTime(38242, "m", 20);
```

... setzt s.eVar1 auf „640 Minuten“

Der tf-Argumentwert („m“) zwingt das Plug-in, die Sekunden in Minuten umzurechnen, aber der bml-Argumentwert (20) zwingt das Plug-in auch, die Minutenumrechnung auf den nächsten 20-Minuten-Benchmark zu runden.

### Beispiel 5

Der folgende Code ...

```js
s.eVar1 = s.formatTime(125, "s", 2);
```

... setzt s.eVar1 auf „126 Sekunden“, was dem nächstgelegenen 2-Sekunden-Benchmark von 125 Sekunden entspricht

### Beispiel 6

Der folgende Code ...

```js
s.eVar1 = s.formatTime(125, "m", 3);
```

... setzt s.eVar1 auf „3 Minuten“, was dem nächstgelegenen 3-Minuten-Benchmark von 125 Sekunden entspricht

### Beispiel 7

Der folgende Code ...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

... setzt s.eVar1 auf „2,4 Minuten“, was dem nächstgelegenen 2/5-Sekunden-Benchmark (z. B. 0.4 = 2/5) von 145 Sekunden entspricht

## Versionsverlauf

### 1.1 (21. Mai 2018)

* Das `bml`-Argument wurde hinzugefügt, um eine flexiblere Rundung zu ermöglichen

### 1.0 (15. April 2018)

* Erste Version.
