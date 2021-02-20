---
title: Util.cookieRead
description: Ruft den Wert aus einem Cookie ab.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 100%

---


# Util.cookieRead

Cookies können Informationen über Seiten in derselben Domäne hinweg speichern und abrufen. Verwenden Sie die `Util.cookieRead()`-Methode, um einen Wert aus einem Cookie abzurufen.

## Lesen von Cookies in Adobe Experience Platform Launch

Sie können Cookies lesen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] [!UICONTROL Core] aus und setzen Sie [!UICONTROL Datenelementtyp] auf [!UICONTROL Cookie].
5. Geben Sie den Namen des Cookies in das Textfeld ein.

Der Wert des Cookies wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.cookieRead() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Rufen Sie die `s.Util.cookieRead()`-Methode auf, um einen gewünschten Cookie-Wert zu lesen. Das einzige Argument ist eine Zeichenfolge, die erforderlich ist. Diese Methode gibt eine Zeichenfolge zurück, die den Cookie-Wert enthält. Wenn die Cookies nicht vorhanden sind, wird eine leere Zeichenfolge zurückgegeben.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
