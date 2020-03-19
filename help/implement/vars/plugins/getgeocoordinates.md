---
title: getGeoCoordinates
description: Verfolgen Sie den GeoLocation eines Besuchers.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getGeoCoordinates

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getGeoCoordinates` Plug-In können Sie die Breiten- und Längengrade der Geräte des Besuchers erfassen. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Daten zum geografischen Standort in Analytics-Variablen erfassen möchten.

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
   * Aktionstyp: getGeoCoordinates initialisieren
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
/* Adobe Consulting Plugin: getGeoCoordinates v1.0 */
s.getGeoCoordinates=function(){var d=this,b="",a=d.c_r("s_ggc").split("|"),e={timeout:5E3,maximumAge:0},f=function(c){c=c.coords;var a=new Date;a.setTime(a.getTime()+18E5);d.c_w("s_ggc",parseFloat(c.latitude.toFixed(4))+"|"+parseFloat(c.longitude.toFixed(4)),a); b="latitude="+parseFloat(c.latitude.toFixed(4))+" | longitude="+parseFloat(c.longitude.toFixed(4))},g=function(a){b="error retrieving geo coordinates"};1<a.length&&(b="latitude="+a[0]+" | longitude="+a[1]);navigator.geolocation&& navigator.geolocation.getCurrentPosition(f,g,e);""===b&&(b="geo coordinates not available");return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getGeoCoordinates` Methode verwendet keine Argumente. Es gibt einen der folgenden Werte zurück:

* `"geo coordinates not available"`: Für Geräte, die zum Zeitpunkt der Ausführung des Plug-Ins keine Geolocation-Daten zur Verfügung haben. Dieser Wert wird beim ersten Treffer des Besuchs häufig verwendet, insbesondere, wenn Besucher zum ersten Mal ihre Zustimmung zur Verfolgung ihres Standorts einholen müssen.
* `"error retrieving geo coordinates"`: Wenn das Plug-In beim Versuch, den Speicherort des Geräts abzurufen, auf Fehler stößt
* `"latitude=[LATITUDE] | longtitude=[LONGITUDE]"`: Dabei [LATITUDE]/[LONGITUDE] der Breiten- bzw. Längen- bzw. Breitengrad

> [!NOTE] Die Koordinatenwerte werden auf das nächstliegende vierte Dezimalzeichen gerundet. Beispielsweise `"40.438635333"` wird der Wert von gerundet, `"40.4386"` um die Anzahl der zu erfassenden eindeutigen Werte zu begrenzen. Die Werte sind nahe genug, um die exakte Position des Geräts innerhalb von 10 Fuß zu bestimmen.

Dieses Plug-in verwendet ein Cookie mit dem Namen, um bei Bedarf Koordinaten zwischen Treffern `"s_ggc"` zu speichern.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.eVar1 = s.getGeoCoordinates();
```

...setzt eVar1 je nach Gerätestatus des Besuchers auf einen der oben genannten Rückgabewerte.

### Beispiel 2

Der folgende Code extrahiert Breiten- und Längengrad in ihre eigenen Variablen finalLatitude und finalLongitude zur Verwendung in anderen Code-/Anwendungen

```js
var coordinates = s.getGeoCoordinates();
if(coordinates.indexOf("latitude") > -1)
{
  var finalLatitude = Number(coordinates.split("|")[0].trim().split("=")[1]),
  finalLongitude = Number(coordinates.split("|")[1].trim().split("=")[1]);
}
```

Von dort können Sie bestimmen, ob sich ein Besucher beispielsweise in der Freiheitsstatue befindet:

```js
if(finalLatitude >= 40.6891 && finalLatitude <= 40.6893 && finalLongtude >= -74.0446 && finalLongitude <= -74.0444)
  var visitorAtStatueOfLiberty = true;
else
  var visitorAtStatueOfLiberty = false;
```

## Versionsverlauf

### 1.0 (25. Mai 2015)

* Erstes Release.
