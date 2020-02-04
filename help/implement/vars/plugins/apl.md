---
title: apl (appendToList)
description: Fügen Sie Werte an Variablen hinzu, die mehrere Werte unterstützen.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in:apl (appendToList)

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `apl` Plug-in können Sie mit Sicherheit neue Werte zu Variablen mit Listentrennzeichen hinzufügen, z. B. `events`, `linkTrackVars`Listenvariablen und andere.

* Wenn der Wert, den Sie hinzufügen möchten, nicht in der Variablen vorhanden ist, fügt der Code den Wert am Ende der Zeichenfolge hinzu.
* Wenn der Wert, den Sie hinzufügen möchten, bereits in der Variablen vorhanden ist, ändert dieses Plug-In den Wert nicht. Diese Funktionen ermöglichen es Ihrer Implementierung, doppelte Werte zu vermeiden.
* Wenn die Variable, der Sie hinzufügen möchten, leer ist, setzt das Plug-In die Variable auf den neuen Wert.

Adobe empfiehlt die Verwendung dieses Plug-Ins, wenn Sie vorhandenen Variablen, die eine Zeichenfolge aus getrennten Werten enthalten, neue Werte hinzufügen möchten. Dieses Plug-in ist nicht erforderlich, wenn Sie Zeichenfolgen für Variablen mit getrennten Werten verknüpfen möchten.

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
   * Aktionstyp: APL initialisieren (an Liste anhängen)
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
/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `apl` Methode verwendet die folgenden Argumente:

* **`lv`**(erforderlich, Zeichenfolge): Die Variable, die eine durch Trennzeichen getrennte Liste von Elementen enthält, der ein neuer Wert hinzugefügt werden soll
* **`vta`**(erforderlich, Zeichenfolge): Eine kommagetrennte Liste der neuen Werte, die dem`lv`Argumentwert hinzugefügt werden sollen.
* **`d1`**(optional, Zeichenfolge): Das Trennzeichen, mit dem die einzelnen Werte getrennt werden, die bereits im`lv`Argument enthalten sind.  Wenn kein Komma festgelegt ist, wird standardmäßig ein Komma (`,`) verwendet.
* **`d2`**(optional, Zeichenfolge): Das Ausgabetrennzeichen. Der Standardwert ist derselbe Wert wie`d1`, wenn er nicht festgelegt wird.
* **`cc`**(optional, boolean): Ein Flag, das anzeigt, ob bei einer Prüfung die Groß-/Kleinschreibung beachtet wird. Wenn`true`bei der Duplizierungsprüfung die Groß- und Kleinschreibung beachtet wird. Bei`false`oder ohne Einstellung wird bei der Duplizierungsprüfung nicht zwischen Groß- und Kleinschreibung unterschieden. Die Standardeinstellung ist`false`.

Die `apl` Methode gibt den Wert des `lv` Arguments sowie alle nicht duplizierten Werte im `vta` Argument zurück.

## Beispielaufrufe

### Beispiel 1

Wenn...

```js
s.events = "event22,event24";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.apl(s.events, "event23");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event24,event23";
```

### Beispiel 2

Wenn...

```js
s.events = "event22,event23";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.apl(s.events, "event23");
```

 ... Der Endwert von s.events lautet weiterhin:

```js
s.events = "event22,event23";
```

In diesem Beispiel hat der apl-Aufruf keine Änderungen an s.events vorgenommen, da s.events bereits &quot;event23&quot;enthielt

### Beispiel 3

Wenn...

```js
s.events = ""; //blank value
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.apl(s.events, "event23");
```

 ... der Endwert von s.events ist...

```js
s.events = "event23";
```

### Beispiel 4

Wenn...

```js
s.prop4 = "hello|people";
```

 ...und der folgende Code wird ausgeführt...

```js
s.eVar5 = s.apl(s.prop4, "today", "|");
```

 ... Der Endwert von s.prop4 bleibt...

```js
s.prop4 = "hello|people";
```

 ...aber der Endwert von s.eVar5 ist

```js
s.eVar5 = "hello|people|today";
```

Beachten Sie, dass das Plug-In nur einen Wert zurückgibt. Es wird nicht unbedingt die Variable zurückgesetzt, die über das lv-Argument übergeben wird.

### Beispiel 5

Wenn...

```js
s.prop4 = "hello|people";
```

 ...und der folgende Code wird ausgeführt...

```js
s.prop4 = s.apl(s.prop4, "today");
```

 ... der Endwert von s.prop4 ist...

```js
s.prop4 = "hello|people,today";
```

