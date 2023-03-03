---
description: Häufig gestellte Fragen zur Verwaltung von Adobe Analytics-Daten
title: Häufig gestellte Fragen zu Data Governance
feature: Data Governance
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: 02d0baee99ad2ea5966788f036644d3e3780016e
workflow-type: tm+mt
source-wordcount: '2076'
ht-degree: 97%

---

# Häufig gestellte Fragen

+++ **Wie unterstützt Adobe Analytics Zugriffs- und Löschanfragen für Endbenutzenden (Datensubjekte), die von Kundinnen und Kunden (Datenverantwortlichen) validiert wurden?**

Wenn verschiedene Datenschutzregeln (DSGVO, CCPA) in Kraft treten, unterstützt Adobe Analytics das Verarbeiten von verifizierten Anfragen, die von Datenverantwortlichen an die Datenschutz-API der Experience Cloud gesendet werden, um einen stärker automatisierten Prozess zu ermöglichen. Die Datenschutz-API von Adobe ist dafür konzipiert, die Verarbeitung individueller Rechtsanfragen (z. B. Zugriffs- und Löschanfragen) für die Daten unserer Kundinnen und Kunden zu unterstützen, die in den Adobe Experience Cloud-Lösungen gespeichert sind. Dies ist flexibel und kann entsprechend der Anzahl der Datenzugriffs- und Löschanfragen skaliert werden, die Ihr Unternehmen von Datensubjekten erhält.

Zudem ermöglicht die Datenschutz-API den Kundinnen und Kunden, zu überprüfen, inwiefern die Datenzugriffs- und Löschanfragen erfüllt werden. Weitere Informationen finden Sie in der Dokumentation zur [Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/).

+++

+++ **Wer ist für das Empfangen, Akzeptieren und Erfüllen von Datenschutz-Anfragen von Endbenutzenden zuständig?**

Der oder die Datenverantwortliche ist allein dafür verantwortlich, Anfragen zu empfangen und zu akzeptieren. Der oder die Datenverantwortliche validiert die Identität des Datensubjekts und erfüllt dann die Anfrage. Zu dieser Verantwortung kann gehören, Adobe mit den IDs der betroffenen Personen zu kontaktieren, die mit in Adobe Analytics gespeicherten Daten verknüpft sein können.

Adobe muss als Auftragsverarbeiter den Datenverantwortlichen oder die Datenverantwortliche angemessen dabei unterstützen, verifizierte Anfragen innerhalb einer akzeptablen Zeitspanne zu verarbeiten.

+++

+++ **Wie finden Adobe-Kundinnen und -Kunden (Datenverantwortliche) heraus, welchen IDs Datenschutzanfragen in Adobe Analytics zur Datenschutzverarbeitung zugeordnet sind?**

Die Datenverantwortlichen bestimmen, wie die Identität bei Anfragen von betroffenen Personen aufgelöst wird. Ziehen Sie den Einsatz des Tags zum Abrufen der Datenschutz-ID von Adobe in Erwägung. Ihre Entwicklungs-Teams sparen Zeit, indem sie unser Tag zum Abrufen der Datenschutz-ID verwenden, um Benutzer-IDs (Cookie-IDs) zu erfassen. Sie können dann unsere Datenschutz-API verwenden, um diese Benutzer-IDs zur Verarbeitung von Datenschutzanfragen an die entsprechenden Lösungen in Adobe Experience Cloud zu senden. Die Datenschutz-API kann eine Vielzahl von Benutzer-IDs in mehreren Adobe-Lösungen unterstützen.

Wenn eine betroffene Person eine Anfrage zusammen mit einer Kennzeichnung (benutzerdefinierte Variable – Prop oder eVar) sendet, prüft Adobe Analytics den gesamten gespeicherten Verlauf der Daten, die für die jeweilige Kennzeichnung erfasst wurden. Weitere Informationen zum Konfigurieren von benutzerdefinierten IDs, die in Props oder eVars von Analytics gespeichert sind, finden Sie in der [Analytics-Dokumentation zu Namespaces](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md).

+++

+++ **Wie kann Adobe Analytics Data Governance bei der Verarbeitung von Datenschutzanfragen helfen?**

