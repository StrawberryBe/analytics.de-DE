---
description: Daten, die aus Websites oder mobilen Apps erfasst bzw. über Web-Service-APIs oder Datenquellen hochgeladen werden, werden im Adobe Data Warehouse verarbeitet und gespeichert. Diese Clickstream-Rohdaten bilden die Grundlage für den Datensatz, der von Adobe Analytics genutzt wird.
keywords: Clickstream;Daten-Feed;Daten-Feed;Data Feed
title: Analytics-Daten-Feed-Dokumentation
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 84bdeb5d502e46c922fc5123fcdd5b6819426c0e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 69%

---

# Analytics-Daten-Feed-Dokumentation

Daten-Feeds sind eine leistungsstarke Methode, Rohdaten aus Adobe Analytics abzurufen. Diese Rohdaten können nach Ermessen Ihrer Organisation auf anderen Plattformen außerhalb von Adobe verwendet werden. Die Daten werden in stündlichen Stapeln am Ende jeder Stunde oder in täglichen Stapeln am Ende jedes Tages bereitgestellt.

## Voraussetzungen

Bevor Sie Daten-Feeds verwenden, müssen Sie alle folgenden Anforderungen erfüllen.

* Eine funktionierende Implementierung, die Daten an Adobe-Datenerfassungsserver sendet. Siehe [Implementierung validieren und veröffentlichen](/help/implement/launch/validate-publish-prod.md) im Implementierungshandbuch.
* Ihr Konto ist ein Analytics-Produktadministrator, oder Ihr Konto gehört zu einem Produktprofil mit Zugriff auf Daten-Feeds.
* Ein Bucket, der für Amazon S3, Google Cloud Platform, Azure RBAC oder Azure SAS konfiguriert wurde.
* (Veraltet: Nur für veraltete FTP- und SFTP-Zieltypen erforderlich) Verwenden Sie eine FTP-Site und Ihre Anmeldeinformationen (FTP-Anmeldeinformationen, die von Ihrem Unternehmen bereitgestellt werden).

## Nächste Schritte

Die folgenden Ressourcen helfen Ihnen dabei, den grundlegenden Arbeitsablauf beim Abrufen von Daten-Feeds zu verstehen. Nachdem Sie den grundlegenden Workflow verstanden haben, können Sie mit Teams in Ihrem Unternehmen zusammenarbeiten, um Rohdaten in einer Datenbank zu speichern oder zu erfassen.

* [Best Practices für Datenfeeds](/help/export/analytics-data-feed/data-feeds-best-practices.md): Best Practices zum Erstellen und Verwalten von Daten-Feeds.
* [Erstellen von Daten-Feeds](create-feed.md): Technische Details zum Erstellen eines Daten-Feed, detaillierte Erläuterungen einzelner Felder
* [Verwalten von Daten-Feeds](df-manage-feeds.md): Weitere Informationen zum Navigieren in der Daten-Feed-Benutzeroberfläche
* [Daten-Feed-Inhalte](c-df-contents/datafeeds-contents.md): Informationen zum Inhalt der komprimierten Datei <!-- Is this still the output users can download from the destination? I aske Jun. -->
* [Definitionen der Datenspalten](c-df-contents/datafeeds-reference.md): Eine vollständige Liste aller verfügbaren Spalten.
* Video zur Navigation auf der Daten-Feed-Oberfläche:

  >[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

* Video zur Suche nach Ihrer Daten-Feed-ID:

  >[!VIDEO](https://video.tv.adobe.com/v/335747/?quality=12)