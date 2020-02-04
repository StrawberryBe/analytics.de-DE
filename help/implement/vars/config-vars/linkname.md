---
title: linkName
description: Legen Sie den Namen des Treffers für den benutzerspezifischen Link fest.
translation-type: tm+mt
source-git-commit: e500332fe16887fa004858b07b59644837e183aa

---


# linkName

Verwenden Sie die `linkName` Variable, um den Dimensionswert von benutzerspezifischen Links, Downloadlinks oder Exitlinks beim Ausführen der nächsten `tl()` Funktion zu bestimmen.

Wenn diese Variable leer ist, kehrt AppMeasurement zur `linkURL` Variablen zurück.

## Linkname beim Start der Adobe Experience Platform

Sie können das Feld für den Linknamen festlegen, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter &quot; [!UICONTROL Aktionen]&quot;auf das Symbol &quot;+&quot;
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Beacon senden fest.
6. Klicken Sie auf das `s.tl()` Optionsfeld, über das das Feld [!UICONTROL Linkname] angezeigt wird.

## s.linkName in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `s.linkName` Variable ist eine Zeichenfolge, die den Dimensionswert für benutzerspezifische Links, Downloadlinks oder Exitlinks bestimmt (je nachdem, was `s.linkType` ist). Er kann bis zu 100 Byte lang sein.

> [!TIP] Diese Variable ist der dritte Parameter der `tl()` Funktion und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkName` Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()` Funktion festlegen möchten.

```js
s.linkName = "Example custom link";
```

## Beispiel

Die folgenden beiden Beispiel-Linkverfolgungsaufrufe sind funktionell identisch. Es gibt verschiedene Methoden, um denselben Link-Verfolgungshit zu erzielen.

```js
// Set link tracking arguments as individual variables
s.linkType = "d";
s.linkName = "Example download link";
s.tl();

// Set link tracking arguments directly in the tl() function
s.tl(this,"d","Example download link");
```
