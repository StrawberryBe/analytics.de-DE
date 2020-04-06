---
title: visitorID
description: Verwenden Sie eine benutzerdefinierte Besucher-ID.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# visitorID

Adobe verwendet verschiedene Methoden zur Identifizierung von Besuchern Ihrer Website. Die `visitorID`-Variable setzt alle anderen Methoden zur Besucheridentifizierung außer Kraft.

>[!IMPORTANT] Adobe empfiehlt, diese Variable nicht zu verwenden. Verwenden Sie stattdessen den [Adobe Experience Cloud-Identitätsdienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html).

## Besucher-ID in Adobe Experience Platform Launch

[!UICONTROL Visitor ID] ist ein Feld unter dem [!UICONTROL Cookies] Akkordeon, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Cookies] Akkordeon, das das [!UICONTROL Visitor ID] Feld aufdeckt.

Weisen Sie dieses Feld dem Datenelement zu, das Ihre benutzerdefinierte Besucher-ID enthält. Legen Sie für dieses Feld keinen statischen Wert fest.

## s.visitorID in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.visitorID`-Variable ist eine Zeichenfolge, die eine benutzerdefinierte eindeutige Kennung für den Besucher enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Verwenden Sie in dieser Variablen keine Bindestriche, Leerzeichen, Unterstriche oder Symbole.

>[!WARNING] Wenn Sie die `visitorID`-Variable während eines Besuchs festlegen, führen die Daten zu zwei separaten Unique Visitors.

```js
s.visitorID = "abc123";
```
