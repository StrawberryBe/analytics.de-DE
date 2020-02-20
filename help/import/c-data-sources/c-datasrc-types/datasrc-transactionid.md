---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Arbeitsablauf bei der Verwendung von Transaktions-ID-Datenquellen.
translation-type: tm+mt
source-git-commit: c54704bef49a2c3076caac6fe7dd3ec8d40596ef

---


# Transaktions-ID-Datenquellen

Transaktions-ID-Datenquellen ermöglichen es Ihnen, nicht nur Online- und Offlinedaten nebeneinander anzuzeigen, sondern die Daten miteinander zu verbinden. Es erfordert die Verwendung der [`transactionID`](/help/implement/vars/page-vars/transactionid.md) Variablen in Ihrer Analytics-Implementierung.

Wenn Sie einen Online-Treffer senden, der einen `transactionID` Wert enthält, erstellt Adobe einen &quot;Schnappschuss&quot;aller Variablen, die zu diesem Zeitpunkt festgelegt wurden oder beibehalten wurden. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Data Sources hochgeladen wurde, werden die Offline- und Onlinedaten miteinander verknüpft. Es spielt keine Rolle, welche Datenquelle zuerst gesehen wird.

## Gesamtarbeitsablauf für Transaktions-ID-Datenquellen

Verwenden Sie den folgenden generischen Arbeitsablauf, um mit der Verwendung von Transaktions-ID-Datenquellen zu beginnen:

1. Erstellen Sie eine Datenquelle (&quot;Generisch&quot;und &quot;Generische Datenquelle (Transaktions-ID)&quot;).
1. Folgen Sie dem Setup-Assistenten für Datenfeeds, um einen FTP-Speicherort zum Hochladen von Daten und Herunterladen einer Vorlagendatei für Datenquellen abzurufen.
1. Aktualisieren Sie Ihre Implementierung, um die `transactionID` Variable einzuschließen.
1. Laden Sie eine Datenquellen-Datei mit einer `.fin` Datei auf die FTP-Site hoch.

## Beispiel für Upload-Datei und Implementierungscode

Wenn Sie die folgende Datenquellen-Datei hochgeladen und den folgenden Code auf Ihrer Site implementiert haben, werden Daten in Berichten verknüpft. Die Datenquellen-Datei verwendet eVar1 und event1, während die Online-Implementierung eVar2 und event2 verwendet. Da die Transaktions-ID übereinstimmt, können Sie Ereignisdaten für eVar1 und Ereignisdaten1 für eVar2 sehen.

### Beispieldatei

Laden Sie die Vorlage herunter, aktualisieren Sie die Werte und laden Sie sie dann in den FTP-Speicherort der Datenquellen hoch:

| `# Generic Data Source (Transaction ID) template file (user: 0 ds_id: 1)` |  |  |  |
|---|---|---|---|
| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### Beispielimplementierungscode

Eine ausführlichere Erläuterung zur Transaktions-ID finden Sie unter [`transactionID`](/help/implement/vars/page-vars/transactionid.md) Im Handbuch Implementierung.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
