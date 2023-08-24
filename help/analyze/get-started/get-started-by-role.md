---
description: Allgemeine Übersichtsinformationen zu Adobe Analytics, einschließlich Informationen zur Analytics-Oberfläche sowie Informationen zu den ersten Schritten für Administratoren, Analysten, Benutzer und Entwickler.
title: Erste Schritte für Administratoren, Analysten, Endbenutzer und Entwickler
feature: Analytics Basics
hide: true
hidefromtoc: true
source-git-commit: f23e0c74072d38d5c6559288b2ced60d98634fac
workflow-type: tm+mt
source-wordcount: '1812'
ht-degree: 34%

---

# Erste Schritte für Administratoren, Analysten, Endbenutzer und Entwickler

In einer typischen Organisation gibt es drei Arten von Adobe Analytics-Benutzern: Administratoren, Analysten und Endbenutzer.

Administratoren implementieren und konfigurieren Adobe Analytics; Analysten richten Projekte ein und erstellen Analysen mithilfe von Analysis Workspace. Endbenutzer erhalten umsetzbare Einblicke in ihre Kunden, indem sie entweder eigene Analysen erstellen oder mit Analysten zusammenarbeiten, um diese zu erstellen.

Die folgenden Informationen zeigen, wie jeder dieser Benutzer mit Adobe Analytics beginnen kann.

## Erste Schritte für Administratoren

Analytics-Administratoren sind für die Auswahl der Implementierungsmethode verantwortlich, die für ihre Organisation am besten geeignet ist.

Nachdem Adobe Analytics implementiert wurde, müssen Administratoren verschiedene Konfigurationsaufgaben durchführen, um sicherzustellen, dass Analysten und Endbenutzer von Adobe Analytics den vollen Nutzen ziehen. Administratoren sollten außerdem regelmäßig ihre Analytics-Umgebung überwachen, um sicherzustellen, dass das System effizient ausgeführt wird.

### Bestimmen der zu erfassenden Datentypen

Mit Adobe Analytics können Sie Daten aus mehreren Kanaltypen erfassen und zusammenführen, um aussagekräftige Echtzeit-Kundeneinblicke zu liefern.

Im Folgenden finden Sie einige der unterstützten Kanäle, in denen Daten erfasst werden können:

* Mobiltelefone

* Das Internet der Dinge

* TV

* Sprachassistenten

* Verbundene Fahrzeuge

* Und mehr (regelmäßig werden neue unterstützte Kanäle hinzugefügt)

Die [Implementierungsmethode](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de) bestimmt, welche Art von Daten erfasst werden können.

### Implementieren von Adobe Analytics

Bei der Implementierung von Adobe Analytics auf Ihrer Website oder in Ihrer App stehen verschiedene Implementierungsmethoden zur Verfügung.

Informationen zu den einzelnen verfügbaren Methoden finden Sie unter [Implementieren von Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/home.html?lang=de).

| | Methoden der Implementierung |
|---------|---------|
| **Websites** | <ul><li>Web SDK-Erweiterung (empfohlen)</li><li>Web SDK</li><li>Analytics-Erweiterung</li><li>Legacy-JavaScript</li></ul> |
| **Mobile Anwendungen** | <ul><li>Mobile SDK-Erweiterung (empfohlen)</li><li>Analytics-Erweiterung</li></ul> |

{style="table-layout:auto"}

### Konfigurieren von Adobe Analytics

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

### Überwachen von Adobe Analytics

Es stehen verschiedene Funktionen zur Verfügung, mit denen Sie Ihre Adobe Analytics-Umgebung überwachen können.

Analytics-Administratoren sollten sich der folgenden Funktionen bewusst sein, die zur Überwachung wichtiger Aspekte Ihrer Analytics-Umgebung verfügbar sind:

