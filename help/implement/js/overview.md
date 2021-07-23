---
title: AppMeasurement für JavaScript
description: Erfahren Sie, wie Sie Adobe Analytics mit JavaScript ohne Tag-Management-System implementieren.
exl-id: 25b9d768-c641-4f6c-a4ae-0d6c238c4776
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 89%

---

# AppMeasurement für JavaScript

AppMeasurement für JavaScript ist seit jeher eine gängige Methode zur Implementierung von Adobe Analytics. Da Tag Management Systems jedoch immer beliebter wird, wird empfohlen, [Tags in Adobe Experience Platform](../launch/overview.md) zu verwenden.

## Genereller Workflow zum Senden von Daten an Adobe mit JavaScript

1. Laden Sie die `AppMeasurement.js`-Datei. Diese Datei enthält die Bibliotheken, die zum Senden von Daten an Adobe erforderlich sind.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. Definieren Sie Konfigurationsvariablen in `AppMeasurement.js`. Wenn das Analytics-Objekt instanziiert wird, stellen diese Variablen sicher, dass die Datenerfassungseinstellungen korrekt sind. Eine vollständige Liste der Variablen, die Sie definieren können, finden Sie unter [Konfigurationsvariablen](../vars/config-vars/configuration-variables.md).

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.data.adobedc.net";
   ```

3. Definieren Sie Variablen auf Seitenebene im Seiten-Code Ihrer Website. Diese Variablen bestimmen spezifische Dimensionen und Metriken, die an Adobe gesendet werden. Eine vollständige Liste der Variablen, die Sie definieren können, finden Sie unter [Seitenvariablen](../vars/page-vars/page-variables.md).

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. Wenn alle Variablen auf Seitenebene definiert sind, senden Sie die Daten mit der `t()`-Methode an Adobe. Weitere Informationen finden Sie unter [t](../vars/functions/t-method.md).

   ```js
   s.t();
   ```
