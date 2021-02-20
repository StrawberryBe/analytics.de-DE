---
title: getQueryParam
description: Extrahieren Sie den Wert des Abfragezeichenfolgenparameters einer URL.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 100%

---


# Adobe-Plug-in: getQueryParam

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getQueryParam`-Plug-in können Sie den Wert eines beliebigen Abfragezeichenfolgenparameters extrahieren, der in einer URL enthalten ist. Dies ist nützlich, um interne und externe Kampagnencodes aus den Landingpage-URLs zu extrahieren. Dies ist auch beim Extrahieren von Suchbegriffen oder anderen Abfragezeichenfolgenparametern nützlich.

Dieses Plug-in bietet stabile Funktionen zum Analysieren komplexer URLs, einschließlich Hashes und URLs, die mehrere Abfragezeichenfolgenparameter enthalten. Wenn Sie nur einfache Abfragezeichenfolgenparameter benötigen, empfiehlt Adobe die Verwendung der URL-Parameterfunktionen in Launch oder der in AppMeasurement enthaltenen [`Util.getQueryParam()`](../functions/util-getqueryparam.md)-Methode.

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
   * Aktionstyp: getQueryParam initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v3.3 (Requires pt plug-in) */
s.getQueryParam=function(qsp,de,url){var g=this,e="",k=function(b,de){de=de.split("?").join("&");de=de.split("#").join("&");var d=de.indexOf("&"),url="";b&&(-1<d||de.indexOf("=")>d)&&(d=de.substring(d+1),url=g.pt(d,"&","gpval",b));return url};qsp=qsp.split(",");var l=qsp.length;g.gpval=function(de,b){if(de){var d=de.split("="),url=d[0];d=d[1]?d[1]:!0;if(b.toLowerCase() ==url.toLowerCase())return"boolean"===typeof d?d:this.unescape(d)}return""};de=de?de:"";url=(url?url:g.pageURL?g.pageURL: location.href)+"";if((4<de.length||-1<de.indexOf("="))&&url&&4>url.length){var b=de;de=url;url=b}for(var h=0;h<l;h++)b=k(qsp[h],url) ,"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,e+=e?de+b:b):e=""===e?b:e+(de+b);return e};

/* Adobe Consulting Plugin: pt v2.01 */ 
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getQueryParam`-Methode verwendet die folgenden Argumente:

* **`qsp`** (erforderlich): Eine durch Komma getrennte Liste von Abfragezeichenfolgenparametern, nach denen in der URL gesucht werden soll. Es wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* **`de`** (optional): Das zu verwendende Trennzeichen, wenn mehrere Abfragezeichenfolgenparameter übereinstimmen. Der Standardwert ist eine leere Zeichenfolge.
* **`url`** (optional): Eine benutzerdefinierte URL, Zeichenfolge oder Variable, aus der die Parameterwerte der Abfragezeichenfolge extrahiert werden. Die Standardeinstellung ist `window.location`.

Der Aufruf dieser Methode gibt einen Wert zurück, der von den oben genannten Argumenten und der URL abhängt:

* Wenn kein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, gibt die Methode eine leere Zeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, gibt die Methode den Parameterwert der Abfragezeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgenparameter gefunden wird, der Wert jedoch leer ist, gibt die Methode `true` zurück.
* Wenn mehrere übereinstimmende Abfragezeichenfolgenparameter gefunden werden, gibt die Methode eine Zeichenfolge zurück, bei der jeder Parameterwert durch die Zeichenfolge im `de`-Argument getrennt wird.

## Beispielaufrufe

### Beispiel 1

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1
```

Der folgende Code setzt s.campaign auf „trackingcode1“:

```js
s.campaign=s.getQueryParam('cid');
```

### Beispiel 2

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Der folgende Code setzt s.campaign auf „trackingcode1:123456“:

```js
s.campaign=s.getQueryParam('cid,ecid',':');
```

### Beispiel 3

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Der folgende Code setzt s.campaign auf „trackingcode1123456“:

```js
s.campaign=s.getQueryParam('cid,ecid');
```

### Beispiel 4

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456#location
```

Der folgende Code setzt s.campaign auf „123456“:

```js
s.campaign=s.getQueryParam('ecid');
```

### Beispiel 5

Wenn die aktuelle URL die folgende ist:

```js
http://www.abc123.com/#location&cid=trackingcode1&ecid=123456
```

Der folgende Code setzt s.campaign auf „123456“

```js
s.campaign=s.getQueryParam('ecid');
```

**Hinweis:** Das Plug-in ersetzt die URL zum Hash-Zeichen durch ein Fragezeichen, wenn kein Fragezeichen vorhanden ist.  Wenn die URL ein Fragezeichen vor dem Hash-Zeichen enthält, ersetzt das Plug-in die URL zum Hash-Zeichen durch ein kaufmännisches Und.

### Beispiel 6

Wenn die aktuelle URL die folgende ist ...

```js
http://www.abc123.com/
```

... und wenn die Variable s.testURL wie folgt eingestellt ist:

```js
s.testURL="http://www.abc123.com/?cid=trackingcode1&ecid=123456#location&pos=300";
```

Der folgende Code setzt s.campaign überhaupt nicht:

```js
s.campaign=s.getQueryParam('cid');
```

Allerdings setzt der folgende Code s.campaign auf „trackingcode1“:

```js
s.campaign=s.getQueryParam('cid','',s.testURL);
```

**Hinweis:** Der dritte Parameter kann jede beliebige Zeichenfolge/Variable sein, die der Code verwendet, um die Abfragezeichenfolgenparameter zu finden in

Der folgende Code setzt s.eVar2 auf „123456|trackingcode1|true|300“:

```js
s.eVar2=s.getQueryParam('ecid,cid,location,pos','|',s.testURL);
```

* Der Wert „123456“ stammt aus dem ecid-Parameter in der Variablen s.testURL
* Der Wert von trackingcode1 stammt aus dem Parameter cid in der Variablen s.testURL
* Der Wert „true“ ergibt sich aus der Existenz (aber nicht dem Wert) des Standortparameters nach dem Hash-Zeichen in der Variablen s.testURL

Der Wert „300“ stammt aus dem Wert des pos-Parameters in der Variablen s.testURL

## Versionsverlauf

### 3.3 (24. September 2019)

* Unnötige Logik umgangen, um die Code-Größe zu reduzieren

### 3.2 (15. Mai 2018)

* Funktionen `findParameterValue` und `getParameterValue` in die Funktion `getQueryParam` verschoben

### 3.1 (10. Mai 2018)

* Problem mit der Erfassung von Abfragezeichenfolgenparametern ohne Wert behoben

### 3.0 (16. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Hilfsfunktionen aus Gründen der Lesbarkeit in `findParameterValue` und `getParameterValue` umbenannt.
* Die Notwendigkeit, ein Argument hinzuzufügen, um im URL-Hash enthaltene Parameter zu finden, wurde entfernt

### 2.5 (8. Januar 2016)

* Kompatibel mit H-Code und AppMeasurement (`s.pt` für AppMeasurement erforderlich).

### 2,4

* Der `h`-Parameter wurde hinzugefügt, sodass der Code nach Abfragezeichenfolgenparametern suchen kann, die nach dem Hash-Zeichen (`#`) gefunden wurden

### 2,3

* Es wurde ein Regressionsproblem behoben, bei dem das Plug-in nur funktionierte, wenn der Hash nach dem Tracking-Code vorhanden war

### 2,2

* Entfernt jetzt Hash-Zeichen (und alles Weitere danach) aus dem Rückgabewert

### 2,1

* Kompatibel mit H.10-Code
