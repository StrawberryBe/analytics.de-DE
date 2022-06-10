---
title: registerPreTrackCallback
description: Erstellen Sie Callback-Funktionen, bevor Sie einen Treffer an Adobe senden.
feature: Variables
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 55%

---

# registerPreTrackCallback

Mit der `registerPreTrackCallback`-Variablen kann Ihr Unternehmen eine JavaScript-Funktion verbinden, nachdem eine Bildanforderungs-URL kompiliert wurde, aber bevor sie gesendet wird. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden.

>[!WARNING]
>
>Rufen Sie keine Tracking-Aufrufe wie [`t()`](t-method.md) oder [`tl()`](tl-method.md) innerhalb der [`registerPostTrackCallback`](registerposttrackcallback.md)-Variablen auf. Tracking-Funktionen in dieser Variablen verursachen eine Endlosschleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPreTrackCallback`-Variable aufrufen, binden Sie diese Funktion jedes Mal ein, um sie bei jeder Kompilierung der URL einer Bildanforderung auszuführen. Vermeiden Sie es, dieselbe Funktion mehrmals mit demselben Seitenladevorgang zu registrieren.

>[!NOTE]
>
>Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen `registerPreTrackCallback` und `registerPostTrackCallback` ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Rückruf-Vorverfolgung mit der Web SDK-Erweiterung

Das Web-SDK kann eine Funktion nicht verbinden, nachdem Daten kompiliert wurden, aber bevor sie an Adobe gesendet wird. Sie können jedoch `onBeforeEventSend` um eine Funktion zu registrieren, die kurz vor dem Senden von Daten ausgeführt wird.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Erweiterungen] und klicken Sie auf die **[!UICONTROL Konfigurieren]** Schaltfläche unter [!UICONTROL Adobe Experience Platform Web SDK].
1. under [!UICONTROL Datenerfassung], klicken Sie auf die **[!UICONTROL Bearbeiten am vor dem Senden des Callback-Codes eines Ereignisses]** Schaltfläche.
1. Platzieren Sie den gewünschten Code im Editor.

## Rückruf manuell zurückverfolgen, um das Web SDK manuell zu implementieren

Das Web-SDK kann eine Funktion nicht verbinden, nachdem Daten kompiliert wurden, aber bevor sie an Adobe gesendet wird. Sie können jedoch `onBeforeEventSend` , um eine Funktion zu registrieren, die kurz vor dem Senden von Daten ausgeführt wird, ähnlich wie bei `doPlugins`. Siehe [Globale Änderung von Ereignissen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in der Web SDK-Dokumentation finden Sie weitere Informationen.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Rückruf-Vorverfolgung mit der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.registerPreTrackCallback in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Funktion `s.registerPreTrackCallback` akzeptiert als einziges Argument eine Funktion. Die verschachtelte Funktion wird direkt vor dem Senden einer Bildanforderung ausgeführt.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl`-Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl`-Variable für Ihre gewünschte Verwendung parsen. Die Anpassung dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Sie können zusätzliche Argumente in die Funktion `s.registerPreTrackCallback` einfügen, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

>[!NOTE]
>
>Das Festlegen von Seitenvariablen oder das Ändern der `requestUrl`-Zeichenfolge in dieser Funktion hat **keine** Auswirkungen auf die Bildanforderung, die kurz nach diesem Funktionsaufruf gesendet wird. Verwenden Sie stattdessen die Variable [`doPlugins()`](doplugins.md).