| Aufgabe | Vorgesehene Verwendung | Weitere Informationen |
|---------|----------|---------|
| Reporting Activity Manager | Reporting Activity Manager zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Es bietet eine detaillierte Übersicht über den Berichtsverbrauch und hilft Ihnen, während Spitzenzeiten der Berichterstellung mühelos Kapazitätsprobleme zu diagnostizieren und zu beheben. | [Reporting Activity Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html?lang=en) |
| Nutzung von Server-Aufrufen | Ein Server-Aufruf, auch als „Treffer“ oder „Bildanforderung“ bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Es steht ein Dashboard zur Nutzung von Server-Aufrufen zur Verfügung, in dem die Verbrauchsdaten Ihrer Server-Aufrufe verfolgt und mit Ihrem vertraglichen Limit verglichen werden. Sie können Warnhinweise einrichten, um Überschüsse zu vermeiden. | [Übersicht über die Nutzung der Server-Aufrufe](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html?lang=en) |
| Protokolldateien | Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. | [Protokolle](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html?lang=de) |

{style="table-layout:auto"}

## Erste Schritte für Analysten

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

## Erste Schritte für Endbenutzer

Endbenutzer, die keine professionellen Analysten sind, können entweder mit Analysten in ihrem Unternehmen zusammenarbeiten, um die volle Leistungsfähigkeit von Adobe Analytics und Analysis Workspace zu nutzen, oder sie können die Grundlagen von Analysis Workspace lernen, um praktische Einblicke über ihre Kunden zu erhalten.

### Arbeiten mit Analysten

Normalerweise sind Benutzer in einem Unternehmen, die mehr über das Kundenverhalten auf ihren verschiedenen Sites erfahren möchten, keine professionellen Analysten.

Idealerweise sollten diese Benutzer mit [Analysten](#analysts) innerhalb einer Organisation:

1. Definieren Sie Anforderungen für die Analysen, indem Sie dem Analysten erklären, was er über Kunden zu erfahren hofft.

1. Überprüfen Sie die Analysen, um sicherzustellen, dass sie die Ziele erreichen.

1. Beschreiben Sie die aus den Analysen gewonnenen Daten.

1. Ändern Sie die Analysen nach Bedarf im Laufe der Zeit.

### Erstellen von Analysen in Analysis Workspace

Sie müssen kein Datenanalyst sein, um von Adobe Analytics umsetzbare Einblicke zu erhalten.

Für einige Benutzer ist es möglicherweise hilfreich, mit einem Datenanalyst zusammenzuarbeiten, um ein Projekt in Analysis Workspace einzurichten und zu erklären, wie die Daten interpretiert werden, wie unter [Arbeiten mit Analysten](#work-with-analysts); andere Benutzer können sich möglicherweise damit befassen, das Projekt zu erstellen und die Daten selbst zu interpretieren.

Mit Analysis Workspace können Sie schnell Analysen erstellen, um Einblicke zu gewinnen und diese Einblicke dann für andere freizugeben. Mithilfe der Drag-and-Drop-Browser-Oberfläche können Sie Ihre Analyse erstellen, Visualisierungen hinzufügen, um Daten lebendig werden zu lassen, einen Datensatz kuratieren sowie Projekte für andere in Ihrer Organisation freigeben und planen.

Informationen zum Erstellen von Analysen in Analysis Workspace finden Sie unter [Übersicht über Analysis Workspace](/help/analyze/analysis-workspace/home.md).

## Erste Schritte für Entwickler

[Mit Analytics-APIs können Sie Adobe-Server direkt aufrufen, um fast alle Aktionen auszuführen, die Sie in der Benutzeroberfläche ausführen können.](https://developer.adobe.com/analytics-apis/docs/2.0/)

Sie können Berichte erstellen, um wichtige Fragen zu Ihren Daten zu untersuchen, zu beantworten oder Einblicke zu ihnen zu erhalten. Sie können auch Komponenten von Adobe Analytics verwalten, z. B. die Erstellung von Segmenten oder berechneten Metriken.