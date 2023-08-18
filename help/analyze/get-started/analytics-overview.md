---
description: Allgemeine Übersichtsinformationen zu Adobe Analytics, einschließlich Informationen zur Analytics-Oberfläche sowie Informationen zu den ersten Schritten für Administratoren, Analysten, Benutzer und Entwickler.
title: Übersicht über Adobe Analytics
feature: Analytics Basics
hide: true
hidefromtoc: true
source-git-commit: f2f1d21989b609bf069da28b3b90785ccd14ef19
workflow-type: tm+mt
source-wordcount: '5049'
ht-degree: 41%

---

# Übersicht über Adobe Analytics

Mit Adobe Analytics können Unternehmen Daten erfassen und aus jeder digitalen Kundeninteraktion relevante Einblicke gewinnen. Mit detaillierten Analysen, vielseitiger Berichterstellung und prädiktiver Intelligenz erhalten Unternehmen die aufschlussreiche Grundlage, die sie zum Aufbau besserer Erlebnisse für ihre Kunden benötigen.

## Wesentliche Vorteile

Im Folgenden finden Sie einige der wichtigsten Möglichkeiten, wie Adobe Analytics Unternehmen dabei unterstützt, wichtige Einblicke zu gewinnen, um ihren Kunden besser zu helfen.

Weitere Informationen zu den Vorteilen, die Adobe Analytics bietet, finden Sie unter [Adobe Analytics-Produktseite](https://business.adobe.com/products/analytics/adobe-analytics.html).

### Webanalyse

Adobe Analytics bietet die folgenden komplexen Segmentierungs- und Prognosewerkzeuge zur Analyse des Website-Traffics:

* [Ad-hoc-Analysen in Analysis Workspace](/help/analyze/analysis-workspace/home.md)

* [Flussanalyse](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)

* [Erweiterte Segmentierung](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de)

### Marketing-Analyse

Adobe Analytics hilft Unternehmen dabei zu verstehen, wo Kunden mit ihren Marken interagieren, welche Kanäle sie bevorzugen und welche Erlebnisse bei ihnen Resonanz finden.

Die folgenden wichtigen Funktionen in Adobe Analytics bieten diese Marketingfunktionen:

* Multichannel-Datenerfassung

* [Offline-Datenintegration](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en)

* [Ad-hoc-Analysen in Analysis Workspace](/help/analyze/analysis-workspace/home.md)

### Attribution

Mit Attribution können Unternehmen sehen, wie verschiedene Interaktionen auf der gesamten Journey die Konversion beeinflussen. Neben den herkömmlichen Attributionsoptionen wie Linear- oder Erstkontaktmodellen verwendet die Attribution in Adobe Analytics auch maschinelles Lernen und erweiterte statistische Modelle, um die genauen Auswirkungen jedes Kontakts zu verstehen.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md).


### Predictive Analytics

Predictive Analytics verwendet maschinelles Lernen und erweiterte statistische Modellierung, um Kundendaten zu analysieren, Muster zu finden und zukünftiges Verhalten wie Abwanderung oder eine Wahrscheinlichkeit für eine Konversion vorherzusagen. Dadurch können Datenanalysten von riesigen Datensätzen profitieren, die andernfalls verschwendet werden könnten.

Die folgenden Schlüsselfunktionen in Adobe Analytics bieten diese Prognosefunktionen:

