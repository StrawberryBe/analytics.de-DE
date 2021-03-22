---
title: addProductEvent
description: Fügt den Variablen „products“ und „events“ benutzerspezifische Ereignisse hinzu.
translation-type: tm+mt
source-git-commit: 3359ed8e7ef7979be57ca5ec9ca1803fc52afe88
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 98%

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
/* Adobe Consulting Plugin: addProductEvent v2.0 */
function addProductEvent(en,ev,ap){var f=en,g=ev,c=ap;if("-v"===f)return{plugin:"addProductEvent",version:"2.0"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,e;b<window.s_c_il.length;b++)if(e=window.s_c_il[b],e._c&&"s_c"===e._c)return e}();if("undefined"!==typeof d&&(d.contextData.addProductEvent="2.0",window.apl=window.apl||function(b,e,c,d,f){function g(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!b||"string"===typeof b){if("string"!==typeof e||""===e)return b;c=c||",";d=d||c;1==d&&(d=c,f||(f=1));2==d&&1!=f&&(d=c);e=e.split(",");k=e.length;for(var h=0;h<k;h++)g(b,e[h],c,f)||(b=b?b+d+e[h]:e[h])}return b},"string"===typeof f))if(g=isNaN(g)?"1":String(g),c=c||!1,d.events=window.apl(d.events,f),d.products){var l=d.products.split(","),m=l.length;c=c?0:m-1;for(var b;c<m;c++)b=l[c].split(";"),b[4]&&-1<b[4].indexOf("event")?b[4]=b[4]+"|"+f+"="+g:b[5]?b[4]=f+"="+g:b[4]||(b[3]||(b[3]=""),b[2]||(b[2]=""),b[1]||(b[1]=""),b[4]=f+"="+g),l[c]=b.join(";");d.products=l.join(",")}else d.products=";;;;"+f+"="+g};
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

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (7. Oktober 2019)

* Erste Version.
