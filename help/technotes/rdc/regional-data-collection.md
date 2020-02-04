---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
translation-type: tm+mt
source-git-commit: 449a64e361523d7a68514d60541c443a4f696c9d

---


# Regionale Datenerfassung

Die Adobe Experience Cloud verwendet regionale Datenerfassung (Regional Data Collection, RDC), damit die Interaktionen zwischen Ihren Endbenutzern und der Adobe Experience Cloud Ihren Endbenutzern so nahe wie möglich stehen. Dadurch wird die Leistung Ihrer Site/App verbessert und sichergestellt, dass Daten so schnell wie möglich gesammelt werden, um das Benutzererlebnis zu optimieren. Sobald Daten aus Ihren digitalen Eigenschaften in einem Datenerfassungscenter (DCC) regional erfasst wurden, werden sie über eine sichere Verbindung zu einem Datenverarbeitungscenter (DPC) weitergeleitet, wo sie verarbeitet und für Produkte in der Adobe Experience Cloud verfügbar gemacht werden.

RDC enthält derzeit die folgenden Speicherorte (kann geändert werden):

## Drittanbieter- und HTTP-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standardeinstellung | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |

Note: If your Analytics image request is sent to the `2o7.net` or `omtdrc.net` endpoints, then you have third-party data collection. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

## Erstanbieter-HTTPS-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Global (Standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Nur Amerika | Oregon, Virginia |
| Nur Europa | Irland, Paris |
| Nur Asien | Mumbai, Singapur, Tokio, Sydney |

Hinweis: Erlebnis Edge Global bietet die beste Leistung für Ihre Endbenutzer.  Wenn Sie einen alternativen RDC-Typ verwenden möchten, wenden Sie sich zwecks Hilfe an den Adobe-Kundendienst.

## Funktionsweise von RDC

In der folgenden Liste wird der von Adobe verwendete Datenerfassungsprozess beschrieben:

1. DNS löst den Hostnamen der Datenerfassung automatisch in die IP-Adresse des Data Collection Centers auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.

## Vorteile von RDC

| Vorteil | Beschreibung |
|---------|-----------|
| Leistung | Mit RDC werden Ihre Besucher eine Verbindung zum nächsten DCC herstellen. Das bedeutet, dass die Antwortzeiten auf Ihrer Seite beschleunigt werden, was wiederum zu genauerer Verfolgung und schnelleren Ladezeiten führt. |
| Redundanz | Bei Unterbrechungen der Kommunikation mit einem DCC wird die Datenerfassung automatisch an den nächstgelegenen DCC weitergeleitet, um die Dienstkontinuität sicherzustellen. |
| Redundanz | Im Falle einer Unterbrechung der Kommunikation zwischen dem DCC und Ihrem DPC speichert die RDC-Infrastruktur von Adobe die Daten lokal und leitet sie bei der Wiederherstellung der Datenverbindung an das DPC weiter. |

## Dokumentationsüberarbeitungsverlauf

| Update | Beschreibung |
|--------|---------|
| 4. Februar 2020 | Aktualisieren von RDC-Positionen |
| 20. Februar 2019 | Umschreiben abgeschlossen. RDC-Netzwerkinformationen hinzugefügt. |