* [Fehlererkennung](#anomaly-detection)

* [Beitragsanalyse](#contribution-analysis)

* [Intelligente Warnhinweise](#intelligent-alerts)

## Voraussetzungen für die Verwendung von Adobe Analytics

Bevor Sie Adobe Analytics verwenden können, müssen Sie über Folgendes verfügen:

* Eine gültige Adobe Analytics-Lizenz

  Adobe Analytics erfordert eine Site-Lizenz. Wenden Sie sich für weitere Informationen an Ihren Adobe-Kundenbetreuer. <!--is this phrased correctly? Is this important? -->

* Ein unterstützter Browser

  Jeder Benutzer, der auf Adobe Analytics zugreift, muss einen unterstützten Browser verwenden. Weitere Informationen finden Sie unter [Systemanforderungen von Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/sys-reqs.html?lang=en).

<!-- are there more? -->

## Analytics-Oberfläche - Grundlagen

Die Benutzeroberfläche von Adobe Analytics umfasst die folgenden Hauptbereiche:

### Registerkarte &quot;Arbeitsbereich&quot;

Die [!UICONTROL Arbeitsbereich] zeigt die Registerkarte [!UICONTROL Projekte] -Bereich standardmäßig angezeigt, in dem der Ordner Firma, alle von Ihnen erstellten persönlichen Ordner, Ihre Projekte und mobile Scorecards angezeigt werden.

1. Wählen Sie in Adobe Analytics die [!UICONTROL **Arbeitsbereich**] Registerkarte.

   ![Registerkarte &quot;Arbeitsbereich&quot;](assets/landing-all2.png)

Weitere Informationen zu den Funktionen finden Sie im Abschnitt [!UICONTROL Arbeitsbereich] Registerkarte, siehe [Adobe Analytics-Landingpage](/help/analyze/landing.md).

### Registerkarte „Berichte“

Adobe beabsichtigt, Reports &amp; Analytics und die zugehörigen Berichte und Funktionen zum 31. Dezember 2023 einzustellen.

Verwenden Sie stattdessen die [!UICONTROL **Berichte**] Bereich in der linken Leiste auf der [!UICONTROL **Arbeitsbereich**] Registerkarte. Weitere Informationen finden Sie unter *Navigieren zur Registerkarte Berichte* in [Adobe Analytics-Landingpage](/help/analyze/landing.md).

### Registerkarte „Komponenten“

Die [!UICONTROL Komponenten] enthält Funktionen, mit denen Sie Ihre Datenanalyse optimieren können.

1. Wählen Sie in Adobe Analytics die [!UICONTROL **Komponenten**] Registerkarte und wählen Sie [!UICONTROL **Alle Komponenten**].

   ![Registerkarte &quot;Arbeitsbereich&quot;](assets/components-tab.png)

2. Wählen Sie eine der folgenden Produktfunktionen aus, um sie zu konfigurieren:


   | Produktfunktion | Funktion | Weitere Informationen |
   |---------|----------|----------|
   | Segmente  | Mit Adobe Analytics können Sie leistungsstarke, fokussierte Zielgruppensegmente erstellen, verwalten, freigeben und anwenden, um Berichte mithilfe von Analytics-Funktionen, der Adobe Experience Cloud, Adobe Target und anderen integrierten Adobe-Produkten zu erstellen. | [Analytics-Segmentierung](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de) |
   | Berechnete Metriken  | Berechnete und erweiterte berechnete (abgeleitete) Metriken sind benutzerdefinierte Metriken, die Sie aus vorhandenen Metriken erstellen können.  Damit können Marketing-Experten, Produktmanager und Analysten Fragen zu den Daten stellen, ohne die Analytics-Implementierung ändern zu müssen. | [Berechnete und erweiterte berechnete (abgeleitete) Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html?lang=de) |
   | Datumsbereiche | Analysis Workspace enthält eine Liste der Standarddatumsbereiche, die Benutzer beim Erstellen von Analysen verwenden können. Darüber hinaus können Sie benutzerdefinierte Datumsbereiche erstellen und sie für Benutzer in Analysis Workspace verfügbar machen. | [Erstellen von benutzerdefinierten Datumsbereichen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=de) <!-- should create an article in the Components Guide for managing/creating date ranges. This article in the Tools Guide needs updating. --> |
   | Virtual Report Suites | Virtual Report Suites segmentieren die Adobe Analytics-Daten, sodass der Zugriff auf die einzelnen Segmente gesteuert werden kann. | [Virtual Report Suites – Übersicht](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=de) |
   | Warnhinweise | Intelligente Warnhinweise ermöglichen eine präzisere Kontrolle über Warnhinweise und integrieren die Anomalieerkennung in das Warnhinweissystem. | [Intelligente Warnhinweise](https://experienceleague.adobe.com/docs/analytics/components/alerts/intellligent-alerts.html?lang=en) |
   | Zielgruppen | Mithilfe von Zielen können Sie die Leistung Ihrer Website messen und den Fortschritt bei der Erreichung Ihrer Zielsetzungen verfolgen. Mit der Zielsetzung legen Sie fest, welche Attributmetriken oder eVars gemessen werden sollen oder ob Sie Ihre gesamte Website mit einer bestimmten Metrik vergleichen möchten. <p>Ziele sind Teil von Reports &amp; Analytics. Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://express.adobe.com/page/6WnF8JK6IRDhf/) von Reports &amp; Analytics.</p> | [Zielgruppen](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/targets.html?lang=en) |
   | Kalenderereignisse | Bei Berichten mit Trendansicht im Zeitverlauf können Sie mit Kalenderereignissen Ereignisse grafisch anzeigen und sehen, ob Kampagnen oder andere Ereignisse Ihren Site-Traffic, Umsatz oder andere Metriken beeinflusst haben. | [Kalenderereignisse](https://experienceleague.adobe.com/docs/analytics/components/t-calendar-event.html?lang=en) |
   | Anmerkungen | Mit Anmerkungen im Arbeitsbereich können Sie Ihrer Organisation kontextbezogene Informationen und Erkenntnisse zu Daten effektiv übermitteln. Damit können Sie Kalenderereignisse mit bestimmten Dimensionen und Metriken verknüpfen. | [Verwalten von Anmerkungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/manage-annotations.html?lang=en) |
   | Klassifizierungssätze | Klassifizierungssätze bieten eine einzige Oberfläche zur Verwaltung von Klassifizierungen und Regeln. <p>Eine Classification ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, sobald Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Classifications können für die meisten benutzerdefinierten Dimensionen wie Trackingcode, Props und eVars verwendet werden.</p> | [Klassifizierungssätze – Übersicht](https://experienceleague.adobe.com/docs/analytics/components/classifications/sets/overview.html?lang=de) |
   | Standorte | Um Adobe Analytics-Classification-Daten aus einem Cloud-Ziel zu importieren, müssen Sie zunächst den Speicherort hinzufügen und konfigurieren, an dem die Classification-Daten erfasst werden sollen. Sie können Standorte erstellen, bearbeiten oder löschen. | [Standorte-Manager](https://experienceleague.adobe.com/docs/analytics/components/locations/locations-manager.html?lang=en) |
   | Geplante Projekte | Bei der Verwaltung geplanter Projekte können Sie wiederkehrende Projektpläne bearbeiten und löschen, in der Suchleiste nach einem Zeitplan suchen oder die Filteroptionen in der linken Leiste verwenden und nach Tag, genehmigten Zeitplänen, Inhabern und mehr filtern. | [Geplante Projekte](/help/components/scheduled-projects-manager.md) |
   | Lesezeichen | Anhand von Lesezeichen haben Sie Zugriff auf die Berichte, die Sie am meisten verwenden. Die von Ihnen erstellten Lesezeichen werden der Experience Cloud hinzugefügt und sind in integrierten Funktionen wie Data Connectors verfügbar. <p>Lesezeichen sind Teil von Reports &amp; Analytics. Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://express.adobe.com/page/6WnF8JK6IRDhf/) von Reports &amp; Analytics. | [Lesezeichen-Manager](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/bookmarks.html?lang=en) |
   | Dashboards | Dashboards werden erstellt, um Metriken zu visualisieren und interaktive Analysefunktionen mit Daten bereitzustellen. Durch Klicken auf Elemente in einem Dashboard können Sie die Daten schnell und einfach segmentieren, um Informationen aus Ihrer Analyse abzuleiten. <p>Dashboards sind Teil von Data Workbench. Mehr über die Data Workbench [Mitteilung zum Ende der Nutzungsdauer](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=en). | [Dashboard-Manager](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/dashboard-manage.html?lang=en) |
   | Terminierte Berichte | Benutzer auf Administratorebene können terminierte Berichte innerhalb der Organisation anzeigen und verwalten. | [Warteschlange für terminierte Berichte](https://experienceleague.adobe.com/docs/analytics/components/scheduled-reports-admin.html?lang=en) |
   | Berichtseinstellungen | Diese Einstellungen beziehen sich auf veraltete Adobe Analytics-Produkte, die Analysis Workspace und die zugehörigen Komponenten ausschließen. Um Anpassungen an den Analysis Workspace-Einstellungen vorzunehmen, gehen Sie zu Komponenten > Voreinstellungen. |  |
   | Voreinstellungen | Verwalten Sie Einstellungen für Analysis Workspace und die zugehörigen Komponenten für alle neuen Projekte oder Bereiche, die Sie erstellen. Bestehende Projekte und Bedienfelder sind davon nicht betroffen. | [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md) |

   {style="table-layout:auto"}

### Registerkarte „Tools“

<!-- The Tools tab ... -->

1. Wählen Sie in Adobe Analytics die [!UICONTROL **Instrumente**] Registerkarte und wählen Sie [!UICONTROL **Alle Tools**].

   ![Registerkarte &quot;Arbeitsbereich&quot;](assets/tools-tab.png)

2. Wählen Sie eine der folgenden Produktfunktionen aus, um sie zu konfigurieren:

   | Produktfunktion | Funktion | Weitere Informationen |
   |---------|----------|----------|
   | Data Warehouse | Data Warehouse bezeichnet die Kopie von Analytics-Daten für Speicherberichte und benutzerdefinierte Berichte, die Sie durch Filtern der Daten ausführen können. <p>Der Anforderungs-Manager ermöglicht es Ihnen, Anforderungen anzuzeigen, zu duplizieren und neu zu priorisieren.</p> | [Verwalten von Data Warehouse-Anforderungen](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=en) |
   | Activity Map | Activity Map ist so konzipiert, dass die Linkaktivität mithilfe visueller Überlagerungen nach Rang geordnet wird und ein Dashboard mit Echtzeitanalysen zur Verfügung gestellt wird, um die Interaktion der Zielgruppe mit Ihren Webseiten zu überwachen. Sie können damit verschiedene Ansichten einrichten, um die Beschleunigung der Kundenaktivität visuell zu identifizieren, Marketing-Initiativen zu quantifizieren und auf die Bedürfnisse und Verhaltensweisen der Zielgruppe zu reagieren. | [Übersicht über Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html?lang=de) |
   | Recommendations Classic | Recommendations ist eine Adobe Target-Funktion, mit der automatisch Produkte, Dienste oder Inhalte angezeigt werden, die basierend auf früheren Benutzeraktivitäten, Voreinstellungen oder anderen Kriterien für Ihre Besucher interessant sein könnten. | [Empfehlungen](https://experienceleague.adobe.com/docs/target/using/recommendations/recommendations.html?lang=en) |
   | Search&amp;Promote |  |  |
   | Mobile Services |  |  |
   | Analytics-Dashboards (mobile App) | Die Adobe Analytics-Dashboards-App bietet jederzeit und überall Erkenntnisse aus Adobe Analytics. Über das Programm können Benutzer intuitive Scorecards anzeigen, die Sie mithilfe der Adobe Analytics-Desktop-Benutzeroberfläche erstellen. | Die Adobe Analytics-Dashboards-App im iOS App Store- oder Google Play-Store |
   | Report Builder | Adobe Report Builder ist ein Add-in für Microsoft Excel. Mit Report Builder können Sie benutzerdefinierte Anfragen aus Adobe Analytics-Daten erstellen, die Sie in Excel-Arbeitsblätter einfügen können. Anforderungen können dynamisch auf Zellen innerhalb Ihres Arbeitsblatts verweisen, und die Darstellung der Daten in Report Builder lässt sich aktualisieren und anpassen. | [Was ist Report Builder?](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html?lang=de) |

   {style="table-layout:auto"}

### Admin-Registerkarte

Die Registerkarte &quot;Admin&quot;enthält Funktionen und Konfigurationsoptionen für die Verwaltung von Adobe Analytics.

1. Wählen Sie in Adobe Analytics die [!UICONTROL **Admin**] Registerkarte und wählen Sie [!UICONTROL **Alle Administratoren**].

   ![Registerkarte &quot;Arbeitsbereich&quot;](assets/admin-tab.png)

2. Wählen Sie eine der folgenden Produktfunktionen aus, um sie zu konfigurieren:

   | Produktfunktion | Funktion | Weitere Informationen |
   |---------|----------|----------|
   | Analytics-Benutzer und -Assets | Während die meisten Benutzer- und Produktverwaltungsfunktionen jetzt nur noch im [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html), sind die Verwaltungsfunktionen zum Übertragen von Assets von einem Benutzer auf einen anderen sowie zum Festlegen eines Ablaufdatums für ein Benutzerkonto nur im Admin-Bereich von Adobe Analytics verfügbar. | [Übertragen von Benutzer-Assets oder Festlegen des Kontoablaufs](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/users-assets.html?lang=en) |
   | Benutzer-ID-Migration | Die Migration der Analytics-Benutzer-ID ermöglicht es Administratoren, Benutzerkonten einfach vom Analytics User Management zur Adobe Admin Console zu migrieren. | [Analytics-Benutzermigration zur Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/migrate-users/c-migration-tool.html?lang=de) |
   | Homepage für Benutzerverwaltung (alt) | Die Verwaltung von Benutzenden und Produkten wurde in die Adobe Admin Console verschoben. Verwenden Sie die Adobe Admin Console, um mit der Verwaltung von Benutzerberechtigungen für Adobe Analytics-Benutzer zu beginnen. | [Analytics in der Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de) |
   | Gruppen (veraltet) | Die Gruppenverwaltung wurde in die Adobe Admin Console verschoben. Verwenden Sie die Adobe Admin Console, um mit der Gruppenverwaltung für Adobe Analytics zu beginnen. | [Analytics in der Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de) |
   | Zugriff auf Report Suites | Die Methode zur Gewährung des Zugriffs auf Report Suite-Tools wurde in die Adobe Admin Console verschoben. Verwenden Sie die Adobe Admin Console, um Adobe Analytics-Benutzern Zugriff auf die Report Suite zu gewähren. | [Produktprofilberechtigungen für Report Suite-Werkzeuge](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/report-suite-tools.html?lang=en) |
   | Admin Tools-Homepage |  |  |
   | Report Suites | Hier können Sie die Regeln definieren, die steuern, wie Daten in einer Report Suite verarbeitet werden. | [Report Suite Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/report-suites-admin.html?lang=en) |
   | Analytics-Benutzer und -Assets | Die Benutzer- und Asset-Verwaltung wurde in die Adobe Admin Console verschoben. Verwenden Sie die Adobe Admin Console, um mit der Verwaltung von Benutzerberechtigungen für Adobe Analytics-Benutzer zu beginnen. | [Analytics in der Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de) |
   | Classification Importer | Mit dem Klassifizierungsimport laden Sie Klassifizierungen in Adobe Analytics hoch. Darüber hinaus können Sie die Daten zum Aktualisieren vor dem Import exportieren. | [Übersicht über Classifications importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html?lang=en) |
   | Classification Rule Builder | Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. | [Classification Rule Builder-Workflow](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-rulebuilder/classification-rule-builder.html?lang=en) |
   | Datenquellen  | Verwenden Sie den Datenquellen-Manager, um Datenquellen zu erstellen, zu bearbeiten oder zu deaktivieren. Sie können diese Benutzeroberfläche auch verwenden, um den Status von Dateien zu verfolgen, die an FTP-Speicherorte für Datenquellen hochgeladen wurden. | [Datenquellen verwalten](https://experienceleague.adobe.com/docs/analytics/import/data-sources/manage.html?lang=en) |
   | Code-Manager | Mithilfe des Code-Managers können Sie Datenerfassungscode für Web- und mobile Plattformen herunterladen | [Code-Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=de) |
   | Traffic-Management | Auf der Seite „Traffic-Management“ können Sie Informationen zu erwarteten Änderungen des Trafficvolumens angeben. Auf der Grundlage dieser Einstellungen kann Adobe die entsprechenden Ressourcen zuweisen, damit der Traffic rechtzeitig nachverfolgt und verarbeitet werden kann. | [Übersicht über das Traffic-Management](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/traffic-management.html?lang=en) |
   | Nutzung von Server-Aufrufen | Ein Server-Aufruf, auch als „Treffer“ oder „Bildanforderung“ bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Es steht ein Dashboard zur Nutzung von Server-Aufrufen zur Verfügung, in dem die Verbrauchsdaten Ihrer Server-Aufrufe verfolgt und mit Ihrem vertraglichen Limit verglichen werden. Sie können Warnhinweise einrichten, um Überschüsse zu vermeiden. | [Übersicht über die Nutzung der Server-Aufrufe](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html?lang=en) |
   | Protokolle | Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. | [Protokolle](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html?lang=de) |
   | Advertising Analytics | Konfigurieren Sie Adobe Analytics so, dass alle Ihre gebührenpflichtigen Google- und Bing-Suchdaten nebeneinander angezeigt werden. | [Konfigurieren von Advertising Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/advertising-analytics-config.html?lang=en) |
   | Datenfeeds | Daten-Feeds sind eine leistungsstarke Methode, Rohdaten aus Adobe Analytics abzurufen. Diese Rohdaten können nach Ermessen Ihrer Organisation auf anderen Plattformen außerhalb von Adobe verwendet werden. | [Analytics-Daten-Feed-Dokumentation](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=de) |
   | Nach IP ausschließen | Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Durch das Ausschließen von Daten nach der IP-Adresse wird die Genauigkeit der Berichte erhöht. Zudem können Sie Daten entfernen, die auf DoS-Angriffen oder anderen böswilligen Ereignissen beruhen und Ihre Berichte verfälschen könnten. Die Ausschlüsse lassen sich wahlweise oder über die Firewall konfigurieren. | [Nach IP-Adresse ausschließen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/exclude-ip.html?lang=en) |
   | Veröffentlichungs-Widgets |  |  |
   | Reporting Activity Manager | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Es bietet eine detaillierte Übersicht über den Berichtsverbrauch und hilft Ihnen, während Spitzenzeiten der Berichterstellung mühelos Kapazitätsprobleme zu diagnostizieren und zu beheben. | [Reporting Activity Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html?lang=en) |
   | Datenschutzkennzeichnung für Data Governance | Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. | [Report Suite-Daten beschriften](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) |
   | Startseite der Unternehmenseinstellungen | Auf der Seite Unternehmenseinstellungen können Sie Einstellungen konfigurieren, die für alle von Ihrer Organisation verwalteten Report Suites gelten. | [Übersicht über Unternehmenseinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=en) |
   | Sicherheitsmanager | Mit dem Sicherheits-Manager können Sie den Zugriff auf Berichtsdaten kontrollieren. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen. | [Sicherheits-Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/security-manager.html?lang=en) |
   | Support-Info | Auf der Seite &quot;Support-Informationen&quot;werden die in Reports &amp; Analytics angezeigten Supportinformationen verwaltet. Reports &amp; Analytics. <p>Adobe beabsichtigt, Reports &amp; Analytics und die zugehörigen Berichte und Funktionen zum 31. Dezember 2023 einzustellen. Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://www.adobe.com/go/analytics_rnaeol_de) von Reports &amp; Analytics.</p> |  |
   | Web-Services | Die Web Services APIs bieten Programmierungszugriff auf Marketing-Berichte und andere Suite-Services, mit denen Sie die Funktionalität der Analytics-Oberfläche duplizieren und erweitern können. | [Webdienste](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/web-services-admin.html?lang=en) |
   | Report Builder-Berichte | Verwalten von Lizenzen, die Report Builder-Benutzern zugewiesen wurden. | [Report Builder-Berichte](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/report-builder-reports-admin.html?lang=en) |
   | Single Sign-On-Dienst | Single Sign-On ist in Adobe Experience Cloud über die Admin Console implementiert. | [Analytics in der Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de) |
   | Co-Branding der Adobe Experience Cloud | Mit Hilfe der Seite „Co-Branding-Image verwalten“ können Sie Ihr Firmenlogo in über Reports &amp; Analytics heruntergeladenen Berichten und Legacy-Dashboards anzeigen. Co-Branding wird in Analysis Workspace nicht verwendet.<p>Adobe beabsichtigt, Reports &amp; Analytics und die zugehörigen Berichte und Funktionen zum 31. Dezember 2023 einzustellen. Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://www.adobe.com/go/analytics_rnaeol_de) von Reports &amp; Analytics.</p> | [Co-Branding](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/co-branding-admin.html?lang=en) |
   | Ausblenden von Report Suites | Ermöglicht das Ausblenden von Report Suites in der Benutzeroberfläche von Adobe Analytics, wenn Sie nicht mehr möchten, dass eine Report Suite für Sie und Ihre Benutzer verfügbar ist. | [Report Suites ausblenden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-hide-report-suites.html?lang=en) |  |

   {style="table-layout:auto"}

### Analysis Workspace

Mit Analysis Workspace können Sie schnell Analysen erstellen, um Einblicke zu gewinnen und diese Einblicke dann für andere freizugeben. Mithilfe der Drag-and-Drop-Browser-Oberfläche können Sie Ihre Analyse erstellen, Visualisierungen hinzufügen, um Daten lebendig werden zu lassen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.

Das folgende Bild und die zugehörige Tabelle erläutern einige der Hauptbereiche in Analysis Workspace.

Einen detaillierteren Überblick über Analysis Workspace finden Sie unter [Übersicht über Analysis Workspace](/help/analyze/analysis-workspace/home.md).

![Analysis Workspace – Übersicht](assets/analysis-workspace-overvew.png)

| Position im Bild | Name und Funktion |
|---------|----------|
| A  | **Ganz linke Leiste:** Enthält Registerkarten zum Hinzufügen von Bedienfeldern, Visualisierungen und Komponenten zu Analysis Workspace. Enthält außerdem das Datenwörterbuchsymbol, mit dem das Datenwörterbuch geöffnet wird. |
| B | **Linke Leiste:** Je nachdem, welche Registerkarte in der linken Leiste ausgewählt ist, enthält dieser Bereich einzelne Bedienfelder, Visualisierungen oder Komponenten. |
| C  | **Arbeitsfläche:** Dies ist der Hauptbereich, in den Sie Inhalte aus den linken Leisten ziehen, um Ihr Projekt zu erstellen. Das Projekt wird dynamisch aktualisiert, wenn Sie Bereiche, Visualisierungen und Komponenten zur Arbeitsfläche hinzufügen. |
| D | **Dropdown-Menü „Report Suite“:** Für jedes Bedienfeld in Analysis Workspace können Sie im Dropdown-Menü „Report Suite“ die Report Suite auswählen, die Sie als Datenquelle verwenden möchten. |

## Erste Schritte für Administratoren, Analysten, Endbenutzer und Entwickler

In einer typischen Organisation gibt es drei Arten von Adobe Analytics-Benutzern: Administratoren, Analysten und Endbenutzer.

Administratoren implementieren und konfigurieren Adobe Analytics; Analysten richten Projekte ein und erstellen Analysen mithilfe von Analysis Workspace. Endbenutzer erhalten umsetzbare Einblicke in ihre Kunden, indem sie entweder eigene Analysen erstellen oder mit Analysten zusammenarbeiten, um diese zu erstellen.

Erweitern Sie die folgenden Abschnitte, um zu erfahren, wie diese Benutzer mit Adobe Analytics beginnen können.

### Erste Schritte für Administratoren

Analytics-Administratoren sind für die Auswahl der Implementierungsmethode verantwortlich, die für ihre Organisation am besten geeignet ist.

Nachdem Adobe Analytics implementiert wurde, müssen Administratoren verschiedene Konfigurationsaufgaben durchführen, um sicherzustellen, dass Analysten und Endbenutzer von Adobe Analytics den vollen Nutzen ziehen. Administratoren sollten außerdem regelmäßig ihre Analytics-Umgebung überwachen, um sicherzustellen, dass das System effizient ausgeführt wird.

#### Bestimmen der zu erfassenden Datentypen

Mit Adobe Analytics können Sie Daten aus mehreren Kanaltypen erfassen und zusammenführen, um aussagekräftige Echtzeit-Kundeneinblicke zu liefern.

Im Folgenden finden Sie einige der unterstützten Kanäle, in denen Daten erfasst werden können:

* Mobiltelefone

* Das Internet der Dinge

* TV

* Sprachassistenten

* Verbundene Fahrzeuge

* Und mehr (regelmäßig werden neue unterstützte Kanäle hinzugefügt)

Die [Implementierungsmethode](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de) bestimmt, welche Art von Daten erfasst werden können.

#### Implementieren von Adobe Analytics

Bei der Implementierung von Adobe Analytics auf Ihrer Website oder in Ihrer App stehen verschiedene Implementierungsmethoden zur Verfügung.

Informationen zu den einzelnen verfügbaren Methoden finden Sie unter [Implementieren von Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de).

| | Methoden der Implementierung |
|---------|---------|
| **Websites** | <ul><li>Web SDK-Erweiterung (empfohlen)</li><li>Web SDK</li><li>Analytics-Erweiterung</li><li>Legacy-JavaScript</li></ul> |
| **Mobile Anwendungen** | <ul><li>Mobile SDK-Erweiterung (empfohlen)</li><li>Analytics-Erweiterung</li></ul> |

{style="table-layout:auto"}

#### Konfigurieren von Adobe Analytics

Analytics-Administratoren sollten die folgenden Aufgaben ausführen, bevor sie Adobe Analytics für Benutzer in der Organisation verfügbar machen:

| Aufgabe | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Definieren von Administratorrollen | In Adobe Analytics gibt es verschiedene Arten von Administrierenden | [Administratorrollen in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html?lang=en) |
| Berechtigungen definieren | Analytics-Administratoren müssen Produktprofile in der Admin Console für Adobe Analytics, Report Suite-Tools und Analytics-Tools zuweisen. | [Analytics-Berechtigungen in Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=de) |
| Report Suites einrichten und Einstellungen für Ihr Unternehmen definieren | Bei einer Report Suite handelt es sich um ein Datensilo, mit dem Adobe Analytics Berichte generiert.<p>Administratoren können auch [Virtual Report Suites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=de) zur weiteren Segmentierung von Daten.</p> | <ul><li>[Erstellen einer Report Suite](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html?lang=en)</li><li>[Übersicht über Unternehmenseinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=en)</li></ul> |
| Daten importieren | Mit Adobe Analytics-Datenquellen können Sie zusätzliche Online- oder Offline-Daten für die Berichterstellung importieren. | [Datenquellen - Übersicht](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en) |
| Daten mit Classifications klassifizieren | Klassifizierungen ermöglichen es Ihnen, Daten zu klassifizieren, um Variablen besser zu nutzen und so mehr Inhalt in eine Variable einzuschließen. | |
| Komponenten verwalten | Verwenden Sie das Datenwörterbuch und die Verwaltungsbereiche für jeden Komponententyp, um zu definieren, welche Komponenten in Ihrer Analytics-Implementierung verfügbar sind und welche für Ihr Unternehmen genehmigt sind.<p>Dies sollte eine fortlaufende Aktivität sein, um sicherzustellen, dass Komponenten in Ihrem Unternehmen effektiv verwendet werden. </p> | <ul><li>[Datenwörterbuch – Überblick](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html?lang=de)</li><li>[Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=en)</li><li>[Segmente verwalten](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de)</li><li>[Erstellen Sie benutzerdefinierte Datumsbereiche](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=de)</li></ul> |
| Fehlererkennung | Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat. | [Übersicht über die Anomalieerkennung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html?lang=de) |
| Beitragsanalyse | Die Beitragsanalyse erkennt versteckte Muster, mit denen sich statistische Anomalien erklären und Korrelationen für nicht erwartete Kundenaktionen, Wertbereichsüberschreitungen und plötzliche Anstiege oder Rückgänge für ausgewählte Metriken in konvergenten Zielgruppensegmenten feststellen lassen. | [Übersicht über die Beitragsanalyse](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=de) |
| Analytics-Segmentierung | Ermöglicht Ihnen das Erstellen, Verwalten, Freigeben und Anwenden leistungsstarker, fokussierter Zielgruppensegmente auf Ihre Berichte mithilfe von Analytics-Funktionen, Adobe Experience Cloud, Adobe Target und anderen integrierten Adobe-Produkten. | [Analytics-Segmentierung](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de) |
| Veröffentlichen von Zielgruppen in Audience Manager | | |
| Integrationen | Sie können Informationen aus anderen Anwendungen in Adobe Analytics aufdecken. <p>Im Folgenden finden Sie einige gängige Integrationen:</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=en">Analytics for Target</a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=de">Media Analytics</a></li> | |

{style="table-layout:auto"}

#### Überwachen von Adobe Analytics

Es stehen verschiedene Funktionen zur Verfügung, mit denen Sie Ihre Adobe Analytics-Umgebung überwachen können.

Analytics-Administratoren sollten sich der folgenden Funktionen bewusst sein, die zur Überwachung wichtiger Aspekte Ihrer Analytics-Umgebung verfügbar sind:

| Aufgabe | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Reporting Activity Manager | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Es bietet eine detaillierte Übersicht über den Berichtsverbrauch und hilft Ihnen, während Spitzenzeiten der Berichterstellung mühelos Kapazitätsprobleme zu diagnostizieren und zu beheben. | [Reporting Activity Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html?lang=en) |
| Nutzung von Server-Aufrufen | Ein Server-Aufruf, auch als „Treffer“ oder „Bildanforderung“ bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Es steht ein Dashboard zur Nutzung von Server-Aufrufen zur Verfügung, in dem die Verbrauchsdaten Ihrer Server-Aufrufe verfolgt und mit Ihrem vertraglichen Limit verglichen werden. Sie können Warnhinweise einrichten, um Überschüsse zu vermeiden. | [Übersicht über die Nutzung der Server-Aufrufe](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html?lang=en) |
| Protokolldateien | Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. | [Protokolle](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html?lang=de) |

{style="table-layout:auto"}

### Erste Schritte für Analysten

Während jeder Mitarbeiter eines Unternehmens Adobe Analytics verwenden kann, um verwertbare Einblicke in das Kundenverhalten von Websites und Apps zu erhalten, wird Adobe Analytics unter Berücksichtigung von Datenanalysten entwickelt.

Im Folgenden finden Sie wichtige Aufgaben und Funktionen, mit denen Analysten vertraut sein sollten, um die volle Leistungsfähigkeit von Adobe Analytics und Analysis Workspace zu nutzen.

| Funktion | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Erstellen und Freigeben von Projekten in Analysis Workspace | Analysis Workspace ist ein flexibles Browser-Tool, mit dem Sie schnell Analysen erstellen und Insights austauschen können. Mithilfe der Drag-and-Drop-Oberfläche können Sie Ihre Analyse gestalten, Visualisierungen hinzufügen, um Daten optisch darzustellen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.<p>Datenanalysten sind häufig für das Erstellen von Projekten in Analysis Workspace für Benutzer in ihrem Unternehmen verantwortlich.</p><p>Nachdem Projekte erstellt wurden, teilen Analysten diese Projekte für die [Endbenutzer](#end-users)(Nicht-Analytiker) in ihren Organisationen, die die Daten angefordert und ihnen dabei helfen, die Interpretation zu verstehen.</p> | <ul><li>[Projekte erstellen](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attribution | Analysten können anpassen, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden, indem sie verschiedene Attributionsmodelle und Lookback-Fenster in Analysis Workspace verwenden.<p>Die linearen Attributionsmodelle geben jedem Touchpoint, der zu einer Konversion führt, die gleiche Gewichtung, während Erstkontakt dem Erstkontaktpunkt die volle Gutschrift zuweist. Es stehen viele weitere Attributionsmodelle zur Verfügung, darunter das algorithmische Modell, das mithilfe statistischer Verfahren die optimale Zuordnung dynamisch bestimmt. </p> | [Attributionsmodelle und Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md) |
| Fehlererkennung | Die statistische Modellierung in Analysis Workspace findet automatisch unerwartete Trends in Ihren Daten, indem Sie Metriken analysieren und eine untere, obere Grenze und einen erwarteten Wertebereich bestimmen. Treten unerwartete Spitzen oder Verwerfungen auf, meldet das System dies im entsprechenden Bericht. | [Übersicht über die Anomalieerkennung](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| Beitragsanalyse | Verwenden Sie Analysis Workspace, um versteckte Muster in Ihren Daten zu ermitteln, um statistische Anomalien zu erklären und Korrelationen für unerwartete Kundenaktionen, Wertbereichsüberschreitungen und plötzliche Spitzen oder Tiefpunkte für Metriken in allen Zielgruppensegmenten zu identifizieren. | [Übersicht über die Beitragsanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| Intelligente Warnhinweise | Warnhinweise erstellen und verwalten, die auf Datenanomalien und &quot;gestapelten&quot;Warnhinweisen basieren, die mehrere Metriken in einem Warnhinweis erfassen. | [Übersicht über intelligente Warnhinweise](/help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md) |
| Datenexport | Mit Data Warehouse und Daten-Feeds können Sie Daten an verschiedene Cloud-Ziele exportieren, z. B. Google Cloud Platform, Azure RBAC, Azure SAS und Amazon S3. | [Exportleitfaden für Analytics](https://experienceleague.adobe.com/docs/analytics/export/home.html?lang=de) |
| Activity Map | Activity Map ist eine Adobe Analytics-Anwendung, die der Link-Aktivität mithilfe von visuellen Überlagerungen einen Rang zuweist und ein Dashboard mit Echtzeitanalyse bereitstellt, um die Interaktion der Zielgruppe mit Ihren Web-Seiten zu überwachen.<p>Activity Map ermöglicht Ihnen, verschiedene Ansichten einzurichten, um beschleunigte Kundenaktivität zu erkennen, Marketinginitiativen zu quantifizieren und auf die Bedürfnisse und das Verhalten der Zielgruppe zu reagieren.</p> | [Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html?lang=de) |
| Report Builder | Report Builder ist ein Add-in für Microsoft Excel. Mit Report Builder können Sie benutzerdefinierte Anfragen aus Adobe Analytics-Daten erstellen, die in Ihre Excel-Arbeitsblätter eingefügt werden. Anforderungen können dynamisch auf Zellen innerhalb Ihres Arbeitsblatts verweisen, und die Darstellung der Daten in Report Builder lässt sich aktualisieren und anpassen. | [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html?lang=de) |

{style="table-layout:auto"}

<!-- * Realtime reporting? -->

### Erste Schritte für Endbenutzer

Endbenutzer, die keine professionellen Analysten sind, können entweder mit Analysten in ihrem Unternehmen zusammenarbeiten, um die volle Leistungsfähigkeit von Adobe Analytics und Analysis Workspace zu nutzen, oder sie können die Grundlagen von Analysis Workspace lernen, um praktische Einblicke über ihre Kunden zu erhalten.

#### Arbeiten mit Analysten

Normalerweise sind Benutzer in einem Unternehmen, die mehr über das Kundenverhalten auf ihren verschiedenen Sites erfahren möchten, keine professionellen Analysten.

Idealerweise sollten diese Benutzer mit [Analysten](#analysts) innerhalb einer Organisation:

1. Definieren Sie Anforderungen für die Analysen, indem Sie dem Analysten erklären, was er über Kunden zu erfahren hofft.

1. Überprüfen Sie die Analysen, um sicherzustellen, dass sie die Ziele erreichen.

1. Beschreiben Sie die aus den Analysen gewonnenen Daten.

1. Ändern Sie die Analysen nach Bedarf im Laufe der Zeit.

#### Erstellen von Analysen in Analysis Workspace

Sie müssen kein Datenanalyst sein, um von Adobe Analytics umsetzbare Einblicke zu erhalten.

Für einige Benutzer ist es möglicherweise hilfreich, mit einem Datenanalyst zusammenzuarbeiten, um ein Projekt in Analysis Workspace einzurichten und zu erklären, wie die Daten interpretiert werden, wie unter [Arbeiten mit Analysten](#work-with-analysts); andere Benutzer können sich möglicherweise damit befassen, das Projekt zu erstellen und die Daten selbst zu interpretieren.

Mit Analysis Workspace können Sie schnell Analysen erstellen, um Einblicke zu gewinnen und diese Einblicke dann für andere freizugeben. Mithilfe der Drag-and-Drop-Browser-Oberfläche können Sie Ihre Analyse erstellen, Visualisierungen hinzufügen, um Daten lebendig werden zu lassen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.

Informationen zum Erstellen von Analysen in Analysis Workspace finden Sie unter [Übersicht über Analysis Workspace](/help/analyze/analysis-workspace/home.md).

### Erste Schritte für Entwickler

[Mit Analytics-APIs können Sie Adobe-Server direkt aufrufen, um fast alle Aktionen auszuführen, die Sie in der Benutzeroberfläche ausführen können.](https://developer.adobe.com/analytics-apis/docs/2.0/)

Sie können Berichte erstellen, um wichtige Fragen zu Ihren Daten zu untersuchen, zu beantworten oder Einblicke zu ihnen zu erhalten. Sie können auch Komponenten von Adobe Analytics verwalten, z. B. die Erstellung von Segmenten oder berechneten Metriken.

## Videoüberblick

Weitere Informationen zu den Adobe Analytics-Grundlagen finden Sie in diesem *Einführung in Adobe Analytics - Skill Builder-Webinar* Video. Das Video führt Sie durch die Grundlagen, wie Daten erfasst werden, wie Daten an Adobe Analytics gesendet werden und welche Visualisierungsfunktionen Sie in Adobe Analytics verwenden können. Das Video bietet eine Grundlage für Sie, Daten zu erstellen, bereitzustellen, zu sammeln und zu interpretieren, sodass Sie anhand der erfassten Daten umsetzbare Einblicke und Empfehlungen bereitstellen können.

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Eine Erörterung, welches Tool verwendet werden sollte, finden Sie unter [Welches Adobe Analytics-Tool sollte ich verwenden?](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/which-analytics-tool.html?lang=de).

## Weiter mit Customer Journey Analytics

Customer Journey Analytics ist eine Analytics-Lösung der nächsten Generation von Adobe, mit der Sie die Funktionen von Analysis Workspace mit Daten von Adobe Experience Platform nutzen können. Sie kann die Daten mehrerer Jahre aufschlüsseln, filtern, abfragen und visualisieren und wird mit der Fähigkeit von Platform kombiniert, alle Arten von Datenschemata und -typen zu speichern.

Im Folgenden finden Sie einige der Vorteile von Customer Journey Analytics gegenüber Adobe Analytics:

* **Unbegrenzte Variablen und Ereignisse**: Die Konzepte von eVars, Props und Ereignissen existieren nicht mehr. Die Daten werden in erster Linie in Dimensionen und Metriken betrachtet. Datensätze können eine unbegrenzte Anzahl an eindeutigen Dimensionen und Metriken aufweisen.

* **Unbegrenzte Anzahl eindeutiger Werte**: Bei Adobe Experience Platform ist die Anzahl eindeutiger Werte nicht beschränkt.

* **Historische Daten ändern**: Mit Adobe Experience Platform können Daten entfernt oder korrigiert werden.

* **Report Suite-übergreifende Daten**: Vorhandene Implementierungen aus mehreren Datensätzen können in Platform kombiniert werden.

Weitere Informationen finden Sie unter [Customer Journey Analytics - Übersicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de).

