---
title: linkName
description: Legen Sie den Namen des Treffers für den benutzerspezifischen Link fest.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkName

Use the `linkName` variable to determine the dimension value of custom links, download links, or exit links when running the next [`tl()`](../functions/tl-method.md) method.

Wenn diese Variable leer ist, kehrt AppMeasurement zur [`linkURL`](linkurl.md)-Variablen zurück.

## Link-Name in Adobe Experience Platform Launch

Sie können das Feld für den Link-Namen festlegen, wenn Sie eine Regel zum Senden eines Beacons konfigurieren.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie [!UICONTROL Aktionstyp] auf „Beacon senden“.
6. Klicken Sie auf die Optionsschaltfläche `s.tl()`, wodurch das Feld [!UICONTROL Link-Name] angezeigt wird.

## s.linkName in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkName`-Variable ist eine Zeichenfolge, die den Dimensionswert für benutzerspezifische Links, Downloadlinks oder Exitlinks bestimmt (je nachdem, was [`s.linkType`](linktype.md) ist). Sie kann bis zu 100 Byte enthalten.

>[!TIP] Diese Variable ist der dritte Parameter der `tl()` Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. However, you can use the `linkName` variable if you do not want to set values as arguments in the `tl()` method.

```js
s.linkName = "Example custom link";
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
