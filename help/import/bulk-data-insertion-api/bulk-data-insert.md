---
title: Bulk-Dateneinfüge-API
description: Die Bulk Data Insertion API (BDIA) ist eine Adobe Analytics-Funktion, mit der Sie Server-Aufrufdaten in Dateistapeln hochladen können, anstatt Client-seitige Bibliotheken wie AppMeasurement zu verwenden. Die Server-Aufrufe in diesen Batch-Dateien können entweder aktuelle (Live-) Daten oder historische Daten sein. Es ist ein skalierbarerer Nachfolger der Dateneinfüge-API in früheren Versionen der Adobe Analytics-API.
solution: Analytics
feature: API
source-git-commit: d8603ddd6cee2ccc930281003d9ff1befa15c95c
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 27%

---


# Bulk-Dateneinfüge-API

Die Masseneinfügung von Daten löst verschiedene Anwendungsfälle, z. B.:

* Erfassen von historischen Daten aus einem früheren Analysesystem

* Ein internes Analytics-Erfassungssystem, das die Verwendung von AppMeasurement unmöglich macht. Sie können Extract-Transform-Load (ETL)-Prozesse verwenden, um Daten in Batch-Dateien einzufügen, und diese dann mit BDIA in Adobe Analytics hochladen.

* Datenerfassung von Geräten, die nur gelegentlich eine Internetverbindung haben. Diese Geräte speichern die Interaktionen, bis sie eine Verbindung erhalten. Das Gerät kann dann die Daten über BDIA alle gleichzeitig hochladen.

Dateneinfüge-API und [Bulk Data Insertion API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html?lang=de#!AdobeDocs/analytics-2.0-apis/master/bdia.md)sind beide Methoden, um Server-seitige Erfassungsdaten an Adobe Analytics zu senden. Aufrufe der Data Insertion-API erfolgen jeweils für ein Ereignis. Die Bulk Data Insertion-API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Wenn Sie an einer neuen Implementierung der Server-seitigen Sammlung arbeiten, empfehlen wir die Verwendung der Bulk Data Insertion-API.