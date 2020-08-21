---
title: linkType
description: Verwenden Sie die Variable „linkType“, um zu bestimmen, zu welcher Linktracking-Dimension der Treffer gehört.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '239'
ht-degree: 100%

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
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie [!UICONTROL Aktionstyp] auf „Beacon senden“.
6. Klicken Sie auf die Optionsschaltfläche `s.tl()`, wodurch das Dropdown-Menü [!UICONTROL Link-Typ] angezeigt wird.

Sie können dieses Dropdown-Menü auf [!UICONTROL Benutzerspezifischer Link], [!UICONTROL Downloadlink] oder [!UICONTROL Exitlink] setzen.

## s.linkType in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkType`-Variable ist eine Zeichenfolge, die einen von drei Einzelzeichenwerten akzeptiert: `o`, `d` oder `e`. Wenn eine `tl()`-Methode ohne Link-Typ aufgerufen wird, wird standardmäßig der benutzerspezifische Link verwendet.

* `o` – Benutzerspezifische Links
* `d` – Downloadlinks
* `e` – Exitlinks

>[!TIP]
>
>Diese Variable ist der zweite Parameter der `tl()`-Methode und muss normalerweise nicht als eigenständige Variable festgelegt werden. Sie können die `linkType`-Variable jedoch verwenden, wenn Sie Werte nicht als Argumente in der `tl()`-Methode festlegen möchten.

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
