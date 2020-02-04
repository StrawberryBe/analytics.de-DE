---
title: linkType
description: Verwenden Sie die Variable "linkType", um zu bestimmen, zu welcher Linkverfolgungsdimension der Treffer gehört.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkType

Treffer zur Linkverfolgung können eine der drei Dimensionen ausfüllen:

* Benutzerspezifische Links
* Ausstiegslinks
* Download-Links

Verwenden Sie die `linkType` Variable, um festzulegen, welche Dimension Sie beim Ausführen der nächsten `tl()` Funktion füllen möchten.

## Linktyp beim Starten der Adobe Experience Platform

Legen Sie den Linktyp fest, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter &quot; [!UICONTROL Aktionen]&quot;auf das Symbol &quot;+&quot;
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Beacon senden fest.
6. Klicken Sie auf das `s.tl()` Optionsfeld, über das die Dropdownliste [!UICONTROL Linktyp] angezeigt wird.

Sie können dieses Dropdownmenü auf [!UICONTROL Benutzerspezifischen Link], [!UICONTROL Link]herunterladen oder [!UICONTROL Ausstiegslink]einstellen.

## s.linkType in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkType` Variable ist eine Zeichenfolge, die einen von drei Werten für einzelne Zeichen akzeptiert: `o`, `d`oder `e`. Wenn eine `tl()` Funktion ohne Linktyp aufgerufen wird, wird standardmäßig der benutzerdefinierte Link verwendet.

* `o` - Benutzerspezifische Links
* `d` - Download-Links
* `e` - Ausstiegslinks

> [!TIP] Diese Variable ist der zweite Parameter der `tl()` Funktion und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkType` Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()` Funktion festlegen möchten.

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
