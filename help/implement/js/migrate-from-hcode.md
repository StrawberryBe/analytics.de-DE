---
title: Migration zu AppMeasurement für JavaScript
description: Bestimmen Sie, was erforderlich ist, um Ihre H-Code-Implementierung zu migrieren.
translation-type: tm+mt
source-git-commit: 09b453c1b4cd8555c5d1718759003945f5c230c5
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%

---


# Migration zu AppMeasurement für JavaScript

Wenn Ihre Implementierung weiterhin H-Code verwendet, empfiehlt Adobe dringend eine Migration auf die neueste Version von AppMeasurement. Es wird empfohlen, Analytics über [Adobe Experience Platform Launch](../launch/overview.md) zu implementieren. Es kann jedoch eine aktualisierte JavaScript-Implementierung verwendet werden.

Die folgenden wichtigen Änderungen sind in AppMeasurement im Vergleich zum H-Code vorhanden:

* 3- bis 7-mal schneller als H-Code.
* Schlanker als H-Code – unkomprimiert 21 KB im Vergleich zu H-Code, der unkomprimiert 33 KB ist.
* Der Bibliotheks- und Seiten-Code kann innerhalb des `<head>`-Tags bereitgestellt werden.
* Der vorhandene H-Code auf Seitenebene ist mit AppMeasurement kompatibel.
* Die Bibliothek enthält native Hilfsprogramme zum Abrufen von Abfrageparametern, zum Lesen und Schreiben von Cookies und zum Durchführen des erweiterten Linktrackings.
* Die Bibliothek unterstützt keine Konfigurationsvariablen für dynamische Konten (einschließlich `dynamicAccountSelection`, `dynamicAccountMatch` und `dynamicAccountList`).

Die folgenden Schritte beschreiben einen typischen Migrations-Workflow.

1. **Neue AppMeasurement-Datei herunterladen**: Greifen Sie auf die neue Datei zu, indem Sie sich bei Adobe Analytics anmelden und dann zu „Admin“ > „Code-Manager“ navigieren. Die heruntergeladene komprimierte Datei enthält eine minimierte `AppMeasurement.js`-Datei sowie das Medien- und das Integrationsmodul.
1. **Ihre `s_code.js`-Anpassungen nach`AppMeasurement.js`** kopieren: Verschieben Sie den gesamten Code vor dem `DO NOT ALTER ANYTHING BELOW THIS LINE`-Abschnitt in `s_code.js` an den Anfang von `AppMeasurement.js`.
1. **Alle Plug-ins aktualisieren**: Vergewissern Sie sich, dass Sie die neueste Version jedes in Ihrer `s_code.js`-Datei aufgelisteten Plug-ins verwenden. Dazu gehören das Medien- und das Integrationsmodu.
1. **AppMeasurement.js bereitstellen**: Laden Sie Ihre `AppMeasurement.js`-Datei auf Ihren Webserver hoch.
1. **Skriptverweise aktualisieren, um`AppMeasurement.js`** zu referenzieren: Stellen Sie sicher, dass alle Seiten auf `AppMeasurement.js` anstatt auf `s_code.js` verweisen.

## Beispiel-AppMeasurement-Code

Eine typische `AppMeasurement.js`-Datei. Vergewissern Sie sich, dass die Konfigurationsvariablen über der `doPlugins`-Funktion eingestellt sind.

```js
// Initialize AppMeasurement
var s = s_gi("examplersid");

/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/;
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE");

/************************** CONFIG SECTION **************************/;
/* You may add or alter any code config here. */
s.trackDownloadLinks = true;
s.trackExternalLinks = true;
s.trackInlineStats = true;
s.linkDownloadFileTypes = "exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx";
s.linkInternalFilters = "javascript:,example.com";

s.usePlugins = true;
function s_doPlugins(s) {

// Use implementation plug-ins that are defined below in this section

}
s.doPlugins = s_doPlugins;

/* WARNING: Changing any of the below variables will cause drastic
changes to how your visitor data is collected.  Changes should only be
made when instructed to do so by your account manager.*/
s.trackingServer="example.data.adobedc.net";

/************************** PLUGINS SECTION *************************/

// Copy and paste implementation plug-ins here. Plug-ins can then be used in the s_doPlugins(s) function above

/****************************** MODULES *****************************/

// Copy and paste implementation modules (Media, Integrate) here.

/* ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ===============  */
```

## Beispiel-Seiten-Code

Typischer Code, der auf jeder Seite geladen wird.

```html
<script src="AppMeasurement.js"></script>
<script language="JavaScript" type="text/javascript">
s.pageName = "Example page name";
s.eVar1 = "Example eVar value";
s.events = "event1";
s.t();
</script>
```

Stellen Sie sicher, dass Sie auf jeder Seite stets auf `AppMeasurement.js` und `VisitorAPI.js` verweisen. Weitere Informationen finden Sie unter [JavaScript-Implementierung](/help/implement/js/overview.md).
