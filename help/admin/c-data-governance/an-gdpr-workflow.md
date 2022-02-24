---
description: Erläutert die Schritte, mit denen Sie in Ihrer Adobe Analytics-Implementierung die Zugriffs- und Löschrechte der betroffenen Personen für den Datenschutz unterstützen.
title: Workflow zum Datenschutz
feature: Privacy
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: df16d37de742d96f66fd74d7a7b47729f0454fd5
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 87%

---

# Workflow zum Datenschutz

Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die Datenschutz-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

1. **Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest.** Eine Richtlinie zur Datenaufbewahrung ist erforderlich, damit Adobe Zugriffs-/Löschanfragen für Datenschutzdaten bearbeiten kann. Weitere Informationen finden Sie unter [Häufig gestellte Fragen zur Datenaufbewahrung](/help/technotes/data-retention.md).
1. **Machen Sie sich mit den DULE/Datenschutzbeschriftungen, Adobe Analytics-IDs, Namespaces und der ID-Erweiterung vertraut.** Siehe [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/c-data-governance/gdpr-labels.md) und [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md).
1. **Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.** Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie sollten die Beschriftung auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen aufzeigen können, für die möglicherweise eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. Siehe [Beschriften von Report Suite-Daten](/help/admin/c-data-governance/gdpr-setup-reportsuite.md).
1. **Stellen Sie eine Verbindung zur Adobe-Datenschutz-API her und reichen Sie Zugriffs- und Löschanfragen ein.** Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf von [Adobe Experience Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=en). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md)).
1. **Sehen Sie sich die Datenschutzeinstellungen Ihrer Report Suite an und verwalten Sie sie.** Siehe [Anzeigen der Data Governance-Einstellungen einer Report Suite](/help/admin/c-data-governance/gdpr-view-settings.md).
