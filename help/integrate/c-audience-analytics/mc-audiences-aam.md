---
description: Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Erstanbieter-, Zweitanbieter-/Partner- und Drittanbieter-Datenintegrationen erstellen können. Advertiser können mithilfe dieser Zielgruppenprofile die wertvollsten Segmente für beliebige digitale Kanäle ermitteln.
solution: Experience Cloud
title: Audience Analytics-Übersicht
feature: Audience Analytics
exl-id: 1665a554-8a6f-4b20-99b7-bb3c2c4bf8cc
source-git-commit: c947de8eaa4e4dc3a0c10989ef6ae450cebc1f3e
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 42%

---

# Audience Analytics-Übersicht

Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Erstanbieter-, Zweitanbieter-/Partner- und Drittanbieter-Datenintegrationen erstellen können. Advertiser können mithilfe dieser Zielgruppenprofile die wertvollsten Segmente für beliebige digitale Kanäle ermitteln.

Mit der Audience Analytics-Integration können Sie Adobe Audience Manager-Zielgruppendaten wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Ad-Impression-Daten in beliebige Analytics-Workflows integrieren.

>[!VIDEO](https://video.tv.adobe.com/v/25450/?quality=12)

## Wesentliche Vorteile  {#benefits}

Die Audience Analytics-Integration umfasst die folgenden wesentlichen Vorteile:

* Es ist die erste zu einem eigenen Produkt gemachte Integration zwischen einer Daten-Management-Plattform (DMP) und einer Analyse-Engine auf dem Markt.
* Segmente werden in Echtzeit von Adobe Audience Manager für Analytics freigegeben, um die Erkennung, Segmentierung und Optimierung von Zielgruppen zu unterstützen.
* Alle Adobe Audience Manager-Segmente werden standardmäßig freigegeben, wodurch Kundenprofile in Analytics vollständig angereichert werden.
* Administratoren der Lösung können die Integration über die Benutzeroberfläche aktivieren. Dabei ist nur eine minimale Anpassung des Codes erforderlich.
* Es werden nur Segmente freigegeben, die den Bestimmungen für das Exportieren von Audience Manager-Daten entsprechen.

## Funktionsweise von Audience Analytics {#works}

![](assets/mc-aud-dataflow.png)

1. Bei jedem Besuch eines Benutzers Ihrer digitalen Eigenschaften werden Treffer gesammelt und an Analytics weitergeleitet.
1. Mit [serverseitige Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md), wird jeder Treffer, den Analytics erhält, automatisch in Echtzeit an Adobe Audience Manager gesendet.
1. Durch die Audience Analytics-Integration wird für jeden Treffer die Zielgruppenzugehörigkeit eines Besuchers in Adobe Audience Manager nachgeschlagen und eine Liste mit Segment-IDs wird zur Verarbeitung in Echtzeit an Analytics zurückgegeben.

Da Adobe Audience Manager-Segmente auf der Basis von Treffern eingefügt werden, können Sie sicherstellen, dass alle in Adobe Audience Manager verfügbaren Daten über einen Besucher nicht verpasst werden und für diesen Treffer auf dem neuesten Stand sind. Dies ist einem AppMeasurement-Plugin überlegen, da ein Plugin diese Segmente erst beim nächsten Treffer (und nicht schon beim aktuellen Treffer) verfügbar machen kann.

Darüber hinaus klassifizieren wir die Adobe Audience Manager-Segment-IDs automatisch nach ihren Anzeigenamen, sodass Sie in Analytics-Berichten nicht nach alphanumerischen IDs suchen müssen.

## Voraussetzungen {#prerequisites}

Stellen Sie sicher, dass folgende Voraussetzungen erfüllt sind:

* Sie sind Kunde sowohl von Audience Manager als auch von Adobe Analytics.
* Sie sind ein Audience Manager-Administrator.
* Sie verwenden den Identitätsdienst v1.5 oder höher.
* Adobe Audience Manager- und Adobe Analytics-Report Suites sind derselben Experience Cloud-Organisation zugeordnet.
* Sie nutzen [die serverseitige Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md) und haben das [Zielgruppen-Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=de) AppMeasurement 1.5 oder höher (kein DIL-Code) implementiert.

Diese Voraussetzungen werden im [Audience Analytics-Workflow](/help/integrate/c-audience-analytics/c-workflow/audiences-workflow.md) beschrieben.
