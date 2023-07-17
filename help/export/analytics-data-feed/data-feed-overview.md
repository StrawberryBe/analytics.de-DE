---
description: Daten, die aus Websites oder mobilen Apps erfasst bzw. über Web-Service-APIs oder Datenquellen hochgeladen werden, werden im Adobe Data Warehouse verarbeitet und gespeichert. Diese Clickstream-Rohdaten bilden die Grundlage für den Datensatz, der von Adobe Analytics genutzt wird.
keywords: Clickstream;Daten-Feed;Daten-Feed;Data Feed
title: Analytics-Daten-Feed-Dokumentation
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: f66cc6252ecd54c143c08be1e0e7e5bf90cc42e9
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 87%

---

# Analytics-Daten-Feed-Dokumentation

Daten-Feeds sind eine leistungsstarke Methode, Rohdaten aus Adobe Analytics abzurufen. Diese Rohdaten können nach Ermessen Ihrer Organisation auf anderen Plattformen außerhalb von Adobe verwendet werden. Die Daten werden in stündlichen Stapeln am Ende jeder Stunde oder in täglichen Stapeln am Ende jedes Tages bereitgestellt.

## Voraussetzungen

Bevor Sie Daten-Feeds verwenden, müssen Sie alle folgenden Anforderungen erfüllen.

* Eine funktionierende Implementierung, die Daten an Adobe-Datenerfassungsserver sendet. Siehe [Implementierung validieren und veröffentlichen](/help/implement/launch/validate-publish-prod.md) im Implementierungshandbuch.
* Ihr Konto ist ein Analytics-Produktadministrator, oder Ihr Konto gehört zu einem Produktprofil mit Zugriff auf Daten-Feeds.
* Ein Bucket, der für Amazon S3, Google Cloud Platform, Azure RBAC oder Azure SAS konfiguriert wurde.
* (Veraltet: Nur für veraltete FTP- und SFTP-Zieltypen erforderlich) Verwenden Sie eine FTP-Site und Ihre Anmeldeinformationen (FTP-Anmeldeinformationen, die von Ihrem Unternehmen bereitgestellt werden).

## Empfohlene Daten-Feed-Ressourcen

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Navigieren Sie in der oberen Navigationsleiste zu „Admin“ > „Daten-Feeds“.
4. Klicken Sie auf [!UICONTROL Hinzufügen]. Eine neue Seite mit drei Hauptkategorien wird angezeigt: [!UICONTROL Feed-Informationen], [!UICONTROL Ziel] und [!UICONTROL Datenspaltendefinitionen].
5. Füllen Sie die Felder [!UICONTROL Feed-Informationen] aus.
   * Name: Beliebiger Name, z. B. „Test-Daten-Feed“.
   * Report Suite: Wählen Sie die gewünschte Report Suite aus.
   * E-Mail nach Abschluss: Geben Sie Ihre E-Mail-Adresse ein.
   * Feed-Intervall: Wählen Sie das gewünschte Intervall aus (stündlich oder täglich).
   * Verarbeitung verzögern: Kann auf [!UICONTROL Keine Verzögerung] eingestellt bleiben.
   * Start- und Enddaten: Wählen Sie ein Startdatum vor einigen Tagen und heute als Enddatum aus.
6. Füllen Sie die [!UICONTROL Ziel]-Felder aus.
   * Typ: FTP
   * Host: Geben Sie die gewünschte FTP-Ziel-URL ein. Beispiel: `ftp://ftp.omniture.com`.
   * Pfad: Kann leer gelassen werden
   * Benutzername: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.
   * Kennwort und Kennwort bestätigen: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.
7. Füllen Sie die [!UICONTROL Datenspaltendefinitionen] aus.
   * Wählen Sie in der Dropdown-Liste die neueste Vorlage &quot;Alle Adobe Columns&quot; aus.
   * Komprimierungsformat: Gzip
   * Verpackungstyp: Mehrere Dateien
   * Manifest: Keine Datei
8. Klicken Sie oben rechts auf [!UICONTROL Speichern].
9. Nach dem Speichern beginnt die Verarbeitung der historischen Daten. Wenn die Verarbeitung der Daten für einen Tag abgeschlossen ist, wird die Datei auf der FTP-Site abgelegt.
10. Melden Sie sich mit Windows Explorer oder einem dedizierten FTP-Client bei der FTP-Site an.
11. Laden Sie die komprimierte Daten-Feed-Datei auf Ihren lokalen Computer herunter.
12. Dekomprimieren Sie die komprimierte Datei mit einem Programm, das `.tar.gz`-Dateierweiterungen unterstützt.
13. Öffnen Sie die `hit_data.tsv`-Datei in Ihrer gewünschten Tabellenkalkulations- oder Datenbankanwendung, um die Rohdaten für diesen Tag anzuzeigen.

## Nächste Schritte

Sobald Sie den grundlegenden Workflow beim Abrufen von Daten-Feeds kennen, können Sie mit Teams in Ihrer Organisation zusammenarbeiten, um Rohdaten in einer Datenbank zu speichern oder zu erfassen.

* [Best Practices für Datenfeeds](/help/export/analytics-data-feed/data-feeds-best-practices.md): Best Practices zum Erstellen und Verwalten von Daten-Feeds.
* [Erstellen von Daten-Feeds](create-feed.md): Technische Details zum Erstellen eines Daten-Feed, detaillierte Erläuterungen einzelner Felder
* [Verwalten von Daten-Feeds](df-manage-feeds.md): Weitere Informationen zum Navigieren in der Daten-Feed-Benutzeroberfläche
* [Daten-Feed-Inhalte](c-df-contents/datafeeds-contents.md): Informationen zum Inhalt der komprimierten Datei <!-- Is this still the output users can download from the destination? I aske Jun. -->
* [Definitionen der Datenspalten](c-df-contents/datafeeds-reference.md): Eine vollständige Liste aller verfügbaren Spalten.
* Video zur Navigation auf der Daten-Feed-Oberfläche:

  >[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

* Video zur Suche nach Ihrer Daten-Feed-ID:

  >[!VIDEO](https://video.tv.adobe.com/v/335747/?quality=12)