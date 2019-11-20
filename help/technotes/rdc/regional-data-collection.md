---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
translation-type: tm+mt
source-git-commit: 6d8f081d5ed86dfd6aeb0b68c5ae9624edb84b21

---


# Regionale Datenerfassung

Erfahren Sie mehr über die regionale Datenerfassung (RDC) von und wie Sie bei Bedarf Ihr Netzwerk für die Datenerfassung ändern können.

Zur Verbesserung der Datenerfassungsleistung wurden alle Adobe Experience Cloud-Kunden in regionale Datenerfassung (Regional Data Collection, RDC) konvertiert, sodass die Datenerfassung möglichst nahe bei Ihren Endbenutzern erfolgt. Dadurch wird die Leistung Ihrer Site/App verbessert und sichergestellt, dass Daten so schnell wie möglich gesammelt werden, um das Benutzererlebnis zu optimieren. Sobald Daten aus Ihren digitalen Eigenschaften regional in einem Data Collection Center (DCC) erfasst wurden, werden sie über eine sichere Verbindung an ein Data Processing Center (DPC) weitergeleitet, wo sie verarbeitet und für Produkte in Adobe Experience Cloud bereitgestellt werden. RDC ist seit 2009 der Standard bei neuen Implementierungen.

RDC enthält derzeit die folgenden Speicherorte (kann geändert werden):

## Datenerfassung durch Dritte

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standardeinstellung | San Jose, Virginia, London, Singapur, Hongkong, Sydney, Amsterdam |

Note: If your Analytics image request is sent to the `2o7.net` or `omtdrc.net` endpoints, then you have third-party data collection. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

## First-Party-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standard | San Jose, Virginia, London, Singapur |
| Alle | Standard plus Hong Kong, Sydney, Amsterdam |
| Nur USA | San Jose, Virginia |
| Nur EU | London, Amsterdam |
| Nur Indien | Mumbai |

## Funktionsweise von RDC

In der folgenden Liste wird der von Adobe verwendete Datenerfassungsprozess beschrieben:

1. DNS löst den Hostnamen der Datenerfassung automatisch in die IP-Adresse des Data Collection Centers auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.

## Vorteile von RDC

| Vorteil | Beschreibung |
|---------|-----------|
| Leistung | Mit RDC werden Ihre Besucher eine Verbindung zum nächsten DCC herstellen. Das bedeutet, dass die Antwortzeiten auf Ihrer Seite beschleunigt werden, was wiederum zu genauerer Verfolgung und schnelleren Ladezeiten führt. Ausführlichere Informationen zu Antwortzeiten finden Sie unter „Leistungsverbesserungen mit RDC“. |
| Redundanz | Bei Unterbrechungen der Kommunikation mit einem DCC wird die Datenerfassung automatisch an den nächstgelegenen DCC weitergeleitet, um die Dienstkontinuität sicherzustellen. |
| Redundanz | Im Falle einer Unterbrechung der Kommunikation zwischen dem DCC und Ihrem DPC speichert die RDC-Infrastruktur von Adobe die Daten lokal und leitet sie bei der Wiederherstellung der Datenverbindung an das DPC weiter. |

## Dokumentationsüberarbeitungsverlauf

| Update | Beschreibung |
|--------|---------|
| 20. Februar 2019 | Umschreiben abgeschlossen. RDC-Netzwerkinformationen hinzugefügt. |
