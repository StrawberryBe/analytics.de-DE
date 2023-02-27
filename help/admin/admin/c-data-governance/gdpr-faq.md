---
description: Häufig gestellte Fragen zur Verwaltung von Adobe Analytics-Daten
title: Häufig gestellte Fragen zu Data Governance
feature: Data Governance
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: c774d05ca3b1f9f45ec118b0e7b8a839a03b87e3
workflow-type: tm+mt
source-wordcount: '2076'
ht-degree: 52%

---

# Häufig gestellte Fragen

+++ **Wie unterstützt Adobe Analytics Zugriffs- und Löschanfragen für Endbenutzer (Datensubjekte), die von Kunden (Datenverantwortlichen) validiert wurden?**

Wenn verschiedene Datenschutzregeln (DSGVO, CCPA) in Kraft treten, unterstützt Adobe Analytics die Verarbeitung verifizierter Anfragen, die von Datenverantwortlichen an die Experience Cloud Data Privacy API gesendet werden, um einen stärker automatisierten Prozess zu ermöglichen. Die Datenschutz-API von Adobe ist dafür konzipiert, die Verarbeitung individueller Rechtsanfragen (z. B. Zugriffs- und Löschanfragen) für die Daten unserer Kunden zu unterstützen, die in den Adobe Experience Cloud-Lösungen gespeichert sind. Sie ist flexibel und wird entsprechend der Anzahl der Datenzugriffs- und Löschanfragen skaliert, die Ihr Unternehmen von betroffenen Personen erhält.

