---
product: analytics
audience: admin
user-guide-title: Administratorhandbuch für Analytics
breadcrumb-title: Administratorhandbuch
user-guide-description: Erfahren Sie mehr über Analytics-Verwaltungsaufgaben, wie z. B. das Verwalten von Benutzern und Produkten in der Experience Cloud Admin Console, das Konfigurieren von Report Suites und mehr.
source-git-commit: 709483bd7a4573004100c9508f5bd78f1f3f253e
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 95%

---


# Administratorhandbuch für Adobe Analytics {#admin}

+ [Administratorhandbuch für Analytics](home.md)
+ [Versionshinweise zu Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=de)
+ Adobe Admin Console {#admin-console}
   + [Überblick](admin-console/home.md)
   + [Erstes Adobe Analytics-Handbuch für Admins](admin-console/first-admin-guide.md)
   + [Administratorrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Übersicht über die Berechtigungen für Analytics-Tools {#permissions}
      + [Analytics-Berechtigungen in der Admin Console](admin-console/permissions/summary-tables.md)
      + [Produktprofile für Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Produktprofil-Berechtigungen für Report Suite-Werkzeuge](admin-console/permissions/report-suite-tools.md)
      + [Produktprofilberechtigungen für Analytics-Werkzeuge](admin-console/permissions/analytics-tools.md)
   + Benutzer und Produkte verwalten (alt) {#user-product-management}
      + [Verwalten von Benutzern und Produkten (Legacy)](admin-console/user-management2/user-management.md)
      + Migrieren von Benutzern zur Adobe Admin Console {#migrate-users}
         + [Analytics-Benutzermigration zur Admin Console](admin-console/user-management2/user-migration/c-migration-tool.md)
         + [Migrieren von Analytics-Benutzerkonten für Adobe IDs](admin-console/user-management2/user-migration/t-migrate-users.md)
         + [Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs](admin-console/user-management2/user-migration/migrate-enterprise.md)
         + [Deaktivieren von veralteten Anmeldedaten](admin-console/user-management2/user-migration/t-disable-legacy-login.md)
         + [Von der Migration betroffene APIs](admin-console/user-management2/user-migration/developer.md)
+ Admin Tools für Analytics {#admin-tools}
   + [Übersicht über Admin Tools](admin/c-admin-tools.md)
   + [Abrechnung](admin/billing-admin.md)
   + [Code-Manager](admin/code-manager-admin.md)
   + [Währungs-Codes](admin/currency.md)
   + [Datenquellen](admin/data-sources.md)
   + [Standardmetriken](admin/default-metrics.md)
   + [Nach IP-Adresse ausschließen](admin/exclude-ip.md)
   + [Protokolle](admin/logs.md)
   + [Datenschutzberichte](admin/privacy-reporting.md)
   + [Reporting Activity Manager](admin/reporting-activity.md)
   + [Warteschlange für terminierte Berichte](admin/scheduled-reports-admin.md)
   + Report Suite Manager {#manage-report-suites}
      + [Verwalten von Report Suites](admin/c-manage-report-suites/report-suites-admin.md)
      + [Datenaggregations-Report Suites und globale Report Suites](admin/c-manage-report-suites/rollup-report-suite.md)
      + [Speichern einer Report Suite-Suche](admin/c-manage-report-suites/t-report-suite-saved-search.md)
      + [Herunterladen von Report Suite-Einstellungen](admin/c-manage-report-suites/t-download-rs-settings.md)
      + Neue Report Suite {#c-new-report-suite}
         + [Erstellen einer Report Suite](admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)
         + [Erstellen einer Datenaggregations-Report Suite](admin/c-manage-report-suites/c-new-report-suite/t-rollups.md)
         + [Erstellen einer Report Suite-Gruppe](admin/c-manage-report-suites/c-new-report-suite/t-create-rs-group.md)
         + [Neue Report Suite – Einstellungen](admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md)
         + [Aus einer Quell-Report Suite nicht kopierte Einstellungen](admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)
      + Report Suite-Vorlagen {#report-suite-templates}
         + [Übersicht über Report Suite-Vorlagen](admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)
         + [Aggregatorportal](admin/c-manage-report-suites/c-report-suite-templates/aggregator-portal.md)
         + [Handel](admin/c-manage-report-suites/c-report-suite-templates/commerce-admin.md)
         + [Inhalte und Medien](admin/c-manage-report-suites/c-report-suite-templates/content-media.md)
         + [Standardvorlage](admin/c-manage-report-suites/c-report-suite-templates/default-rs-template.md)
         + [Finanzdienste](admin/c-manage-report-suites/c-report-suite-templates/financial-services.md)
         + [Job-Portal](admin/c-manage-report-suites/c-report-suite-templates/job-portal.md)
         + [Lead-Generierung](admin/c-manage-report-suites/c-report-suite-templates/lead-generation.md)
         + [Unterstützungsmedien](admin/c-manage-report-suites/c-report-suite-templates/support-media.md)
      + Bearbeiten der Einstellungen einer Report Suite {#edit-report-suite}
         + Allgemein {#report-suite-general}
            + [Allgemeine Kontoeinstellungen](admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
            + [Interne URL-Filter](admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)
            + Erkennung von Paid Search {#paid-search-detection}
               + [Übersicht über die Paid-Search-Erkennung](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)
               + [Konfigurieren der Erkennung von Paid Search](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)
            + [Benutzerspezifische Menüeinstellung](admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md)
            + [Anpassen von Kalendern](admin/c-manage-report-suites/c-edit-report-suites/general/custom-calendar.md)
            + Verarbeitungsregeln {#c-processing-rules}
               + [Übersicht über Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md)
               + Konfiguration der Verarbeitungsregeln {#c-processing-rules-configuration}
                  + [Funktionsweise von Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/processing-rules-about.md)
                  + [Erstellen von Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)
                  + [Anzeigen der aktiven Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-view.md)
                  + [Anzeigen des Verlaufs von Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rule-view-history.md)
                  + [Wiederherstellen von Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-restore.md)
                  + [Kopieren von Verarbeitungsregeln in eine andere Report Suite](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md)
                  + [Für Verarbeitungsregeln verfügbare Dimensionen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rule-dimensions.md)
               + Beispiele für Verarbeitungsregeln {#processing-rules-examples}
                  + [Beispiele für Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-examples.md)
                  + [Füllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populate-campaign-id.md)
                  + [Festlegen des Produktansichtsereignisses auf der Seite „Produktübersicht“](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/setting-the-product-view-event.md)
                  + [Hinzufügen einer Unterkategorie durch Verketten von Kategorie und Seitenname](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/subcategory-concatenating.md)
                  + [Bestimmen eines Pfads durch Kopieren eines eVar-Werts in eine Eigenschaft](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-determining-path.md)
                  + [Bereinigen von Werten in einem Bericht](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md)
                  + [Füllen interner Suchbegriffe mithilfe eines Abfragezeichenfolgenparameters](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populating-internal-search.md)
                  + [Kopieren einer Kontextdatenvariable in eine eVar](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md)
                  + [Festlegen eines Ereignisses mit einer Kontextdatenvariablen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md)
                  + [Entfernen eines Ereignisses aus einem Treffer](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-remove-event.md)
               + [Verarbeitungsregeln – Tipps und Tricks](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-tips.md)
            + Bot-Regeln {#bot-removal}
               + [Bot-Entfernung](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)
               + [Übersicht über Bot-Regeln](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)
               + [Allgemeine Bot-Signaturen](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-signatures.md)
               + [Bot-Ausschlussmethoden](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-exclusion-methods.md)
            + [Datenschutzeinstellungen](admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)
            + [Zeitstempel optional](admin/c-manage-report-suites/c-edit-report-suites/general/timestamp-optional.md)
            + Server-seitige Weiterleitung {#server-side-forwarding}
               + [Übersicht über die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
               + [DSGVO/ePrivacy – Einhaltung und Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Anforderungen an die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-requirements.md)
               + [Daten- und Codereferenz für die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-reference.md)
               + [Überprüfen der Server-seitigen Weiterleitungsimplementierung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md)
               + [Häufig gestellte Fragen zur Server-seitigen Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md)
         + Traffic-Variablen {#traffic-variables}
            + [Übersicht über Traffic-Variablen (Eigenschaft)](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
            + [Aktivieren von Traffic-Variablen-Berichten](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/t-traffic-variable.md)
            + [Traffic-Klassifizierungen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-classifications.md)
            + [Beschreibung benutzerspezifischer Berichte](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/custom-desc-admin.md)
         + Konversionsvariablen {#conversion-variables}
            + [Konversionsvariablen (eVars)](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md)
            + [Suchmethoden](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/finding-methods.md)
            + [Konversionsklassifizierungen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-classifications.md)
            + Unique-Visitor-Variable {#unique-visitor-variable}
               + [Festlegen der Unique-Visitor-Variable](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [Anwendungsfall – Extrahieren von Besucher-IDs](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + Erfolgsereignisse {#success-events}
               + [Übersicht über Erfolgsereignisse](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)
               + [Konfigurieren von Erfolgsereignissen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/t-success-events.md)
               + [Informationen zum Ändern des Ereignistyps](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/event-type.md)
            + [Klassifizierungshierarchien](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/classification-hierarchies.md)
            + [Listenvariablen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md)
            + [Merchandising-eVars](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/merchandising-evars.md)
         + [Marketing-Kanäle](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels-admin.md)
         + Traffic-Management {#traffic-management}
            + [Überblick](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/traffic-management.md)
            + [Spitze planen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)
            + [Dauerhafter Traffic](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)
         + [Mobile-App-Verwaltung](admin/c-manage-report-suites/c-edit-report-suites/mobile-management.md)
         + Echtzeitberichte {#real-time-reports}
            + [Übersicht über Echtzeitberichte](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)
            + [Konfiguration von Echtzeitberichten](admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md)
            + [Unterstützte Echtzeit-Metriken und -Dimensionen](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md)
   + Unternehmenseinstellungen {#company-settings}
      + [Übersicht über Unternehmenseinstellungen](admin/company/c-company-settings.md)
      + [Sicherheits-Manager](admin/company/security-manager.md)
      + [Web-Services](admin/company/web-services-admin.md)
      + [Report Builder-Berichte](admin/company/report-builder-reports-admin.md)
      + [Single Sign-on](admin/company/single-signon-admin.md)
      + [Co-Branding](admin/company/co-branding-admin.md)
      + [Ausblenden von Report Suites](admin/company/c-hide-report-suites.md)
      + [Voreinstellungs-Manager](admin/company/preferences-manager.md)
      + [Ausstehende Aktionen](admin/company/pending-actions-admin.md)
      + [Funktionszugriffsebenen](admin/company/feature-access-levels.md)
   + [Video-Management](admin/video-management.md)
   + Nutzung der Server-Aufrufe {#server-call-usage}
      + [Übersicht zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/overage-overview.md)
      + [Anzeigen der aktuellen Nutzung der Server-Aufrufe](admin/c-server-call-usage/server-call-usage-dashboard.md)
      + [Anzeigen der Nutzung der Report Suite](admin/c-server-call-usage/report-suite-usage.md)
      + [Warnhinweise zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/scu-alerts.md)
      + [Häufig gestellte Fragen zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/overage-faq.md)
+ Data Governance {#data-governance}
   + [Adobe Analytics-Workflow zum Datenschutz](c-data-governance/an-gdpr-workflow.md)
   + [Häufig gestellte Fragen](c-data-governance/gdpr-faq.md)
   + Datenbeschriftung {#data-labels}
      + [Datenschutzbezeichnungen für Analytics-Komponenten](c-data-governance/data-labeling/gdpr-labels.md)
      + [Report Suite-Daten beschriften](c-data-governance/data-labeling/gdpr-setup-reportsuite.md)
      + [Datenschutzbezeichnungen von Report Suites anzeigen/verwalten](c-data-governance/data-labeling/gdpr-view-settings.md)
      + [Best Practices für Beschriftungen](c-data-governance/data-labeling/gdpr-analytics-ids.md)
      + [Beschriftungsbeispiel](c-data-governance/data-labeling/gdpr-labeling-example.md)
      + [Namespaces](c-data-governance/data-labeling/gdpr-namespaces.md)
   + [Zugriffs- und Löschanfragen einreichen](c-data-governance/gdpr-submit-access-delete.md)
   + [ID-Erweiterung](c-data-governance/gdpr-id-expansion.md)
   + [CNIL-Zustimmungsfreistellung](c-data-governance/cnil-consent-exemption.md)
+ [Admin-API](c-admin-api/c-admin-api.md)
