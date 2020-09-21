---
title: dynamicAccountMatch
description: Die Variable „dynamicAccountMatch“ legt fest, welcher Wert in dynamischen Konten betrachtet werden soll.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '126'
ht-degree: 100%

---


# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder in Adobe Experience Platform Launch nicht unterstützt.

Die Variable `dynamicAccountMatch` ist der Wert, den `dynamicAccountList` betrachtet und vergleicht. Wenn `dynamicAccountSelection` nicht auf `true` gesetzt ist, wird diese Variable ignoriert.

Wenn diese Variable nicht definiert ist, lautet ihr Standardwert `window.location.host`.

## Syntax

```js
s.dynamicAccountMatch=[DOM object]
```

## Beispiele

```js
// Look at the URL path to determine report suite
s.dynamicAccountMatch = location.pathname;

// Use a query string
s.dynamicAccountMatch = location.search;

// Use the full URL
s.dynamicAccountMatch = location.href;

// Use concatenated variables
s.dynamicAccountMatch =  location.hostname + location.pathname + location.search;
```

## Weitere Hinweise

* Auf Seiten, die auf einer Festplatte gespeichert werden, sind nicht mehrere `location`-Variablen definiert (z. B. ist `location.host` leer). Stellen Sie sicher, dass in `s_account` eine standardmäßige Report Suite enthalten ist.
* Bei über ein Web-basiertes Tool (wie z. B. Google) übersetzten Seiten funktioniert die dynamisches Kontoauswahl nicht richtig. Für eine präzisere Nachverfolgung müssen Sie die Variable  `s_account` Server-seitig auffüllen.
