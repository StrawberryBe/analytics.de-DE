---
description: 'null'
title: Transaktions-ID und Besucherprofile
topic: Developer and implementation
uuid: 7a72779c-7f67-4872-ad5e-edf298d53cac
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 100%

---


# Transaktions-ID und Besucherprofile

Dieser Abschnitt enthält wichtige Informationen zu den Daten aus dem Besucherprofil, die beim Hochladen von Daten mit einer Transaktions-ID verwendet werden.

## Transaktions-ID {#section_B248FA93ECC84F6290D237EB83618070}

Beim Aufzeichnen einer Transaktions-ID wird ein „Schnappschuss“ des aktuellen Besucherprofils gespeichert und mit der Transaktions-ID verbunden. Dieser „Schnappschuss“ enthält alle aktuell für den Besucher eingestellten Variablenwerte, inklusive Variablen, die bestehen bleiben (z. B. eVars und Kampagnen). Werte in diesem „Schnappschuss“ erhalten eine Zuordnung für Erfolgsereignisse, Kaufereignisse und Umsätze, die später mit derselben Transaktions-ID hochgeladen werden.

Nachdem der „Schnappschuss“ des Besucherprofils erstellt wurde, wird er nicht aktualisiert, wenn das aktuelle Besucherprofil geändert wird (aufgrund des Online-Verhaltens). Er wird lediglich mit Daten aktualisiert, die mithilfe von Transaktions-ID-Datenquellen hochgeladen werden. Wenn Sie den Wert für die Transaktions-ID auf mehreren Seiten während desselben Besuchs festlegen, wird der später stattfindende Datenquellen-Upload an den „Schnappschuss“ gebunden, der erstellt wurde, als die ID zum ersten Mal festgelegt wurde.

**Mehrere Uploads**

Innerhalb des gesamten Transaktions-ID-Ablauffensters (siehe unten) können mehrere Datenzeilen für dieselbe Transaktions-ID hochgeladen werden.

**Ablauf von Variablen**

Der Ablauf von Variablen wird in Bezug auf Transaktions-IDs nicht berücksichtigt, da die verbundenen Besucherprofildaten den Besucherstatus zum Zeitpunkt der Transaktion reflektieren sollen. Beispiel: Wenn eVar1 so konfiguriert wird, dass sie nach dem Besuch abläuft, erhält der Wert im „Schnappschuss“ des Besucherprofils eine Gutschrift, selbst wenn der Wert abgelaufen ist oder im aktuellen Besucherprofil beim Hochladen von Transaktions-ID-Daten ersetzt wurde.

**Produkte**

Produktinformationen (aus `s.products`) sind nicht im „Schnappschuss“ des Besucherprofils enthalten. Daher müssen Sie alle verbundenen Produktdaten in der Datenquellendatei zusammen mit der Transaktions-ID hochladen. Beachten Sie, dass Sie pro Zeile nur ein Produkt angeben können. Daher kann es erforderlich sein, mehrere Zeilen mit derselben Transaktions-ID hochzuladen, um alle Produkte einzubeziehen.

**Hochgeladene eVar-Persistenz**

eVars, die mit Transaktions-ID-Datenquellen hochgeladen wurden, werden dem „Schnappschuss“ des Besucherprofils hinzugefügt und nicht dem aktuellen Besucherprofil oder dem virtuellen Cookie. Dies bedeutet, dass das Online-Verhalten, das nach dem Upload auftritt, nicht den hochgeladenen eVars gutgeschrieben wird, da diese Werte nicht Bestandteil des aktuellen Besucherprofils sind.

**Transaktions-ID-Ablauffenster**

Der „Schnappschuss“ des Besucherprofils, der mit einer Transaktions-ID verbunden ist, kann nach 90 Tagen gelöscht werden. Der tatsächliche Löschplan kann jedoch abweichen. Sie können sich, falls erforderlich, an die Adobe-Kundenunterstützung wenden, um das Ablauffenster erweitern zu lassen. Wird eine Zeile nach dem Transaktions-ID-Ablauffenster hochgeladen, werden die Zeilendaten zwar aufgezeichnet, aber keine der Daten im „Schnappschuss“ des Besucherprofils werden gutgeschrieben, wenn das Profil gelöscht wurde.

## Aufschlüsselungen und Segmentierung mithilfe von Transaktions-IDs   {#section_A4D39291200A42C496122FDB9EF6EF68}

Mit Datenquellen hochgeladene eVars können verwendet werden, um im „Schnappschuss“ des Besucherprofils enthaltene eVars aufzuschlüsseln. Da diese Daten vom aktuellen Besucherprofil getrennt sind, können Sie keine anderen eVars zur Aufschlüsselung verwenden, die festgelegt wurden, bevor oder nachdem die Transaktions-ID festgelegt wurde, die aber nicht Teil des „Schnappschusses“ sind.

Es gibt verschiedene Möglichkeiten, verbundene Besucherdaten anzuzeigen, die nicht in einer Aufschlüsselung verfügbar sind. In Data Warehouse-Berichten können Sie Transaktions-ID-Daten mit einer Besucher-ID anzeigen, die mit den anderen Treffern des Besuchers übereinstimmt. Während diese Transaktions-ID-Zeilen bei der Zählung von Besuchen/Besuchern pro Tag ausgeschlossen sind, werden sie beim Berechnen der meisten Metriken und in Segmenten verwendet.

Aus diesem Grund können Sie ein Segment mit Besuchern erstellen, die ein Offline-Ereignis durchführen, das mithilfe von Transaktions-ID-Datenquellen hochgeladen wurde. Dieses Segment gibt alle Aktionen des Besuchers vor und nach dem Transaktions-ID-Ereignis zurück.

Gleichermaßen können Sie anhand der Besucherbeiträge feststellen, auf welche Weise Transaktions-ID-Props und -eVars einem Online-Ereignis vorausgingen oder auf welche Weise Online-Props und -eVars einem Transaktions-ID-Ereignis vorausgingen.
