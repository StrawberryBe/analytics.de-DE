---
description: In diesem Abschnitt werden die Schritte beschrieben, mit denen Sie Ihre Adobe Analytics-Implementierung aktivieren können, um die Zugriffsrechte der betroffenen Personen auf den Datenschutz und Löschrechte zu unterstützen.
title: Workflow zum Datenschutz
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: tm+mt
source-git-commit: b3ea538d0d6e6ebbbbd17871aacaed7527cf3976
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 94%

---


# Workflow zum Datenschutz

Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die Datenschutz-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

| Beschreibung der Aufgabe | Links zu Anweisungen und weiteren Informationen |
|--- |--- |
| **Schritt 1**: Stellen Sie sicher, dass all Ihre Report Suites, die möglicherweise datenschutzrelevante Daten enthalten, Ihrer Experience Cloud- oder IMS-Organisation zugewiesen sind.  Datenschutzanfragen werden unter Verwendung einer Experience Cloud-Organisation eingereicht und auf alle Report Suites dieser Organisation angewendet. Anfragen gelten nicht für Report Suites, die nicht der entsprechenden Organisation zugeordnet sind, selbst wenn sie Ihrem Anmeldeunternehmen angehören. | Weitere Informationen finden Sie unter [Report Suites einer Organisation zuordnen](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html). |
| **Schritt 2**: Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest. | Eine Richtlinie zur Datenaufbewahrung muss vorhanden sein, damit Adobe Datenschutzanfragen zum Datenzugriff und zur Datenlöschung bearbeiten kann.  Weitere Informationen finden Sie unter [Häufig gestellte Fragen zur Datenaufbewahrung in Analytics](/help/technotes/data-retention.md). |
| **Schritt 3**: Machen Sie sich mit den DULE/Datenschutzbezeichnungen, Adobe Analytics-IDs, Namensräumen und der ID-Erweiterung vertraut. | Lesen Sie hierzu folgende Themen dieser Dokumentation:<ul><li>[Datenschutzbezeichnungen für Analytics-Variablen](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **Schritt 4**: Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.  Hinweis: Beachten Sie, dass die Beschriftung bei jeder Erstellung einer neuen Report Suite überprüft werden muss und immer dann, wenn für eine vorhandene Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. | Befolgen Sie die Anweisungen unter [Report Suite-Daten beschriften](/help/admin/c-data-governance/gdpr-setup-reportsuite.md). |
| **Schritt 5**: Stellen Sie eine Verbindung zur Adobe Data Privacy API her und reichen Sie Zugriffs- und Löschanfragen ein. | Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf der [Data Privacy API von Adobe Experience Cloud einreichen](https://www.adobe.io/apis/experienceplatform/gdpr.html). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md)). |
| **Schritt 6**: Sehen Sie sich die Datenschutzeinstellungen Ihrer Report Suite an und verwalten Sie sie. | Befolgen Sie die Anweisungen unter [Data-Governance-Einstellungen von Report Suites anzeigen](/help/admin/c-data-governance/gdpr-view-settings.md). |
