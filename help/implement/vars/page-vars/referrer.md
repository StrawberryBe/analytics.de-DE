---
title: referrer
description: Überschreiben Sie den automatisch erfassten Referrer für einen Treffer.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 95%

---


# referrer

Die `referrer`-Variable überschreibt den automatisch erfassten Referrer in Berichten. Diese Variable ist hilfreich in Situationen, in denen der Referrer verloren gehen könnte, z. B. bei Redirects oder vorübergehender Weiterleitung des Besuchers an einen Zahlungsverarbeiter. Diese Variable hilft beim Ausfüllen der Dimensionen „Referrer“ und „Referrer-Domäne“.

## referrer in Adobe Experience Platform Launch

Sie können „referrer“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Referrer].

Sie können den Referrer auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.referrer in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.referrer`-Variable ist eine Zeichenfolge, die die URL der vorherigen Seite enthält. Diese Variable kann maximal 255 Byte speichern. Werte, die länger als 255 Byte sind, werden abgeschnitten. AppMeasurement setzt diese Variable automatisch auf `document.referrer`. Sie müssen diese Variable nur dann festlegen, wenn Sie den automatisch erfassten Wert überschreiben möchten.

```js
s.referrer = "https://example.com";
```

Bei Verwendung der `digitalData` Datenschicht [](../../prepare/data-layer.md):

```js
s.referrer = digitalData.page.pageInfo.referringURL;
```

>[!CAUTION]
>
>Vermeiden Sie es, diese Variable auf Nicht-URL-Werte festzulegen. Entfernen Sie nicht das Protokoll der URL.

## Beispiel

Viele Unternehmen beschäftigen sich mit Implementierungen rund um Redirects. Mit dem Dienstprogramm [`Util.getQueryParam()`](../functions/util-getqueryparam.md) können Sie den Referrer aus der URL abrufen, wenn Ihre Website dies zulässt. Stellen Sie sicher, dass Ihre URL alle Werte codiert, die in der Abfragezeichenfolge enthalten sind.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
