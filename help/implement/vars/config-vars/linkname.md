---
title: linkName
description: Legen Sie den Namen des Treffers für den benutzerspezifischen Link fest.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 80%

---


# linkName

Use the `linkName` variable to determine the dimension item of custom links, download links, or exit links when running the next [`tl()`](../functions/tl-method.md) method.

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

The `s.linkName` variable is a string that determines the dimension item for custom links, download links, or exit links (depending on what [`s.linkType`](linktype.md) is). Sie kann bis zu 100 Byte enthalten.

>[!TIP]
>
>Diese Variable ist der dritte Parameter der `tl()`-Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkName`-Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()`-Methode festlegen möchten.

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