Data Governance ist ein neues Tool in Adobe Analytics, das Datenverantwortlichen die Möglichkeit bietet, Datenkontrollen und Klassifizierungen auf ihre Analytics-Daten anzuwenden. Dank dieses neuen Tools können Adobe-Kunden die Verarbeitung ihrer Datenschutzanfragen zum Datenzugriff und zur Datenlöschung anpassen. In der Data Governance-Konsole können Administratoren die gewünschten Einstellungen definieren, die auf verschiedene Datenspalten in Adobe Analytics angewendet werden sollen. Nachdem diese Beschriftungen definiert wurden, berücksichtigt und verarbeitet Adobe die nachfolgenden Zugriffs- oder Löschanfragen gemäß den gewünschten Beschriftungseinstellungen des Kunden. Der oder die Datenverantwortliche ist dafür zuständig, diese Kennzeichnungseinstellungen zu überprüfen und sich mit ihren Rechtsvertretern darüber zu beraten.

Das Data Governance-Tool beinhaltet die folgenden Datenkennzeichnungen:

* **Kennzeichnungen für Identitätsdaten**: Werden zum Klassifizieren von Daten verwendet, mit deren Hilfe eine Einzelperson direkt oder in Kombination mit anderen Daten identifiziert werden kann. (None, I1, I2)

* **Kennzeichnungen für vertrauliche Daten**: Werden zum Klassifizieren von Daten verwendet, die unter geltendem Recht als vertraulich definiert werden können. (None, S1, S2) Beachten Sie, dass derzeit die Verwendung vertraulicher Daten in Adobe Analytics generell untersagt ist. Eine Ausnahme stellen präzise, nach geltendem Recht ordnungsgemäß erfasste Standortdaten dar, die in einigen Rechtssystemen möglicherweise als vertrauliche Daten erachtet werden.

* **Kennzeichnungen für Datenschutzdaten**: Werden zum Definieren der Felder verwendet, die möglicherweise personenbezogene, in Datenschutzanfragen verwendete Kennzeichnungen enthalten oder die im Rahmen der Datenschutz-Löschanfrage entfernt werden sollen. In einigen Fällen können sich diese Kennzeichnungen mit den Kennzeichnungen für Identitätsdaten und vertrauliche Daten überschneiden.

Weitere Informationen zu den Data Governance-Beschriftungen finden Sie unter [Datenschutzkennzeichnungen für Analytics-Variablen](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md).

+++

+++ **Wie kann ich überprüfen, ob die Privacy Service-Anfragen ordnungsgemäß funktionieren, um Daten aus Adobe Analytics zu löschen?**

In der Regel richten Kundinnen und Kunden von Analytics einige Report Suites zum Testen ein, um die Funktionalität zu überprüfen, bevor sie Ressourcen der Öffentlichkeit zur Verfügung stellen. Bevor echter Traffic an die Produktions-Report-Suites gesendet wird, senden Staging-Websites und -Apps die Daten an die entsprechenden Test-, Entwicklungs- oder QS-Report-Suites, um zu überprüfen, wie sie nach Veröffentlichung des Codes funktionieren werden.

Mit einer normalen Konfiguration kann die Verarbeitung von DSGVO-Anfragen jedoch nicht erst an diesen Test-Report-Suites getestet werden, bevor sie auf die Produktions-Report-Suites angewendet wird. Grund hierfür ist, dass eine Datenschutzanfrage automatisch auf alle Report Suites in der Experience Cloud-Organisation angewendet wird, was häufig allen Report Suites für Ihr Unternehmen entspricht.

Es gibt jedoch einige Möglichkeiten, wie Sie Ihre Datenschutzverarbeitung vor der Anwendung auf all Ihre Report Suites testen können:

* Eine Option ist die Einrichtung einer separaten Experience Cloud-Organisation, die nur Test-Report Suites enthält. Verwenden Sie dann diese Experience Cloud-Organisation für Ihren Datenschutztest und Ihre normale Experience Cloud-Organisation für die eigentliche Datenschutzverarbeitung.

