---
description: Die s_gi()-Funktion wird dazu verwendet, Ihre Instanz von AppMeasurement nach Report Suite-ID zu erstellen oder zu suchen. Intern verfolgt AppMeasurement jede erstellt Instanz, und die s_gi()-Funktion gibt die vorhandene Instanz an eine Report Suite zurück, sofern eine Instanz vorhanden ist. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt und zurückgegeben.
keywords: Analytics-Implementierung
seo-description: Die s_gi()-Funktion wird dazu verwendet, Ihre Instanz von AppMeasurement nach Report Suite-ID zu erstellen oder zu suchen. Intern verfolgt AppMeasurement jede erstellt Instanz, und die s_gi()-Funktion gibt die vorhandene Instanz an eine Report Suite zurück, sofern eine Instanz vorhanden ist. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt und zurückgegeben.
seo-title: Die s_gi()-Funktion
solution: Analytics
title: Die s_gi()-Funktion
topic: Entwickler und Implementierung
uuid: a 77 de 90 e-c 60 e -4946-90 cf-tauf 8 aa 3 d 755
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Die s_gi()-Funktion

Die s_gi()-Funktion wird dazu verwendet, Ihre Instanz von AppMeasurement nach Report Suite-ID zu erstellen oder zu suchen. Intern verfolgt AppMeasurement jede erstellt Instanz, und die s_gi()-Funktion gibt die vorhandene Instanz an eine Report Suite zurück, sofern eine Instanz vorhanden ist. Wenn keine Instanz vorhanden ist, wird eine neue Instanz erstellt und zurückgegeben.

We recommend calling `s_gi()` before setting variables and making tracking calls throughout your page code. Dadurch wird sichergestellt, dass für den Nachverfolgungsaufruf das richtige Objekt verwendet wird, sollte die Variable „s“ versehentlich überschrieben werden.

## Verwenden mehrerer Report Suites {#section_F2F3B76E7AFD4B4B91CDC8BBEB34BBC5}

Das zurückgegebene Objekt hängt von der übergebenen Report Suite-ID bzw. von den übergebenen Report Suite-IDs ab. Z. B. bei folgendem initialen Aufruf an `s_gi()`:

```
var s=s_gi('rsid1,rsid2')
```

In der folgenden Tabelle ist aufgeführt, was von den nachfolgenden Aufrufen zurückgegeben wird:

| ** Nachfolgender Aufruf an s_ gi** | ** Beschreibung des zurückgegebenen Objekts** |
|---|---|
| `s=s_gi('rsid1,rsid2')` | Dasselbe Objekt, auf das vorher verwiesen wurde. |
| `s=s_gi('rsid1')` | Eine Kopie des vorher erstellten Objekts, aber nicht das Original. |
| `s=s_gi('rsid1,rsid3')` | Eine Kopie des vorher erstellten Objekts, aber nicht das Original. |
| `s=s_gi('rsid3')` | Ein neues leeres Objekt, bei dem keine Konfigurationsvariablen gesetzt wurden (z. B. „linkTrackVars“ ist leer genauso wie „linkDownloadFileTypes“). |

