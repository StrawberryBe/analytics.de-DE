---
description: Daten, die aus Websites oder mobilen Apps erfasst bzw. über Web-Service-APIs oder Datenquellen hochgeladen werden, werden im Adobe Data Warehouse verarbeitet und gespeichert. Diese Clickstream-Rohdaten bilden die Grundlage für den Datensatz, der von Adobe Analytics genutzt wird.
keywords: clickstream;data feed;datafeed;Data Feed
solution: Analytics
title: Analytics-Daten-Feed-Dokumentation
uuid: 6bdbe90c-e6ed-4bb0-b5be-24fd795adde4
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Analytics-Daten-Feed-Dokumentation

Data Feeds sind eine leistungsstarke Methode, Rohdaten aus Adobe Analytics zu erhalten. Diese Rohdaten können nach Ermessen Ihres Unternehmens auf anderen Plattformen außerhalb von Adobe verwendet werden. Die Daten werden in stündlichen Stapeln am Ende jeder Stunde oder in täglichen Stapeln am Ende jedes Tages bereitgestellt.

## Voraussetzungen

Bevor Sie Datenfeeds verwenden, müssen Sie alle folgenden Anforderungen erfüllen.

* Haben Sie eine FTP-Site und Anmeldeinformationen praktisch. Datenfeeds können nur an ein Serverziel gesendet werden. Ihr Unternehmen stellt in der Regel FTP-Anmeldeinformationen bereit. Adobe kann auf Anfrage einen FTP-Speicherort mit einer bescheidenen Menge Speicher bereitstellen. Wenden Sie sich an den Kundendienst, um ein FTP-Ziel für Datenfeeds anzufordern.
* Eine funktionierende Implementierung, die Daten an Adobe-Datenerfassungsserver sendet. Siehe Implementierung [überprüfen und veröffentlichen unter Starten](../../implement/implement-with-launch/validate-publish-prod.md) im Implementierungs-Benutzerhandbuch.
* Ihr Konto ist ein Analytics-Produktadministrator oder Ihr Konto gehört zu einem Produktprofil mit Zugriff auf Datenfeeds.

## Erste Schritte

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Navigieren Sie in der oberen Navigationsleiste zu Admin &gt; Datenfeeds.
4. Klicken Sie auf [!UICONTROL Hinzufügen]. Eine neue Seite mit drei Hauptkategorien wird angezeigt: [!UICONTROL Feed-Informationen], [!UICONTROL Ziel]und [!UICONTROL Datenspaltendefinitionen].
5. Füllen Sie die Felder [!UICONTROL Feed-Informationen] aus.
   * Name: Beliebiger Name, z. B. "Testdatenfeed".
   * Report Suite: Wählen Sie die gewünschte Report Suite aus.
   * E-Mail nach Abschluss: Geben Sie Ihre E-Mail ein.
   * Feed-Intervall: Wählen Sie das gewünschte Intervall aus (stündlich oder täglich).
   * Verarbeitung verzögern: Kann als [!UICONTROL Keine Verzögerung]gelassen werden.
   * Start- und Enddaten: Wählen Sie ein Startdatum aus, das vor einigen Tagen und heute als Enddatum festgelegt wurde.
6. Füllen Sie die [!UICONTROL Felder Ziel] aus.
   * Typ: FTP
   * Host: Geben Sie die gewünschte FTP-Ziel-URL ein. Beispiel, `ftp://ftp.omniture.com`.
   * Pfad: Kann leer gelassen werden
   * Benutzername: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.
   * Kennwort und Kennwort bestätigen: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.
7. Füllen Sie die [!UICONTROL Datenspaltendefinitionen]aus.
   * Wählen Sie die neueste Vorlage "Alle Adobe-Spalten"im Dropdownmenü aus.
   * Komprimierungsformat: Gzip
   * Verpackungstyp: Mehrere Dateien
   * Manifest: Keine Datei
8. Klicken Sie oben rechts auf [!UICONTROL Speichern] .
9. Nach dem Speichern beginnt die Verarbeitung der historischen Daten. Wenn die Verarbeitung der Daten für einen Tag abgeschlossen ist, wird die Datei auf der FTP-Site abgelegt.
10. Melden Sie sich mit Windows Explorer oder einem dedizierten FTP-Client bei der FTP-Site an.
11. Laden Sie die komprimierte Data Feed-Datei auf Ihren lokalen Computer herunter.
12. Dekomprimieren Sie die komprimierte Datei mit einem Programm, das `.tar.gz` Dateierweiterungen unterstützt.
13. Öffnen Sie die `hit_data.tsv` Datei in Ihrer gewünschten Tabelle oder Datenbankanwendung, um die Rohdaten für diesen Tag anzuzeigen.

## Nächste Schritte

Sobald Sie den grundlegenden Arbeitsablauf beim Abrufen von Datenfeeds kennen, können Sie mit Teams in Ihrem Unternehmen zusammenarbeiten, um Rohdaten in einer Datenbank zu speichern oder zu erfassen.

[Erstellen Sie einen Datenfeed](create-feed.md): Technische Details zum Erstellen eines Datenfeeds, Erläuterungen zu einzelnen Feldern im Detail[Datenfeeds](df-manage-feeds.md)verwalten: Weitere Informationen zum Navigieren in der Data Feed-Oberfläche[Data Feed-Inhalte](c-df-contents/datafeeds-contents.md): Verstehen Sie, was sich in den Definitionen der komprimierten Datei[-Datenspalte befindet](c-df-contents/datafeeds-reference.md): Eine umfassende Liste aller verfügbaren Spalten

## Zusätzliche Ressourcen

Video in der Data Feed-Oberfläche:

> [!VIDEO](https://www.youtube.com/watch?v=m_fb--gNtR4)
