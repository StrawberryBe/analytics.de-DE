---
title: visitorID
description: Verwenden Sie eine benutzerdefinierte Besucher-ID.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# visitorID

Adobe verwendet verschiedene Methoden zur Identifizierung von Besuchern Ihrer Site. Die `visitorID` Variable setzt alle anderen Methoden zur Besucheridentifizierung außer Kraft.

> [!IMPORTANT] Adobe empfiehlt, diese Variable nicht zu verwenden. Verwenden Sie stattdessen den [Adobe Experience Cloud-Identitätsdienst](https://docs.adobe.com/content/help/en/id-service/using/home.html) .

## Besucher-ID beim Start der Adobe Experience Platform

[!UICONTROL Besucher-ID] ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Cookies] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies] , das das Feld [!UICONTROL Besucher-ID] anzeigt.

Weisen Sie dieses Feld dem Datenelement zu, das Ihre benutzerdefinierte Besucher-ID enthält. Legen Sie für dieses Feld keinen statischen Wert fest.

## s.visitorID in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.visitorID` Variable ist eine Zeichenfolge, die einen benutzerdefinierten eindeutigen Bezeichner für den Besucher enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Verwenden Sie in dieser Variablen keine Bindestriche, Leerzeichen, Unterstriche oder Symbole.

> [!WARNING] Wenn Sie die `visitorID` Variable durch einen Besuch getrennt festlegen, ergeben die Daten zwei separate Unique Visitors.

```js
s.visitorID = "abc123";
```
