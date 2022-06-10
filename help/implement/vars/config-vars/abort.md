---
title: abort
description: Die Variable „abort“ ist ein boolescher Wert, der verhindert, dass ein Treffer an die Adobe-Datenerfassungs-Server gesendet wird.
feature: Variables
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 40%

---

# abort

Die Variable `abort` ist ein boolescher Wert, der verhindern kann, dass der nächste Tracking-Aufruf an Adobe gesendet wird. Ähnliche Funktionen gibt es im Web SDK, mit denen Sie `false` bevor ein XDM-Ereignis gesendet wird.

## Senden eines Ereignisses mit der Web SDK-Erweiterung abbrechen

Verwenden Sie die [!UICONTROL Ein vor Ereignis - Rückruf senden] Code-Editor und Rückgabe `false`.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Erweiterungen] und klicken Sie auf die **[!UICONTROL Konfigurieren]** Schaltfläche unter [!UICONTROL Adobe Experience Platform Web SDK].
1. under [!UICONTROL Datenerfassung], klicken Sie auf die **[!UICONTROL Bearbeiten am vor dem Senden des Callback-Codes eines Ereignisses]** Schaltfläche.
1. Fügen Sie im Code-Editor den folgenden Code unter allen Bedingungen ein, die Sie abbrechen möchten, um Daten an Edge zu senden:

```js
return false;
```

## Abbrechen des manuellen Versands eines Ereignisses zur Implementierung des Web SDK

Verwenden Sie die `onBeforeEventSend` Callback und Rückgabe `false`. Siehe [Globale Änderung von Ereignissen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in der Web SDK-Dokumentation finden Sie weitere Informationen.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## Verwenden der abort-Variablen in der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.abort in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.abort`-Variable ist ein boolescher Wert. Der Standardwert lautet `false`.

* Wenn auf `true` gesetzt, sendet der nächste Tracking-Aufruf ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) keine Daten an Adobe.
* Wenn diese Variable auf `false` gesetzt oder nicht definiert ist, hat sie keine Auswirkung.

```js
s.abort = true;
```

>[!NOTE]
>
>Die `abort`-Variable wird nach jedem Tracking-Aufruf auf `false` zurückgesetzt. Wenn Sie nachfolgende Tracking-Aufrufe auf derselben Seite abbrechen müssen, setzen Sie `abort` erneut auf `true`.

Beispiel: die `abort` kann in der Variablen [`doPlugins()`](../functions/doplugins.md) -Funktion, die zuletzt ausgeführt wird, bevor eine Bildanforderung an Adobe gesendet wird. Dieses Beispiel funktioniert ähnlich wie die `onBeforeEventSend` Callback mit dem Web SDK.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.
