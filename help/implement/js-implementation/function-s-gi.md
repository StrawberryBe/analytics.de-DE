---
description: Die s_gi()-Funktion wird dazu verwendet, Ihre Instanz von AppMeasurement nach Report Suite-ID zu erstellen oder zu suchen. Intern verfolgt AppMeasurement jede erstellt Instanz, und die s_gi()-Funktion gibt die vorhandene Instanz an eine Report Suite zurück, sofern eine Instanz vorhanden ist. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt und zurückgegeben.
keywords: Analytics Implementation
title: Die s_gi()-Funktion
topic: Developer and implementation
uuid: a77de90e-c60e-4946-90cf-deaf8aa3d755
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Die s_gi()-Funktion

Die s_gi()-Funktion wird dazu verwendet, Ihre Instanz von AppMeasurement nach Report Suite-ID zu erstellen oder zu suchen. Intern verfolgt AppMeasurement jede erstellt Instanz, und die s_gi()-Funktion gibt die vorhandene Instanz an eine Report Suite zurück, sofern eine Instanz vorhanden ist. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt und zurückgegeben.

Wir empfehlen, die Funktion `s_gi()` aufzurufen, bevor in Ihrem gesamten Seiten-Code Variablen gesetzt und Nachverfolgungsaufrufe ausgeführt werden. Dadurch wird sichergestellt, dass für den Nachverfolgungsaufruf das richtige Objekt verwendet wird, sollte die Variable „s“ versehentlich überschrieben werden.

## Verwenden mehrerer Report Suites {#section_F2F3B76E7AFD4B4B91CDC8BBEB34BBC5}

Das zurückgegebene Objekt hängt von der übergebenen Report Suite-ID bzw. von den übergebenen Report Suite-IDs ab. Z. B. bei folgendem initialen Aufruf an `s_gi()`:

```
var s=s_gi('rsid1,rsid2')
```

In der folgenden Tabelle ist aufgeführt, was von den nachfolgenden Aufrufen zurückgegeben wird:

| **Nachfolgender Aufruf an s_gi** | **Beschreibung des zurückgegebenen Objekts** |
|---|---|
| `s=s_gi('rsid1,rsid2')` | Dasselbe Objekt, auf das vorher verwiesen wurde. |
| `s=s_gi('rsid1')` | Eine Kopie des vorher erstellten Objekts, aber nicht das Original. |
| `s=s_gi('rsid1,rsid3')` | Eine Kopie des vorher erstellten Objekts, aber nicht das Original. |
| `s=s_gi('rsid3')` | Ein neues leeres Objekt, bei dem keine Konfigurationsvariablen gesetzt wurden (z. B. „linkTrackVars“ ist leer genauso wie „linkDownloadFileTypes“). |
