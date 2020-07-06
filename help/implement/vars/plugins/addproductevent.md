---
title: addProductEvent
description: Fügt den Variablen „products“ und „events“ benutzerspezifische Ereignisse hinzu.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 100%

---


# Adobe-Plug-in: addProductEvent

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das Plug-in `addProductEvent` fügt der [`products`](../page-vars/products.md)-Variablen ein numerisches oder Währungsereignis hinzu. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie der `products`-Variablen ein numerisches oder Währungs-Ereignis hinzufügen möchten, ohne sich um das Format der Produktzeichenfolge zu sorgen. Dieses Plug-in ist nicht erforderlich, wenn Sie keine numerischen oder Währungsereignisse in der `products`-Variablen verwenden.

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
   * Aktionstyp: addProductEvent initialisieren
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
/* Adobe Consulting Plugin: addProductEvent v1.0 (Requires apl v3.1 and inList v2.0+ plug-ins) */
s.addProductEvent=function(en,ev,ap){var s=this;if("string"===typeof en)if(ev=isNaN(ev)?"1":String(ev),ap=ap||!1,s.events= s.apl(s.events,en),s.products){var e=s.products.split(",");ap=ap?0:e.length-1;for(var a;ap<e.length;ap++)a=e[ap].split(";") ,a[4]&&a[4].includes("event")?a[4]=a[4]+"|"+en+"="+ev:a[5]?a[4]=en+"="+ev:a[4]||(a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[4]=en+"="+ev),e[ap]=a.join(";");s.products=e.join(",")}else s.products=";;;;"+en+"="+ev};

/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `addProductEvent`-Methode verwendet die folgenden Argumente:

* **`en`** (erforderlich, Zeichenfolge): Das Ereignis, das zum letzten Eintrag in der `products`-Variablen hinzugefügt wird. Wenn die `products`-Variable leer ist, wird ein „leerer“ Produkteintrag mit dem angehängten Ereignis (und dessen Wert) erstellt.
* **`ev`** (erforderlich, Zeichenfolge): Der Wert, der dem numerischen Ereignis oder dem Währungsereignis im `en`-Argument zugewiesen wird.  Die Standardeinstellung ist `1`, wenn nicht festgelegt.
* **`ap`** (optional, boolesch): Wenn die Variable „products“ derzeit mehr als einen Produkteintrag enthält, wird mit dem Wert `true` (oder `1`) das Ereignis allen Produkteinträgen hinzugefügt.  Die Standardeinstellung ist `false`, wenn nicht festgelegt.

`addProductEvent` gibt nichts zurück. Stattdessen werden das Ereignis und sein Wert der `products`-Variablen hinzugefügt. Das Plug-in fügt das Ereignis auch automatisch der [`events`](../page-vars/events/events-overview.md)-Variablen hinzu, da es auch dort benötigt wird.

## Cookies

Das addProductEvent-Plug-in erstellt und verwendet keine Cookies.

## Beispielaufrufe

### Beispiel 1

Der folgende Code setzt die Variable `s.products` auf `";product1;3;300,;product2;2;122,;product3;1;25;event35=25"`.

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25"
s.events="purchase";
s.addProductEvent("event35", "25");
```

Der obige Code setzt außerdem die Variable `s.events` auf `"purchase,event35"`

### Beispiel 2

Der folgende Code setzt die Variable `s.products` auf `";product1;3;300;event35=25,;product2;2;122;event35=25,;product3;1;25;event35=25"`

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
s.addProductEvent("event35", 25, 1);
```

Wenn das dritte Argument im `addProductEvent`-Aufruf `true` (oder `1`) lautet, wird für jeden Produkteintrag das im Aufruf angegebene Ereignis zu seinem Wert hinzugefügt.

### Beispiel 3

Der folgende Code setzt die Variable `s.products` auf `";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25;event33= 12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25";
s.events="purchase,event2";
s.addProductEvent("event33", "12");
s.addProductEvent("event34", "10");
s.addProductEvent("event35", "15");
```

Der obige Code setzt außerdem die Variable `s.events` auf `"purchase,event2,event33,event34,event35"`

### Beispiel 4

Der folgende Code setzt die Variable `s.products` auf `";product1;3;300;event2=10|event33=12|event34=10|event35=15;eVar33=large|eVar34=men|eVar35=blue, ;product2;2;122;event33=12|event34=10|event35=15,;product3;1;25;event33=12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
s.addProductEvent("event33", "12", 1);
s.addProductEvent("event34", 10, 1);
s.addProductEvent("event35", "15", 1);
```

Der obige Code setzt auch die Variable `s.events` auf `"purchase,event2,event33,event34,event35"`.

>[!NOTE]
>
>Das zweite Argument im Aufruf kann entweder eine Ganzzahl **oder** eine Zeichenfolge sein, die eine Ganzzahl/Zahl darstellt

### Beispiel 5

Wenn `s.products` noch nicht festgelegt ist, setzt der folgende Code die Variable auf `";;;;event35=25"`

```js
s.addProductEvent("event35", "25");
```

Der oben genannte Code hängt auch `"event35"` an das Ende von `s.events` **oder**, falls `s.events` noch nicht spezifiziert ist, setzt der oben genannte Code `s.events` auf `"event35"`

## Versionsverlauf

### 1.0 (7. Oktober 2019)

* Erste Version.
