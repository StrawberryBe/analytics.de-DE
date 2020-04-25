---
title: cookieLifetime
description: Überschreiben Sie die Gültigkeit für von AppMeasurement erstellte Cookies.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# cookieLifetime

Von AppMeasurement gesetzte Cookies haben in der Regel eine Gültigkeit von 2 Jahren. Verwenden Sie die `cookieLifetime`-Variable, um das Ablaufdatum für Cookies zu überschreiben, die von AppMeasurement gesetzt werden.

>[!NOTE] Diese Variable wirkt sich auf die Zählung und Zuordnung von Unique Visitors aus. Gehen Sie beim Festlegen dieser Variablen mit Bedacht vor.

## Cookie-Lebensdauer in Adobe Experience Platform Launch

Cookie-Lebensdauer ist ein Dropdown-Menü unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Dropdown-Menü [!UICONTROL Cookie-Lebensdauer] angezeigt wird.

Dieses Dropdown-Menü enthält die folgenden Werte:

* **Standardmäßig**: Cookie läuft nach 2 Jahren ab.
* **Keine**: AppMeasurement setzt keine Cookies.
* **Sitzung**: Cookie läuft am Ende der Sitzung des Besuchers ab.
* **Sekunden**: Cookie läuft nach der angegebenen Anzahl von Sekunden ab. Wenn Sie dieses Dropdown-Menü beispielsweise auf [!UICONTROL Sekunden] festlegen und `86400` in das benutzerdefinierte Feld platzieren, laufen Cookies nach genau 24 Stunden ab.

## s.cookieLifetime in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.cookieLifetime`-Variable ist eine Zeichenfolge, die das Ablaufdatum der von AppMeasurement gesetzten Cookies festlegt.

* Wenn auf `SESSION` gesetzt, laufen von AppMeasurement gesetzte Cookies nach Abschluss der Browser-Sitzung ab.
* Wenn auf `NONE` gesetzt, versucht AppMeasurement nicht, Cookies zu setzen.
* Wenn auf eine ganzzahlige Zeichenfolge gesetzt, laufen die von AppMeasurement gesetzten Cookies nach Ablauf der angegebenen Anzahl von Sekunden ab.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";

