---
title: getResponsiveLayout
description: Bestimmen Sie, welches Layout einer Website derzeit angezeigt wird.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in:getResponsiveLayout

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getResponsiveLayout` Plug-in können Sie verfolgen, welche Version Ihrer Website auf reaktionsfähigem Design aktuell von einem Besucher angesehen wird. Adobe empfiehlt die Verwendung dieses Plugins, wenn Ihre Site reaktionsfähiges Design verwendet und Sie die Version der von einem Besucher angezeigten Site verfolgen möchten. Dieses Plug-in ist nicht erforderlich, wenn Ihre Site kein reaktionsfähiges Design verwendet.

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
/* Adobe Consulting Plugin: getResponsiveLayout v1.0 */
var getResponsiveLayout=function(ppw,plw,tw){if(!(isNaN(ppw)||isNaN(plw)||isNaN(tw)||plw<ppw||tw<plw)){var b=window.innerWidth|| document.documentElement.clientWidth||document.body.clientWidth;return(ppw<plw&&b<=plw?b<=ppw?"phone portrait layout":"phone landscape layout":b<=plw?"phone layout":b<=tw?"tablet layout":"desktop layout")+":"+b+"x"+(window.innerHeight|| document.documentElement.clientHeight||document.body.clientHeight)}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getResponsiveLayout` Methode verwendet die folgenden Argumente:

* **`ppw`**(erforderlich, ganze Zahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Hochformat-Layout zu einem Smartphone-Querformat-Layout wechselt
* **`plw`**(erforderlich, ganze Zahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Querformat-Layout zu einem Tablet-Layout wechselt
* **`tw`**(erforderlich, Boolescher Wert): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Tablet-Layout zu einem Desktop-Layout wechselt

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

 ...Im folgenden Code wird eVar10 mit dem aktuellen reaktionsfähigen Design-Layout als Erlebnis des Besuchers sowie mit der Breite und den Abmessungen des Browsers identisch.

```js
s.eVar10 = getResponsiveLayout(500, 700, 1000);
```

### Beispiel 2

Wenn...

* Ihre Site verfügt nur über einen Telefonmodus, einen Tablet-Modus und einen Desktop-Modus
* Ihre Site wechselt vom Telefonmodus zum Tablet-Modus, wenn die Browserbreite größer als 500 Pixel ist
* Ihre Site wechselt vom Tablet- zum Desktop-Modus, wenn die Browserbreite größer als 1.100 Pixel ist

 ...Im folgenden Code wird eVar10 mit dem aktuellen reaktionsfähigen Design-Layout als Erlebnis des Besuchers sowie mit der Breite und den Abmessungen des Browsers identisch.

```js
s.eVar10 = getResponsiveLayout(500, 500, 1100);
```

## Versionsverlauf

### 1.0 (2. Mai 2018)

* Erstes Release.
