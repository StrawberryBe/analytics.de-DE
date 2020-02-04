---
title: dynamicAccountMatch
description: Die Variable "dynamicAccountMatch"bestimmt, welchen Wert in dynamischen Konten angezeigt werden soll.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# dynamicAccountMatch

> [!IMPORTANT] Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder beim Starten der Adobe Experience Platform nicht unterstützt.

Die `dynamicAccountMatch` `dynamicAccountList` Variable ist der Wert, der die Werte betrachtet und vergleicht. Ist `dynamicAccountSelection` dies nicht der Fall, wird diese Variable ignoriert `true`.

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

* Auf Seiten, die auf einer Festplatte gespeichert werden, sind nicht mehrere `location` Variablen definiert (z. B. `location.host` leer). Stellen Sie sicher, dass `s_account` eine Standard-Report Suite enthalten ist.
* Wenn eine Seite über eine webbasierte Übersetzungs-Engine wie Google übersetzt wird, funktioniert die dynamische Kontoauswahl nicht wie vorgesehen. Für eine präzisere Nachverfolgung müssen Sie die Variable `s_account` Server-seitig auffüllen.
