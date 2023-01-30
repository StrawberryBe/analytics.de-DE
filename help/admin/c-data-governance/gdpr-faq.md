---
description: Häufig gestellte Fragen zur Verwaltung von Adobe Analytics-Daten
title: Häufig gestellte Fragen zu Data Governance
feature: Data Governance
exl-id: 57399c1b-cf08-405b-8c1b-9d23e4c38716
source-git-commit: 82c69131fcc5a22795e44ed97246240aec31f4d9
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 88%

---

# Häufig gestellte Fragen

+++ **Wie unterstützt Adobe Analytics Zugriffs- und Löschanfragen für Endbenutzer (Datensubjekte), die von Kunden (Datenverantwortlichen) validiert wurden?**

Wenn verschiedene Datenschutzregeln (DSGVO, CCPA) in Kraft treten, unterstützt Adobe Analytics die Verarbeitung verifizierter Anfragen, die von Datenverantwortlichen an die Experience Cloud Data Privacy API gesendet werden, um einen stärker automatisierten Prozess zu ermöglichen. Die Datenschutz-API von Adobe ist dafür konzipiert, die Verarbeitung individueller Rechtsanfragen (z. B. Zugriffs- und Löschanfragen) für die Daten unserer Kunden zu unterstützen, die in den Adobe Experience Cloud-Lösungen gespeichert sind. Sie ist flexibel und wird entsprechend der Anzahl der Datenzugriffs- und Löschanfragen skaliert, die Ihr Unternehmen von Datensubjekten erhält.

