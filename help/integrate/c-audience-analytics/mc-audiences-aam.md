---
description: Adobe Audience Manager (AAM) ist eine leistungsfähige Datenverwaltungsplattform, mit deren Hilfe Sie eindeutige Zielgruppenprofile durch Integration von Daten aus erster, zweiter (Partner) und dritter Hand aufbauen können. Advertiser können mithilfe dieser Zielgruppenprofile die wertvollsten Segmente für beliebige digitale Kanäle ermitteln.
seo-description: Adobe Audience Manager (AAM) ist eine leistungsfähige Datenverwaltungsplattform, mit deren Hilfe Sie eindeutige Zielgruppenprofile durch Integration von Daten aus erster, zweiter (Partner) und dritter Hand aufbauen können. Advertiser können mithilfe dieser Zielgruppenprofile die wertvollsten Segmente für beliebige digitale Kanäle ermitteln.
seo-title: Audience Analytics-Übersicht
solution: Experience Cloud
title: Audience Analytics-Übersicht
uuid: 86ef9391-dd6a-495f-a10e-e98bc069dde4
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Audience Analytics-Übersicht

Adobe Audience Manager (AAM) ist eine leistungsfähige Datenverwaltungsplattform, mit deren Hilfe Sie eindeutige Zielgruppenprofile durch Integration von Daten aus erster, zweiter (Partner) und dritter Hand aufbauen können. Advertiser können mithilfe dieser Zielgruppenprofile die wertvollsten Segmente für beliebige digitale Kanäle ermitteln.

Mit der Integration von Audience Analytics können Sie AAM-Zielgruppendaten wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Daten zu Anzeigenimpressionen in einen beliebigen Analytics-Arbeitsablauf aufnehmen.

## Wesentliche Vorteile {#section_94816D17283349E0BA28521BE55BB868}

Die Audience Analytics-Integration umfasst die folgenden wesentlichen Vorteile:

* Es ist die erste zu einem eigenen Produkt gemachte Integration zwischen einer Daten-Management-Plattform (DMP) und einer Analyse-Engine auf dem Markt.
* Segmente werden in Echtzeit von AAM an Analytics freigegeben, um Informationen über erkannte Zielgruppen, Segmentierung und Optimierung zu liefern.
* Alle AAM-Segmente werden standardmäßig freigegeben und bereichern somit vollständig die Kundenprofile in Analytics.
* Administratoren der Lösung können die Integration über die Benutzeroberfläche aktivieren. Dabei ist nur eine minimale Anpassung des Codes erforderlich.
* Es werden nur Segmente freigegeben, die den Bestimmungen für das Exportieren von Audience Manager-Daten entsprechen.

## Funktionsweise {#section_CECDF5A0FEC64264B206EFEF54F19EF2}

![](assets/mc-aud-dataflow.png)

1. Bei jedem Besuch eines Benutzers Ihrer digitalen Eigenschaften werden Treffer gesammelt und an Analytics weitergeleitet.
1. Mit [Serverseitige Weiterleitung](/help/admin/admin/c-server-side-forwarding/ssf.md) wird jeder Treffer, den Analytics erhält, automatisch in Echtzeit an AAM gesendet.
1. Durch die Integration von Audience Analytics wird für jeden Treffer die Zielgruppenmitgliedschaft eines Besuchers in AAM nachgeschlagen und eine Liste der Segment-IDs wird zur Verarbeitung in Echtzeit an Analytics zurückgegeben.

Da AAM-Segmente auf Grundlage übereinstimmender Treffer eingefügt werden, haben Sie die Gewissheit, dass die in AAM verfügbaren Daten zu einem Besucher für den jeweiligen Treffer vollständig und aktuell sind. Dies ist einem AppMeasurement-Plugin überlegen, da ein Plugin diese Segmente erst beim nächsten Treffer (und nicht schon beim aktuellen Treffer) verfügbar machen kann.

Darüber hinaus klassifizieren wir die AAM-Segment-IDs automatisch nach Anzeigenamen, sodass Sie sich nicht die alphanumerischen IDs in Analytics-Berichten ansehen müssen.

## Voraussetzungen {#section_A345DC31F7D44EAE9DC1AB53E824C0CC}

Stellen Sie sicher, dass folgende Voraussetzungen erfüllt sind:

* Sie sind Kunde sowohl von Audience Manager als auch von Adobe Analytics.
* Sie sind ein Audience Manager-Administrator.
* Sie verwenden den Identitätsdienst v1.5 oder höher.
* AAM und Adobe Analytics werden [derselben Experience Cloud-Organisation zugeordnet](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html).
* You use [server-side forwarding](/help/admin/admin/c-server-side-forwarding/ssf.md) and have implemented the [Audience Management module](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html) (no DIL code) - AppMeasurement 1.5 or later.

Diese Voraussetzungen werden im Arbeitsablauf für [Zielgruppenanalysen](../../integrate/c-audience-analytics/c-workflow/audiences-workflow.md#concept_A5F067D14C794B759A1D92526DE27F83)beschrieben.
