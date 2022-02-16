---
description: Erstellen Sie einen einfachen Container für die Datenerfassung in Adobe Analytics
title: Erstellen einer Report Suite
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 66%

---

# Erstellen einer Report Suite

Bei einer Report Suite handelt es sich um einen Datenspeicher, mit dem Adobe Analytics Berichte abruft. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Auch wenn in der Vergangenheit separate Report Suites wichtig waren, hat sich eine einzelne Report Suite als vorteilhafter erwiesen. Die Einführung von [Virtual Report Suites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=en#virtual-report-suites) und die Berichtszeitverarbeitung ermöglichen es Administratoren, eigene Datenuntergruppen zu erstellen, sodass sie flexibel sowohl globale als auch Site-spezifische Daten abrufen können.

Dieser Artikel richtet sich an Administratoren auf Systemebene oder Adobe Analytics-Administratoren, die sich auf die Datenerfassung vorbereiten.

## Voraussetzungen

[Erste Administratorhandbuch für Adobe Analytics](/help/admin/admin-console/first-admin-guide.md): Stellen Sie sicher, dass Ihnen ein Administrator auf Systemebene über die Experience Cloud-Admin Console Zugriff auf Adobe Analytics gewährt hat.

## Erstellen einer Report Suite {#create-report-suite}

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Klicken Sie auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Report Suite]**.
1. Wenn Sie die Einstellungen einer Report Suite kopieren möchten, wählen Sie in der Vorlagenliste eine vordefinierte Vorlage oder eine vorhandene Report Suite als [Vorlage](/help/admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md) aus.

   >[!NOTE]
   >
   >Es können nur Einstellungen und keine Daten kopiert werden. Wenn die Kundenunterstützung die Einstellungen kopiert, müssen Sie den Haftungsausschluss der Kundenunterstützung bezüglich der involvierten Risiken schriftlich bestätigen. Weitere Informationen finden Sie unter [Aus einer Quell-Report Suite nicht kopierte Einstellungen](/help/admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md).

1. Füllen Sie die unter [Neue Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md) beschriebenen Felder aus.
1. Klicken Sie auf **[!UICONTROL Report Suite erstellen]**.

Eine Report Suite-ID hat eine maximale Länge von 40 Byte. Ein benutzerfreundlicher Name einer Report Suite hat eine maximale Länge von 255 Byte.

## Fehlerbehebung

**Nach der Anmeldung bei Experience Cloud ist das Analytics-Symbol grau ausgeblendet.**

Das bedeutet, dass Ihrem Konto nicht die richtigen Berechtigungen für Analytics erteilt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrer Organisation zusammen, um sicherzustellen, dass Sie zu einem Profil gehören, das über ausreichende Zugriffsberechtigungen für Adobe Analytics verfügt.

**Nach der Anmeldung bei Adobe Analytics fehlt das Popup- und Dropdown-Menü „Willkommen bei Adobe Analytics“.**

Stellen Sie sicher, dass Sie sich über die [Experience Cloud](https://experience.adobe.com)und nicht über my.omniture.com. Für Benutzer, die sich über my.omniture.com anmelden, steht der Assistent zur Report Suite-Einrichtung nicht zur Verfügung.

## Nächste Schritte

[Erstellen einer Adobe Analytics-Tag-Eigenschaft ](/help/implement/launch/create-analytics-property.md): Erstellen eines Bereichs zur Verwaltung Ihrer Analytics-Implementierung
