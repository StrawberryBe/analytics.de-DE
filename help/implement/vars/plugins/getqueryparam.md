---
title: getQueryParam
description: Extrahieren Sie den Wert des Abfragezeichenfolgenparameters einer URL.
translation-type: ht
source-git-commit: 03c3a954c40d17f11f4f80ee3a378fd43948cc5c
workflow-type: ht
source-wordcount: '896'
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
/* Adobe Consulting Plugin: getQueryParam v4.0 */
function getQueryParam(b,c,d){function h(b,a){a=a.split("?").join("&");a=a.split("#").join("&");var c=a.indexOf("&");if(b&&(-1<c||a.indexOf("=")>c)){c=a.substring(c+1);c=c.split("&");for(var d=0,k=c.length;d<k;d++){var f=c[d].split("="),e=f[1];if(f[0].toLowerCase()===b.toLowerCase())return decodeURIComponent(e||!0)}}}if("-v"===b)return{plugin:"getQueryParam",version:"4.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getQueryParam="4.0");if(b){c=c||"";d=(d||"undefined"!==typeof a&&a.pageURL||location.href)+"";(4<c.length||-1<c.indexOf("="))&&d&&4>d.length&&(a=c,c=d,d=a);a="";for(var g=b.split(","),l=g.length,e=0;e<l;e++)b=h(g[e],d),"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,a+=a?c+b:b):a=""===a?b:a+(c+b);return a}};
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

### 4.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.
* Abhängigkeiten vom Plug-in `pt` entfernt.

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
