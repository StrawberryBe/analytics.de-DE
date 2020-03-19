---
title: linkName
description: Legen Sie den Namen des Treffers für den benutzerspezifischen Link fest.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkName

Verwenden Sie die `linkName` Variable, um den Dimensionswert von benutzerspezifischen Links, Downloadlinks oder Exitlinks beim Ausführen der nächsten [`tl()`](../functions/tl-method.md) Methode zu bestimmen.

Wenn diese Variable leer ist, kehrt AppMeasurement zur [`linkURL`](linkurl.md) Variablen zurück.

## Linkname beim Start der Adobe Experience Platform

Sie können das Feld für den Linknamen festlegen, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Actions]dem Symbol &quot;+&quot;auf
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und das [!UICONTROL Action Type] auf Beacon senden fest.
6. Klicken Sie auf das `s.tl()` Optionsfeld, mit dem das [!UICONTROL Link Name] Feld angezeigt wird.

## s.linkName in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `s.linkName` Variable ist eine Zeichenfolge, die den Dimensionswert für benutzerspezifische Links, Downloadlinks oder Exitlinks bestimmt (je nachdem, was [`s.linkType`](linktype.md) ist). Er kann bis zu 100 Byte lang sein.

> [!TIP] Diese Variable ist der dritte Parameter der `tl()` Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkName` Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()` Methode festlegen möchten.

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