* Eine weitere Option ist es, den IDs in Ihren Test-Report-Suites andere Namespaces zuzuweisen als in den Produktions-Report-Suites. Sie können beispielsweise jedem Namespace in Ihren Test-Report Suites „qs-“ voranstellen. Wenn Sie Datenschutzanfragen senden, die nur Namespaces mit dem Präfix „qs-“ enthalten, werden diese Anfragen nur im Rahmen Ihrer Test-Report Suites ausgeführt. Wenn Sie die Anfragen später ohne das Präfix senden, werden sie auf Ihre Produktions-Report Suites angewendet. **Dies ist der empfohlene Ansatz, es sei denn, Sie verwenden die Namespaces visitorId, AAID, ECID oder customVisitorId. Diese Namespaces sind hartcodiert, und Sie können keine alternativen Namen für sie in Ihren Test-Report-Suites angeben.**

+++

+++ **Was sind meine ersten Schritte bei der Vorbereitung von Adobe Analytics auf den Datenschutz?**

Eine schrittweise Anleitung zur Vorbereitung auf die Datenschutzregeln finden Sie unter [Adobe Analytics-Workflow zum Datenschutz](/help/admin/admin/c-data-governance/an-gdpr-workflow.md).

+++

+++ **Was sollten die Datenverantwortlichen bei der Einwilligung bezüglich der Benutzerinteraktion beachten?**

DSGVO und CCPA bieten gute Möglichkeiten, Ihre Strategie und Ihre Vorgehensweisen für die Einverständnisverwaltung zu überdenken. Dazu gehört, zu bestimmen, wann eine Einwilligung erforderlich ist, und über das Wertversprechen für die Benutzenden nachzudenken. Denken Sie über das Wertversprechen bezüglich des Datenschutzes von Kundinnen und Kunden nach. Dies kann auch für Konversionen und die Kundentreue förderlich sein. Der Bereich der Einverständnisverwaltung (z. B. Tools, Standards, Best Practices) entwickelt sich schnell weiter und sollte im Auge behalten werden. Um die Auswirkungen auf die Benutzerinteraktion zu minimieren, sollten die Verantwortlichen sowohl mit Anbietern in diesem Bereich als auch mit ihrem Rechtsbeistand zusammenarbeiten, um sicherzustellen, dass sie die neuen Gesetze und Richtlinien zu Einverständnis und Cookies befolgen. Ein auf Erfahrungen beruhender Datenschutz mithilfe eines markenbezogenen, kontextabhängigen relevanten Erlebnisses, das das Wertversprechen Ihrer Datenerfassung zum Ausdruck bringt, ist eine gute Strategie.

