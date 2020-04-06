---
title: linkType
description: Verwenden Sie die Variable „linkType“, um zu bestimmen, zu welcher Linktracking-Dimension der Treffer gehört.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkType

Linktracking-Treffer können eine der drei Dimensionen ausfüllen:

* Benutzerspezifische Links
* Exitlinks
* Downloadlinks

Verwenden Sie die `linkType`-Variable, um festzulegen, welche Dimension Sie beim Ausführen der nächsten [`tl()`](../functions/tl-method.md)-Funktion füllen möchten.

## Link-Typ in Adobe Experience Platform Launch

Legen Sie den Link-Typ fest, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Under [!UICONTROL Actions], click the &#39;+&#39; icon
5. Set the [!UICONTROL Extension] dropdown to Adobe Analytics, and the [!UICONTROL Action Type] to Send Beacon.
6. Click the `s.tl()` radio button which reveals the [!UICONTROL Link Type] dropdown.

Sie können dieses Dropdown-Menü auf [!UICONTROL Custom Link], [!UICONTROL Download Link]oder [!UICONTROL Exit Link]einstellen.

## s.linkType in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkType`-Variable ist eine Zeichenfolge, die einen von drei Einzelzeichenwerten akzeptiert: `o`, `d` oder `e`. If a `tl()` method is called without a link type, it defaults to Custom link.

* `o` – Benutzerspezifische Links
* `d` – Downloadlinks
* `e` – Exitlinks

>[!TIP] Diese Variable ist der zweite Parameter der `tl()` Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. However, you can use the `linkType` variable if you do not want to set values as arguments in the `tl()` method.

```js
s.linkType = "e";
```

## Beispiel

Die folgenden beiden beispielhaften Linktracking-Aufrufe sind funktionell identisch. Es handelt sich um verschiedene Methoden, um denselben Linktracking-Treffer zu erzielen.

```js
// Set link tracking arguments as individual variables
s.linkType = "d";
s.linkName = "Example download link";
s.tl();

// Set link tracking arguments directly in the tl() function
s.tl(this,"d","Example download link");
```
