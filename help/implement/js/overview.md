---
title: Implementieren von Adobe Analytics mit AppMeasurement für JavaScript
description: Erfahren Sie, wie Sie Adobe Analytics mit JavaScript ohne Tag-Management-System implementieren.
feature: Implementation Basics
source-git-commit: 93e16a538d6dc05c9cbf0703664aa5320f45b731
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 45%

---

# Implementieren von Adobe Analytics mit AppMeasurement für JavaScript

AppMeasurement für JavaScript ist seit jeher eine gängige Methode zur Implementierung von Adobe Analytics. Da Tag-Management-Systeme jedoch immer beliebter werden, wird empfohlen, [Tags in Adobe Experience Platform](../launch/overview.md) zu verwenden.

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Übersicht über das Implementieren von Adobe Analytics mit AppMeasurement](../assets/appmeasurement-annotated.png)

<table>

<tr>
<th style="width:5%"></th><th><b>Aufgabe</b></th><th><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td><td>Stellen Sie sicher, dass <b>Report Suite definiert haben</b></td><td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td><td><b>Herunterladen des erforderlichen JavaScript-Codes für AppMeasurement</b> vom Code-Manager aus. Entpacken Sie die Datei.</td><td><a href="../../admin/admin/code-manager-admin.md">Code-Manager</a></td>
</tr>

<tr>
<td>3</td><td><b>Hinzufügen <code>AppMeasurement.js</code> in die Vorlagendatei Ihrer Website</b>. Der Code enthält die Bibliotheken, die zum Senden von Daten an Adobe erforderlich sind.

```html
<head>
  <script src="AppMeasurement.js"></script>
  …
</head>
```

</td><td></td>
</tr>

<tr>
<td>4</td><td><b>Definieren Sie Konfigurationsvariablen in <code>AppMeasurement.js</code></b>. Wenn das Analytics-Objekt instanziiert wird, stellen diese Variablen sicher, dass die Datenerfassungseinstellungen korrekt sind.

```JavaScript
// Instantiate the Analytics tracking object with report suite ID
var s_account = "examplersid";
var s=s_gi(s_account);
 
// Make sure data is sent to the correct tracking server
s.trackingServer = "example.data.adobedc.net";
```

</td><td><a href="../vars/config-vars/configuration-variables.md">Konfigurationsvariablen</a></td>
</tr>

<tr>
<td>5</td><td><b>Definieren Sie Variablen auf Seitenebene im Seiten-Code Ihrer Website</b>. Diese Variablen bestimmen spezifische Dimensionen und Metriken, die an Adobe gesendet werden.

```js
s.pageName = "Example page";
s.eVar1 = "Example eVar";
s.events = "event1";
```

</td><td><a href="../vars/page-vars/page-variables.md">Seitenvariablen</a></td>
</tr>

<tr>
<td>6</td><td><b>Senden Sie die Daten an die Adobe mit der <code>t()</code> method</b>, wenn alle Seitenvariablen definiert sind.

```js
s.t();
```

</td><td><a href="../vars/functions/t-method.md">t()-Methode</a></td>
</tr>

<tr>
<td>7</td><td><b>Implementierung erweitern und validieren</b> bevor sie in die Produktion verschoben wird.</b></td><td></td>
</tr>

</table>

## Zusätzliche Ressourcen

- [Übersicht über Variablen, Funktionen, Methoden und Plug-ins](../vars/overview.md)
