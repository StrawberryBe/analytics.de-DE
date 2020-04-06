---
description: Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Abrechnung, Protokolle usw.), Unternehmensverwaltung, Tools, Web-Services, Report Builder und die Data Connectors-Integration.
keywords: groups;permissions
subtopic: Users and groups
title: Anpassen von Berechtigungen für Analytics-Tools
topic: Admin tools
uuid: 8e86bc17-46d3-4c5e-ac25-9f3bfc29b8fa
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Anpassen von Berechtigungen für Analytics-Tools

>[!IMPORTANT]
>
>Die Verwaltung von Benutzern und Produkten wurde in die [Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) verschoben. Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen. After all customers have migrated, help content for **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** will be retired.

Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Abrechnung, Protokolle usw.), Unternehmensverwaltung, Tools, Web-Services, Report Builder und die Data Connectors-Integration.

**[!UICONTROL User Management]** > **[!UICONTROL Groups]** > **[!UICONTROL All Report Access]** > **[!UICONTROL Analytics Tools]** > **[!UICONTROL Customize]**

>[!NOTE] In der Herbstversion 2016 (20. Oktober) wurden neue Gruppenverwaltungsfunktionen eingeführt. Unter [Administrative Änderungen – Herbst 2016](/help/admin/user-management2/c-user-management/permissions-changes.md) finden Sie eine Zusammenfassung der Neuheiten.

## Berichtszugriff – Analytics-Tools

![](assets/report-access-analytics-tools.png)

Click **[!UICONTROL Customize]** to select items to which this group will have access.

## Feldbeschreibungen

Die Einstellungen auf dieser Seite beziehen sich auf die auf der [!UICONTROL Define User Groups] Seite ausgewählten Report Suites.

| Element | Beschreibung |
|--- |--- |
| **Allgemein** |  |
| [Code-Manager](/help/admin/admin/code-manager-admin.md) | Ermöglicht das Herunterladen von Datenerfassungscode für Web- und mobile Plattformen. |
| Code-Manager – Web-Services | Ermöglicht Nichtadministratoren den Zugriff auf den Code-Manager über Web-Services. |
| [Protokolle](/help/admin/admin/logs.md) | Ermöglicht Zugriff auf Protokolldateien, mit deren Hilfe Sie sehen können, wann sich Benutzer anmelden, wie sie nutzen, auf die Dateien zugreifen, Report Suites erstellen und Admin-Änderungen vornehmen. |
| Protokolle – Web-Services | Ermöglicht es Nichtadministratoren, über Web-Services auf die Admin Tools-Protokolle zuzugreifen. |
| [Traffic-Management](/help/admin/c-traffic-management/traffic-management.md) | Auf der Seite &quot;Traffic-Management&quot;können Sie erwartete Änderungen des Traffic-Volumens angeben. |
| Berechtigungsverwaltung | Ermöglicht Nichtadministratoren Zugriff auf die Seiten zur Benutzerverwaltung in den Admin Tools. Diese Benutzer haben Lese-, aber keine Schreibberechtigung. |
| Berechtigungen (schreiben) – Web-Services | Ermöglicht Nichtadministratoren die Lese- und Schreibberechtigungseinstellungen unter Benutzerverwaltung in Web-Services.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| Berechtigungen (lesen) – Web-Services | Ermöglicht Nichtadministratoren die Ansicht von Berechtigungseinstellungen unter Benutzerverwaltung in Web-Services.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| **Unternehmensverwaltung** |  |
| [Sicherheit](/help/admin/company/security-manager.md) | Gewährt Zugriff auf die Sicherheits-Manager-Seite, über die der Zugriff auf Berichtsdaten gesteuert wird. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen. |
| Supportinfo | Gewährt Zugriff auf die Supportinformationen in den Unternehmenseinstellungen. |
| [Web-Services](/help/admin/company/web-services-admin.md) | Ermöglicht den Zugriff auf die Seite &quot;Web-Services&quot;in der Oberfläche der Admin Tools ([!UICONTROL Company Settings] > [!UICONTROL Web Services]).<br>Mit der Web Services API erhalten Sie programmatischen Zugriff auf Adobe Analytics-Dienste, mit denen Sie verfügbare Funktionen über die Benutzeroberfläche duplizieren und erweitern können. |
| Single-Sign-On (veraltet) | Gewährt Zugriff auf die Single Sign-On-Seite in den Admin Tools.<br>**Hinweis:**Single Sign-on wird in Adobe Experience Cloud mithilfe der[Kontoverknüpfung](https://marketing.adobe.com/resources/help/de_DE/mcloud/organizations.html)zwischen Experience Cloud und anderen Lösungen ermöglicht. |
| [Ausstehende Aktionen](/help/admin/company/pending-actions-admin.md) | Grants permission to manage pending actions in [!UICONTROL Company Settings]. |
| [Co-Branding](/help/admin/company/co-branding-admin.md) | Ermöglicht das Co-Branding von Analytics. |
| [Voreinstellungen](/help/admin/admin/preferences-manager.md) | Grants permission to the [!UICONTROL Preference Manager]. |
| [Report Suites ausblenden](/help/admin/company/c-hide-report-suites.md) | Erteilt die Berechtigung zum Ausblenden von Report Suites in der Benutzeroberfläche von Adobe Analytics. |
| **Tools** | Diese Einstellungen gewähren Zugriff auf Analytics-Tools (Schnittstellen und Anwendungen) und erweiterte Funktionen wie Segmentierung und berechnete Metriken. |
| [Aktuelle Daten](https://marketing.adobe.com/resources/help/de_DE/reference/data_latency.html) | Ermöglicht die Verwendung der Funktion &quot;Aktuelle Daten&quot;in Berichte. |
| [Ad Hoc Analysis-Lizenzanwender](https://marketing.adobe.com/resources/help/de_DE/dsc/) | Ermöglicht Zugriff [!UICONTROL Ad Hoc Analysis]. |
| Zugriff auf Web Services | Aktiviert den Web-Services-Zugriff für Nicht-Administratoren. Generiert Webdienst-Anmeldeinformationen. |
| [Report Builder](https://marketing.adobe.com/resources/help/de_DE/arb/setup.html) | Gewährt Mitgliedern dieser Gruppe Zugriff auf [!UICONTROL Report Builder] Lizenzen. |
| [Zugriff auf Analysis Workspace](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/) | Gewährt Benutzern Zugriff auf Analysis Workspace, die für [!DNL Adobe Analytics] empfohlene Berichtsschnittstelle. |
| [Reports &amp; Analytics](https://marketing.adobe.com/resources/help/de_DE/sc/user/) | Gewährt Benutzern Zugriff auf Reports &amp; Analytics. |
| [Erstellung berechneter Metriken](https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics/) | Ermöglicht Benutzern das Erstellen von berechneten Metriken. |
| [Erstellung von Segmenten](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/) | Ermöglicht Benutzern das Erstellen von Segmenten. |
| **Data Connectors** |  |
| Integrationen (Erstellen, Aktualisieren oder Löschen) | Ermöglicht das Erstellen, Aktualisieren und Löschen von Data Connector-Integrationen. |
