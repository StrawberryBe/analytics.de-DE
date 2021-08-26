---
description: Erläutert die Schritte, mit denen Sie in Ihrer Adobe Analytics-Implementierung die Zugriffs- und Löschrechte der betroffenen Personen für den Datenschutz unterstützen.
title: Workflow zum Datenschutz
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 7cb2489c2deaf8e75c71589895314067a010caf8
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 58%

---

# Workflow zum Datenschutz

Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die Datenschutz-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

1. **Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest.** Eine Richtlinie zur Datenaufbewahrung ist erforderlich, damit die Adobe Datenschutzdatenzugriffs-/Löschanfragen bearbeiten kann.  Weitere Informationen finden Sie in den [FAQ zur Datenaufbewahrung](/help/technotes/data-retention.md).
1. **Machen Sie sich mit den DULE/Datenschutzbeschriftungen, Adobe Analytics-IDs, Namespaces und der ID-Erweiterung vertraut.** Siehe  [Datenschutzbezeichnungen für Analytics-](/help/admin/c-data-governance/gdpr-labels.md) Variablen und Best Practices  [für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md).
1. **Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.** Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Überprüfen Sie auch die Beschriftung, wenn neue Lösungsintegrationen aktiviert sind, da sie neue Variablen verfügbar machen können, für die möglicherweise eine Beschriftung erforderlich ist. Eine erneute Implementierung Ihrer mobilen Apps oder Websites kann die Art und Weise ändern, wie vorhandene Variablen verwendet werden. Dies kann auch Aktualisierungen der Beschriftungen erfordern. Siehe [Report Suite-Daten beschriften](/help/admin/c-data-governance/gdpr-setup-reportsuite.md).
1. **Stellen Sie eine Verbindung zur Adobe-Datenschutz-API her und reichen Sie Zugriffs- und Löschanfragen ein.** Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf der [Data Privacy API von Adobe Experience Cloud einreichen](https://www.adobe.io/apis/experienceplatform/gdpr.html). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/c-data-governance/gdpr-analytics-ids.md)).
1. **Sehen Sie sich die Datenschutzeinstellungen Ihrer Report Suite an und verwalten Sie sie.** Siehe  [Data-Governance-Einstellungen von Report Suites anzeigen](/help/admin/c-data-governance/gdpr-view-settings.md).
