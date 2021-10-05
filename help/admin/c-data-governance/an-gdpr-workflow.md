---
description: Erläutert die Schritte, mit denen Sie in Ihrer Adobe Analytics-Implementierung die Zugriffs- und Löschrechte der betroffenen Personen für den Datenschutz unterstützen.
title: Workflow zum Datenschutz
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 7cb2489c2deaf8e75c71589895314067a010caf8
workflow-type: ht
source-wordcount: '279'
ht-degree: 100%

---

# Workflow zum Datenschutz

Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die Datenschutz-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

1. **Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest.** Eine Richtlinie zur Datenaufbewahrung ist erforderlich, damit Adobe Zugriffs-/Löschanfragen für Datenschutzdaten bearbeiten kann. Weitere Informationen finden Sie unter [Häufig gestellte Fragen zur Datenaufbewahrung](/help/technotes/data-retention.md).
1. **Machen Sie sich mit den DULE/Datenschutzbeschriftungen, Adobe Analytics-IDs, Namespaces und der ID-Erweiterung vertraut.** Siehe [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/c-data-governance/gdpr-labels.md) und [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md).
1. **Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.** Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie sollten die Beschriftung auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen aufzeigen können, für die möglicherweise eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. Siehe [Beschriften von Report Suite-Daten](/help/admin/c-data-governance/gdpr-setup-reportsuite.md).
1. **Stellen Sie eine Verbindung zur Adobe-Datenschutz-API her und reichen Sie Zugriffs- und Löschanfragen ein.** Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf der [Data Privacy API von Adobe Experience Cloud einreichen](https://www.adobe.io/apis/experienceplatform/gdpr.html). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md)).
1. **Sehen Sie sich die Datenschutzeinstellungen Ihrer Report Suite an und verwalten Sie sie.** Siehe [Anzeigen der Data Governance-Einstellungen einer Report Suite](/help/admin/c-data-governance/gdpr-view-settings.md).
