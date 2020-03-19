---
title: getResponsiveLayout
description: Bestimmen Sie, welches Layout einer Website derzeit angezeigt wird.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getResponsiveLayout

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getResponsiveLayout` Plug-In können Sie verfolgen, welche Version Ihrer Website mit reaktionsfähigem Design derzeit von einem Besucher geprüft wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Ihre Site reaktionsfähiges Design verwendet und Sie die Version der von einem Besucher angezeigten Site verfolgen möchten. Dieses Plug-in ist nicht erforderlich, wenn Ihre Site kein reaktionsfähiges Design verwendet.

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
   * Aktionstyp: getResponsiveLayout initialisieren
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.0 */
var getResponsiveLayout=function(ppw,plw,tw){if(!(isNaN(ppw)||isNaN(plw)||isNaN(tw)||plw<ppw||tw<plw)){var b=window.innerWidth|| document.documentElement.clientWidth||document.body.clientWidth;return(ppw<plw&&b<=plw?b<=ppw?"phone portrait layout":"phone landscape layout":b<=plw?"phone layout":b<=tw?"tablet layout":"desktop layout")+":"+b+"x"+(window.innerHeight|| document.documentElement.clientHeight||document.body.clientHeight)}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getResponsiveLayout` Methode verwendet die folgenden Argumente:

* **`ppw`** (erforderlich, ganze Zahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Hochformat-Layout zu einem Smartphone-Querformat-Layout wechselt
* **`plw`** (erforderlich, ganze Zahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Querformat-Layout zu einem Tablet-Layout wechselt
* **`tw`** (erforderlich, Boolescher Wert): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Tablet-Layout zu einem Desktop-Layout wechselt

Beim Aufrufen dieser Methode wird eine Zeichenfolge mit zwei Teilen zurückgegeben. Der erste Teil verwendet die folgenden Werte, je nach Browserbreite und obigen Argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (für Sites ohne Layouts im Hoch- und Querformat)
* `"tablet layout"`
* `"desktop layout"`

Der zweite Teil der zurückgegebenen Zeichenfolge ist die Breite und Höhe des Browsers. Beispiel: `"desktop layout:1243x700"`.

## Beispielaufrufe

### Beispiel 1

Wenn...

* Ihre Site wechselt vom Hochformat für Smartphones zum Querformat, wenn die Browserbreite größer als 500 Pixel ist
* Ihre Site wechselt vom Querformat des Telefons zum Tablet-Modus, wenn die Browserbreite größer als 700 Pixel ist
* Ihre Site wechselt vom Tablet- zum Desktop-Modus, wenn die Browserbreite größer als 1000 Pixel ist

...Im folgenden Code wird eVar10 mit dem aktuellen reaktionsfähigen Designlayout als Erlebnis des Besuchers sowie mit der Breite und den Abmessungen des Browsers identisch.

```js
s.eVar10 = getResponsiveLayout(500, 700, 1000);
```

### Beispiel 2

Wenn...

* Ihre Site verfügt nur über einen Telefonmodus, einen Tablet-Modus und einen Desktop-Modus
* Ihre Site wechselt vom Telefonmodus zum Tablet-Modus, wenn die Browserbreite größer als 500 Pixel ist
* Ihre Site wechselt vom Tablet- zum Desktop-Modus, wenn die Browserbreite größer als 1.100 Pixel ist

...Im folgenden Code wird eVar10 mit dem aktuellen reaktionsfähigen Designlayout als Erlebnis des Besuchers sowie mit der Breite und den Abmessungen des Browsers identisch.

```js
s.eVar10 = getResponsiveLayout(500, 500, 1100);
```

## Versionsverlauf

### 1.0 (2. Mai 2018)

* Erstes Release.
