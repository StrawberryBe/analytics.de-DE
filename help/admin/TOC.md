---
product: analytics
audience: admin
user-guide-title: Administratorhandbuch für Analytics
breadcrumb-title: Administratorhandbuch
user-guide-description: Erfahren Sie mehr über Analytics-Verwaltungsaufgaben, wie z. B. das Verwalten von Benutzern und Produkten in der Experience Cloud Admin Console, das Konfigurieren von Report Suites und mehr.
source-git-commit: c8e3d9bd40a427387da746c084188b5d13f45bcd
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 94%

---


# Administratorhandbuch für Adobe Analytics {#admin}

+ [Administratorhandbuch für Analytics](home.md)
+ [Versionshinweise zu Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=de)
+ Adobe Admin Console {#admin-console}
   + [Überblick](admin-console/home.md)
   + [Adobe Analytics-Handbuch für erste Administratoren](admin-console/first-admin-guide.md)
   + [Administratorrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Übersicht über die Berechtigungen für Analytics-Tools {#permissions}
      + [Analytics-Berechtigungen in der Admin Console](admin-console/permissions/summary-tables.md)
      + [Produktprofile für Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Produktprofil-Berechtigungen für Report Suite-Werkzeuge](admin-console/permissions/report-suite-tools.md)
      + [Produktprofilberechtigungen für Analytics-Werkzeuge](admin-console/permissions/analytics-tools.md)
+ Admin-Tools für Analytics {#admin-tools}
   + [Übersicht über Admin-Tools](admin/c-admin-tools.md)
   + [Abrechnung](admin/billing-admin.md)
   + [Code-Manager](admin/code-manager-admin.md)
   + [Datenquellen](admin/data-sources.md)
   + [Nach IP-Adresse ausschließen](admin/exclude-ip.md)
   + [Protokolle](admin/logs.md)
   + [Reporting Activity Manager](admin/reporting-activity.md)
   + Report Suite Manager {#manage-report-suites}
      + Bearbeiten der Einstellungen einer Report Suite {#edit-report-suite}
         + Allgemein {#report-suite-general}
            + [Allgemeine Kontoeinstellungen](admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
            + [Interne URL-Filter](admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)
            + [Anpassen von Kalendern](admin/c-manage-report-suites/c-edit-report-suites/general/custom-calendar.md)
            + Erkennung gebührenpflichtiger Suchvorgänge {#paid-search-detection}
               + [Übersicht über die Paid-Search-Erkennung](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)
               + [Konfigurieren der Erkennung von Paid Search](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)
            + [Menüs benutzerspezifisch einstellen](admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md)
            + Verarbeitungsregeln {#c-processing-rules}
               + [Übersicht über Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md)
               + Verarbeitungsregeln {#c-processing-rules-configuration}
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
            + Bot-Regeln{#bot-removal}
               + [Bot-Entfernung](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)
               + [Übersicht über Bot-Regeln](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)
               + [Allgemeine Bot-Signaturen](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-signatures.md)
               + [Bot-Ausschlussmethoden](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-exclusion-methods.md)
            + [Datenschutzeinstellungen](admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)
            + [Zeitstempelkonfiguration](admin/c-manage-report-suites/c-edit-report-suites/general/timestamp-optional.md)
            + Serverseitige Weiterleitung {#server-side-forwarding}
               + [Übersicht über die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
               + [DSGVO/ePrivacy – Einhaltung und Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Anforderungen an die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-requirements.md)
               + [Daten- und Codereferenz für die Server-seitige Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-reference.md)
               + [Überprüfen der Server-seitigen Weiterleitungsimplementierung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md)
               + [Häufig gestellte Fragen zur Server-seitigen Weiterleitung](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md)
         + Traffic {#traffic-variables}
            + [Traffic-Variablen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
            + [Aktivieren von Traffic-Variablen-Berichten](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/t-traffic-variable.md)
            + [Traffic-Classifications](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-classifications.md)
            + [Beschreibung benutzerspezifischer Berichte](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/custom-desc-admin.md)
         + Konversion {#conversion-variables}
            + [Konversionsvariablen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md)
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
         + Marketing-Kanäle {#marketing-channels}
            + [Marketingkanal-Manager](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)
            + [Marketingkanal-Verarbeitungsregeln](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)
            + [Marketingkanal-Klassifizierungen](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md)
            + [Marketing-Kanalablauf](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md)
         + Traffic-Management {#traffic-management}
            + [Überblick](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/traffic-management.md)
            + [Spitze planen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)
            + [Dauerhafter Traffic](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)
         + [Standardmetriken](admin/c-manage-report-suites/c-edit-report-suites/default-metrics.md)
         + [App-Verwaltung](admin/c-manage-report-suites/c-edit-report-suites/mobile-management.md)
         + [Medienverwaltung](admin/c-manage-report-suites/c-edit-report-suites/media-management.md)
         + [Activity Map](admin/c-manage-report-suites/c-edit-report-suites/activity-map.md)
         + [AEM](admin/c-manage-report-suites/c-edit-report-suites/adobe-experience-manager.md)
         + [Adobe Campaign](admin/c-manage-report-suites/c-edit-report-suites/adobe-campaign.md)
         + [Datenschutzberichte](admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)
         + Document Cloud-Management {#doc-cloud-mgt}
            + [Konfigurieren von Document Cloud mit Adobe Analytics](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-mgt.md)
            + [Document Cloud Reporting konfigurieren](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-config.md)
         + [Advertising Analytics-Konfiguration](admin/c-manage-report-suites/c-edit-report-suites/advertising-analytics-config.md)
         + Echtzeit {#real-time-reports}
            + [Übersicht über Echtzeitberichte](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)
            + [Konfiguration von Echtzeitberichten](admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md)
            + [Unterstützte Echtzeit-Metriken und -Dimensionen](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md)
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
   + Datenschutzkennzeichnung für Data Governance {#data-governance}
      + [Adobe Analytics-Workflow zum Datenschutz](admin/c-data-governance/an-gdpr-workflow.md)
      + [Häufig gestellte Fragen](admin/c-data-governance/gdpr-faq.md)
      + Datenbeschriftung {#data-labels}
         + [Datenschutzkennzeichnungen für Analytics-Komponenten](admin/c-data-governance/data-labeling/gdpr-labels.md)
         + [Kennzeichnen von Report Suite-Daten](admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)
         + [Anzeigen/Verwalten von Datenschutzkennzeichnungen von Report Suites](admin/c-data-governance/data-labeling/gdpr-view-settings.md)
         + [Best Practices für Beschriftungen](admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)
         + [Beschriftungsbeispiel](admin/c-data-governance/data-labeling/gdpr-labeling-example.md)
         + [Namespaces](admin/c-data-governance/data-labeling/gdpr-namespaces.md)
      + [ID-Erweiterung](admin/c-data-governance/gdpr-id-expansion.md)
      + [CNIL-Zustimmungsfreistellung](admin/c-data-governance/cnil-consent-exemption.md)
   + Nutzung der Server-Aufrufe {#server-call-usage}
      + [Übersicht zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/overage-overview.md)
      + [Anzeigen der aktuellen Nutzung der Server-Aufrufe](admin/c-server-call-usage/server-call-usage-dashboard.md)
      + [Anzeigen der Nutzung der Report Suite](admin/c-server-call-usage/report-suite-usage.md)
      + [Warnhinweise zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/scu-alerts.md)
      + [Häufig gestellte Fragen zur Nutzung von Server-Aufrufen](admin/c-server-call-usage/overage-faq.md)
   + Benutzer und Produkte verwalten (alt) {#user-product-management}
      + [Verwalten von Benutzenden und Produkten  (veraltet)](admin/user-management2/user-management.md)
      + Migrieren von Benutzern zur Adobe Admin Console {#migrate-users}
         + [Analytics-Benutzermigration zur Admin Console](admin/user-management2/user-migration/c-migration-tool.md)
         + [Migrieren von Analytics-Benutzerkonten für Adobe IDs](admin/user-management2/user-migration/t-migrate-users.md)
         + [Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs](admin/user-management2/user-migration/migrate-enterprise.md)
         + [Deaktivieren von veralteten Anmeldedaten](admin/user-management2/user-migration/t-disable-legacy-login.md)
         + [Von der Migration betroffene APIs](admin/user-management2/user-migration/developer.md)
+ [Admin-API](c-admin-api/c-admin-api.md)

