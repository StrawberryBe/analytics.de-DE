---
title: t
description: Senden Sie einen Seitenansichts-Tracking-Aufruf an Adobe.
feature: Variables
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 52%

---

# t()

Die `t()`-Methode ist eine wichtige Kernkomponente von Adobe Analytics. Sie nimmt alle auf der Seite definierten Analytics-Variablen, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungs-Server.

Betrachten Sie beispielsweise den folgenden JavaScript-Code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension item";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Beim Ausführen der `t()`-Methode werden alle definierten Analytics-Variablen verwendet und eine URL auf der Grundlage dieser Variablen formuliert. Einige Analytics-Variablen bestimmen die URL des Bildes, während andere Variablen die Parameterwerte der Abfragezeichenfolge bestimmen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe empfängt die Bildanforderung und analysiert dann die Parameter für Anforderungsheader, URL und Abfragezeichenfolge. Datenerfassungs-Server geben dann ein transparentes 1x1-Pixel-Bild zurück, das unsichtbar auf Ihrer Website angezeigt wird.

## Ereignis mit der Web SDK-Erweiterung senden

Verwenden Sie eine Aktion, um das Senden von XDM-Ereignisdaten an Adobe zu konfigurieren. Der Datastream empfängt diese Daten, wendet konfigurierte Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Dienst für diesen Datastream handelt.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. under [!UICONTROL Aktionen], klicken Sie auf die gewünschte Aktion oder klicken Sie auf die **&#39;+&#39;** -Symbol, um eine Aktion hinzuzufügen.
1. Legen Sie die [!UICONTROL Erweiterung] Dropdown zu **[!UICONTROL Adobe Experience Platform Web SDK]** und [!UICONTROL Aktionstyp] nach **[!UICONTROL Ereignis senden]**.

## Ereignis manuell zur Implementierung des Web SDK senden

Verwenden Sie die `sendEvent` -Befehl, um Daten an Adobe zu senden. Der Datastream empfängt diese Daten, wendet konfigurierte Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Dienst für diesen Datastream handelt.

```js
alloy("sendEvent", {
  "xdm": {}
});
```

Siehe [Ereignisse verfolgen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de) in der Web SDK-Dokumentation finden Sie weitere Informationen.

## Seitenansichts-Tracking-Aufruf mit der Adobe Analytics-Erweiterung

Die Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung verfügt über einen speziellen Speicherort, um einen Seitenansichts-Tracking-Aufruf festzulegen.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. under [!UICONTROL Aktionen], klicken Sie auf die gewünschte Aktion oder klicken Sie auf die **&#39;+&#39;** -Symbol, um eine Aktion hinzuzufügen.
1. Legen Sie die [!UICONTROL Erweiterung] Dropdown zu **[!UICONTROL Adobe Analytics]** und die [!UICONTROL Aktionstyp] nach **[!UICONTROL Signal senden]**.
1. Klicken Sie auf die Optionsschaltfläche `s.t()`.

## s.t()-Methode in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.t()`-Methode auf, wenn Sie einen Tracking-Aufruf an Adobe senden möchten.

```js
s.t();
```

Optional können Sie ein Objekt als Argument verwenden, um Variablenwerte zu überschreiben. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md).

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In früheren Versionen von AppMeasurement wurden mehrere Code-Zeilen verwendet, um diese Funktion aufzurufen. Der zusätzliche Code enthielt historisch gesehen Workarounds für verschiedene Browser. Die Standardisierung und Best Practices in modernen Browsern erfordern diesen Code-Block nicht mehr. Jetzt wird nur noch der `s.t()`-Methodenaufruf benötigt.
