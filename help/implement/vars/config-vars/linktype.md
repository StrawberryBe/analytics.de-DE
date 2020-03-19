---
title: linkType
description: Verwenden Sie die Variable "linkType", um zu bestimmen, zu welcher Linkverfolgungsdimension der Treffer gehört.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkType

Treffer zur Linkverfolgung können eine der drei Dimensionen ausfüllen:

* Benutzerspezifische Links
* Ausstiegslinks
* Download-Links

Verwenden Sie die `linkType` Variable, um festzulegen, welche Dimension Sie beim Ausführen der nächsten [`tl()`](../functions/tl-method.md) Funktion füllen möchten.

## Linktyp beim Starten der Adobe Experience Platform

Legen Sie den Linktyp fest, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Actions]dem Symbol &quot;+&quot;auf
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und das [!UICONTROL Action Type] auf Beacon senden fest.
6. Klicken Sie auf das `s.tl()` Optionsfeld, über das die [!UICONTROL Link Type] Dropdownliste angezeigt wird.

Sie können dieses Dropdown-Menü auf [!UICONTROL Custom Link], [!UICONTROL Download Link]oder [!UICONTROL Exit Link]einstellen.

## s.linkType im AppMeasurement- und Starten des benutzerdefinierten Code-Editors

Die `s.linkType` Variable ist eine Zeichenfolge, die einen von drei Werten für einzelne Zeichen akzeptiert: `o`, `d`oder `e`. Wenn eine `tl()` Methode ohne Linktyp aufgerufen wird, wird standardmäßig der benutzerdefinierte Link verwendet.

* `o` - Benutzerspezifische Links
* `d` - Download-Links
* `e` - Ausstiegslinks

> [!TIP] Diese Variable ist der zweite Parameter der `tl()` Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkType` Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()` Methode festlegen möchten.

```js
s.linkType = "e";
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
