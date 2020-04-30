---
description: Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Abrechnung, Protokolle usw.), Unternehmensverwaltung, Tools, Web-Services, Report Builder und die Data Connectors-Integration.
keywords: groups;permissions
subtopic: Users and groups
title: Anpassen von Berechtigungen für Analytics-Tools
topic: Admin tools
uuid: 8e86bc17-46d3-4c5e-ac25-9f3bfc29b8fa
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

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

The settings on this page pertain to the report suites selected on the [!UICONTROL Define User Groups] page.

| Element | Beschreibung |
|--- |--- |
| **Allgemein** |  |
| [Code-Manager](/help/admin/admin/code-manager-admin.md) | Ermöglicht das Herunterladen von Datensammlungs-Code für Web- und mobile Plattformen. |
| Code-Manager – Web-Services | Ermöglicht es Nichtadministratoren, über Web-Services auf den Code-Manager zuzugreifen. |
| [Protokolle](/help/admin/admin/logs.md) | Ermöglicht Zugriff auf Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. |
| Protokolle – Web-Services | Ermöglicht es Nichtadministratoren, über Web-Services auf Admin Tools-Protokolle zuzugreifen. |
| [Traffic-Management](/help/admin/c-traffic-management/traffic-management.md) | Auf der Seite „Traffic-Management“ können Sie Informationen zu erwarteten Änderungen des Trafficvolumens angeben. |
| Berechtigungsverwaltung | Ermöglicht Nichtadministratoren Zugriff auf Benutzerverwaltungsseiten in den Admin Tools. Diese Benutzer können die Einstellungen zwar lesen, aber nicht bearbeiten. |
| Berechtigungen (schreiben) – Web-Services | Erteilt Benutzern ohne Administratorrechte Lese- und Schreibberechtigungen für das Benutzermanagement der Web-Services.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| Berechtigungen (lesen) – Web-Services | Ermöglicht es Nichtadministratoren, Berechtigungseinstellungen in der Benutzerverwaltung über Web-Services einzusehen.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| **Unternehmensverwaltung** |  |
| [Sicherheit](/help/admin/company/security-manager.md) | Gewährt Zugriff auf die Sicherheits-Manager-Seite, über die der Zugriff auf Berichtsdaten gesteuert wird. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen. |
| Support-Info | Gewährt Zugriff auf die Supportinformationen in den Unternehmenseinstellungen. |
| [Web-Services](/help/admin/company/web-services-admin.md) | Ermöglicht den Zugriff auf die Seite &quot;Web-Services&quot;in der Oberfläche der Admin Tools ([!UICONTROL Company Settings] > [!UICONTROL Web Services]).<br>Mit der Web Services API erhalten Sie programmatischen Zugriff auf Adobe Analytics-Dienste, mit denen Sie verfügbare Funktionen über die Benutzeroberfläche duplizieren und erweitern können. |
| Single Sign-on (veraltet) | Gewährt Zugriff auf die Single Sign-on-Seite in den Admin Tools.<br>**Hinweis:**Single Sign-on wird in Adobe Experience Cloud mithilfe der[Kontoverknüpfung](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/organizations.html)zwischen Experience Cloud und anderen Lösungen ermöglicht. |
| [Ausstehende Aktionen](/help/admin/company/pending-actions-admin.md) | Grants permission to manage pending actions in [!UICONTROL Company Settings]. |
| [Co-Branding](/help/admin/company/co-branding-admin.md) | Ermöglicht das Co-Branding von Analytics. |
| [Voreinstellungen](/help/admin/admin/preferences-manager.md) | Grants permission to the [!UICONTROL Preference Manager]. |
| [Report Suites ausblenden](/help/admin/company/c-hide-report-suites.md) | Erteilt die Berechtigung zum Ausblenden von Report Suites in der Benutzeroberfläche von Adobe Analytics. |
| **Tools** | Mit diesen Einstellungen kann Zugriff auf Analytics-Tools (Oberflächen und Anwendungen) und erweiterte Funktionen wie Segmentierung und berechnete Metriken gewährt werden. |
| [Aktuelle Daten](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/current-data.html) | Ermöglicht die Verwendung der Funktion „Aktuelle Daten“ für Berichte. |
| [Ad Hoc Analysis-Lizenzanwender](https://docs.adobe.com/content/help/de-DE/analytics/analyze/ad-hoc-analysis/adhoc-home.html) | Grants permission to access [!UICONTROL Ad Hoc Analysis]. |
| Zugriff auf Web Services | Ermöglicht Nichtadministratoren Zugriff auf Web-Services. Erstellt Anmeldedaten für Web-Services. |
| [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/t-install-arb.html) | Grants members of this group access to [!UICONTROL Report Builder] licenses. |
| [Zugriff auf Analysis Workspace](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/analysis-workspace-features.html) | Gewährt Benutzern Zugriff auf Analysis Workspace, die für [!DNL Adobe Analytics] empfohlene Berichtsschnittstelle. |
| [Reports &amp; Analytics](https://docs.adobe.com/content/help/en/analytics/landing/an-key-concepts.html) | Gewährt Benutzern Zugriff auf Reports &amp; Analytics. |
| [Erstellung berechneter Metriken](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/cm-overview.html) | Ermöglicht es Benutzern, berechnete Metriken zu erstellen. |
| [Erstellung von Segmenten](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/seg-home.html) | Ermöglicht es Benutzern, Segmente zu erstellen. |
| **Data Connectors** |  |
| Integrationen (erstellen, aktualisieren oder löschen) | Ermöglicht das Erstellen, Aktualisieren und Löschen von Data Connector-Integrationen. |