Zudem ermöglicht die Datenschutz-API dem Kunden zu überprüfen, inwiefern die Datenzugriffs- und Löschanfragen erfüllt werden. Weitere Informationen finden Sie in der [](https://developer.adobe.com/experience-platform-apis/references/privacy-service/)Dokumentation zur Datenschutz-API.

+++

+++ **Wer ist für das Empfangen, Akzeptieren und Erfüllen von Datenschutz-Anfragen von Endbenutzern zuständig?**

Der Datenverantwortliche (d. h. der Adobe-Kunde) ist allein dafür verantwortlich, den Datensubjekten im Rahmen einer Datenschutzanfrage personenbezogene Daten zur Verfügung zu stellen. Zudem ist der Datenverantwortliche allein dafür zuständig, Anfragen zu empfangen und zu akzeptieren, die Identität des Datensubjekts zu validieren und anschließend die Anfrage zu erfüllen. Dies kann auch das Kontaktieren von Adobe mit den IDs der Datensubjekte umfassen, die den in Adobe Analytics gespeicherten Daten möglicherweise zugeordnet sind.

Adobe muss als Auftragsverarbeiter den Datenverantwortlichen angemessen dabei unterstützen, verifizierte Anfragen innerhalb einer akzeptablen Zeitspanne zu verarbeiten.

+++

+++ **Wie finden Adobe-Kunden (Datenverantwortliche) heraus, welchen IDs Datenschutzanfragen in Adobe Analytics zur Datenschutzverarbeitung zugeordnet sind?**

Die Datenverantwortlichen bestimmen, wie die Identität für Anfragen von Datensubjekten aufgelöst wird. Ziehen Sie die Bereitstellung des Datenschutz-ID-Abruftags von Adobe in Erwägung. Durch die Verwendung unseres Datenschutz-ID-Abruftags zum Erfassen der Benutzer-IDs (Cookie-IDs) und das anschließende Senden dieser IDs per Datenschutz-API an die relevanten Lösungen in der Adobe Experience Cloud zur Datenschutz-Anfragenverarbeitung sparen Ihren Entwicklungsteams Zeit. Die Datenschutz-API kann eine Vielzahl von Benutzer-IDs in mehreren Adobe-Lösungen unterstützen.

Wenn ein Datensubjekt eine Anfrage zusammen mit einer Kennzeichnung (benutzerdefinierte Variable – Prop oder eVar) sendet, prüft Adobe Analytics den gesamten gespeicherten Verlauf der Daten, die für die jeweilige Kennzeichnung erfasst wurden. Weitere Informationen zum Konfigurieren von benutzerdefinierten IDs, die in Props oder eVars von Analytics gespeichert sind, finden Sie im Abschnitt [Analytics-Dokumentation zu Namespaces](/help/admin/c-data-governance/data-labeling/gdpr-namespaces.md).

+++

+++ **Wie kann Adobe Analytics Data Governance bei der Verarbeitung von Datenschutzanfragen helfen?**

Data Governance ist ein neues Tool in Adobe Analytics, das Datenverantwortlichen die Möglichkeit bietet, Datenkontrollen und Klassifizierungen auf ihre Analytics-Daten anzuwenden. Dank dieses neuen Tools können Adobe-Kunden die Verarbeitung ihrer Datenschutzanfragen zum Datenzugriff und zur Datenlöschung anpassen. In der Data Governance-Konsole können Administratoren die gewünschten Einstellungen definieren, die auf verschiedene Datenspalten in Adobe Analytics angewendet werden sollen. Nachdem diese Beschriftungen definiert wurden, berücksichtigt und verarbeitet Adobe die nachfolgenden Zugriffs- oder Löschanfragen gemäß den gewünschten Beschriftungseinstellungen des Kunden. Der Datenverantwortliche ist dafür zuständig, diese Beschriftungseinstellungen zu überprüfen und sich mit den gesetzlichen Vertretern darüber zu beraten. Adobe Analytics empfiehlt Kunden, die Datenkennzeichnung vor dem Inkrafttreten der DSGVO am 25. Mai 2018 korrekt einzurichten, um die Fertigstellung von Anfragen mithilfe der Datenschutz-API anzupassen.

Das Data Governance-Tool beinhaltet die folgenden Datenbeschriftungen:

* Beschriftungen für Identitätsdaten:  Werden zum Klassifizieren von Daten verwendet, mit deren Hilfe eine Einzelperson direkt oder in Kombination mit anderen Daten identifiziert werden kann. (None/I1/I2)

* Beschriftungen für vertrauliche Daten:  Werden zum Klassifizieren von Daten verwendet, die unter geltendem Recht als vertraulich definiert werden können. (None, S1, S2) Beachten Sie, dass die Verwendung vertraulicher Daten in Adobe Analytics momentan untersagt ist. Eine Ausnahme stellen präzise, nach geltendem Recht ordnungsgemäß erfasste Standortdaten dar, die in einigen Rechtssystemen möglicherweise als vertrauliche Daten erachtet werden.

* Beschriftungen von Datenschutzdaten:  Werden zum Definieren der Felder verwendet, die möglicherweise persönliche, in Datenschutzanfragen verwendete Kennzeichnungen enthalten oder die im Rahmen der Datenschutz-Löschanfrage entfernt werden sollen. In einigen Fällen können sich diese Beschriftungen mit den Beschriftungen für Identitätsdaten und vertrauliche Daten überschneiden.

Weitere Informationen zu den Data Governance-Beschriftungen finden Sie unter [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/c-data-governance/data-labeling/gdpr-labels.md).

+++

+++ **Was sind meine ersten Schritte bei der Vorbereitung von Adobe Analytics auf den Datenschutz?**

Eine schrittweise Anleitung zur Vorbereitung auf die Datenschutzregeln finden Sie unter [Adobe Analytics-Workflow zum Datenschutz](/help/admin/c-data-governance/an-gdpr-workflow.md).

+++

+++ **Was sollten die Datenverantwortlichen bei der der Einwilligung bezüglich der Benutzerinteraktion beachten?**

Die DSGVO und der CCPA bieten eine gute Gelegenheit, die Managementstrategie bezüglich der Einwilligung zu überdenken. Dazu gehört neben der Festlegung, wann eine Einwilligung nötig ist, auch das Wertversprechen für den Benutzer. Denken Sie über das Wertversprechen bezüglich des Datenschutzes von Kunden nach. Dies kann auch für Konversionen und die Kundentreue förderlich sein.  Der Bereich des Einwilligungsmanagements (z. B. Tools, Standards, Best Practices) entwickelt sich schnell weiter und sollte im Auge behalten werden. Um den Einfluss auf die Benutzerinteraktion zu minimieren, sollten die Datenverantwortlichen in diesem Bereich mit den Lieferanten und ihren Beratern zusammenarbeiten und die kommenden EU-Gesetze und Auflagen bezüglich Einwilligung und Cookies befolgen. Ein auf Erfahrungen beruhender Datenschutz mithilfe eines markenbezogenen, kontextabhängigen relevanten Erlebnisses, das das Wertversprechen Ihrer Datenerfassung zum Ausdruck bringt, ist eine gute Strategie.

Als Datenverantwortlicher sind Sie dafür zuständig, die ausdrückliche Einwilligung von den betroffenen Personen einzuholen, bevor Sie Daten über sie erfassen (möglicherweise auch Adobe Analytics-Daten). Zudem liegt es in Ihrer Verantwortung, auf Ihrer Website einen [Abmeldemechanismus](https://www.adobe.com/de/privacy/opt-out.html#customeruse) zu implementieren. Über einen solchen Mechanismus können Datensubjekte zu einem späteren Zeitpunkt der Datenerfassung durch Adobe Experience Cloud widersprechen.

+++

+++ **Was sollten die Datenverantwortlichen bei der Datenaufbewahrung bezüglich des Datenschutzes beachten?**

Datenschutz sieht generell vor, dass persönliche Daten nicht länger als nötig aufbewahrt werden, um den Zweck zu erfüllen, für den sie erfasst wurden.  Wie Adobe in der Kundenkommunikation im Februar detailliert mitgeteilt hat, werden wir für die meisten Kunden einen 25-monatigen Datenaufbewahrungsplan anwenden, sofern keine anderen Vereinbarungen getroffen wurden (gemäß Kundenbenachrichtigung und -autorisierung). Kunden müssen ihre Datenspeicherungsrichtlinien festlegen, bevor Adobe Datenschutzanfragen bearbeiten kann.

Adobe Analytics fordert von den Kunden die Festlegung der Datenaufbewahrung für die Verarbeitung ihrer Datenschutzanfragen. Die aktuelle Datenhaltungsrichtlinie jeder Berichtssuite wird in der neuen Data Governance Admin-Benutzeroberfläche angezeigt. Kunden sollten sich an ihren Adobe-Support-Mitarbeiter wenden, wenn sie ihre Richtlinien zur Datenaufbewahrung anpassen möchten. Siehe [Häufig gestellte Fragen zur Datenaufbewahrung in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=en).

+++

+++ **Kann ein Kunde die Standardzeitspanne für die Datenaufbewahrung reduzieren oder verlängern?**

Kunden können beim Kundendienst anrufen und veranlassen, dass ihre Daten vor Ablauf der 25 Monate gelöscht werden. Kunden können die Datenaufbewahrung über die 25 Monate hinaus verlängern, indem sie eine Verlängerung erwerben. Verlängerungen sind in Schritten von 1 (einem) zusätzlichen Jahr bis zu maximal 8 (acht) zusätzlichen Jahren (für insgesamt 10 Jahre) möglich. Für derartige Verlängerungen müssen möglicherweise die Vertragsbedingungen aktualisiert werden, und es können Zusatzgebühren anfallen.

+++

+++ **Was sollte ein Datenverantwortlicher bezüglich des Datenschutzes berücksichtigen, wenn persönliche Daten aus Adobe Analytics exportiert werden?**

Wenn ein Kunde Daten mit Adobe Analytics Daten-Feeds aus Analytics in das Data Warehouse seines Unternehmens oder in andere Systeme außerhalb von Adobe exportiert, ist der Kunde (der Datenverantwortliche) dafür verantwortlich, sicherzustellen, dass Löschanfragen auf die Daten angewendet werden. Dies gilt auch für On-Premise-Implementierungen der Adobe-Data Workbench, bei denen ein fortlaufender Adobe Analytics-Daten-Feed die Daten der Data Workbench ausfüllt. Adobe kann Tools bereitstellen, die Ihnen beim Suchen und Löschen von Datensätzen aus bestimmten Daten-Feeds, einschließlich der für Data Workbench verwendeten, helfen. Der Kunde (Datenverantwortliche) ist dennoch dafür verantwortlich, sicherzustellen, dass die Daten in Übereinstimmung mit den eigenen, internen Richtlinien zur Aufbewahrung und Löschung von Daten gelöscht werden.

Beachten Sie auch die Fälle, in denen Mitarbeiter Adobe Analytics-Berichte mit persönlichen Daten heruntergeladen haben. Diese Berichte müssen möglicherweise aktualisiert oder gelöscht werden, wenn eine datenschutzbezogene Löschanfrage mit einer ID empfangen wird, die im Bericht vorhanden ist. Kunden sollten mit dem Rechtsbeistand Ihres Unternehmens zusammenarbeiten, um die Aufbewahrungszeiträume und die Datenschutz- und Sicherheitsanforderungen zu bestimmen, die auf derartige Dokumente angewendet werden sollen.

+++

+++ **Einige Daten, die wir nicht sammeln sollten, wurden versehentlich an Adobe Analytics gesendet. Können wir die Datenschutz-API verwenden, um diese Daten zu bereinigen?**

Die [Data Privacy Service-API](https://developer.adobe.com/experience-platform-apis/references/privacy-service/) wurde bereitgestellt, um Ihnen bei der Erfüllung zeitkritischer Datenschutzanfragen zu helfen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen. Wir möchten Sie bitten, die Datenschutz-API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden. Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Datenschutz-API für diese Verwendung ungeeignet ist.

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
