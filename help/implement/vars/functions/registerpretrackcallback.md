---
title: registerPreTrackCallback
description: Erstellen Sie Callback-Funktionen, bevor Sie einen Treffer an Adobe senden.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# registerPreTrackCallback

Mit der `registerPreTrackCallback`-Variablen kann Ihr Unternehmen eine JavaScript-Funktion verbinden, nachdem eine Bildanforderungs-URL kompiliert wurde, aber bevor sie gesendet wird. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden.

>[!IMPORTANT] Rufen Sie keine Tracking-Aufrufe wie [`t()`](t-method.md) oder [`tl()`](tl-method.md) innerhalb der [`registerPostTrackCallback`](registerposttrackcallback.md)-Variablen auf. Tracking-Funktionen in dieser Variablen verursachen eine Endlosschleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPreTrackCallback`-Variable aufrufen, binden Sie diese Funktion jedes Mal ein, um sie bei jeder Kompilierung der URL einer Bildanforderung auszuführen. Vermeiden Sie es, dieselbe Funktion mehrmals mit demselben Seitenladevorgang zu registrieren.

>[!NOTE] Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen `registerPreTrackCallback` und `registerPostTrackCallback` ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Registrieren von Callback vor Tracking in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.registerPreTrackCallback in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die Funktion `s.registerPreTrackCallback` ist eine Funktion, die als einziges Argument eine Funktion akzeptiert. Die verschachtelte Funktion wird direkt vor dem Senden einer Bildanforderung ausgeführt.

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

>[!NOTE] Das Festlegen von Seitenvariablen oder das Ändern der `requestUrl`-Zeichenfolge in dieser Funktion hat **keine** Auswirkungen auf die Bildanforderung, die kurz nach diesem Funktionsaufruf gesendet wird. Verwenden Sie stattdessen die Variable [`doPlugins()`](doplugins.md).
