---
title: Util.cookieRead
description: Ruft den Wert aus einem Cookie ab.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Util.cookieRead

Cookies können Informationen über Seiten in derselben Domäne hinweg speichern und abrufen. Verwenden Sie die `Util.cookieRead` Methode, um einen Wert aus einem Cookie abzurufen.

## Cookies in Adobe Experience Platform Launch lesen

Sie können Cookies lesen, indem Sie Werte in Datenelementen festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Legen Sie die [!UICONTROL Erweiterungs] -Dropdownliste auf [!UICONTROL Core]und den [!UICONTROL Datenelementtyp] auf [!UICONTROL Cookie]fest.
5. Geben Sie den Namen des Cookies in das Textfeld ein.

Der Wert des Cookies wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.cookieRead() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Rufen Sie die `s.Util.cookieRead()` Methode auf, um einen gewünschten Cookie-Wert zu lesen. Das einzige Argument ist eine Zeichenfolge, die erforderlich ist. Diese Methode gibt eine Zeichenfolge zurück, die den Cookie-Wert enthält. Wenn die Cookies nicht vorhanden sind, wird eine leere Zeichenfolge zurückgegeben.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
