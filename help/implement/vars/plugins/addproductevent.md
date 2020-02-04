---
title: addProductEvent
description: Fügt der Variablen "products"und "events"benutzerspezifische Ereignisse hinzu.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in:addProductEvent

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `addProductEvent` Plug-In fügt der Variablen ein numerisches oder Währungsereignis hinzu `products` . Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie der Variablen ein numerisches oder Währungs-Ereignis hinzufügen möchten, ohne sich um das Format der Produktzeichenfolge zu sorgen. `products` Dieses Plug-in ist nicht erforderlich, wenn Sie keine numerischen oder Währungsereignisse in der `products` Variablen verwenden.

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
/* Adobe Consulting Plugin: addProductEvent v1.0 (Requires apl v3.1 and inList v2.0+ plug-ins) */
s.addProductEvent=function(en,ev,ap){var s=this;if("string"===typeof en)if(ev=isNaN(ev)?"1":String(ev),ap=ap||!1,s.events= s.apl(s.events,en),s.products){var e=s.products.split(",");ap=ap?0:e.length-1;for(var a;ap<e.length;ap++)a=e[ap].split(";") ,a[4]&&a[4].includes("event")?a[4]=a[4]+"|"+en+"="+ev:a[5]?a[4]=en+"="+ev:a[4]||(a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[4]=en+"="+ev),e[ap]=a.join(";");s.products=e.join(",")}else s.products=";;;;"+en+"="+ev};

/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `addProductEvent` Methode verwendet die folgenden Argumente:

* **`en`**(erforderlich, Zeichenfolge): Das Ereignis, das zum letzten Eintrag in der`products`Variablen hinzugefügt wird. Wenn die`products`Variable leer ist, wird ein &quot;leerer&quot;Produkteintrag mit dem angehängten Ereignis (und dessen Wert) erstellt.
* **`ev`**(erforderlich, Zeichenfolge): Der Wert, der dem numerischen Ereignis oder dem Währungsereignis im`en`Argument zugewiesen wird.  Die Standardeinstellung ist`1`nicht festgelegt.
* **`ap`**(optional, boolean): Wenn die Produktvariable derzeit mehr als einen Produkteintrag enthält, wird das Ereignis mit dem Wert`true`(oder`1`) allen Produkteinträgen hinzugefügt.  Die Standardeinstellung ist`false`nicht festgelegt.

Die `addProductEvent` gibt nichts zurück. Stattdessen werden das Ereignis und sein Wert der `products` Variablen hinzugefügt. Das Plug-In fügt das Ereignis automatisch der `events` Variablen hinzu, da es auch dort benötigt wird.

## Cookies

Das addProductEvent-Plug-in erstellt keine Cookies oder verwendet keine Cookies

## Beispielaufrufe

### Beispiel 1

Wenn...

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25"
s.events="purchase"
```

 ...und der folgende Code wird ausgeführt...

```js
s.addProductEvent("event35", "25");
```

 ... der Endwert von s.products lautet:

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25;event35=25"
```

 ...und der Endwert von s.events lautet:

```js
s.events="purchase,event35"
```

### Beispiel 2

Wenn...

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25"
```

 ...und der folgende Code wird ausgeführt...

```js
s.addProductEvent("event35", 25, 1);
```

 ... der Endwert von s.products lautet:

```js
s.products=";product1;3;300;event35=25,;product2;2;122;event35=25,;product3;1;25;event35=25"
```

Wenn das dritte Argument true (oder 1) ist, wird für jeden Produkteintrag das Ereignis angegeben, das im Aufruf zum Wert hinzugefügt wird

### Beispiel 3

Wenn...

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
```

 ...und der folgende Code wird ausgeführt...

```js
s.addProductEvent("event33", "12");
s.addProductEvent("event34", "10");
s.addProductEvent("event35", "15");
```

 ... Der Endwert von s.products ist...

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25;event33= 12|event34=10|event35=15"
```

 ...und s.events wie folgt festgelegt werden:

```js
s.events="purchase,event2,event33,event34,event35"
```

### Beispiel 4

Wenn...

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
```

 ...und der folgende Code wird ausgeführt...

```js
s.addProductEvent("event33", "12", 1);
s.addProductEvent("event34", 10, 1); //The second argument can be an integer or a string representing an integer/number
s.addProductEvent("event35", "15", 1);
```

 ... Der Endwert von s.products ist...

```js
s.products=";product1;3;300;event2=10|event33=12|event34=10|event35=15;eVar33=large|eVar34=men|eVar35=blue, ;product2;2;122;event33=12|event34=10|event35=15,;product3;1;25;event33=12|event34=10|event35=15"
```

 ...und s.events wie folgt festgelegt werden:

```js
s.events="purchase,event2,event33,event34,event35"
```

### Beispiel 5

Wenn s.products nicht eingestellt ist und der folgende Code ausgeführt wird...

```js
s.addProductEvent("event35", "25");
```

 ... der Endwert von s.products lautet:

```js
s.products=";;;;event35=25"
```

In diesem Fall wird event35 auch am Ende von s.events angehängt

## Versionsverlauf

### 1.0 (7. Oktober 2019)

* Erstes Release.
