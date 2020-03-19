---
title: clearVars
description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# clearVars

Bei einigen Implementierungen, z. B. bei Einzelseitenanwendungen, sind mehrere Treffer erforderlich, die beim Laden derselben Seite gesendet werden. Verwenden Sie die `clearVars()` Methode, um Variablenwerte zu löschen, damit sie nicht auf nachfolgenden Treffern bestehen bleiben.

Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Der einzige Zweck besteht darin, Variablenwerte aus dem Instanzobjekt zu löschen. Diese Methode setzt die folgenden Elemente auf `undefined`:

* `prop1` - `prop75`
* `eVar` - `eVar250`
* `hier1` - `hier5`
* `list1` - `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## Variablen beim Start der Adobe Experience Platform löschen

Legen Sie beim Konfigurieren einer Regel die Aktion &quot;Variablen löschen&quot;fest.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Actions]dem Symbol &quot;+&quot;auf
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Clear Variables].

## s.clearVars() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Sie können die `s.clearVars()` Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie die Analytics-Objektinstanz instanziiert haben.

```js
s.clearVars();
```
