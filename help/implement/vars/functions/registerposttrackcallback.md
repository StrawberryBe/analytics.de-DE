---
title: registerPostTrackCallback
description: Erstellen Sie Rückruffunktionen, nachdem Sie einen Treffer an Adobe gesendet haben.
translation-type: tm+mt
source-git-commit: acfcb1f27650649581875680e7897e5c9813765a

---


# registerPostTrackCallback

Mit der `registerPostTrackCallback` Variablen kann Ihr Unternehmen eine JavaScript-Funktion unmittelbar nach erfolgreichem Senden eines Treffers an Adobe in einen Haken setzen. Wenn ein Verfolgungsaufruf fehlschlägt, wird diese Funktion nicht ausgeführt. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden oder Variablenwerte in Einzelseitenanwendungen bereinigen.

> [!IMPORTANT] Rufen Sie keine Verfolgungsfunktionen wie `t` oder `tl` innerhalb der `registerPostTrackCallback` Variablen auf. Tracking-Funktionen in dieser Variablen verursachen eine unendliche Schleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPostTrackCallback` Variable aufrufen, stellen Sie eine Verknüpfung zu dieser Funktion her, um sie unmittelbar nach dem erfolgreichen Senden einer Bildanforderung auszuführen. Vermeiden Sie es, dieselbe Funktion mehrmals beim Laden derselben Seite zu registrieren.

> [!NOTE] Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen- `registerPreTrackCallback` und `registerPostTrackCallback` -ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Rückruffunktion bei der Nachverfolgung beim Starten der Adobe Experience Platform registrieren

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.registerPostTrackCallback in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die Funktion `s.registerPostTrackCallback` ist eine Funktion, die als einziges Argument eine Funktion akzeptiert. Die verschachtelte Funktion wird direkt vor dem Senden einer Bildanforderung ausgeführt.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl` Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl` Variable für die gewünschte Verwendung analysieren. Das Anpassen dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Zusätzliche Argumente können in die `s.registerPostTrackCallback` Funktion aufgenommen werden, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Verwendungsfallbeispiel

Die Registrierung der `clearVars()` Funktion im Nachverfolgungsrückruf kann für Einzelseitenanwendungen von Vorteil sein. Jedes Mal, wenn Sie einen Treffer erfolgreich an Adobe senden, wird die `clearVars()` Funktion ausgeführt. Ihre Implementierung kann dann Variablen erneut definieren, ohne sich Gedanken über falsch vorhandene Werte machen zu müssen.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