Als Datenverantwortliche sind Sie dafür zuständig, die ausdrückliche Einwilligung von den betroffenen Personen einzuholen, bevor Sie Daten über sie erfassen (möglicherweise auch Adobe Analytics-Daten). Zudem liegt es in Ihrer Verantwortung, auf Ihrer Website einen [Opt-out-Mechanismus](https://www.adobe.com/de/privacy/opt-out.html#customeruse) zu implementieren. Über einen solchen Mechanismus können betroffene Personen zu einem späteren Zeitpunkt der Datenerfassung durch Adobe Experience Cloud widersprechen.

+++

+++ **Was sollten die Datenverantwortlichen bei der Datenaufbewahrung bezüglich des Datenschutzes beachten?**

Personenbezogene Daten sollten im Allgemeinen nicht länger aufbewahrt werden, als notwendig ist, um den Zweck zu erfüllen, für den sie erfasst wurden. Die Allgemeinen Geschäftsbedingungen von Adobe sehen eine standardmäßige Datenaufbewahrung von 25 Monaten vor, es sei denn, eine andere Datenaufbewahrungsdauer wird vertraglich vereinbart. Kundinnen und Kunden müssen ihre Datenspeicherungsrichtlinien festlegen, bevor Adobe Datenschutzanfragen bearbeiten kann.

Die aktuelle Datenhaltungsrichtlinie jeder Report Suite wird in der neuen Data Governance Admin-Benutzeroberfläche angezeigt. Kundinnen und Kunden sollten sich an den Adobe-Support wenden, wenn sie ihre Richtlinien zur Datenspeicherung anpassen möchten. Lesen Sie die Informationen unter [Häufig gestellte Fragen zur Datenaufbewahrung in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=de).

+++

+++ **Kann kundenseitig der Standardzeitraum für die Datenaufbewahrung reduziert oder verlängert werden?**

Kundinnen und Kunden können mit der Kundenunterstützung in Kontakt treten und veranlassen, dass ihre Daten vor Ablauf der Frist von 25 Monaten gelöscht werden. Kunden können die Datenaufbewahrung auch über die 25 Monate hinaus verlängern, indem sie eine Verlängerung erwerben. Verlängerungen sind in Schritten von 1 zusätzlichen Jahr bis zu maximal 8 zusätzlichen Jahren (für insgesamt 10 Jahre) möglich. Für derartige Verlängerungen müssen die Vertragsbedingungen aktualisiert werden, und es können Zusatzgebühren anfallen.

+++

+++ **Was sollten Datenverantwortliche bezüglich des Datenschutzes berücksichtigen, wenn persönliche Daten aus Adobe Analytics exportiert werden?**

Wenn Kundinnen oder Kunden Daten mit Adobe Analytics-Daten-Feeds aus Analytics in das Data Warehouse ihres Unternehmens oder in andere Systeme außerhalb von Adobe exportieren, sind sie (d. h. die Datenverantwortlichen) dafür verantwortlich sicherzustellen, dass Löschanfragen auf die Daten angewendet werden. Dies gilt auch für On-Premise-Implementierungen von Adobe Data Workbench, bei denen die Data Workbench-Daten über einen fortlaufenden Adobe Analytics-Daten-Feed gefüllt werden. Adobe kann Tools bereitstellen, die Ihnen beim Suchen und Löschen von Datensätzen aus bestimmten Daten-Feeds, einschließlich der für Data Workbench verwendeten, helfen. Die Kundinnen und Kunden (Datenverantwortlichen) sind dennoch dafür verantwortlich sicherzustellen, dass die Daten in Übereinstimmung mit den eigenen, internen Richtlinien zur Aufbewahrung und Löschung von Daten gelöscht werden.

Beachten Sie auch die Fälle, in denen Mitarbeitende Adobe Analytics-Berichte mit persönlichen Daten heruntergeladen haben. Diese Berichte müssen möglicherweise aktualisiert oder gelöscht werden, wenn eine datenschutzbezogene Löschanfrage mit einer ID empfangen wird, die im Bericht vorhanden ist. Kundinnen und Kunden sollten mit der Rechtsabteilung ihres Unternehmens zusammenarbeiten, um die Aufbewahrungszeiträume und die Datenschutz- und Sicherheitsanforderungen zu bestimmen, die auf derartige Dokumente angewendet werden sollen.

+++

+++ **Einige Daten, die wir nicht sammeln sollten, wurden versehentlich an Adobe Analytics gesendet. Können wir die Datenschutz-API verwenden, um diese Daten zu bereinigen?**

Die [Data Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) soll Ihnen dabei helfen, zeitkritische Datenschutzanfragen zu erfüllen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, anderen Kundinnen und Kunden von Adobe eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität zu bieten.

Wir möchten Sie bitten, die Datenschutz-API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden. Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Datenschutz-API für diese Verwendung ungeeignet ist.

Wenden Sie sich an Ihr Kundenbetreuungsteam, um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Daten oder Datenproblemen zu unternehmen.

+++

+++ **Unser Rechts-Team hat festgestellt, dass Werte, die wir seit Jahren in einer Variablen sammeln, nicht mehr unserer aktualisierten Datenschutzrichtlinie entsprechen. Können wir die Datenschutz-API verwenden, um alle Werte aus dieser Variable zu löschen?**

Die [Data Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) soll Ihnen dabei helfen, zeitkritische Datenschutzanfragen zu erfüllen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, anderen Kundinnen und Kunden von Adobe eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität zu bieten. Wir möchten Sie bitten, die Datenschutz-API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Datenschutz-API für diese Verwendung ungeeignet ist.

Wenden Sie sich an Ihr Kundenbetreuungsteam, um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Daten oder Datenproblemen zu unternehmen.

+++

Zusätzliche Datenschutzressourcen:

* [Allgemeine DSGVO-Begriffe](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud-Datenschutz-[Carepaket](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* [Blogpost](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/) zum auf Erfahrungen beruhenden Datenschutz
