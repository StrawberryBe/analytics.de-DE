---
title: rfl
description: Entfernen Sie einen bestimmten Wert aus einer durch Zeichen getrennten Zeichenfolge.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in: rfl (Aus Liste entfernen)

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `rfl` Plug-in können Sie Werte aus getrennten Zeichenfolgen wie `events`, `products`, Listenvariablen und anderen &quot;sicher&quot;entfernen. Dieses Plug-in ist nützlich, wenn Sie bestimmte Werte aus einer mit Trennzeichen versehenen Zeichenfolge entfernen möchten, ohne sich Gedanken über Trennzeichen machen zu müssen. Einige andere Plug-ins hängen von diesem Code ab, um korrekt ausgeführt zu werden. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht gleichzeitig eine bestimmte Funktion für mehrere Analytics-Variablen ausführen müssen oder wenn Sie keine abhängigen Plug-ins verwenden.

Das Plug-In verwendet folgende Logik:

* Wenn der Wert, den Sie entfernen möchten, vorhanden ist, behält das Plug-In alle Elemente in der Variablen mit Ausnahme des zu entfernenden Werts bei.
* Wenn der Wert, den Sie entfernen möchten, nicht vorhanden ist, behält das Plug-In die ursprüngliche Zeichenfolge unverändert bei.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Fügen Sie für jede Startregel, bei der Sie das Plug-In verwenden möchten, eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialisieren von addProductEvar
1. Speichern und veröffentlichen Sie die Änderungen an der Regel

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
/* Adobe Consulting Plugin: rfl (removeFromList) v2.01 */
s.rfl=function(lv,vr,d1,d2,df){if(!lv||!vr)return"";var d=[],b="";d2=d2?d2:d1;df=df?!0:!1;lv=lv.split(d1?d1:",");d1=lv.length;for(var c=0;c<d1;c++)-1<lv[c].indexOf(":")&&(b=lv[c].split(":"),b[1]=b[0]+":"+b[1],lv[c]=b[0]),-1<lv[c].indexOf("=")&&(b=lv[c].split("="), b[1]=b[0]+"="+b[1],lv[c]=b[0]),lv[c]!==vr&&b?d.push(b[1]):lv[c]!==vr?d.push(lv[c]):lv[c]===vr&&df&&(b?d.push(b[1]):d.push(lv[c]),df=!1),b="";return d.join(d2)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `rfl` Methode verwendet die folgenden Argumente:

* **`lv`**(erforderlich, Zeichenfolge): Eine Variable (oder Zeichenfolge), die eine Liste mit getrennten Werten enthält
* **`vr`**(erforderlich, Zeichenfolge): Der Wert, der aus dem`lv`Argument entfernt werden soll. Adobe empfiehlt, während eines einzelnen`rfl`Aufrufs nicht mehrere Werte zu entfernen.
* **`d1`**(optional, Zeichenfolge): Das Trennzeichen, das vom`lv`Argument verwendet wird. Der Standardwert ist Komma (`,`).
* **`d2`**(optional, Zeichenfolge): Das Trennzeichen, das die Rückgabezeichenfolge verwenden soll. Die Standardeinstellung ist derselbe Wert wie das`d1`Argument.
* **`df`**(optional, boolean): Wenn`true`dies der Fall ist, werden anstelle aller Instanzen nur doppelte Instanzen des`vr`Arguments vom`lv`Argument erzwungen. Die Standardeinstellung ist`false`nicht festgelegt.

Der Aufruf dieser Methode gibt eine geänderte Zeichenfolge zurück, die das `lv` Argument enthält, jedoch keine Instanzen (oder doppelten Instanzen) des im `vr` Argument angegebenen Werts.

## Beispielaufrufe

### Beispiel 1

Wenn...

```js
s.events = "event22,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event24");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event25";
```

### Beispiel 2

Wenn...

```js
s.events = "event22,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event26");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event24,event25";
```

In diesem Beispiel hat der rfl-Aufruf keine Änderungen an s.events vorgenommen, da s.events &quot;event26&quot;nicht enthielt

### Beispiel 3

Wenn...

```js
s.events = "event22,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events);
```

 ... Der Endwert von s.events lautet:

```js
s.events = "";
```

Wenn entweder das Argument lv oder vr in einem s.rfl-Aufruf leer sind, gibt das Plug-In nichts zurück

### Beispiel 4

Wenn...

```js
s.prop4 = "hello|people|today";
```

 ...und der folgende Code wird ausgeführt...

```js
s.eVar5 = s.rfl(s.prop4,"people","|");
```

 ... Der Endwert von s.prop4 bleibt...

```js
s.prop4 = "hello|people|today";
```

 ...Der Endwert von s.eVar5 ist jedoch:

```js
s.eVar5 = "hello|today";
```

Beachten Sie, dass das Plug-In nur einen Wert zurückgibt. Es wird die Variable, die über das lv-Argument übergeben wird, nicht &quot;zurückgesetzt&quot;.

### Beispiel 5

Wenn...

```js
s.prop4 = "hello|people|today";
```

 ...und der folgende Code wird ausgeführt...

```js
s.prop4 = s.rfl(s.prop4,"people");
```

 ... Der Endwert von s.prop4 bleibt...

```js
s.prop4 = "hello|people|today";
```

Stellen Sie sicher, dass Sie das d1-Argument festlegen, wenn der Wert des lv-Arguments ein anderes Trennzeichen als der Standardwert (d. h. Komma) enthält.

### Beispiel 6

Wenn...

```js
s.events = "event22,event23,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"EVenT23");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23,event25";
```

Dieses Beispiel ist zwar nicht praktikabel, zeigt aber, wie wichtig es ist, die Groß- und Kleinschreibung zu berücksichtigen.

### Beispiel 7

Wenn...

```js
s.events = "event22,event23:12345,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event25";
```

### Beispiel 8

Wenn...

```js
s.events = "event22,event23:12345,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23:12345");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23:12345,event25";
```

Wenn Sie ein Ereignis entfernen müssen, das eine Serialisierung und/oder numerische/Währungs-Syntax verwendet, sollten Sie im s.rfl-Aufruf nur das Ereignis selbst angeben (d. h. ohne die Werte für Serialisierung/Nummerisch/Währung).

### Beispiel 9

Wenn...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event24,event25");
```

### Beispiel #10

Wenn...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23", "", "",true);
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23,event24,event25");
```

### Beispiel #11

Wenn...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23", "", "|",true);
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22|event23|event24|event25");
```

### Beispiel 12

Wenn...

```js
s.events = "event22,event23,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23,event24");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23,event24,event25";
```

Das Festlegen mehrerer Werte im vr-Argument wird nicht unterstützt. Die rfl-Logik im obigen Beispiel teilte zunächst die Werte im lv-Argument (d.h. s.events) und versuchte dann, jeden getrennten Wert mit dem vollständigen vr-Argumentwert (d.h. &quot;event23,event24&quot;).

### Beispiel 13

Wenn...

```js
s.events = "event22,event23,event24,event25";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.rfl(s.events,"event23");
s.events = s.rfl(s.events,"event24");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event25");
```

Jeder aus der Liste zu entfernende Wert sollte in seinem eigenen s.rfl-Aufruf enthalten sein.

### Beispiel #14

Wenn...

```js
s.linkTrackVars = "events,eVar1,eVar2,eVar3";
```

 ...und der folgende Code wird ausgeführt...

```js
s.linkTrackVars = s.rfl(s.linkTrackVars,"eVar2", ",", ",", false);
```

 ... Der Endwert von s.linkTrackVars lautet:

```js
s.linkTrackVars = "events,eVar1,eVar3";
```

Die letzten drei Argumente (d.h. &quot;,&quot;,&quot;,&quot;,false) am Ende dieses s.rfl-Aufrufs sind nicht erforderlich, aber auch nicht &quot;verletzen irgendetwas&quot;, da sie vorhanden sind, da sie mit den Standardeinstellungen übereinstimmen.

### Beispiel #15

Wenn...

```js
s.events = "event22,event23,event24";
```

 ...und der folgende Code wird ausgeführt...

```js
s.rfl(s.events,"event23");
```

 ... Der Endwert von s.events lautet weiterhin:

```js
s.events = "event22,event23,event24";
```

Beachten Sie erneut, dass das Plug-In nur einen Wert zurückgibt. Es wird die Variable, die über das lv-Argument übergeben wird, nicht &quot;zurückgesetzt&quot;.

## Versionsverlauf

### 2.01 (17. September 2019)

* Geringfügige Fehlerbehebung für den Standardwert des Trennzeichens

### 2.0 (16. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).
* Die Notwendigkeit für das `join` Plug-In wurde entfernt.

### 1.0 (18. Juli 2016)

* Erstes Release.
