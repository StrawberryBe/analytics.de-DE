---
title: cookieLifetime
description: Überschreiben Sie den Ablauf für Cookies, die AppMeasurement erstellt.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# cookieLifetime

Cookies, die von AppMeasurement eingestellt werden, laufen in der Regel zwei Jahre ab. Verwenden Sie die `cookieLifetime` Variable, um das Ablaufdatum für Cookies zu überschreiben, die von AppMeasurement gesetzt werden.

> [!NOTE] Diese Variable wirkt sich auf die Zählung und Zuordnung individueller Besucher aus. Gehen Sie beim Festlegen dieser Variablen mit Bedacht vor.

## Cookie-Lebensdauer beim Start der Adobe Experience Platform

Die Cookie-Lebensdauer ist eine Dropdown-Liste unter dem Akkordeon &quot; [!UICONTROL Cookies] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Cookies] &quot;, das die Dropdown-Liste &quot; [!UICONTROL Cookie-Lebensdauer] &quot;enthält.

Dieses Dropdown-Menü enthält die folgenden Werte:

* **Standard**: Cookie läuft nach 2 Jahren ab.
* **Keine**: AppMeasurement setzt keine Cookies.
* **Sitzung**: Cookie läuft am Ende der Sitzung des Besuchers ab.
* **Sekunden**: Das Cookie läuft ab, nachdem die angegebene Anzahl von Sekunden abgelaufen ist. Wenn Sie dieses Dropdown-Feld beispielsweise auf [!UICONTROL Sekunden] festlegen und `86400` in das benutzerdefinierte Feld platzieren, laufen Cookies nach genau 24 Stunden ab.

## s.cookieLifetime in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.cookieLifetime` Variable ist eine Zeichenfolge, die das Ablaufdatum der von AppMeasurement eingestellten Cookies bestimmt.

* Wenn auf `SESSION`festgelegt, laufen von AppMeasurement eingestellte Cookies nach Abschluss der Browsersitzung ab.
* Wenn dies auf `NONE`festgelegt ist, versucht AppMeasurement nicht, Cookies einzustellen.
* Bei Festlegung auf eine Ganzzahlzeichenfolge laufen die von AppMeasurement festgelegten Cookies ab, nachdem die angegebene Anzahl von Sekunden abgelaufen ist.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";

