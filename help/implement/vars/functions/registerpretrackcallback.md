---
title: registerPreTrackCallback
description: Erstellen Sie Rückruffunktionen, bevor Sie einen Treffer an Adobe senden.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# registerPreTrackCallback

Mit der `registerPreTrackCallback` Variablen kann Ihr Unternehmen eine JavaScript-Funktion verbinden, nachdem eine Bildanforderungs-URL kompiliert wurde, aber bevor sie gesendet wird. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an einen Partner oder eine interne Infrastruktur senden.

> [!IMPORTANT] Rufen Sie keine Verfolgungsfunktionen wie `t` oder `tl` innerhalb der `registerPostTrackCallback` Variablen auf. Tracking-Funktionen in dieser Variablen verursachen eine unendliche Schleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPreTrackCallback` Variable aufrufen, stellen Sie eine Verknüpfung zu dieser Funktion her, um sie bei jeder Kompilierung der URL einer Bildanforderung auszuführen. Vermeiden Sie es, dieselbe Funktion mehrmals beim Laden derselben Seite zu registrieren.

> [!NOTE] Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen- `registerPreTrackCallback` und `registerPostTrackCallback` -ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Pre-Track-Rückruf beim Start der Adobe Experience Platform registrieren

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.registerPreTrackCallback in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die Funktion `s.registerPreTrackCallback` ist eine Funktion, die als einziges Argument eine Funktion akzeptiert. Die verschachtelte Funktion wird direkt vor dem Senden einer Bildanforderung ausgeführt.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl` Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl` Variable für die gewünschte Verwendung analysieren. Das Anpassen dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Zusätzliche Argumente können in die `s.registerPreTrackCallback` Funktion aufgenommen werden, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

> [!NOTE] Das Festlegen von Seitenvariablen oder das Ändern der `requestUrl` Zeichenfolge in dieser Funktion hat *keine* Auswirkungen auf die Bildanforderung, die kurz nach diesem Funktionsaufruf gesendet wird.
