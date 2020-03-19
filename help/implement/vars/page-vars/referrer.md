---
title: referrer
description: Überschreiben Sie den automatisch erfassten Werber für einen Treffer.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# referrer

Die `referrer` Variable setzt den automatisch erfassten Werber in Berichten außer Kraft. Diese Variable ist hilfreich in Situationen, in denen der Werber verloren gehen könnte, z. B. bei Umleitungen oder vorübergehender Weiterleitung des Besuchers an einen Zahlungsverarbeiter. Diese Variable hilft beim Ausfüllen der Dimensionen &quot;Werber&quot;und &quot;Verweisende Domäne&quot;.

## Werber beim Starten der Adobe Experience Platform

Sie können Werber entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Referrer] section.

Sie können Werber auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.Werber in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Die `s.referrer` Variable ist eine Zeichenfolge, die die URL der vorherigen Seite enthält. Diese Variable kann maximal 255 Byte speichern. Werte, die größer als 255 Byte sind, werden abgeschnitten. AppMeasurement setzt diese Variable automatisch auf `document.referrer`; Sie müssen diese Variable nur dann festlegen, wenn Sie den automatisch erfassten Wert außer Kraft setzen möchten.

```js
s.referrer = "https://example.com";
```

Vermeiden Sie es, diese Variable auf Nicht-URL-Werte festzulegen.

## Beispiel

Viele Organisationen beschäftigen sich mit Implementierungen rund um Weiterleitungen. Sie können das [`Util.getQueryParam()`](../functions/util-getqueryparam.md) Dienstprogramm verwenden, um Werber von der URL abzurufen, wenn Ihre Site diese aufnimmt. Vergewissern Sie sich, dass Sie alle in der Abfrage-Zeichenfolge enthaltenen Werte mit einer URL kodieren.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
