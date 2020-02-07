---
title: tl
description: Senden Sie einen Link-Verfolgungsaufruf an Adobe.
translation-type: tm+mt
source-git-commit: 8494e8bb08b45006b357dd114e6bf9507f0cd54a

---


# tl

Die `tl` Methode ist eine wichtige Kernkomponente von Adobe Analytics. Es nimmt alle auf der Seite definierten Analytics-Variablen auf, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungsserver. Es funktioniert ähnlich wie die `t` Methode, allerdings inkrementiert diese Methode keine Seitenansichten. Es ist nützlich, um Links und andere Elemente zu verfolgen, die nicht als vollständige Seitenladung betrachtet werden.

Wenn `trackDownloadLinks` oder `trackExternalLinks` aktiviert, ruft AppMeasurement automatisch die `tl` Methode auf, um Download- und Ausstiegslink-Verfolgungsdaten zu senden. Wenn Ihr Unternehmen mehr Kontrolle über die zu verfolgenden Links und deren Verhalten hat, können Sie die `tl` Methode manuell aufrufen. Benutzerspezifische Links können nur manuell verfolgt werden.

## Link-Verfolgungsaufruf beim Start der Adobe Experience Platform

&quot;Launch&quot;hat einen eigenen Standort, der einen Link-Verfolgungsaufruf einrichtet.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. Klicken Sie unter &quot; [!UICONTROL Aktionen]&quot;auf das Symbol &quot;+&quot;
1. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Beacon senden fest.
1. Click the `s.tl()` radio button.

Sie können keine optionalen Argumente in Launch festlegen.

## s.tl()-Methode in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Rufen Sie die `s.tl()` Methode auf, wenn Sie einen Verfolgungsaufruf an Adobe senden möchten.

```js
s.tl();
```

Optional akzeptiert diese Methode mehrere Argumente:

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### Link-Objekt

Das link-Objekt-Argument bestimmt, ob der Browser bis zu 500 ms wartet, bevor er von der Seite weg navigiert. Wenn eine Bildanforderung früher als 500 ms gesendet wird, navigiert die Seite sofort zum angeklickten Link.

> [!NOTE] AppMeasurement aktiviert automatisch die `useBeacon` Variable für Exitlinks, sodass dieses Argument in modernen Browsern nicht mehr benötigt wird. Dieses Argument wurde in früheren Versionen von AppMeasurement häufiger verwendet.

* `this`: Warten Sie bis zu 500 ms, damit AppMeasurement Zeit zum Senden einer Bildanforderung hat. Standardwert.
* `true`: Nicht warten.

```JavaScript
// Include a 500ms delay
s.tl(this);

// Do not include a 500ms delay
s.tl(true);
```

### Link-Typ

Das Linktypargument ist eine Zeichenfolge aus einem einzelnen Buchstaben, die den Typ des Linkverfolgungsaufrufs bestimmt. Es entspricht dem Festlegen der `linkType` Variablen.

```js
// Send a custom link
s.tl(true,"o");

// Send a download link
s.tl(true,"d");

// Send an exit link
s.tl(true,"e");
```

### Linkname

Das Linknamenargument ist eine Zeichenfolge, die den Wert der Linktracking-Dimension bestimmt. Es entspricht dem Festlegen der `linkName` Variablen.

```js
s.tl(true,"d","Example download link");
```

### Variablenüberschreibungen

Ermöglicht die Änderung von Variablenwerten für einen einzelnen Aufruf. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md) .

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## Beispiele und Anwendungsfälle

Senden Sie einen einfachen Link-Verfolgungsaufruf direkt in einen HTML-Link:

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

Verwenden Sie JavaScript, um einen einfachen Linktracking-Aufruf mithilfe von Methodenargumenten durchzuführen:

```JavaScript
s.tl(true,"o","Example link");
```

Verwenden Sie JavaScript, um denselben einfachen Linkverfolgungsaufruf mit separaten Variablen durchzuführen:

```js
s.linkType = "o";
s.linkName = "Example link";
s.tl();
```

### Linktracking-Aufrufe innerhalb einer benutzerdefinierten Funktion

Sie können den Linktracking-Code in einer eigenständige JavaScript-Funktion zusammenfassen, die auf der Seite oder in einer verknüpften JavaScript-Datei definiert ist. Aufrufe können dann in der onClick-Funktion jedes Links erfolgen. Legen Sie Folgendes in einer JavaScript-Datei fest:

```JavaScript
function trackClickInteraction(name){
  s.linkTrackVars = "eVar1,eVar2";
  s.eVar1 = name;
  s.eVar2 = s.pageName;
  s.tl(true,"o",name);
}
```

Sie können die Funktion dann immer dann aufrufen, wenn Sie einen bestimmten Link verfolgen möchten:

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

### Vermeiden der Verfolgung doppelter Links

Wenn AppMeasurement aktiviert `trackDownloadLinks` oder `trackExternalLinks` aktiviert ist, führt automatisch einen Link-Verfolgungsaufruf durch, wenn die richtigen Filter übereinstimmen. Wenn Sie auch manuell `s.tl()` für diese Link-Klicks aufrufen, können Sie doppelte Daten an Adobe senden. Duplizierte Daten führen zu einer Erhöhung der Berichtszahlen und deren Genauigkeit.

Beispielsweise sendet die folgende Funktion zwei Linktracking-Aufrufe für denselben Link-Klick (manuelle und automatische Downloadlinks):

```JavaScript
function trackDownload(obj) {
  s.tl(obj,"d","Example PDF download");
}
```

Mithilfe der folgenden geänderten Funktion können Sie doppelte Linktracking-Aufrufe vermeiden. Zunächst wird geprüft, ob ein Linkobjekt vorhanden ist, und es wird nur ein manueller Linkverfolgungsaufruf gesendet, wenn das Linkobjekt eine leere Zeichenfolge ist.

```JavaScript
function linkCode(obj) {
  var lt = obj.href != null ? s.lt(obj.href) : "";
  if (lt=="") {
    s.tl(obj,"d","Example PDF download");
  }
}
```
