---
title: VISTA-Regeln in Adobe Analytics
description: Erfahren Sie mehr über VISTA-Regeln und ihre Funktionen.
exl-id: fab2acc3-b037-48f9-bb20-625ccb75b4cc
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: ht
source-wordcount: '266'
ht-degree: 100%

---

# VISTA-Regeln in Adobe Analytics

VISTA-Regeln sind eine alternative Form der benutzerdefinierten Datenänderung, die Sie zwischen der Datenerfassung und -verarbeitung anwenden können. Weitere Informationen zu der Phase in der Daten-Pipeline, für die die VISTA-Regeln angewendet werden, finden Sie unter [Verarbeitungsreihenfolge](processing-order.md). VISTA-Regeln wirken sich nur auf aktuelle Daten zum Zeitpunkt ihrer Erfassung aus. Vorhandene Daten werden durch sie nicht geändert.

Typische Anwendungsfälle von VISTA-Regeln sind etwa:

* Kopieren eines Analytics-Treffers zwischen Report Suites mit möglicher Datenänderung in der kopierten Report Suite
* Benutzerdefinierter IP-Ausschluss, der über die möglichen Anwendungsfälle von [Nach IP ausschließen](/help/admin/admin/exclude-ip.md) hinausgeht
* Bedingte oder globale Änderung eines Variablenwerts
* Duplizieren von Variablenwerten in andere Variablen
* Hochladen von Dateien auf eine Adobe-FTP-Site mit möglichen Auswirkungen auf Variablenwerte

Viele Anwendungsfälle für VISTA-Regeln werden bereits von [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md), [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md), [Virtual Report Suites](/help/components/vrs/vrs-about.md) oder einfach durch eine Aktualisierung Ihrer Adobe Analytics-Implementierung abgedeckt. Adobe empfiehlt VISTA-Regeln nur als letztes Mittel.

>[!IMPORTANT]
>
>VISTA-Regeln erfordern eine entgeltliche Vereinbarung zwischen Ihrem Unternehmen und Adobe Professional Services. Wenden Sie sich an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer, wenn Sie eine VISTA-Regel erstellen oder aktualisieren möchten.

## Erstellen einer VISTA-Regel

Sie müssen mit Adobe Professional Services zusammenarbeiten, um eine VISTA-Regel zu erstellen. Wenden Sie sich an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer, wenn Sie eine VISTA-Regel erstellen möchten.

## Anzeigen vorhandener VISTA-Regeln.

Adobe bietet keine Benutzeroberfläche zum Anzeigen vorhandener VISTA-Regeln. Wenden Sie sich mit der gewünschten Report Suite an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer oder die Adobe-Kundenunterstützung, um eine Liste der vorhandenen VISTA-Regeln zu erhalten.
