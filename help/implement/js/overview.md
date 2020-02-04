---
title: AppMeasurement für JavaScript
description: Erfahren Sie, wie Sie Adobe Analytics mit JavaScript ohne Tag-Management-System implementieren.
translation-type: tm+mt
source-git-commit: 0439440e10dddf8a5d64e4ea8f9868b521e5ca20

---


# AppMeasurement für JavaScript

AppMeasurement für JavaScript ist seit jeher eine häufige Methode zur Implementierung von Adobe Analytics. Da Tag-Management-Systeme jedoch immer beliebter werden, wird empfohlen, [Adobe Experience Platform Launch](../launch/overview.md) zu verwenden.

## Genereller Workflow zum Senden von Daten an Adobe mit JavaScript

1. Laden Sie die `AppMeasurement.js` Datei. Diese Datei enthält die Bibliotheken, die zum Senden von Daten an Adobe erforderlich sind.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. Definieren Sie Konfigurationsvariablen in `AppMeasurement.js`. Wenn das Analytics-Objekt instanziiert wird, stellen diese Variablen sicher, dass die Datenerfassungseinstellungen korrekt sind. Eine vollständige Liste der Variablen, die Sie definieren können, finden Sie unter [Konfigurationsvariablen](../vars/config-vars/configuration-variables.md) .

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.omtrdc.net";
   ```

3. Definieren Sie Variablen auf Seitenebene im Seitencode Ihrer Site. Diese Variablen bestimmen bestimmte Dimensionen und Metriken, die an Adobe gesendet werden. Eine vollständige Liste der Variablen, die Sie definieren können, finden Sie unter [Seitenvariablen](../vars/page-vars/page-variables.md) .

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. Wenn alle Variablen auf Seitenebene definiert sind, senden Sie die Daten mit der `t` Funktion an Adobe. Weitere Informationen finden Sie [in diesem Abschnitt](../vars/functions/t.md) .

   ```js
   s.t();
   ```
