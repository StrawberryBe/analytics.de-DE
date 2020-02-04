---
title: s_gi()
description: Erstellen und verfolgen Sie Instanzen von AppMeasurement.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# s_gi

Die `s_gi()` Funktion instanziiert oder findet eine Instanz von AppMeasurement nach Report Suite-ID. AppMeasurement keeps track of every instance created, and `s_gi()` returns the existing instance for a report suite if one exists. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt.

## s_gi() in Adobe Experience Platform Launch

Die Analytics-Erweiterung instanziiert und verwaltet das Verfolgungsobjekt für Sie. Sie können jedoch auch ein globales Verfolgungsobjekt im Akkordeon &quot; [!UICONTROL Bibliotheksverwaltung] &quot;festlegen, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Bibliotheksverwaltung] &quot;und wählen Sie ein anderes Optionsfeld als &quot;Bibliothek für mich [!UICONTROL verwalten&quot;].

Im Textfeld für globale Variable können Sie ein benutzerdefiniertes Verfolgungsobjekt festlegen. Its default value is `s`.

## s_gi() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Rufen Sie die `s_gi()` Funktion auf, um ein Verfolgungsobjekt zu instanziieren. Das einzige Argument enthält eine kommagetrennte Zeichenfolge aus Report Suite-IDs. Das Argument der Report Suite-ID ist erforderlich.

> [!TIP] Adobe empfiehlt, die `s` Variable als Verfolgungsobjekt zu verwenden. Adobe verwendet `s` in seiner Dokumentation, Implementierungsbeispiele und Plug-ins. Sie können jedoch jede beliebige Variable verwenden, solange Sie auf Ihrer Site konsistent sind.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

> [!WARNING] Die folgenden Abschnitte und Beispiele enthalten komplexe Implementierungsthemen. Testen Sie Ihre Implementierung gründlich und verfolgen Sie wichtige Anpassungen im [Lösungsdesigndokument](../../prepare/solution-design.md)Ihres Unternehmens.

## Verwalten mehrerer Implementierungen mit verschiedenen Verfolgungsobjekten

Sie können verschiedene Daten an verschiedene Report Suites senden, wenn Sie mehrere Verfolgungsobjekte instanziieren. Diese beiden Verfolgungsobjekte funktionieren unabhängig voneinander.

```js
// Instantiate two separate tracking objects to two different report suites
var s = s_gi('examplersid1');
var z = s_gi('examplersid2');

// The s object and z object contain their own independent Analytics variables simultaneously
s.pageName = "Example page name 1";
z.pageName = "Example page name 2";

// Send data to the examplersid1 report suite
s.t();

// Send data to the examplersid2 report suite
z.t();
```

## Stellen Sie AppMeasurement-Variablen nach dem Überschreiben des s-Objekts wieder her

Einige Werkzeuge von Drittanbietern können auch das JavaScript- `s` Objekt verwenden. Wenn Sie versehentlich das `s` Objekt auf Ihrer Site überschreiben, können Sie `s_gi` mit demselben RSID-Zeichenfolgenargument aufrufen, um alle überschriebenen Variablen und Methoden wiederherzustellen.

```js
// Step 1: Instantiate the tracking object
var s = s_gi("examplersid");

// Step 2: Set eVar1
s.eVar1 = "Example value";

// Step 3: Accidentally overwrite the tracking object
s = "3rd party tool";

// Step 4: If you attempt to send a tracking call, an error is returned. Instead, re-instantiate the tracking object
s = s_gi("examplersid");

// Step 5: The previous values of all variables are preserved. You can send a tracking call and eVar1 is correctly set
s.t();
```

## Auf dasselbe Verfolgungsobjekt mit mehreren Variablen verweisen

Wenn zwei Variablen auf dieselbe `s_gi()` Funktion mit derselben Report Suite verweisen, können Sie die Variablen austauschbar verwenden.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
