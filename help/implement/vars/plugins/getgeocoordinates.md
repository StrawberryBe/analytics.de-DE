---
title: getGeoCoordinates
description: Verfolgen Sie den Standort (geoLocation) eines Besuchers.
translation-type: tm+mt
source-git-commit: d0947b075923956a4a48e09f8eeffc38e7fc0672
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 98%

---


# Adobe-Plug-in: getGeoCoordinates

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getGeoCoordinates`-Plug-in können Sie die Breiten- und Längengrade der Geräte von Besuchern erfassen. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Daten zum geografischen Standort in Analytics-Variablen erfassen möchten.

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
   * Aktionstyp: getGeoCoordinates initialisieren
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
/* Adobe Consulting Plugin: getGeoCoordinates v2.0  */
function getGeoCoordinates(){if(arguments&&"-v"===arguments[0])return{plugin:"getGeoCoordinates",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getGeoCoordinates="2.0");window.cookieWrite=window.cookieWrite||function(a,c,f){if("string"===typeof a){var h=window.location.hostname,b=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){b=2<b?b:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<b;)e=h.lastIndexOf(".",e-1),b--;e=0<e?h.substring(e):h}}g=e;c="undefined"!==typeof c?""+c:"";if(f||""===c)if(""===c&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(c)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(a)===c:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var c=" "+document.cookie,b=c.indexOf(" "+a+"="),d=0>b?b:c.indexOf(";",b);return(a=0>b?"":decodeURIComponent(c.substring(b+2+a.length,0>d?c.length:d)))?a:""};var d="";b=cookieRead("s_ggc").split("|");var k={timeout:5E3,maximumAge:0},l=function(a){a=a.coords;cookieWrite("s_ggc",parseFloat(a.latitude.toFixed(4))+"|"+parseFloat(a.longitude.toFixed(4)),30);d="latitude="+parseFloat(a.latitude.toFixed(4))+" | longitude="+parseFloat(a.longitude.toFixed(4))},m=function(a){d="error retrieving geo coordinates"};1<b.length&&(d="latitude="+b[0]+" | longitude="+b[1]);navigator.geolocation&&navigator.geolocation.getCurrentPosition(l,m,k);""===d&&(d="geo coordinates not available");return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getGeoCoordinates`-Methode verwendet keine Argumente. Sie gibt einen der folgenden Werte zurück:

* `"geo coordinates not available"`: Für Geräte, die zum Zeitpunkt der Ausführung des Plug-ins keine Geolocation-Daten verfügbar haben. Dieser Wert wird häufig beim ersten Treffer des Besuchs verwendet, insbesondere dann, wenn Besucher zunächst ihre Zustimmung zum Tracking ihres Standorts geben müssen.
* `"error retrieving geo coordinates"`: Wenn das Plug-in beim Versuch, den Standort des Geräts abzurufen, auf Fehler stößt.
* `"latitude=[LATITUDE] | longtitude=[LONGITUDE]"`: Wobei [BREITENGRAD]/[LÄNGENGRAD] der Breitengrad bzw. der Längengrad ist.

>[!NOTE]
>
>Die Koordinatenwerte werden auf die nächstliegende vierte Dezimalstelle gerundet. Beispielsweise wird der Wert `"40.438635333"` auf `"40.4386"` gerundet, um die Anzahl der zu erfassenden eindeutigen Werte zu begrenzen. Die Werte sind genau genug, um die exakte Position des Geräts innerhalb von etwa 20 Fuß zu bestimmen.

Dieses Plug-in verwendet ein Cookie namens `"s_ggc"`, um gegebenenfalls Koordinaten zwischen den Treffern zu speichern.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
s.eVar1 = s.getGeoCoordinates();
```

... setzt eVar1 je nach Gerätestatus des Besuchers auf einen der oben genannten Rückgabewerte.

### Beispiel 2

Der folgende Code extrahiert Breiten- und Längengrad in ihre eigenen Variablen „finalLatitude“ und „finalLongitude“ zur Verwendung in anderen Codes/Anwendungen.

```js
var coordinates = s.getGeoCoordinates();
if(coordinates.indexOf("latitude") > -1)
{
  var finalLatitude = Number(coordinates.split("|")[0].trim().split("=")[1]),
  finalLongitude = Number(coordinates.split("|")[1].trim().split("=")[1]);
}
```

Von diesen können Sie ermitteln, ob sich ein Besucher beispielsweise bei der Freiheitsstatue befindet:

```js
if(finalLatitude >= 40.6891 && finalLatitude <= 40.6893 && finalLongtude >= -74.0446 && finalLongitude <= -74.0444)
  var visitorAtStatueOfLiberty = true;
else
  var visitorAtStatueOfLiberty = false;
```

## Versionsverlauf

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (25. Mai 2015)

* Erste Version.
