---
title: dynamicAccountMatch
description: Die Variable „dynamicAccountMatch“ legt fest, welcher Wert in dynamischen Konten betrachtet werden soll.
feature: Implementation Basics
exl-id: 3b68f2e6-1bd9-4b16-9d03-a87c9217e1b7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '127'
ht-degree: 100%

---

# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder Tags in Adobe Experience Platform nicht unterstützt.

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
