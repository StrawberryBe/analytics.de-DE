---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: e020e768b7a3a5495fcc86cb3fd1fbc5a421d224
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 78%

---

# Regionale Datenerfassung

Adobe Experience Cloud verwendet regionale Datenerfassung (Regional Data Collection, RDC), damit die Interaktionen zwischen Ihren Endanwendern und Adobe Experience Cloud so nahe wie möglich an den Anwendern stattfinden. Dies verbessert die Leistung Ihrer Site/App und stellt sicher, dass die Daten so schnell wie möglich erfasst werden, um das Endanwendererlebnis zu optimieren. Sobald Daten aus Ihren digitalen Assets regional in einem Data Collection Center (DCC) erfasst wurden, werden sie über eine sichere Verbindung an ein DPC weitergeleitet, wo sie verarbeitet und für Produkte in Adobe Experience Cloud bereitgestellt werden.

>[!IMPORTANT]
>
>Das Add-on-Paket zur regionalen Datenerfassung in China (Leistungsoptimierung für China) ist ein kostenpflichtiges Add-On für Adobe Analytics. Die Leistungsoptimierung von Adobe auf dem chinesischen Festland ermöglicht es Kunden mit Nutzern innerhalb Chinas, diese Daten direkt an den China Edge-Knoten und nicht an andere globale Standorte zu senden. Dies verbessert die Seitenladezeiten und die Datengenauigkeit gegenüber dem Versand der Daten an Knoten außerhalb Chinas. Wenden Sie sich an Ihren Adobe-Vertriebsmitarbeiter, um weitere Informationen zu erhalten.

RDC enthält derzeit die folgenden Speicherorte (kann geändert werden):

## Drittanbieter- und HTTP-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standard | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney, China* |

Hinweis: Wenn Ihre Analytics-Bildanforderung an die Endpunkte `adobedc`, `2o7.net` oder `omtrdc.net` gesendet wird, erfolgt die Datenerfassung durch Dritte. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

*Die regionale Datenerfassung für China benötigt das Add-on-Paket für China. Beachten Sie hierzu auch den wichtigen Hinweis oben.

## Erstanbieter-HTTPS-Datenerfassung

| RDC-Typ | Datenerfassungszentren |
|---------------------|-------------------|
| Global (Standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Global + China* | China*, Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Nur Amerika | Oregon, Virginia |
| Nur Europa | Irland, Paris |
| Nur Asien | Mumbai, Singapur, Tokio, Sydney |
| Nur China* | Peking |

*Nur China und Global + China RDC-Typen erfordern das China Add-On-Paket. Beachten Sie hierzu auch den wichtigen Hinweis oben. Global + China leitet Daten aus China an unsere China RDC weiter, während Daten aus China an die nächstgelegene RDC außerhalb Chinas weitergeleitet werden.

>[!NOTE]
>Experience Edge Global und Global + China bieten die beste Leistung für Ihre Endbenutzer. Wenn Sie einen alternativen RDC-Typ verwenden möchten, wenden Sie sich zur Unterstützung an die Kundenunterstützung von Adobe.

## Vorteile von RDC

| Vorteil | Beschreibung |
| --- | --- |
| Leistung | Mit RDC stellen Ihre Besucher eine Verbindung mit dem nächstgelegenen DCC her. Dadurch erhalten Sie die schnellste Reaktionszeit, was zu einem genaueren Tracking und schnelleren Ladezeiten führt. |
| Redundanz | Im Falle einer Unterbrechung der Kommunikation zwischen dem DCC und Ihrem DPC speichert die RDC-Infrastruktur von Adobe die Daten lokal und leitet sie bei der Wiederherstellung der Datenverbindung an das DPC weiter. |

## Funktionsweise von RDC

In der folgenden Liste wird der von Adobe verwendete Datenerfassungsprozess beschrieben:

1. DNS löst den Hostnamen der Datenerfassung automatisch in die IP-Adresse des Data Collection Centers auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.
