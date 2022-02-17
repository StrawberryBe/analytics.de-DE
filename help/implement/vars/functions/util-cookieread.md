---
title: Util.cookieRead
description: Ruft den Wert aus einem Cookie ab.
feature: Variables
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 100%

---

# Util.cookieRead

Cookies können Informationen über Seiten in derselben Domain hinweg speichern und abrufen. Verwenden Sie die `Util.cookieRead()`-Methode, um einen Wert aus einem Cookie abzurufen.

## Lesen von Cookies mithilfe von Tags in Adobe Experience Platform

Sie können Cookies lesen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] [!UICONTROL Core] aus und setzen Sie [!UICONTROL Datenelementtyp] auf [!UICONTROL Cookie].
5. Geben Sie den Namen des Cookies in das Textfeld ein.

Der Wert des Cookies wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.cookieRead() in AppMeasurement und im benutzerdefinierten Code-Editor

Rufen Sie die `s.Util.cookieRead()`-Methode auf, um einen gewünschten Cookie-Wert zu lesen. Das einzige Argument ist eine Zeichenfolge, die erforderlich ist. Diese Methode gibt eine Zeichenfolge zurück, die den Cookie-Wert enthält. Wenn die Cookies nicht vorhanden sind, wird eine leere Zeichenfolge zurückgegeben.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
