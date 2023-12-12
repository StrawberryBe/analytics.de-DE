---
description: Allgemeine Übersichtsinformationen zu Adobe Analytics, einschließlich Informationen zur Analytics-Oberfläche sowie Informationen zu den ersten Schritten für Admins, Analystinnen und Analysten, Benutzende sowie Entwicklungspersonen.
title: Erste Schritte für Admins, Analystinnen und Analysten, Endbenutzerinnen und Endbenutzer sowie Entwicklungspersonen
feature: Analytics Basics
exl-id: 11800de5-224a-4bd2-8cb1-a6318925db71
source-git-commit: 984406d00e5a5ae966fff60ec9fcfcb000958696
workflow-type: ht
source-wordcount: '1883'
ht-degree: 100%

---

# Erste Schritte für Admins, Analystinnen und Analysten, Endbenutzerinnen und Endbenutzer sowie Entwicklungspersonen

In einer typischen Organisation gibt es vier Arten von Adobe Analytics-Benutzenden:

* **Admins:** Implementieren und konfigurieren Adobe Analytics.

* **Analystinnen und Analysten:** Richten Projekte ein und erstellen Analysen mit Analysis Workspace

* **Endbenutzende:** Verschaffen sich umsetzbare Einblicke zu ihren Kundinnen und Kunden, indem sie entweder eigene Analysen erstellen oder sie in Zusammenarbeit mit Analytikerinnen und Analytikern erstellen lassen.

* **Entwicklungspersonen:** Verwenden die Adobe Analytics 2.0-APIs, um Adobe-Server direkt aufzurufen und fast alle Aktionen auszuführen, die in der Benutzeroberfläche ausgeführt werden können. Dazu gehört etwa das Erstellen von Berichten, um Daten zu untersuchen, Einblicke zu ihnen zu erhalten oder wichtige Fragen über sie zu beantworten.

Im Folgenden wird beschrieben, wie diese Benutzerinnen und Benutzer jeweils mit Adobe Analytics beginnen können.

## Erste Schritte für Admins

Analytics-Admins sind für die Auswahl der Implementierungsmethode verantwortlich, die für ihre Organisation am besten geeignet ist.

Nachdem Adobe Analytics implementiert wurde, müssen Admins verschiedene Konfigurationsaufgaben durchführen, um sicherzustellen, dass Analystinnen und Analysten sowie Endbenutzerinnen und Endbenutzer den vollen Nutzen aus Adobe Analytics ziehen. Admins sollten außerdem regelmäßig ihre Analytics-Umgebung überwachen, um sicherzustellen, dass das System effizient ausgeführt wird.

### Bestimmen der zu erfassenden Datentypen

Mit Adobe Analytics können Sie Daten aus mehreren Kanaltypen erfassen und zusammenführen, um aussagekräftige Echtzeit-Kundenerkenntnisse zu liefern.

Im Folgenden finden Sie einige der unterstützten Kanäle, in denen Daten erfasst werden können:

* Mobiltelefone

* Das Internet der Dinge

* TV

* Sprachassistenten

* Vernetzte Fahrzeuge

* Und mehr (es werden regelmäßig neue unterstützte Kanäle hinzugefügt)

Die von Ihnen ausgewählte [Implementierungsmethode](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de) bestimmt, welche Art von Daten erfasst werden können.

### Implementieren von Adobe Analytics

Bei der Implementierung von Adobe Analytics auf Ihrer Website oder in Ihrer Mobile App stehen verschiedene Implementierungsmethoden zur Verfügung.

Informationen zu den einzelnen verfügbaren Methoden finden Sie unter [Implementieren von Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de).

| | Methoden der Implementierung |
|---------|---------|
| **Websites** | <ul><li>Web SDK-Erweiterung (empfohlen)</li><li>Web SDK</li><li>Analytics-Erweiterung</li><li>Legacy-JavaScript</li></ul> |
| **Mobile Apps** | <ul><li>Mobile SDK-Erweiterung (empfohlen)</li><li>Analytics-Erweiterung</li></ul> |

{style="table-layout:auto"}

### Konfigurieren von Adobe Analytics

Analytics-Admins sollten die folgenden Aufgaben ausführen, bevor sie Adobe Analytics für Benutzerinnen und Benutzer in der Organisation verfügbar machen:

