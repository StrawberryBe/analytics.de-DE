---
title: pageURL
description: Überschreiben Sie die automatisch erfasste Seiten-URL auf Ihrer Website.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '299'
ht-degree: 100%

---


# pageURL

AppMeasurement erfasst automatisch die Seiten-URL bei jedem Treffer. Wenn Sie die automatisch von AppMeasurement erfasste Seiten-URL überschreiben möchten, können Sie diese Variable verwenden. In den meisten Fällen müssen Sie diese Variable nicht festlegen.

>[!NOTE]
>
>Diese Variable ist keine verfügbare Dimension in Analysis Workspace. Sie ist nur in Data Warehouse und Data Feeds verfügbar. Wenn Sie die Seiten-URL als Dimension in Analysis Workspace verwenden möchten, sollten Sie die `pageURL`-Variable bei jedem Treffer an eine eVar übergeben.

Manchmal sind URLs länger als 255 Byte. AppMeasurement verwendet den Abfragezeichenfolgenparameter `g` für die ersten 255 Byte der URL in Bildanforderungen. Wenn eine URL länger als 255 Byte ist, wird der Rest der URL im Abfragezeichenfolgenparameter `-g` gespeichert. Protokoll- und Abfragezeichenfolgen in der URL sind in dieser Variablen enthalten.

## Seiten-URL in Adobe Experience Platform Launch

Launch füllt die Seiten-URL automatisch. Sie können die Seiten-URL-Überschreibung jedoch entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Seiten-URL].

Sie können die Seiten-URL auf einen beliebigen Zeichenfolgenwert einstellen.

## s.pageURL in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.pageURL`-Variable ist eine Zeichenfolge, die die URL der Seite enthält. AppMeasurement erfasst diese Variable automatisch. Sie können jedoch ihren Wert bei Bedarf überschreiben.

```js
s.pageURL = "https://example.com";
```

Wenn Sie die Seiten-URL als Dimension in Berichten verwenden möchten, sollten Sie Folgendes in Ihrer Implementierung berücksichtigen:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```
