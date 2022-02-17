---
title: getQueryParam
description: Extrahieren Sie den Wert des Abfragezeichenfolgenparameters einer URL.
feature: Variables
exl-id: d2d542d1-3a18-43d9-a50d-c06d8bd473b8
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 100%

---

# Adobe-Plug-in: getQueryParam

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getQueryParam`-Plug-in können Sie den Wert eines beliebigen Abfragezeichenfolgenparameters extrahieren, der in einer URL enthalten ist. Dies ist nützlich, um interne und externe Kampagnencodes aus den Landingpage-URLs zu extrahieren. Dies ist auch beim Extrahieren von Suchbegriffen oder anderen Abfragezeichenfolgenparametern nützlich.

Dieses Plug-in bietet stabile Funktionen zum Analysieren komplexer URLs, einschließlich Hashes und URLs, die mehrere Abfragezeichenfolgenparameter enthalten. Wenn Sie nur einfache Abfragezeichenfolgenparameter benötigen, empfiehlt Adobe die Verwendung der URL-Parameterfunktionen mit Tags in Adobe Experience Platform oder die in AppMeasurement enthaltene [`Util.getQueryParam()`](../functions/util-getqueryparam.md)-Methode.

## Installieren des Plug-ins mithilfe von Tags in Adobe Experience Platform

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
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

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v4.0.1  */
function getQueryParam(a,d,f){function n(g,c){c=c.split("?").join("&");c=c.split("#").join("&");var e=c.indexOf("&");if(g&&(-1<e||c.indexOf("=")>e)){e=c.substring(e+1);e=e.split("&");for(var h=0,p=e.length;h<p;h++){var l=e[h].split("="),q=l[1];if(l[0].toLowerCase()===g.toLowerCase())return decodeURIComponent(q||!0)}}return""}if("-v"===a)return{plugin:"getQueryParam",version:"4.0.1"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var g=0,c;g<window.s_c_il.length;g++)if(c=window.s_c_il[g],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getQueryParam="4.0");if(a){d=d||"";f=(f||"undefined"!==typeof b&&b.pageURL||location.href)+"";(4<d.length||-1<d.indexOf("="))&&f&&4>f.length&&(b=d,d=f,f=b);b="";for(var m=a.split(","),r=m.length,k=0;k<r;k++)a=n(m[k],f),"string"===typeof a?(a=-1<a.indexOf("#")?a.substring(0,a.indexOf("#")):a,b+=b?d+a:a):b=""===b?a:b+(d+a);return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getQueryParam`-Funktion verwendet die folgenden Argumente:

* **`qsp`** (erforderlich): Eine durch Komma getrennte Liste von Abfragezeichenfolgenparametern, nach denen in der URL gesucht werden soll. Es wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* **`de`** (optional): Das zu verwendende Trennzeichen, wenn mehrere Abfragezeichenfolgenparameter übereinstimmen. Der Standardwert ist eine leere Zeichenfolge.
* **`url`** (optional): Eine benutzerdefinierte URL, Zeichenfolge oder Variable, aus der die Parameterwerte der Abfragezeichenfolge extrahiert werden. Die Standardeinstellung ist `window.location`.

Der Aufruf dieser Funktion gibt einen Wert zurück, der von den oben genannten Argumenten und der URL abhängt:

* Wenn kein übereinstimmender Abfragezeichenfolgen-Parameter gefunden wird, gibt die Funktion eine leere Zeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgen-Parameter gefunden wird, gibt die Funktion den Parameterwert der Abfragezeichenfolge zurück.
* Wenn ein übereinstimmender Abfragezeichenfolgen-Parameter gefunden wird, der Wert jedoch leer ist, gibt die Funktion `true` zurück.
* Wenn mehrere übereinstimmende Abfragezeichenfolgen-Parameter gefunden werden, gibt die Funktion eine Zeichenfolge zurück, bei der jeder Parameterwert durch die Zeichenfolge im `de`-Argument getrennt wird.

## Beispiele

```js
// Given the URL https://example.com/?cid=trackingcode
// Sets the campaign variable to "trackingcode"
s.campaign = getQueryParam('cid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode:123"
s.campaign = getQueryParam('cid,ecid',':');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode123"
s.campaign = getQueryParam('cid,ecid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123#location
// Sets the campaign variable to "123"
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com/#location&cid=trackingcode&ecid=123
// Sets the campaign variable to "123"
// The plug-in replaces the URL's hash character with a question mark if a question mark doesn't exist.
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com
// Does not set the campaign variable to a value.
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid');

// Given the URL https://example.com
// Sets the campaign variable to "trackingcode"
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid','',s.pageURL);

// Given the URL https://example.com
// Sets eVar2 to "123|trackingcode|true|300"
s.eVar1 = "https://example.com/?cid=trackingcode&ecid=123#location&pos=300";
s.eVar2 = getQueryParam('ecid,cid,location,pos','|',s.eVar1);
```

## Versionsverlauf

### 4.0.1 (26. März 2021)

* Das Problem, bei dem „nicht definiert“ statt „“ zurückgegeben wurde, wenn der Abfrageparameter in der Abfragezeichenfolge nicht vorhanden war, wurde aktualisiert.

### 4.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.
* Abhängigkeiten vom Plug-in pt entfernt.

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