| Aufgabe | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Definieren von Admin-Rollen | In Adobe Analytics gibt es verschiedene Arten von Admins | [Administratorrollen in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html?lang=de) |
| Definieren von Berechtigungen | Analytics-Admins müssen Produktprofile in der Admin Console für Adobe Analytics, Report Suite-Tools und Analytics-Tools zuweisen. | [Analytics-Berechtigungen in Admin Console](/help/admin/admin-console/permissions/analytics-tools.md) |
| Einrichten von Report Suites und Definieren von Einstellungen für Ihr Unternehmen | Bei einer Report Suite handelt es sich um einen Datenspeicher, mit dem Adobe Analytics Berichte generiert.<p>Admins können außerdem [Virtual Report Suites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=de) zur weiteren Segmentierung von Daten einrichten.</p> | <ul><li>[Erstellen einer Report Suite](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html?lang=de)</li><li>[Übersicht über Unternehmenseinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=de)</li></ul> |
| Importieren von Daten | Sie können Adobe Analytics-Datenquellen nutzen, um zusätzliche Online- oder Offline-Daten für die Berichterstellung zu importieren. | [Datenquellen – Übersicht](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=de) |
| Klassifizieren von Daten mit Klassifizierungen | Klassifizierungen ermöglichen es Ihnen, Daten zu klassifizieren, um Variablen besser zu nutzen und so mehr Inhalte in eine Variable einzuschließen. | [Übersicht über Klassifizierungen](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=de) |
| Verwalten von Komponenten | Verwenden Sie das Datenwörterbuch und die Verwaltungsbereiche für jeden Komponententyp, um zu definieren, welche Komponenten in Ihrer Analytics-Implementierung verfügbar sind und welche für Ihr Unternehmen genehmigt sind.<p>Dies sollte eine fortlaufende Aktivität sein, um sicherzustellen, dass Komponenten in Ihrem Unternehmen effektiv verwendet werden. </p> | <ul><li>[Datenwörterbuch – Überblick](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html?lang=de)</li><li>[Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=de)</li><li>[Verwalten von Segmenten](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de)</li><li>[Erstellen von benutzerdefinierten Datumsbereichen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=de)</li></ul> |
| Anomalieerkennung | Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat. | [Übersicht über die Anomalieerkennung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html?lang=de) |
| Beitragsanalyse | Die Beitragsanalyse erkennt versteckte Muster, mit denen sich statistische Anomalien erklären und Korrelationen für nicht erwartete Kundenaktionen, Wertbereichsüberschreitungen und plötzliche Anstiege oder Rückgänge für ausgewählte Metriken in konvergenten Zielgruppensegmenten feststellen lassen. | [Übersicht über die Beitragsanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) |
| Analytics-Segmentierung | Damit können Sie leistungsstarke, fokussierte Zielgruppensegmente erstellen, verwalten, freigeben und anwenden, um mithilfe von Analytics-Funktionen, Adobe Experience Cloud, Adobe Target und anderen integrierten Adobe-Produkten Berichte zu erstellen. | [Analytics-Segmentierung](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de) |
| Veröffentlichen von Zielgruppen in Audience Manager | Adobe Audience Manager ist eine leistungsfähige Datenverwaltungsplattform, mit deren Hilfe Sie eindeutige Zielgruppenprofile durch Integration von Daten aus erster, zweiter (Partner) und dritter Hand aufbauen können. | [Audience Analytics-Übersicht](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=de) |
| Integrationen | Sie können Informationen aus anderen Anwendungen in Adobe Analytics anzeigen lassen. <p>Im Folgenden finden Sie einige gängige Integrationen:</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de">Analytics for Target</a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=de">Media Analytics</a></li> | [Analytics-Integration](https://experienceleague.adobe.com/docs/analytics/integration/home.html?lang=de) |

{style="table-layout:auto"}

### Überwachen von Adobe Analytics

Es stehen verschiedene Funktionen zur Verfügung, mit denen Sie Ihre Adobe Analytics-Umgebung überwachen können.

Analytics-Admins sollten sich der folgenden Funktionen bewusst sein, die zur Überwachung wichtiger Aspekte Ihrer Analytics-Umgebung verfügbar sind:

| Aufgabe | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Reporting Activity Manager | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Er bietet detaillierte Einblicke in die Berichtsnutzung und hilft Ihnen, Kapazitätsprobleme bei Spitzen während der Berichterstellung mühelos zu diagnostizieren und zu beheben. | [Reporting Activity Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html?lang=de) |
| Nutzung von Server-Aufrufen | Ein Server-Aufruf, auch als „Treffer“ oder „Bildanforderung“ bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Es ist ein Dashboard zur Nutzung von Server-Aufrufen verfügbar, das Ihre Verbrauchsdaten bezüglich Server-Aufrufen verfolgt und mit Ihrem vertraglich festgelegten Limit vergleicht. Sie können Warnhinweise einrichten, um Überschüsse zu vermeiden. | [Nutzung von Server-Aufrufen – Übersicht](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html?lang=de) |
| Protokolldateien | Protokolldateien, die anzeigen, wann sich Benutzende angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. | [Protokolle](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html?lang=de) |

{style="table-layout:auto"}

## Erste Schritte für Analystinnen und Analysten

Während alle Mitarbeiterinnen und Mitarbeiter einer Organisation Adobe Analytics verwenden können, um verwertbare Erkenntnisse über das Kundenverhalten von Websites und Apps zu erhalten, ist Adobe Analytics speziell auf Datenanalystinnen und -analysten zugeschnitten.

Im Folgenden finden Sie wichtige Aufgaben und Funktionen, mit denen Analystinnen und Analysten vertraut sein sollten, um die volle Leistungsfähigkeit von Adobe Analytics und Analysis Workspace zu nutzen.

| Funktion | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Erstellen und Freigeben von Projekten in Analysis Workspace | Analysis Workspace ist ein flexibles Browser-Tool, mit dem Sie schnell Analysen erstellen und Insights austauschen können. Mithilfe der Drag-and-Drop-Oberfläche können Sie Ihre Analyse gestalten, Visualisierungen hinzufügen, um Daten optisch darzustellen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.<p>Datenanalystinnen und -analysten sind häufig für das Erstellen von Projekten in Analysis Workspace für Benutzerinnen und Benutzer in ihrer Organisation verantwortlich.</p><p>Nachdem Projekte erstellt wurden, teilen Analystinnen und Analysten diese Projekte für die [Endbenutzenden](#end-users)(Nicht-Analystinnen und -Analysten) in ihren Organisationen, die die Daten angefordert haben, und helfen ihnen dabei, sie richtig interpretieren zu können.</p> | <ul><li>[Erstellen von Projekten](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attribution | Analystinnen und Analysten können anpassen, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden, indem sie verschiedene Attributionsmodelle und Lookback-Fenster in Analysis Workspace verwenden.<p>Die linearen Attributionsmodelle geben jedem Touchpoint, der zu einer Konversion führt, die gleiche Gewichtung, während „Erstkontakt“ die Konversion allein dem Erstkontaktpunkt zuschreibt. Es stehen viele weitere Attributionsmodelle zur Verfügung, darunter das algorithmische Modell, das mithilfe statistischer Verfahren die optimale Gewichtung dynamisch bestimmt. </p> | [Attributionsmodelle und Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md) |
| Anomalieerkennung | Die statistische Modellierung in Analysis Workspace findet automatisch unerwartete Trends in Ihren Daten, indem sie Metriken analysiert und eine untere Grenze, eine obere Grenze und einen erwarteten Wertebereich bestimmt. Treten unerwartete Spitzen oder Rückgänge auf, meldet das System dies im entsprechenden Bericht. | [Übersicht über die Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Beitragsanalyse | Verwenden Sie Analysis Workspace, um versteckte Muster zu erkennen, mit denen sich statistische Anomalien erklären und Korrelationen für nicht erwartete Kundenaktionen, Wertbereichsüberschreitungen und plötzliche Spitzen oder Tiefpunkte für ausgewählte Metriken in konvergenten Zielgruppensegmenten feststellen lassen. | [Beitragsanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) in [Anomalieerkennung – Übersicht](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Intelligente Warnhinweise | Erstellen und verwalten Sie auf Datenanomalien basierende Warnhinweise sowie „gestapelte“ Warnhinweise, die mehrere Metriken in einem Warnhinweis erfassen. | [Übersicht über intelligente Warnhinweise](/help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md) |
| Datenexport | Mit Data Warehouse und Daten-Feeds können Sie Daten an verschiedene Cloud-Ziele exportieren, z. B. Google Cloud Platform, Azure RBAC, Azure SAS und Amazon S3. | [Leitfaden für Analytics-Exporte](https://experienceleague.adobe.com/docs/analytics/export/home.html?lang=de) |
| Activity Map | Activity Map ist eine Adobe Analytics-Anwendung, die der Link-Aktivität mithilfe von visuellen Überlagerungen einen Rang zuweist und ein Dashboard mit Echtzeitanalyse bereitstellt, um die Interaktion der Zielgruppe mit Ihren Web-Seiten zu überwachen.<p>Activity Map ermöglicht Ihnen, verschiedene Ansichten einzurichten, um beschleunigte Kundenaktivität zu erkennen, Marketinginitiativen zu quantifizieren und auf die Bedürfnisse und das Verhalten der Zielgruppe zu reagieren.</p> | [Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html?lang=de) |
| Report Builder | Report Builder ist ein Add-in für Microsoft Excel. Mit Report Builder können Sie benutzerdefinierte Anfragen aus Adobe Analytics-Daten erstellen, die in Ihre Excel-Arbeitsblätter eingefügt werden. Anforderungen können dynamisch auf Zellen innerhalb Ihres Arbeitsblatts verweisen, und die Darstellung der Daten in Report Builder lässt sich aktualisieren und anpassen. | [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html?lang=de) |

{style="table-layout:auto"}

<!-- * Realtime reporting? -->

## Erste Schritte für Endbenutzerinnen und Endbenutzer

Endbenutzerinnen und -benutzer, die keine professionellen Analystinnen und Analysten sind, können entweder mit Analystinnen und Analysten in ihrer Organisation zusammenarbeiten, um die volle Leistungsfähigkeit von Adobe Analytics und Analysis Workspace zu nutzen, oder sie können die Grundlagen von Analysis Workspace erlernen, um praktische Erkenntnisse über ihre Kundinnen und Kunden zu erhalten.

### Arbeiten mit Analystinnen und Analysten

Normalerweise sind Benutzerinnen und Benutzer in einer Organisation, die mehr über das Kundenverhalten auf ihren verschiedenen Sites erfahren möchten, keine professionellen Analystinnen bzw. Analysten.

Idealerweise sollten diese Personen mit [Analystinnen und Analysten](#analysts) innerhalb einer Organisation zusammenarbeiten, um:

1. Anforderungen für die Analysen zu definieren, indem Sie der Analystin bzw. dem Analysten erklären, was über die Kundschaft in Erfahrung gebracht werden soll.

1. die Analysen zu überprüfen, damit sichergestellt wird, dass sie die Ziele erreichen.

1. die aus den Analysen gewonnenen Daten zu diskutieren.

1. die Analysen im Laufe der Zeit nach Bedarf abzuändern.

### Erstellen von Analysen in Analysis Workspace

Sie müssen keine Datenanalystin bzw. kein Datenanalyst sein, um von Adobe Analytics umsetzbare Erkenntnisse zu erhalten.

Für einige Benutzerinnen bzw. Benutzer ist es möglicherweise hilfreich, mit einer Datenanalystin bzw. einem Datenanalysten zusammenzuarbeiten, um ein Projekt in Analysis Workspace einzurichten und zu erklären, wie die Daten interpretiert werden, wie unter [Arbeiten mit Analystinnen und Analysten](#work-with-analysts) beschrieben wird. Andere Benutzerinnen und Benutzer können hingegen zufrieden damit sein, selbst das Projekt zu erstellen und die Daten zu analysieren.

Mit Analysis Workspace können Sie schnell Analysen erstellen, um Einblicke zu gewinnen und diese Einblicke dann für andere freizugeben. Mithilfe der Drag-and-Drop-Browser-Oberfläche können Sie Ihre Analyse erstellen, Visualisierungen hinzufügen, um Daten lebendig werden zu lassen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.

Informationen zum Erstellen von Analysen in Analysis Workspace finden Sie unter [Analysis Workspace – Übersicht](/help/analyze/analysis-workspace/home.md).

## Erste Schritte für Entwicklerinnen und Entwickler

[Mit Analytics-APIs können Sie die Adobe-Server direkt aufrufen, um fast alle Aktionen auszuführen, die Sie in der Benutzeroberfläche ausführen können.](https://developer.adobe.com/analytics-apis/docs/2.0/)

Sie können Berichte erstellen, um wichtige Fragen zu Ihren Daten zu untersuchen, zu beantworten oder Einblicke zu ihnen zu erhalten. Sie können auch Komponenten von Adobe Analytics verwalten, z. B. die Erstellung von Segmenten oder berechneten Metriken.
