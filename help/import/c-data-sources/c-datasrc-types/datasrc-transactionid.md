---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Workflow bei der Verwendung der Transaktions-ID-Datenquellen.
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 4497ca252c4ee05175141e58d784ca2df215cb94
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 45%

---

# Transaktions-ID-Datenquellen

Mit den Transaktions-ID-Datenquellen können Sie nicht nur Online- und Offline-Daten nebeneinander anzeigen, sondern die Daten auch miteinander verknüpfen. Dazu müssen Sie die [`transactionID`](/help/implement/vars/page-vars/transactionid.md)-Variablen in Ihrer Analytics-Implementierung verwenden.

Wenn Sie einen Online-Treffer senden, der einen `transactionID`-Wert enthält, erstellt Adobe einen „Schnappschuss“ aller zu diesem Zeitpunkt festgelegten oder beibehaltenen Variablen. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Data Sources hochgeladen wurde, werden die Offline- und Online-Daten miteinander verknüpft.

Für die Verwendung von Transaktionen muss der Online-Treffer mit einer Transaktions-ID gesendet und verarbeitet worden sein, bevor Transaktionsdatenquellendaten mit dieser Transaktions-ID gesendet werden. Der Online-Treffer enthält Variablen (eVars usw.), aber keine Ereignisse, die sich auf den Online-Treffer befanden, der mit den Transaktions-ID-Informationen gespeichert wurde.

Wenn ein Transaktionsdatenquellen-Treffer gesendet wird, sucht die Transaktions-ID des Datenquellen-Transaktionstreffer nach den Vars usw. (keine Ereignisse), die mit dem ursprünglichen Online-Treffer mit dieser Transaktions-ID verknüpft waren. Sie verwendet diese Variablen für den Datenquellen-Transaktionstreffer, wenn kein Wert für eine Variable vorhanden war, die beim Datenquellen-Transaktionstreffer übergeben wurde.

## Beispiel

Wenn ein Online-Treffer mit der Transaktions-ID 1256 übergeben und darauf `evar1=blue`, `evar2=water` und `event1` festgelegt wird, werden Transaktionsdaten für die Transaktions-ID 1256 mit `evar1=blue`, `evar2=water` gespeichert. Im Rahmen der Transaktionsinformationen werden keine Ereigniswerte gespeichert.

Nehmen wir nun an, ein Datenquellen-Transaktionstreffer wird dann über das System übergeben, wobei die Transaktions-ID 1256 und `evar1=yellow`, `evar3=mountain` und `event2` festgelegt sind. Das System findet die gespeicherten Transaktionsdaten und in den Treffersätzen der Datenquellentransaktion `evar2=water` (da dies auf den ursprünglichen Treffer festgelegt wurde). Sie wird nicht auf `evar1=blue` gesetzt (wie beim ursprünglichen Treffer), da für `evar1` (gelb) bereits ein Wert für den Datenquellen-Transaktionstreffer festgelegt wurde.  Der Treffer der Datenquellentransaktion führt also zu `evar1=yellow`, `evar2=water` (aus dem ursprünglichen Online-Treffer) und `evar3=mountain`. Diese 3 eVar haben `event2` festgelegt - das -Ereignis aus dem Datenquellen-Transaktionstreffer.

Es werden keine Werte aus dem Datenquellen-Transaktionstreffer `event1` festgelegt, wenn der Datenquellen-Transaktionstreffer verarbeitet wird.

## Allgemeiner Workflow Transaktions-ID-Datenquellen

Verwenden Sie den folgenden generischen Workflow, um mit der Verwendung von Transaktions-ID-Datenquellen zu beginnen:

1. Erstellen Sie eine Datenquelle (Kategorie „Generische“ und Typ „Generische Datenquelle (Transaktions-ID)“).
1. Führen Sie den Einrichtungsassistenten für die Datenquelle aus, um einen FTP-Speicherort zum Hochladen von Daten und Herunterladen einer Vorlagendatei für Datenquellen abzurufen.
1. Aktualisieren Sie Ihre Implementierung, um die `transactionID`-Variable einzuschließen.
1. Laden Sie eine Datenquellendatei mit einer `.fin`-Datei auf die FTP-Site hoch.

## Beispiel für eine Upload-Datei und den Implementierungscode

Wenn Sie die folgende Datenquellendatei hochgeladen und den folgenden Code auf Ihrer Site implementiert haben, werden die Daten in der Berichterstellung verknüpft. Die Datenquellendatei verwendet eVar1 und event1, während die Online-Implementierung eVar2 und event2 verwendet. Da die Transaktions-ID übereinstimmt, können Sie event2-Daten für eVar1 und event1-Daten für eVar2 anzeigen.

### Beispieldatei

Laden Sie die Vorlage herunter, aktualisieren Sie die Werte und laden Sie sie dann auf den FTP-Speicherort der Datenquellen hoch:

| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
|---|---|---|---|
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### Beispiel für den Implementierungscode

Weitere Informationen zur Transaktions-ID finden Sie unter [`transactionID`](/help/implement/vars/page-vars/transactionid.md) im Benutzerhandbuch für die Implementierung.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