Die Privacy Service-API ermöglicht es dem Kunden außerdem, den Status zu überprüfen, wie die Datenzugriffs- und Löschanfragen, die erfüllt werden, ausgeführt werden. Weitere Informationen finden Sie in der [](https://developer.adobe.com/experience-platform-apis/references/privacy-service/)Dokumentation zur Datenschutz-API.

+++

+++ **Wer ist für das Empfangen, Akzeptieren und Erfüllen von Datenschutz-Anfragen von Endbenutzern zuständig?**

Der Datenverantwortliche ist allein dafür verantwortlich, Anfragen zu empfangen und zu akzeptieren. Der Datenverantwortliche validiert die Identität der betroffenen Person und erfüllt dann die Anforderung. Zu dieser Verantwortung kann es gehören, die Adobe mit den IDs der betroffenen Personen zu kontaktieren, die mit in Adobe Analytics gespeicherten Daten verknüpft sein können.

Als Datenverarbeiter muss die Adobe dem Verantwortlichen angemessene Unterstützung bei der Verarbeitung verifizierter Anfragen innerhalb einer akzeptablen Frist gewähren.

+++

+++ **Wie finden Adobe-Kunden (Datenverantwortliche) heraus, welchen IDs Datenschutzanfragen in Adobe Analytics zur Datenschutzverarbeitung zugeordnet sind?**

Die Datenverantwortlichen bestimmen, wie die Identität für Anfragen von den betroffenen Personen aufgelöst wird. Ziehen Sie die Bereitstellung des Datenschutz-ID-Abruftags von Adobe in Erwägung. Ihre Entwicklungsteams sparen Zeit, indem sie unser Datenschutz-ID-Abruftag verwenden, um Benutzer-IDs (Cookie-IDs) zu erfassen. Sie können dann unsere Datenschutz-API verwenden, um diese Benutzer-IDs zur Verarbeitung von Datenschutzanfragen an die entsprechenden Lösungen in der Adobe Experience Cloud zu senden. Die Datenschutz-API kann eine Vielzahl von Benutzer-IDs in mehreren Adobe-Lösungen unterstützen.

Wenn ein Datensubjekt eine Anfrage zusammen mit einer Kennung (benutzerdefinierte Variable - Prop oder eVar) sendet, prüft Adobe Analytics dann den gesamten gespeicherten Verlauf der Daten, die für die jeweilige ID erfasst wurden. Weitere Informationen zum Konfigurieren von benutzerdefinierten IDs, die in Props oder eVars von Analytics gespeichert sind, finden Sie im Abschnitt [Analytics-Dokumentation zu Namespaces](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md).

+++

+++ **Wie kann Adobe Analytics Data Governance bei der Verarbeitung von Datenschutzanfragen helfen?**

Data Governance ist ein neues Tool in Adobe Analytics, das Datenverantwortlichen die Möglichkeit bietet, Datenkontrollen und Klassifizierungen auf ihre Analytics-Daten anzuwenden. Dank dieses neuen Tools können Adobe-Kunden die Verarbeitung ihrer Datenschutzanfragen zum Datenzugriff und zur Datenlöschung anpassen. In der Data Governance-Konsole können Administratoren die gewünschten Einstellungen definieren, die auf verschiedene Datenspalten in Adobe Analytics angewendet werden sollen. Nachdem diese Beschriftungen definiert wurden, berücksichtigt und verarbeitet Adobe die nachfolgenden Zugriffs- oder Löschanfragen gemäß den gewünschten Beschriftungseinstellungen des Kunden. Es liegt in der Verantwortung des Datenverantwortlichen, diese Beschriftungseinstellungen zu überprüfen und sich mit seinen gesetzlichen Vertretern darüber zu beraten.

Das Data Governance-Tool beinhaltet die folgenden Datenbeschriftungen:

* **Beschriftungen für Identitätsdaten**: Dient zur Klassifizierung von Daten, mit denen eine Person direkt oder in Kombination mit anderen Daten identifiziert werden kann. (None/I1/I2)

* **Beschriftungen für vertrauliche Daten**: Wird verwendet, um Daten als Daten zu klassifizieren, die unter geltendem Recht als vertraulich definiert werden können. (None, S1, S2) Beachten Sie, dass die Verwendung vertraulicher Daten in Adobe Analytics momentan untersagt ist. Eine Ausnahme stellen präzise, nach geltendem Recht ordnungsgemäß erfasste Standortdaten dar, die in einigen Rechtssystemen möglicherweise als vertrauliche Daten erachtet werden.

* **Beschriftungen für Datenschutzdaten**: Dient zum Definieren der Felder, die möglicherweise persönliche IDs zur Verwendung in Datenschutzanfragen enthalten oder die im Rahmen einer Datenschutz-Löschanfrage entfernt werden sollen. In einigen Fällen können sich diese Beschriftungen mit den Beschriftungen für Identitätsdaten und vertrauliche Daten überschneiden.

Weitere Informationen zu den Data Governance-Beschriftungen finden Sie unter [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md).

+++

+++ **Wie kann ich überprüfen, ob die Privacy Service-Anforderungen ordnungsgemäß funktionieren, um Daten aus Adobe Analytics zu löschen?**

In der Regel richten Analytics-Kunden einige Test-Report Suites ein, um die Funktionalität zu überprüfen, bevor sie für die allgemeine Öffentlichkeit freigegeben werden. Vorproduktionswebsites oder -apps senden Daten an diese Test-/Dev-/QA-Report Suites, um zu bewerten, wie Dinge funktionieren, wenn der Code veröffentlicht wird, bevor echter Traffic an die Produktions-Report Suites gesendet wird.

Mit einer normalen Konfiguration kann die Verarbeitung von DSGVO-Anfragen jedoch nicht erst an diesen Test-Report Suites getestet werden, bevor sie auf die Produktions-Report Suites angewendet wird. Dies liegt daran, dass eine Datenschutzanfrage automatisch auf alle Report Suites in der Experience Cloud-Organisation angewendet wird, was häufig allen Report Suites für Ihr Unternehmen entspricht.

Es gibt jedoch einige Möglichkeiten, Ihre Datenschutzverarbeitung zu testen, bevor Sie sie auf alle Ihre Report Suites anwenden:

* Eine Option ist die Einrichtung einer separaten Experience Cloud-Organisation, die nur Test-Report Suites enthält. Verwenden Sie dann diese Experience Cloud-Organisation für Ihren Datenschutztest und Ihre normale Experience Cloud-Organisation für die eigentliche Datenschutzverarbeitung.

* Eine weitere Option ist es, den IDs in Ihren Test-Report-Suites andere Namespaces zuzuweisen als in den Produktions-Report-Suites. Sie können beispielsweise jedem Namespace in Ihren Test-Report Suites „qs-“ voranstellen. Wenn Sie Datenschutzanfragen senden, die nur Namespaces mit dem Präfix „qs-“ enthalten, werden diese Anfragen nur im Rahmen Ihrer Test-Report Suites ausgeführt. Wenn Sie die Anfragen später ohne das Präfix senden, werden sie auf Ihre Produktions-Report Suites angewendet. **Dies ist der empfohlene Ansatz, es sei denn, Sie verwenden die visitorId-, AAID-, ECID- oder customVisitorId-Namespaces. Diese Namespaces sind hartcodiert und Sie können keine alternativen Namen für sie in Ihren Test-Report Suites angeben.**

+++

+++ **Was sind meine ersten Schritte bei der Vorbereitung von Adobe Analytics auf den Datenschutz?**

Eine schrittweise Anleitung zur Vorbereitung auf die Datenschutzregeln finden Sie unter [Adobe Analytics-Workflow zum Datenschutz](/help/admin/admin/c-data-governance/an-gdpr-workflow.md).

+++

+++ **Wie sollten Datenverantwortliche über die Einwilligung in Bezug auf die Benutzerinteraktion nachdenken?**

Die DSGVO und der CCPA bieten gute Möglichkeiten, Ihre Strategie und Ihre Vorgehensweisen für das Zustimmungsverwaltung zu überdenken. Dazu gehört die Bestimmung, wann eine Einwilligung erforderlich ist, und das Denken über den Wertvorschlag für den Benutzer. Denken Sie über das Wertversprechen bezüglich des Datenschutzes von Kunden nach. Dies kann auch für Konversionen und die Kundentreue förderlich sein. Der Bereich des Einwilligungsmanagements (z. B. Tools, Standards, Best Practices) entwickelt sich schnell weiter und sollte im Auge behalten werden. Um die Auswirkungen auf die Benutzerinteraktion zu minimieren, sollten die Verantwortlichen sowohl mit Anbietern in diesem Bereich als auch mit ihrem Rechtsbeistand zusammenarbeiten, um sicherzustellen, dass sie die neuen Gesetze und Anleitungen zu Einwilligung und Cookies befolgen. Ein auf Erfahrungen beruhender Datenschutz mithilfe eines markenbezogenen, kontextabhängigen relevanten Erlebnisses, das das Wertversprechen Ihrer Datenerfassung zum Ausdruck bringt, ist eine gute Strategie.

Als Datenverantwortlicher sind Sie dafür verantwortlich, die ausdrückliche Einwilligung von Ihren Datensubjekten einzuholen, bevor Sie Daten über sie erfassen (möglicherweise auch Adobe Analytics-Daten), und eine [Opt-out-Mechanismus](https://www.adobe.com/de/privacy/opt-out.html#customeruse) auf Ihrer Website. Auf diese Weise können sich Ihre betroffenen Personen von der künftigen Adobe Experience Cloud-Datenerfassung abmelden.

+++

+++ **Wie sollten Datenverantwortliche über die Datenaufbewahrung im Hinblick auf den Datenschutz nachdenken?**

Personenbezogene Daten sollten im Allgemeinen nicht länger als notwendig aufbewahrt werden, um den Zweck zu erreichen, für den sie erhoben wurden. Die Allgemeinen Geschäftsbedingungen der Adobe wenden einen standardmäßigen Datenaufbewahrungsplan für 25 Monate an, es sei denn, eine andere Datenaufbewahrungsdauer wird vertraglich vereinbart. Kunden müssen ihre Datenaufbewahrungsrichtlinien festlegen, bevor Adobe eine Datenschutzanfrage verarbeiten kann.

Die aktuelle Datenhaltungsrichtlinie jeder Berichtssuite wird in der neuen Data Governance Admin-Benutzeroberfläche angezeigt. Kunden sollten sich an ihren Kundenbetreuer wenden, wenn sie ihre Datenaufbewahrungsrichtlinien anpassen müssen. Siehe [Häufig gestellte Fragen zur Datenaufbewahrung in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=en).

+++

+++ **Kann ein Kunde die standardmäßige Datenaufbewahrungsdauer verkürzen oder verlängern?**

Kunden können die Löschung ihrer Daten vor Ablauf der 25 Monate anfordern, indem sie die Kundenunterstützung aufrufen. Kunden können die Datenaufbewahrung auch über die 25 Monate hinaus verlängern, indem sie eine Verlängerung erwerben. Verlängerungen sind in Schritten von 1 zusätzlichen Jahr bis zu maximal 8 weiteren Jahren (insgesamt 10 Jahre) möglich. Diese Verlängerungen erfordern aktualisierte Vertragsbedingungen und zusätzliche Gebühren.

+++

+++ **Was sollte ein Datenverantwortlicher bezüglich des Datenschutzes berücksichtigen, wenn persönliche Daten aus Adobe Analytics exportiert werden?**

Wenn ein Kunde Daten mit Adobe Analytics Daten-Feeds aus Analytics in das Data Warehouse seines Unternehmens oder in andere Systeme außerhalb von Adobe exportiert, ist der Kunde (der Datenverantwortliche) dafür verantwortlich, sicherzustellen, dass Löschanfragen auf die Daten angewendet werden. Dies gilt auch für On-Premise-Implementierungen der Adobe-Data Workbench, bei denen ein fortlaufender Adobe Analytics-Daten-Feed die Daten der Data Workbench ausfüllt. Adobe kann Tools bereitstellen, die Ihnen beim Suchen und Löschen von Datensätzen aus bestimmten Daten-Feeds, einschließlich der für Data Workbench verwendeten, helfen. Der Kunde (Datenverantwortliche) ist dennoch dafür verantwortlich, sicherzustellen, dass die Daten in Übereinstimmung mit den eigenen, internen Richtlinien zur Aufbewahrung und Löschung von Daten gelöscht werden.

Beachten Sie auch Fälle, in denen Mitarbeiter Adobe Analytics-Berichte mit personenbezogenen Daten heruntergeladen haben. Diese Berichte müssen möglicherweise aktualisiert oder gelöscht werden, wenn eine datenschutzbezogene Löschanfrage mit einer im Bericht vorhandenen ID empfangen wird. Kunden sollten mit dem Rechtsbeistand ihres eigenen Unternehmens zusammenarbeiten, um Aufbewahrungsfristen sowie Datenschutz- und Sicherheitsanforderungen festzulegen, die auf diese Arten von Dokumenten angewendet werden sollten.

+++

+++ **Einige Daten, die wir nicht sammeln sollten, wurden versehentlich an Adobe Analytics gesendet. Können wir die Datenschutz-API verwenden, um diese Daten zu bereinigen?**

Die [Data Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) wurde bereitgestellt, um Ihnen bei der Erfüllung zeitkritischer Datenschutzanfragen zu helfen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen.

Wir möchten Sie bitten, die Datenschutz-API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden. Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Datenschutz-API für diese Verwendung ungeeignet ist.

Bitte wenden Sie sich an Ihren Kundenbetreuer (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Informationen oder Datenproblemen zu unternehmen.

+++

+++ **Unser Rechtsteam hat festgestellt, dass Werte, die wir seit Jahren in einer Variablen sammeln, nicht mehr mit unserer aktualisierten Datenschutzrichtlinie übereinstimmen. Können wir die Datenschutz-API verwenden, um alle Werte aus dieser Variable zu löschen?**

Die [Data Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) wurde bereitgestellt, um Ihnen bei der Erfüllung zeitkritischer Datenschutzanfragen zu helfen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen. Wir möchten Sie bitten, die Datenschutz-API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Datenschutz-API für diese Verwendung ungeeignet ist.

Bitte wenden Sie sich an Ihren Account Manager (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und die Anstrengungen zur Beseitigung von PII- oder Datenproblemen zu verstärken.

+++

Zusätzliche Datenschutzressourcen:

* [Allgemeine DSGVO-Begriffe](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud-Datenschutz-[Carepaket](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* [Blogpost](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/) zum auf Erfahrungen beruhenden Datenschutz
