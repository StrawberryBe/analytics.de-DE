---
title: getQueryParam
description: Extrahieren Sie den Wert des Abfragezeichenfolgenparameters einer URL.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in: getQueryParam

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getQueryParam` Plug-in können Sie den Wert eines beliebigen Abfragezeichenfolgen-Parameters extrahieren, der in einer URL enthalten ist. Es ist nützlich, um interne und externe Kampagnencodes aus den Einstiegsseiten-URLs zu extrahieren. Sie ist auch beim Extrahieren von Suchbegriffen oder anderen Abfragezeichenfolgenparametern nützlich.

Dieses Plug-in bietet stabile Funktionen zum Analysieren komplexer URLs, einschließlich Hashes und URLs, die mehrere Abfragezeichenfolgenparameter enthalten. Wenn Sie nur einfache Abfragezeichenfolgenparameter benötigen, empfiehlt Adobe die Verwendung der URL-Parameterfunktionen in Launch oder der in AppMeasurement enthaltenen `Util.getQueryParam` Methode.

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
   * Aktionstyp: getQueryParam initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
1. Erweitern Sie die [!UICONTROL Verfolgung mithilfe eines benutzerdefinierten Code] -Akkordeons, das die Schaltfläche zum [!UICONTROL Öffnen des Editors] anzeigt.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v3.3 (Requires pt plug-in) */
s.getQueryParam=function(qsp,de,url){var g=this,e="",k=function(b,de){de=de.split("?").join("&");de=de.split("#").join("&");var d=de.indexOf("&"),url="";b&&(-1<d||de.indexOf("=")>d)&&(d=de.substring(d+1),url=g.pt(d,"&","gpval",b));return url};qsp=qsp.split(",");var l=qsp.length;g.gpval=function(de,b){if(de){var d=de.split("="),url=d[0];d=d[1]?d[1]:!0;if(b.toLowerCase() ==url.toLowerCase())return"boolean"===typeof d?d:this.unescape(d)}return""};de=de?de:"";url=(url?url:g.pageURL?g.pageURL: location.href)+"";if((4<de.length||-1<de.indexOf("="))&&url&&4>url.length){var b=de;de=url;url=b}for(var h=0;h<l;h++)b=k(qsp[h],url) ,"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,e+=e?de+b:b):e=""===e?b:e+(de+b);return e};

/* Adobe Consulting Plugin: pt v2.01 */ 
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getQueryParam` Methode verwendet die folgenden Argumente:

* **`qsp`**(erforderlich): Eine kommagetrennte Liste von Abfragezeichenfolgenparametern, nach denen in der URL gesucht werden soll. Es wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* **`de`**(optional): Das zu verwendende Trennzeichen, wenn mehrere Abfragezeichenfolgenparameter übereinstimmen. Der Standardwert ist eine leere Zeichenfolge.
* **`url`**(optional): Eine benutzerdefinierte URL, Zeichenfolge oder Variable, aus der die Parameterwerte der Abfragezeichenfolge extrahiert werden. Die Standardeinstellung ist`window.location`.

Der Aufruf dieser Methode gibt einen Wert zurück, der von den oben genannten Argumenten und der URL abhängt:

* Wenn kein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, gibt die Methode eine leere Zeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, gibt die Methode den Parameterwert der Abfragezeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, der Wert jedoch leer ist, gibt die Methode `true`zurück.
* Wenn mehrere übereinstimmende Abfragezeichenfolgenparameter gefunden werden, gibt die Methode eine Zeichenfolge zurück, bei der jeder Parameterwert durch die Zeichenfolge im `de` Argument getrennt wird.

## Beispielaufrufe

### Beispiel 1

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1
```

Der folgende Code setzt s.campaign gleich &quot;trackingcode1&quot;:

```js
s.campaign=s.getQueryParam('cid');
```

### Beispiel 2

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Im folgenden Code wird s.campaign auf &quot;trackingcode1:123456&quot;eingestellt:

```js
s.campaign=s.getQueryParam('cid,ecid',':');
```

### Beispiel 3

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Im folgenden Code wird s.campaign auf &quot;trackingcode1123456&quot;eingestellt:

```js
s.campaign=s.getQueryParam('cid,ecid');
```

### Beispiel 4

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456#location
```

