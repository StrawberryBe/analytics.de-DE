---
title: clearVars
description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# clearVars

Bei einigen Implementierungen, z. B. bei Einzelseitenanwendungen, sind mehrere Treffer erforderlich, die beim Laden derselben Seite gesendet werden. Verwenden Sie die `clearVars` Methode, um Variablenwerte zu löschen, damit sie nicht auf nachfolgenden Treffern bestehen bleiben.

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
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter &quot; [!UICONTROL Aktionen]&quot;auf das Symbol &quot;+&quot;
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdown-Menü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL löschen]fest.

## s.clearVars() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Sie können die `s.clearVars()` Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie die Analytics-Objektinstanz instanziiert haben.

```js
s.clearVars();
```
