---
title: s_gi()
description: Erstellen und verfolgen Sie Instanzen von AppMeasurement.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '341'
ht-degree: 100%

---


# s_gi

Die `s_gi()`-Funktion instanziiert oder findet eine Instanz von AppMeasurement nach Report Suite-ID. AppMeasurement verfolgt jede erstellte Instanz, und die `s_gi()`-Funktion gibt die vorhandene Instanz für eine Berichtssuite zurück, falls eine solche existiert. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt.

## s_gi() in Adobe Experience Platform Launch

Die Analytics-Erweiterung instanziiert und verwaltet das Tracking-Objekt für Sie. Sie können jedoch auch ein globales Tracking-Objekt im Akkordeon [!UICONTROL Bibliotheksverwaltung] festlegen, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Bibliotheksverwaltung] und wählen Sie eine andere Optionsschaltfläche als [!UICONTROL Bibliothek für mich verwalten] aus.

Im Textfeld für globale Variablen können Sie ein benutzerdefiniertes Tracking-Objekt festlegen. Der Standardwert lautet `s`.

## s_gi() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Rufen Sie die `s_gi()`-Funktion auf, um ein Tracking-Objekt zu instanziieren. Das einzige Argument enthält eine kommagetrennte Zeichenfolge von Report Suite-IDs. Das Argument der Report Suite-ID ist erforderlich.

>[!TIP]
>
>Adobe empfiehlt, die `s`-Variable als Tracking-Objekt zu verwenden. Adobe verwendet `s` in seiner Dokumentation, Implementierungsbeispielen und Plug-ins. Sie können jedoch jede beliebige Variable verwenden, solange Sie auf Ihrer Website konsistent sind.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

>[!CAUTION]
>
>Die folgenden Abschnitte und Beispiele enthalten komplexe Implementierungsthemen. Testen Sie Ihre Implementierung gründlich und verfolgen Sie wichtige Anpassungen im [Lösungsdesigndokument](../../prepare/solution-design.md) Ihres Unternehmens.

## Verwalten mehrerer Implementierungen mit verschiedenen Tracking-Objekten

Sie können verschiedene Daten an verschiedene Report Suites senden, wenn Sie mehrere Tracking-Objekte instanziieren. Diese beiden Tracking-Objekte funktionieren unabhängig voneinander.

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

## Wiederherstellen von AppMeasurement-Variablen nach dem Überschreiben des s-Objekts

Einige Drittanbieter-Tools können auch das JavaScript-`s`-Objekt verwenden. Wenn Sie versehentlich das `s`-Objekt auf Ihrer Website überschreiben, können Sie `s_gi` mit demselben RSID-Zeichenfolgenargument aufrufen, um alle überschriebenen Variablen und Methoden wiederherzustellen.

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

## Referenzieren desselben Tracking-Objekts mit mehreren Variablen

Wenn zwei Variablen auf dieselbe `s_gi()`-Funktion mit derselben Report Suite verweisen, können Sie die Variablen austauschbar verwenden.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
