---
title: getResponsiveLayout
description: Ermitteln Sie, welches Layout einer Website gerade angezeigt wird.
translation-type: tm+mt
source-git-commit: 16d2bc13a71dfe0b9106dea03da5eaa9da4d704c
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 98%

---


# Adobe-Plug-in: getResponsiveLayout

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getResponsiveLayout`-Plug-in können Sie verfolgen, welche Version Ihrer auf einem responsiven Design basierenden Website aktuell von einem Besucher angesehen wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Ihre Website ein responsives Design verwendet und Sie die Version der von einem Besucher angezeigten Website verfolgen möchten. Dieses Plug-in ist nicht erforderlich, wenn Ihre Website kein responsives Design verwendet.

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
   * Aktionstyp: getResponsiveLayout initialisieren
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getResponsiveLayout`-Methode verwendet die folgenden Argumente:

* **`ppw`** (erforderlich, Ganzzahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Hochformat-Layout zu einem Smartphone-Querformat-Layout wechselt
* **`plw`** (Erforderlich, Ganzzahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Querformat-Layout zu einem Tablet-Layout wechselt
* **`tw`** (erforderlich, boolesch): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Tablet-Layout zu einem Desktop-Layout wechselt

Beim Aufrufen dieser Methode wird eine Zeichenfolge mit zwei Teilen zurückgegeben. Der erste Teil verwendet die folgenden Werte, je nach Browser-Breite und obigen Argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (für Websites ohne Layouts im Hoch- und Querformat)
* `"tablet layout"`
* `"desktop layout"`

Der zweite Teil der zurückgegebenen Zeichenfolge ist die Breite und Höhe des Browsers. Beispiel: `"desktop layout:1243x700"`.

## Beispielaufrufe

### Beispiel 1

Wenn ...

* Ihre Website wechselt vom Smartphone-Hochformat zum Smartphone-Querformat, wenn die Browser-Breite größer als 500 Pixel ist
* Ihre Website wechselt vom Smartphone-Querformat zum Tablet-Modus, wenn die Browser-Breite größer als 700 Pixel ist
* Ihre Website wechselt vom Tablet-Modus zum Desktop-Modus, wenn die Browser-Breite größer als 1000 Pixel ist

... der folgende Code setzt eVar10 auf das aktuelle responsive Design-Layout als Erlebnis für den Besuchers sowie auf die Breite und den Abmessungen des Browsers

```js
s.eVar10 = getResponsiveLayout(500, 700, 1000);
```

### Beispiel 2

Wenn ...

* Ihre Website verfügt nur über einen Smartphone-Modus, einen Tablet-Modus und einen Desktop-Modus
* Ihre Website wechselt vom Smartphone-Modus zum Tablet-Modus, wenn die Browser-Breite größer als 500 Pixel ist
* Ihre Website wechselt vom Tablet-Modus zum Desktop-Modus, wenn die Browser-Breite größer als 1.100 Pixel ist

... der folgende Code setzt eVar10 auf das aktuelle responsive Design-Layout als Erlebnis für den Besuchers sowie auf die Breite und den Abmessungen des Browsers

```js
s.eVar10 = getResponsiveLayout(500, 500, 1100);
```

## Versionsverlauf

### 1.1 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (2. Mai 2018)

* Erste Version.
