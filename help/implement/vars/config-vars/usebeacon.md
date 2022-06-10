---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
feature: Variables
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 54%

---

# useBeacon

Die meisten modernen Browser enthalten die native Methode `navigator.sendBeacon()`. Sie sendet asynchron eine kleine Datenmenge über HTTP an einen Webserver. AppMeasurement kann die `navigator.sendBeacon()`-Methode verwenden, wenn die `useBeacon`-Variable aktiviert ist. Sie ist nützlich für Exitlinks und andere Situationen, in denen Sie Informationen vor dem Entladen der Seite senden möchten.

Wenn `useBeacon` aktiviert ist, verwendet der nächste an Adobe gesendete Treffer die `navigator.sendBeacon()`-Methode des Browsers anstelle einer standardmäßigen `GET`-Bildanforderung. Diese Variable gilt für [`s.t()`](../functions/t-method.md)- und [`s.tl()`](../functions/tl-method.md)-Bildanforderungen. Sie erfordert AppMeasurement 2.17.0 oder höher.

>[!TIP]
>
>AppMeasurement aktiviert automatisch `useBeacon` für Exitlink-Bildanforderungen.

Die `useBeacon`-Variable wird ignoriert, wenn der Besucher einen Browser verwendet, der `navigator.sendBeacon()` nicht unterstützt. Für die Verwendung dieser Variablen ist AppMeasurement 2.16.0 oder höher erforderlich.

## Verwenden der sendBeacon-API mit der Web SDK-Erweiterung

Die **[!UICONTROL Dokument wird entladen]** innerhalb einer Aktionskonfiguration festlegen, ob an Adobe gesendete Daten die sendBeacon-API verwenden.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Regeln] und klicken Sie auf die gewünschte Regel.
1. under [!UICONTROL Aktionen], klicken Sie auf die gewünschte Aktion oder klicken Sie auf die **&#39;+&#39;** -Symbol, um eine neue Aktion hinzuzufügen.
1. Wählen Sie im Dropdown-Menü Erweiterung die Option **[!UICONTROL Adobe Experience Platform Web SDK]** und [!UICONTROL Aktionstyp] nach **[!UICONTROL Ereignis senden]**
1. Klicken Sie auf das Kontrollkästchen **[!UICONTROL Dokument wird entladen]** rechts.

Wenn dieses Kontrollkästchen aktiviert ist, werden Daten mithilfe der sendBeacon-API an Adobe gesendet. Sie ist standardmäßig deaktiviert.

## Verwenden der sendBeacon-API zur manuellen Implementierung des Web SDK

Satz `documentUnloading` nach `true` beim Senden eines Ereignisses. Wenn nicht festgelegt, lautet der Standardwert `false`.

```json
alloy("sendEvent", {
  "documentUnloading": true,
  "xdm": {}
});
```

Siehe [Verwenden der sendBeacon-API](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#using-the-sendbeacon-api) in der Web SDK-Dokumentation finden Sie weitere Informationen.

## Verwenden von Beacon mit der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.useBeacon in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.useBeacon`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `navigator.sendBeacon()`-Methode des Browsers verwendet. Der Standardwert lautet `false`. Setzen Sie diese Variable vor dem Aufruf einer Tracking-Funktion auf `true`, wenn Sie die asynchrone Natur von `navigator.sendBeacon()` nutzen möchten.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nach Ausführung eines Tracking-Aufrufs wird diese Variable auf `false` zurückgesetzt. Wenn Ihre Implementierung mehrere Bildanforderungen mit demselben Seitenladevorgang sendet (z. B. bei Single Page Applications), setzen Sie diese Variable vor jedem Tracking-Aufruf auf `true`.
