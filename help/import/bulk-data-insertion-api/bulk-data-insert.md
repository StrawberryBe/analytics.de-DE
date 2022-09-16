---
title: Bulk-Dateneinfüge-API
description: Die Bulk-Dateneinfüge-API (BDIA) ist eine Adobe Analytics-Funktion, mit der Sie Server-Aufrufdaten in Dateistapeln hochladen können, anstatt Client-seitige Bibliotheken wie AppMeasurement zu verwenden. Die Server-Aufrufe in diesen Batch-Dateien können entweder aktuelle (Live-) Daten oder historische Daten enthalten. Sie ist ein besser skalierbarer Nachfolger der Dateneinfüge-API in früheren Versionen der Adobe Analytics-API.
solution: Analytics
feature: API
exl-id: c9d23fae-2800-42bb-8f8d-adf915cadc62
source-git-commit: b1ebf6e3548ef73217ffff1cbfb66af82e38fb8f
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 100%

---

# Bulk-Dateneinfüge-API

Die Masseneinfügung von Daten ermöglicht verschiedene Anwendungsfälle, z. B.:

* Aufnahme historischer Daten aus einem früheren Analysesystem

* Ein internes System zur Erfassung von Analysen, durch das AppMeasurement nicht verwendet werden kann. Sie können Extract-Transform-Load-Prozesse (ETL) verwenden, um Daten in Batch-Dateien einzufügen, und diese dann mit BDIA in Adobe Analytics hochladen.

* Datenerfassung in Geräten, die nur gelegentlich eine Internetverbindung haben. Diese Geräte speichern die Interaktionen so lange, bis sie eine Verbindung erhalten. Das Gerät kann dann alle Daten gleichzeitig über BDIA hochladen.

Die Dateneinfüge-API und die [Bulk-Dateneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) sind beides Methoden, um Server-seitig erfasste Daten an Adobe Analytics zu senden. Aufrufe der Data Insertion-API erfolgen jeweils für ein Ereignis. Die Bulk Data Insertion-API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Wenn Sie an einer neuen Implementierung der Server-seitigen Sammlung arbeiten, empfehlen wir die Verwendung der Bulk Data Insertion-API.
