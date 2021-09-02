---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '232'
ht-degree: 100%

---

# useBeacon

Die meisten modernen Browser enthalten die native Methode `navigator.sendBeacon()`. Sie sendet asynchron eine kleine Datenmenge über HTTP an einen Webserver. AppMeasurement kann die `navigator.sendBeacon()`-Methode verwenden, wenn die `useBeacon`-Variable aktiviert ist. Sie ist nützlich für Exitlinks und andere Situationen, in denen Sie Informationen vor dem Entladen der Seite senden möchten.

Wenn `useBeacon` aktiviert ist, verwendet der nächste an Adobe gesendete Treffer die `navigator.sendBeacon()`-Methode des Browsers anstelle einer standardmäßigen `GET`-Bildanforderung. Diese Variable gilt für [`s.t()`](../functions/t-method.md)- und [`s.tl()`](../functions/tl-method.md)-Bildanforderungen. Sie erfordert AppMeasurement 2.17.0 oder höher.

>[!TIP]
>
>AppMeasurement aktiviert automatisch `useBeacon` für Exitlink-Bildanforderungen.

Die `useBeacon`-Variable wird ignoriert, wenn der Besucher einen Browser verwendet, der `navigator.sendBeacon()` nicht unterstützt. Für die Verwendung dieser Variablen ist AppMeasurement 2.16.0 oder höher erforderlich.

## Verwenden von Beacon mithilfe von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.useBeacon in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.useBeacon`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `navigator.sendBeacon()`-Methode des Browsers verwendet. Der Standardwert lautet `false`. Setzen Sie diese Variable vor dem Aufruf einer Tracking-Funktion auf `true`, wenn Sie die asynchrone Natur von `navigator.sendBeacon()` nutzen möchten.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nach Ausführung eines Tracking-Aufrufs wird diese Variable auf `false` zurückgesetzt. Wenn Ihre Implementierung mehrere Bildanforderungen mit demselben Seitenladevorgang sendet (z. B. bei Single Page Applications), setzen Sie diese Variable vor jedem Tracking-Aufruf auf `true`.
