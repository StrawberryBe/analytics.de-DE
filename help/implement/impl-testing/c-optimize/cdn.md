---
description: Content Delivery Services oder Content Distribution Networks (CDNs) – wie Akamai oder Speedera – pushen Webinhalte näher an Netzwerk-Edges, sodass sich häufig angeforderte Dokumente näher bei dem Standort befinden, von dem aus auf sie zugegriffen wird.
keywords: Analytics-Implementierung
seo-description: Content Delivery Services oder Content Distribution Networks (CDNs) – wie Akamai oder Speedera – pushen Webinhalte näher an Netzwerk-Edges, sodass sich häufig angeforderte Dokumente näher bei dem Standort befinden, von dem aus auf sie zugegriffen wird.
seo-title: Content Delivery Services/Networks
solution: Analytics
subtopic: Fehlerbehebung
title: Content Delivery Services/Networks
topic: Entwickler und Implementierung
uuid: 6cb57c59-d0f9-4ca5-9f15-0e74e585a4a1
translation-type: ht
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# Content Delivery Services/Networks

Content Delivery Services oder Content Distribution Networks (CDNs) – wie Akamai oder Speedera – pushen Webinhalte näher an Netzwerk-Edges, sodass sich häufig angeforderte Dokumente näher bei dem Standort befinden, von dem aus auf sie zugegriffen wird.

Dadurch können Zugriffslatenzzeiten, belegte Bandbreiten und Infrastrukturkosten für gewöhnlich reduziert werden.

Ihre AppMeasurement-Bibliotheksdatei für JavaScript kann über ein CDN übertragen werden, damit die Datei schneller an die Standorte von Benutzern übertragen wird. Adobe-Kunden müssen sicherstellen, dass sie ihre CDN-Dienste korrekt konfiguriert haben. CDNs sind häufig die Ursache für Schwankungen bei Downloadzeiten und sollten in solchen Fällen zuerst überprüft werden.

Der Tag-Manager speichert alle JavaScript-Dateien in einem CDN.
