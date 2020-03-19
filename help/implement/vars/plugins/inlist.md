---
title: inList
description: Überprüfen Sie, ob ein Wert in einem anderen durch Zeichen getrennten Wert enthalten ist.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: inList

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `inList` Plug-in können Sie überprüfen, ob ein Wert bereits in einer durch Trennzeichen getrennten Zeichenfolge oder in einem JavaScript-Array-Objekt vorhanden ist. Einige andere Plug-Ins hängen von dem `inList` Plug-In ab, um zu funktionieren. Dieses Plug-in bietet einen klaren Vorteil gegenüber der JavaScript-Methode, `indexOf()` bei der partielle Zeichenfolgen nicht übereinstimmen. Wenn Sie dieses Plug-In beispielsweise zur Überprüfung verwendet haben, `"event2"`stimmt es nicht mit einer Zeichenfolge überein, die `"event25"`Folgendes enthält. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht nach Werten in getrennten Zeichenfolgen oder Arrays suchen müssen oder wenn Sie Ihre eigene `indexOf()` Logik verwenden möchten.

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
   * Aktionstyp: InList initialisieren
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
/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `inList` Methode verwendet die folgenden Argumente:

* **`lv`** (erforderlich, Zeichenfolge oder Array): Eine durch Trennzeichen getrennte Liste von Werten oder ein zu suchendes JavaScript-Array-Objekt
* **`vtc`** (erforderlich, Zeichenfolge): Der Wert, nach dem gesucht werden soll
* **`d`** (optional, Zeichenfolge): Das Trennzeichen, das zum Trennen einzelner Werte im `lv` Argument verwendet wird. Wenn kein Komma festgelegt ist, wird standardmäßig ein Komma (`,`) verwendet.
* **`cc`** (optional, boolean): Bei Festlegung auf `true`wird die Groß-/Kleinschreibung überprüft. Wenn dies auf &quot; `false` oder nicht angegeben&quot;festgelegt ist, wird die Groß-/Kleinschreibung nicht überprüft. Die Standardeinstellung ist `false`.

Der Aufruf dieser Methode gibt zurück, `true` wenn eine Übereinstimmung gefunden wird und `false` wenn keine Übereinstimmung gefunden wird.

## Beispielaufrufe

### Beispiel 1

Wenn...

```js
s.events="event22,event24";
```

...und der folgende Code wird ausgeführt...

```js
if(s.inList(s.events,"event22"))
```

...Die bedingte if-Anweisung ist &quot;true&quot;

### Beispiel 2

Wenn...

```js
s.events="event22,event24";
```

...und der folgende Code wird ausgeführt...

```js
if(s.inList(s.events,"event2"))
```

...Die bedingte if-Anweisung lautet &quot;false&quot;(falsch), da der InList-Aufruf keine exakte Übereinstimmung zwischen Ereignis2 und einem der durch Trennzeichen getrennten Werte in s.Ereignisses machte

### Beispiel 3

Wenn...

```js
s.events="event22,event24";
```

...und der folgende Code wird ausgeführt...

```js
if(!s.inList(s.events,"event23"))
```

...Die bedingte if-Anweisung ist &quot;true&quot;, da der InList-Aufruf keine exakte Übereinstimmung zwischen Ereignis23 und einem der durch Trennzeichen getrennten Werte in s.Ereignisses hergestellt hat (beachten Sie den Operator &quot;NOT&quot;am Anfang des InList-Variablenaufrufs).

### Beispiel 4

Wenn...

```js
s.events = "event22,event23";
```

...und der folgende Code wird ausgeführt...

```js
if(s.inList(s.events,"EVenT23","",1))
```

...Die bedingte if-Anweisung lautet false.  Dieses Beispiel ist zwar nicht praktikabel, zeigt aber, dass bei der Verwendung des Flags unter Beachtung der Groß- und Kleinschreibung Vorsicht geboten ist.

### Beispiel 5

Wenn...

```js
s.linkTrackVars = "events,eVar1";
```

...und der folgende Code wird ausgeführt...

```js
if(s.inList(s.linkTrackVars,"eVar1","|"))
```

...Die bedingte if-Anweisung lautet false.  Der Wert des d-Arguments, das an den Aufruf übergeben wird (d.h. &quot;|&quot;) geht davon aus, dass die einzelnen Werte in s.linkTrackVars durch ein Pipe-Zeichen getrennt werden, während die Werte in Wirklichkeit durch ein Komma getrennt werden.  In diesem Fall versucht das Plug-in, eine Übereinstimmung zwischen dem gesamten Wert von s.linkTrackVars (d.h. &quot;Ereignis,eVar1&quot;) und den zu suchenden Wert (d.h. &quot;eVar1&quot;).

## Versionsverlauf

### v2.1 (26. September 2019)

* Es wurde die Option hinzugefügt, dass das `cc` Argument kein boolescher Wert sein darf. Beispiel: `1` ist ein gültiger Wert für die Groß-/Kleinschreibung.

### v2.0 (17. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).

### v1.01 (27. September 2017)

* Optimierter Code zur Verringerung der Größe

### v1.0 (2009)

* Erstes Release.


