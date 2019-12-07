---
description: Content Delivery Services oder Content Distribution Networks (CDNs) – wie Akamai oder Speedera – pushen Webinhalte näher an Netzwerk-Edges, sodass sich häufig angeforderte Dokumente näher bei dem Standort befinden, von dem aus auf sie zugegriffen wird.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Content Delivery Services/Networks
topic: Developer and implementation
uuid: 6cb57c59-d0f9-4ca5-9f15-0e74e585a4a1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Content Delivery Services/Networks

Content Delivery Services oder Content Distribution Networks (CDNs) – wie Akamai oder Speedera – pushen Webinhalte näher an Netzwerk-Edges, sodass sich häufig angeforderte Dokumente näher bei dem Standort befinden, von dem aus auf sie zugegriffen wird.

Dadurch können Zugriffslatenzzeiten, belegte Bandbreiten und Infrastrukturkosten für gewöhnlich reduziert werden.

Ihre AppMeasurement-Bibliotheksdatei für JavaScript kann über ein CDN übertragen werden, damit die Datei schneller an die Standorte von Benutzern übertragen wird. Adobe-Kunden müssen sicherstellen, dass sie ihre CDN-Dienste korrekt konfiguriert haben. CDNs sind häufig die Ursache für Schwankungen bei Downloadzeiten und sollten in solchen Fällen zuerst überprüft werden.

Der Tag-Manager speichert alle JavaScript-Dateien in einem CDN.
