---
title: referrer
description: Überschreiben Sie die automatisch erfasste verweisende Stelle für einen Treffer.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# referrer

Die `referrer` Variable setzt die automatisch erfasste verweisende Stelle in Berichten außer Kraft. Diese Variable ist hilfreich in Situationen, in denen die verweisende Stelle verloren gehen könnte, z. B. bei Umleitungen oder vorübergehender Weiterleitung des Besuchers an einen Zahlungsverarbeiter. Diese Variable hilft beim Ausfüllen der Dimensionen &quot;Verweisende Stelle&quot;und &quot;Verweisende Domäne&quot;.

## Verweisende Stelle beim Starten der Adobe Experience Platform

Sie können Referrer entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Verweisende Stelle] .

Sie können die verweisende Stelle auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.referrer in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.referrer` Variable ist eine Zeichenfolge, die die URL der vorherigen Seite enthält. Diese Variable kann maximal 255 Byte speichern. Werte, die größer als 255 Byte sind, werden abgeschnitten. AppMeasurement setzt diese Variable automatisch auf `document.referrer`; Sie müssen diese Variable nur dann festlegen, wenn Sie den automatisch erfassten Wert außer Kraft setzen möchten.

```js
s.referrer = "https://example.com";
```

Vermeiden Sie es, diese Variable auf Nicht-URL-Werte festzulegen.

## Beispiel

Viele Organisationen beschäftigen sich mit Implementierungen rund um Weiterleitungen. Mit dem [`getQueryParam`](../functions/util-getqueryparam.md) Dienstprogramm können Sie Referrer aus der URL abrufen, wenn diese auf Ihrer Site gespeichert ist. Vergewissern Sie sich, dass Sie alle in der Abfragezeichenfolge enthaltenen Werte mit einer URL kodieren.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
