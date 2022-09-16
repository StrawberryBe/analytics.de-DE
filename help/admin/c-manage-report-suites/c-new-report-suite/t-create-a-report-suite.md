---
description: Erstellen eines einfachen Containers für die Datenerfassung in Adobe Analytics
title: Erstellen einer Report Suite
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
source-git-commit: f4b495b11bcbd55bc8448f2c9c09268547fb9750
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 95%

---

# Erstellen einer Report Suite

Bei einer Report Suite handelt es sich um einen Datenspeicher, mit dem Adobe Analytics Berichte abruft. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Auch wenn in der Vergangenheit separate Report Suites wichtig waren, hat sich eine einzelne Report Suite als vorteilhafter erwiesen. Die Einführung von [Virtual Report Suites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=de#virtual-report-suites) und die Verarbeitung von Berichtszeiten ermöglicht es Administratoren, eigene Untergruppen von Daten zu erstellen, was die Flexibilität bietet, sowohl globale als auch Site-spezifische Daten zu erhalten.

Dieser Artikel wurde für Administratoren oder Adobe Analytics-Administratoren auf Systemebene zur Vorbereitung auf die Datenerfassung erstellt.

## Voraussetzungen

[Adobe Analytics-Handbuch für erste Administratoren](/help/admin/admin-console/first-admin-guide.md): Vergewissern Sie sich, dass Ihnen ein Systemadministrator über die Admin Console von Experience Cloud Zugriff auf Adobe Analytics gewährt hat.

## Erstellen einer Report Suite {#create-report-suite}

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Klicken Sie auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Report Suite]**.
1. Wählen Sie entweder eine vordefinierte Vorlage oder eine vorhandene Report Suite aus, die als [template](../c-report-suite-templates/report-suite-templates.md).

   >[!NOTE]
   >
   >Es können nur Einstellungen und keine Daten kopiert werden. Wenn die Kundenunterstützung die Einstellungen kopiert, müssen Sie den Haftungsausschluss der Kundenunterstützung bezüglich der involvierten Risiken schriftlich bestätigen. Weitere Informationen finden Sie unter [Aus einer Quell-Report Suite nicht kopierte Einstellungen](/help/admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md).

1. Füllen Sie die unter [Neue Report Suite](../c-new-report-suite/new-report-suite.md) beschriebenen Felder aus.
1. Klicken Sie auf **[!UICONTROL Report Suite erstellen]**.

Eine Report Suite-ID hat eine maximale Länge von 40 Byte. Ein benutzerfreundlicher Name einer Report Suite hat eine maximale Länge von 255 Byte.

## Fehlerbehebung

**Nach der Anmeldung bei Experience Cloud ist das Analytics-Symbol grau ausgeblendet.**

Das bedeutet, dass Ihrem Konto nicht die richtigen Berechtigungen für Analytics erteilt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrer Organisation zusammen, um sicherzustellen, dass Sie zu einem Profil gehören, das über ausreichende Zugriffsberechtigungen für Adobe Analytics verfügt.

## Nächste Schritte

[Erstellen einer Adobe Analytics-Tag-Eigenschaft](/help/implement/launch/create-analytics-property.md): Erstellen eines Bereichs zur Verwaltung Ihrer Analytics-Implementierung.
