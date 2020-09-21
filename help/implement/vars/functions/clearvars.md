---
title: clearVars
description: Löscht die folgenden Werte aus dem Instanzobjekt. Diese Funktion entfernt die Elemente (legt sie als „undefiniert“ fest).
translation-type: ht
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---


# clearVars

Einige Implementierungen, z. B. bei Einzelseitenanwendungen, erfordern mehrere Treffer, die mit demselben Seitenladevorgang gesendet werden. Verwenden Sie die `clearVars()`-Methode, um Variablenwerte zu löschen, damit sie nicht auf nachfolgenden Treffern bestehen bleiben.

Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Der einzige Zweck besteht darin, Variablenwerte aus dem Instanzobjekt zu löschen. Diese Methode setzt die folgenden Elemente auf `undefined`:

* `prop1` – `prop75`
* `eVar` – `eVar250`
* `hier1` – `hier5`
* `list1` – `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## Löschen von Variablen in Adobe Experience Platform Launch

Legen Sie beim Konfigurieren einer Regel die Aktion „Variablen löschen“ fest.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen löschen].

## s.clearVars() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Sie können die `s.clearVars()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie die Analytics-Objektinstanz instanziiert haben.

```js
s.clearVars();
```
