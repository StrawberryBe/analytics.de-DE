---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
translation-type: ht
source-git-commit: 449a64e361523d7a68514d60541c443a4f696c9d

---


# Regionale Datenerfassung

Adobe Experience Cloud verwendet regionale Datenerfassung (Regional Data Collection, RDC), damit die Interaktionen zwischen Ihren Endanwendern und Adobe Experience Cloud so nahe wie möglich an den Anwendern stattfinden. Dies verbessert die Leistung Ihrer Site/App und stellt sicher, dass die Daten so schnell wie möglich erfasst werden, um das Endanwendererlebnis zu optimieren. Sobald Daten aus Ihren digitalen Assets regional in einem Data Collection Center (DCC) erfasst wurden, werden sie über eine sichere Verbindung an ein DPC weitergeleitet, wo sie verarbeitet und für Produkte in Adobe Experience Cloud bereitgestellt werden.

RDC enthält derzeit die folgenden Speicherorte (kann geändert werden):

## Drittanbieter- und HTTP-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standardeinstellung | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |

Hinweis: Wenn Ihre Analytics-Bildanforderung an die Endpunkte `2o7.net` oder `omtdrc.net` gesendet wird, dann erfolgt die Datenerfassung durch Dritte. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

## Erstanbieter-HTTPS-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Global (Standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Nur Amerika | Oregon, Virginia |
| Nur Europa | Irland, Paris |
| Nur Asien | Mumbai, Singapur, Tokio, Sydney |

Hinweis: Experience-Edge „Global“ bietet die beste Leistung für Ihre Endanwender.  Wenn Sie einen alternativen RDC-Typ verwenden möchten, wenden Sie sich zur Unterstützung an die Adobe-Kundenunterstützung.

## Funktionsweise von RDC

In der folgenden Liste wird der von Adobe verwendete Datenerfassungsprozess beschrieben:

1. DNS löst den Hostnamen der Datenerfassung automatisch in die IP-Adresse des Data Collection Centers auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.

## Vorteile von RDC

| Vorteil | Beschreibung |
|---------|-----------|
| Leistung | Mit RDC werden Ihre Besucher mit dem nächstgelegenen Daten-Center verbunden. Das bedeutet, dass die Antwortzeiten auf Ihrer Seite beschleunigt werden, was wiederum zu genauerer Verfolgung und schnelleren Ladezeiten führt. |
| Redundanz | Im Falle einer Unterbrechung der Kommunikation mit einem DCC wird die Datenerfassung automatisch an das nächstgelegene DCC weitergeleitet, wodurch die Kontinuität des Dienstes sichergestellt wird. |
| Redundanz | Im Falle einer Unterbrechung der Kommunikation zwischen dem DCC und Ihrem DPC speichert die RDC-Infrastruktur von Adobe die Daten lokal und leitet sie bei der Wiederherstellung der Datenverbindung an das DPC weiter. |

## Verlauf der Dokumentationsüberarbeitung

| Update | Beschreibung |
|--------|---------|
| 4. Februar 2020 | RDC-Positionen aktualisiert. |
| 20. Februar 2019 | Umschreiben abgeschlossen. RDC-Netzwerkinformationen hinzugefügt. |
