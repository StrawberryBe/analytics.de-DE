---
description: In diesem Dokument wird beschrieben, was Sie in Adobe Analytics tun müssen, um die CCPA-Zugriffsrechte und -Löschrechte der betroffenen Personen zu unterstützen.
seo-description: In diesem Dokument wird beschrieben, was Sie in Adobe Analytics tun müssen, um die CCPA-Zugriffsrechte und -Löschrechte der betroffenen Personen zu unterstützen.
seo-title: Adobe Analytics und CCPA
title: Adobe Analytics und CCPA
uuid: 16fd5af8-9148-4e09-ad54-9e3cdd2b3c6d
translation-type: tm+mt
source-git-commit: 21fe6a0ee434e430d77a24d060acd2ffce08e219

---


# Adobe Analytics und CCPA

In diesem Dokument wird beschrieben, was Sie in Adobe Analytics tun müssen, um die CCPA-Zugriffsrechte und -Löschrechte der betroffenen Personen zu unterstützen.

## Adobe-Übersicht

>[!IMPORTANT] Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Für Beratung zu CCPA wenden Sie sich bitte an die Rechtsabteilung Ihres Unternehmens.

Am 1. Januar 2020 tritt das California Consumer Privacy Act (CCPA) in Kraft. For more information about Adobe's response and what this means for you as an Adobe customer, see [Adobe's Privacy Center.](https://www.adobe.com/privacy.html)

Wenn Adobe einem Unternehmen Software und Services bereitstellt, fungiert Adobe als Auftragsverarbeiter für alle personenbezogenen Daten, die wir im Rahmen dieser Services im Namen unserer Kunden empfangen und speichern. Als Datenverarbeiter verarbeitet Adobe personenbezogene Daten gemäß den Genehmigungen und Anweisungen Ihres Unternehmens (z. B. gemäß Ihrer Vereinbarung mit Adobe).

Als Verantwortlicher bestimmen Sie die personenbezogenen Daten, die Adobe in Ihrem Namen verarbeitet und speichert. Wenn Sie Adobe Experience Cloud-Lösungen nutzen, hostet Adobe abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe Experience Cloud-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz.](https://www.adobe.com/privacy/marketing-cloud.html#collect)

## Umgang mit CCPA-Daten durch Adobe

Die Adobe Cloud Platform (ACP) bietet eine integrierte Lösung, die die Data-Governance-Infrastruktur Ihrer Marke mit den Adobe-Tools zur Erstellung und Verwaltung von Kundenerlebnissen verbindet. Die Data-Governance-Funktionen der Adobe Cloud Platform ermöglichen direkte Verbindungen zwischen Data-Governance-Richtlinie und Datennutzung.

Familiarize yourself with [how Adobe Analytics handles GDPR](https://www.adobe.com/data-analytics-cloud/analytics/general-data-protection-regulation.html) which discusses steps for privacy readiness and how to integrate with the Adobe Experience Cloud Privacy Service API.

## CCPA-Bereitschaft und Ihre Adobe Analytics-Daten

Wir wissen, dass Sie die individuellen Daten Ihrer Report Suites am besten kennen. Deshalb bietet Adobe Ihnen die Möglichkeit, Ihre Data-Governance-Einstellungen und -Präferenzen selbst zu definieren.
Hierzu umfasst Adobe Analytics eine Data-Governance-Benutzeroberfläche, über die Sie als Datenverantwortlicher [Datenschutzbeschriftungen](/help/admin/c-data-governance/gdpr-labels.md#concept_F4061E29353446B5B0A7CF248D54E6F2) zu Ihren Analytics Report Suites sowie allen Dimensionen und Metriken in diesen Report Suites festlegen können. Sie können die Spalten in Ihrem Datensatz festlegen, die direkt oder indirekt identifizierbare Daten enthalten, damit Sie Zugriffs- und Löschanfragen zu diesen Daten einreichen können. Bei jeder Anfrage werden die in der Data-Governance-Benutzeroberfläche festgelegten Beschriftungen für die spezifische ID berücksichtigt, die mit der Anfrage übereinstimmt.

Weitere Informationen finden Sie unter [Report Suite-Daten beschriften](/help//admin/c-data-governance/gdpr-setup-reportsuite.md#concept_FAA948AD8CEA4BC38CB482EAF3648731).

## Voraussetzungen

* Familiarize yourself with [Privacy terminology.](/help/admin/c-data-governance/gdpr-terminology.md#concept_83C744A9D077476BAD8F8492DF68EBD7)
* Verbinden Sie Ihr Anmeldeunternehmen ggf. mit einer Experience Cloud-Organisation. Wenden Sie sich an die Adobe-Kundenunterstützung und lesen Sie die Informationen unter [Organisationen und Kontoverknüpfung.](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)
* Map any Adobe Analytics report suite that you want to set up for data governance to [your Experience Cloud organization.](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html)
* Legen Sie für jede Report Suite eine Datenaufbewahrungsrichtlinie fest, damit CCPA-Anforderungen zum Löschen und Zugreifen berücksichtigt werden können.

   Adobe Analytics kann Sie nicht bei der Verarbeitung von Anforderungen an die Datenschutzdienste-API unterstützen, d. h. bei der Verarbeitung von Zugriffs- oder Löschanforderungen, die Sie von Ihren Endbenutzern erhalten, wenn die Datenspeicherungsfrist in Adobe Analytics nicht festgelegt wurde. Wenden Sie sich an Ihren Customer Success Manager, um den Zeitraum der Datenaufbewahrung festzulegen.

* Überprüfen Sie Ihre Berechtigungen: Um die Analytics-Benutzeroberfläche zur Data-Governance-Verwaltung zu verwenden, müssen Sie Adobe Analytics-Administrator sein.
* Erwägen Sie die Implementierung der [Konfigurationsverwaltungsvariablen](/help/admin/c-data-governance/consent-variables.md) , um den Genehmigungsstatus auf Trefferebene zu verfolgen.