Im folgenden Code wird s.campaign auf &quot;123456&quot;eingestellt:

```js
s.campaign=s.getQueryParam('ecid');
```

### Beispiel 5

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/#location&cid=trackingcode1&ecid=123456
```

Im folgenden Code wird s.campaign auf &quot;123456&quot;eingestellt

```js
s.campaign=s.getQueryParam('ecid');
```

**** Hinweis: Das Plug-In ersetzt die URL durch ein Fragezeichen, wenn kein Fragezeichen vorhanden ist.  Wenn die URL ein Fragezeichen enthält, das vor dem Hashzeichen steht, ersetzt das Plug-In die URL durch das Hashzeichen der Prüfung durch ein kaufmännisches Und;

### Beispiel 6

Wenn die aktuelle URL die folgende ist...

```js
http://www.abc123.com/
```

 ...und wenn die Variable s.testURL wie folgt eingestellt ist:

```js
s.testURL="http://www.abc123.com/?cid=trackingcode1&ecid=123456#location&pos=300";
```

Der folgende Code legt s.campaign überhaupt nicht fest:

```js
s.campaign=s.getQueryParam('cid');
```

Im folgenden Code wird s.campaign jedoch gleich &quot;trackingcode1&quot;eingestellt:

```js
s.campaign=s.getQueryParam('cid','',s.testURL);
```

**** Hinweis: Der dritte Parameter kann jede beliebige Zeichenfolge/Variable sein, die der Code verwendet, um die Abfragezeichenfolgenparameter in

Im folgenden Code wird s.eVar2 gleich &quot;123456|trackingcode1|true|300&quot;eingestellt:

```js
s.eVar2=s.getQueryParam('ecid,cid,location,pos','|',s.testURL);
```

* Der Wert 123456 stammt aus dem ecid-Parameter in der Variablen s.testURL
* Der Wert von trackingcode1 stammt aus dem Parameter cid in der Variablen s.testURL
* Der Wert &quot;true&quot;stammt aus der Existenz (aber nicht dem Wert) des Positionsparameters nach dem Hashzeichen in der Variablen &quot;s.testURL&quot;

Der Wert von 300 stammt aus dem Wert des Parameters &quot;pos&quot;in der Variablen &quot;s.testURL&quot;

## Versionsverlauf

### 3.3 (24. September 2019)

* Überflüssige Logik zur Reduzierung der Codegröße

### 3.2 (15. Mai 2018)

* In die `findParameterValue` Funktion verschoben `getParameterValue` und `getQueryParam` Funktionen

### 3.1 (10. Mai 2018)

* Problem mit der Erfassung von Abfragezeichenfolgenparametern ohne Wert behoben

### 3.0 (16. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).
* Umbenannte Hilfsfunktionen für Lesbarkeit `findParameterValue` und `getParameterValue` für Lesbarkeit.
* Die Notwendigkeit, ein Argument hinzuzufügen, um Parameter im URL-Hash zu finden, wurde entfernt

### 2.5 (8. Januar 2016)

* Kompatibel mit H-Code und AppMeasurement (erforderlich `s.pt` mit AppMeasurement).

### 2.4

* Der `h` Parameter wurde hinzugefügt, sodass der Code nach Abfragezeichenfolgen-Parametern suchen kann, die nach dem Hash-Zeichen (`#`) gefunden wurden

### 2.3

* Korrektur des Regressionsproblems, bei dem das Plug-In nur funktionierte, wenn der Hash nach dem Trackingcode vorhanden war

### 2.2

* Entfernt jetzt Hashzeichen (und alles weitere danach) aus dem Rückgabewert

### 2.1

* Kompatibel mit H.10-Code
