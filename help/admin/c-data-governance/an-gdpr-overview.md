---
description: Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um DSGVO-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.
title: Adobe Analytics und die DSGVO
uuid: 16fd5af8-9148-4e09-ad54-9e3cdd2b3c6d
translation-type: ht
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: ht
source-wordcount: '629'
ht-degree: 100%

---


# Adobe Analytics und die DSGVO

Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um DSGVO-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.

## Adobe-Übersicht  {#section_E582A1D77583410EBB790BB646854A2C}

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich zur Unterstützung in DSGVO-Fragen an die Rechtsabteilung Ihres Unternehmens.

Am 25. Mai 2018 trat die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union in Kraft. Weitere Informationen zu den Änderungen bei Adobe und den Auswirkungen auf Sie als Adobe-Kunde finden Sie unter [DSGVO und Ihr Unternehmen.](https://www.adobe.com/de/privacy/general-data-protection-regulation.html)

Wenn Adobe einem Unternehmen Software und Services bereitstellt, fungiert Adobe als Auftragsverarbeiter für alle personenbezogenen Daten, die wir im Rahmen dieser Services im Namen unserer Kunden empfangen und speichern. Als Datenverarbeiter verarbeitet Adobe personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. über Angaben in Ihrer Vereinbarung mit Adobe).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe in Ihrem Namen verarbeitet und speichert. Wenn Sie Adobe Experience Cloud-Lösungen nutzen, hostet Adobe abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe Experience Cloud-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz.](https://www.adobe.com/de/privacy/experience-cloud.html#collect)

![](assets/privacy_ready.png)

## So verarbeitet Adobe DSGVO-Daten {#section_A20BCC08A80B410D97601BFB1CAF83F1}

Die Adobe Cloud Platform (ACP) bietet eine integrierte Lösung, die die Data-Governance-Infrastruktur Ihrer Marke mit den Adobe-Tools zur Erstellung und Verwaltung von Kundenerlebnissen verbindet. Die Data-Governance-Funktionen der Adobe Cloud Platform ermöglichen direkte Verbindungen zwischen Data-Governance-Richtlinie und Datennutzung.

Machen Sie sich mit der [DSGVO-Verarbeitung in Adobe Analytics](https://www.adobe.com/data-analytics-cloud/analytics/general-data-protection-regulation.html) vertraut. Dort werden die Schritte zur DSGVO-Bereitschaft und zur Integration in die DSGVO-API von Adobe Experience Cloud erläutert.

## DSGVO-Bereitschaft und Ihre Adobe Analytics-Daten {#section_9A47CDCD614C42238F6E05CFF0180195}

Wir wissen, dass Sie die individuellen Daten Ihrer Report Suites am besten kennen. Deshalb bietet Adobe Ihnen die Möglichkeit, Ihre Data-Governance-Einstellungen und -Präferenzen selbst zu definieren.

Hierzu umfasst Adobe Analytics eine Data-Governance-Benutzeroberfläche, über die Sie als Datenverantwortlicher [Datenschutzbeschriftungen](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels) zu Ihren Analytics Report Suites sowie allen Dimensionen und Metriken in diesen Report Suites festlegen können. Sie können die Spalten in Ihrem Datensatz festlegen, die direkt oder indirekt identifizierbare Daten enthalten, damit Sie Zugriffs- und Löschanfragen zu diesen Daten einreichen können. Bei jeder Anfrage werden die in der Data-Governance-Benutzeroberfläche festgelegten Beschriftungen für die spezifische ID berücksichtigt, die mit der Anfrage übereinstimmt.

Siehe [Report Suite-Daten beschriften](/help/admin/c-data-governance/gdpr-setup-reportsuite.md).

## Voraussetzungen {#section_3C766371CE0641C0821FE8E750E5AE0C}

* Machen Sie sich mit der [DSGVO-Terminologie](/help/admin/c-data-governance/gdpr-terminology.md) vertraut.
* Verbinden Sie Ihr Anmeldeunternehmen ggf. mit einer Experience Cloud-Organisation. Wenden Sie sich an die Adobe-Kundenunterstützung und lesen Sie die Informationen unter [Organisationen und Kontoverknüpfung.](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/organizations.html)
* Ordnen Sie eine Adobe Analytics Report Suite, die Sie für Data Governance einrichten wollen, [Ihrer Experience Cloud-Organisation](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html) zu.
* Legen Sie für jede Report Suite eine Richtlinie zur Datenaufbewahrung fest, damit DSGVO-Zugriffs- und -Löschanfragen bearbeitet werden können.

   >[!NOTE]
   >
   >Adobe Analytics kann Sie bei der Verarbeitung von Anfragen an die DSGVO-API – also bei der Verarbeitung von Zugriffs- oder Löschanfragen, die Sie von Ihren Endbenutzern erhalten – nicht unterstützen, wenn in Adobe Analytics kein Zeitraum zur Datenaufbewahrung festgelegt wurde. Wenden Sie sich an Ihren Customer Success Manager, um den Zeitraum der Datenaufbewahrung festzulegen.

* Überprüfen Sie Ihre Berechtigungen: Um die Analytics-Benutzeroberfläche zur Data-Governance-Verwaltung zu verwenden, müssen Sie Adobe Analytics-Administrator sein.
