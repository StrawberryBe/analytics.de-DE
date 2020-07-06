---
title: registerPostTrackCallback
description: Erstellen Sie Callback-Funktionen, nachdem Sie einen Treffer an Adobe gesendet haben.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 95%

---


# registerPostTrackCallback

Die `registerPostTrackCallback`-Variable ermöglicht es Ihrer Organisation, eine JavaScript-Funktion unmittelbar nach der erfolgreichen Übermittlung eines Treffers an Adobe zu aktivieren. Wenn ein Tracking-Aufruf fehlschlägt, wird diese Funktion nicht ausgeführt. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden oder Variablenwerte in Einzelseitenanwendungen bereinigen.

>[!IMPORTANT]
>
>Rufen Sie keine Tracking-Aufrufe wie [`t()`](t-method.md) oder [`tl()`](tl-method.md) innerhalb der `registerPostTrackCallback`-Variablen auf. Tracking-Funktionen in dieser Variablen verursachen eine Endlosschleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPostTrackCallback`-Variable aufrufen, binden Sie diese Funktion so ein, dass sie unmittelbar nach dem erfolgreichen Senden einer Bildanforderung ausgeführt wird. Vermeiden Sie es, dieselbe Funktion mehrmals mit demselben Seitenladevorgang zu registrieren.

>[!NOTE]
>
>Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen [`registerPreTrackCallback`](registerpretrackcallback.md) und `registerPostTrackCallback` ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Registrieren von Callback nach Tracking in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.registerPostTrackCallback in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die Funktion `s.registerPostTrackCallback` ist eine Funktion, die als einziges Argument eine Funktion akzeptiert. Die verschachtelte Funktion wird sofort ausgeführt, nachdem eine Bildanforderung erfolgreich gesendet wurde.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl`-Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl`-Variable für Ihre gewünschte Verwendung parsen. Die Anpassung dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Zusätzliche Argumente können in die `s.registerPostTrackCallback`-Funktion aufgenommen werden, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Anwendungsbeispiel

Die Registrierung der [`clearVars()`](clearvars.md)-Funktion im Callback nach Tracking kann für Einzelseitenanwendungen von Vorteil sein. Jedes Mal, wenn Sie einen Treffer erfolgreich an Adobe senden, wird die `clearVars()`-Funktion ausgeführt. Ihre Implementierung kann dann Variablen erneut definieren, ohne sich Gedanken über falsche vorhandene Werte machen zu müssen.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
