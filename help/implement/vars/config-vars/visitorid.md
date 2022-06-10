---
title: visitorID
description: Verwenden Sie eine benutzerdefinierte Besucher-ID.
feature: Variables
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 86%

---

# visitorID

Adobe verwendet verschiedene Methoden zur Identifizierung von Besuchern Ihrer Website. Die `visitorID`-Variable setzt alle anderen Methoden zur Besucheridentifizierung außer Kraft.

>[!IMPORTANT]
>
>Adobe empfiehlt, diese Variable nicht zu verwenden. Verwenden Sie stattdessen den [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de).

## Besucher-ID-Überschreibung mithilfe des Web SDK

In Vorbereitung!

## Besucher-ID mit der Adobe Analytics-Erweiterung

[!UICONTROL Besucher-ID] ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Besucher-ID] angezeigt wird.

Weisen Sie dieses Feld dem Datenelement zu, das Ihre benutzerdefinierte Besucher-ID enthält. Legen Sie für dieses Feld keinen statischen Wert fest.

## s.visitorID in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.visitorID`-Variable ist eine Zeichenfolge, die eine benutzerdefinierte eindeutige Kennung für den Besucher enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Verwenden Sie in dieser Variablen keine Bindestriche, Leerzeichen, Unterstriche oder Symbole.

>[!WARNING]
>
>Wenn Sie die `visitorID`-Variable während eines Besuchs festlegen, führen die Daten zu zwei separaten Unique Visitors.

```js
s.visitorID = "abc123";
```

>[!CAUTION]
>
>Eine ungültige Implementierung von benutzerdefinierten Besucher-IDs kann zu fehlerhaften Daten und schlechter Berichtsleistung führen. Wenn diese Variable einen Standardwert enthält (z. B. `"0"` oder `"NULL"`), behandelt Adobe diese Treffer so, als wären sie derselbe Besucher. Diese Situation führt zu falschen Daten, da die Besucherzahlen niedrig sind und Segmente auf Besucherebene nicht wie erwartet funktionieren. Falsch implementierte benutzerdefinierte Besucher-IDs führen auch zu einer hohen Belastung der Verarbeitungs-Server, was die [Latenz](/help/technotes/latency.md) erhöht und die Berichtsleistung verringert.