Stellen Sie sicher, dass das Trennzeichen zwischen dem Wert des Arguments &quot;lv&quot;und dem, was in den Argumenten &quot;d1/d2&quot;enthalten ist, konsistent ist.

### Beispiel 6

Wenn...

```js
s.events = "event22,event23";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.apl(s.events,"EVenT23", ",", ",", true);
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23,EVentT23";
```

Dieses Beispiel ist zwar nicht praktikabel, zeigt aber, dass bei der Verwendung des Flags unter Beachtung der Groß- und Kleinschreibung Vorsicht geboten ist.

### Beispiel 7

Wenn...

```js
s.events = "event22,event23";
```

 ...und der folgende Code wird ausgeführt...

```js
s.events = s.apl(s.events, "event23,event24,event25");
```

 ... Der Endwert von s.events lautet:

```js
s.events = "event22,event23,event24,event25");
```

Das Plug-In fügt s.events &quot;event23&quot;nicht hinzu, da es bereits in s.events vorhanden ist.  Allerdings werden event24 und event25 zu s.events hinzugefügt, da keines der beiden Ereignisse zuvor in s.events enthalten war.

### Beispiel 8

Wenn...

```js
s.linkTrackVars = "events,eVar1";
```

 ...und der folgende Code wird ausgeführt...

```js
s.linkTrackVars = s.apl(s.linkTrackVars, "campaign", ",", ",", false);
```

 ... Der Endwert von s.linkTrackVars lautet:

```js
s.linkTrackVars = "events,eVar1,campaign";
```

Die letzten drei Argumente (d.h. &quot;,&quot;, &quot;,&quot;, false) am Ende dieses apl-Aufrufs sind nicht erforderlich, sondern auch nicht &quot;verletzen irgendetwas&quot;, da sie eingestellt werden, da sie mit den Standard-Argumentwerten übereinstimmen.

### Beispiel 9

Wenn...

```js
s.events = "event22,event24";
```

 ...und der folgende Code wird ausgeführt...

```js
s.apl(s.events, "event23");
```

 ... Der Endwert von s.events lautet weiterhin:

```js
s.events = "event22,event24";
```

Wenn Sie das Plug-In ganz alleine ausführen (ohne den Rückgabewert einer Variablen zuzuweisen), wird die Variable, die über das lv-Argument übergeben wird, nicht &quot;zurückgesetzt&quot;.

### Beispiel #10

Wenn...

```js
s.list2 = "casesensitivevalue|casesensitiveValue"
```

 ...und der folgende Code wird ausgeführt...

```js
s.list2 = s.apl(s.list2, "CasESensiTiveValuE", "|", "-", true);
```

 ... der Endwert von s.list2 lautet:

```js
s.list2 = "casesensitivevalue-casesensitiveValue-CasESensiTiveValuE"
```

Da die beiden Trennzeichen-Argumente unterschiedlich sind, wird der übergebene Wert durch das erste Trennzeichen-Argument (&quot;|&quot;) getrennt und dann durch das zweite Trennzeichen (&quot;-&quot;) verbunden

## Versionsverlauf

### 3.2 (25. September 2019)

* Kompatibilitätsprobleme mit `apl` Aufrufen behoben, bei denen ältere Versionen des Plug-Ins verwendet wurden
* Entfernen von Konsolenwarnungen zur Verringerung der Größe
* Hinzufügung von `inList 2.1`

### 3.1 (22. April 2018)

* `d2` ist jetzt standardmäßig der Wert des `d1` Arguments, wenn nicht festgelegt

### 3.0 (16. April 2018)

* Vollständige Neuanalyse/Umschreiben des Plugins
* Erweiterte Fehlerprüfung hinzugefügt
* Das `vta` Argument akzeptiert jetzt mehrere Werte gleichzeitig
* Das `d2` Argument zum Formatieren des Rückgabewerts wurde hinzugefügt
* Das `cc` Argument wurde in einen booleschen

### 2.5 (18. Februar 2016)

* Verwendet jetzt die `inList` Methode für die Vergleichsverarbeitung

### 2.0 (26. Januar 2016)

* `d` (Trennzeichen) Argument jetzt optional (standardmäßig ein Komma)
* `u` (Kennzeichen für Groß-/Kleinschreibung) ist jetzt optional (standardmäßig wird nicht zwischen Groß- und Kleinschreibung unterschieden)
* Unabhängig vom Argument `u` (Groß-/Kleinschreibung beachten) hängt das Plug-In keinen Wert mehr an eine Liste an, wenn der Wert bereits in der Liste vorhanden ist