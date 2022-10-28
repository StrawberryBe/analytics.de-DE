---
title: VISTA-Regeln in Adobe Analytics
description: Erfahren Sie mehr über VISTA-Regeln und ihre Funktionen.
source-git-commit: 1e2284fd4a62816b27b33a91f3bee2575a852107
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# VISTA-Regeln in Adobe Analytics

VISTA-Regeln sind eine alternative Form der benutzerdefinierten Datenänderung, die Sie zwischen der Datenerfassung und -verarbeitung anwenden können. Siehe [Verarbeitungsreihenfolge](processing-order.md) für weitere Informationen zur genauen Phase in der Datenpipeline, für die VISTA-Regeln gelten. VISTA-Regeln wirken sich nur auf aktuelle Daten aus, da sie erfasst werden. vorhandene Daten werden dadurch nicht geändert.

Einige gängige Anwendungsfälle von VISTA-Regeln sind:

* Kopieren Sie einen Analytics-Treffer von einer Report Suite in eine andere und ändern Sie optional Daten in die kopierte Report Suite.
* Benutzerdefinierter IP-Ausschluss, der die von [Nach IP ausschließen](/help/admin/admin/exclude-ip.md)
* Bedingte oder globale Änderung eines Variablenwerts
* Variablenwerte in andere Variablen duplizieren
* Hochladen von Dateien auf eine Adoben-FTP-Site, die sich auf Variablenwerte auswirken kann

Viele Anwendungsfälle für VISTA-Regeln werden bereits von [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/processing-rules.md), [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md), [Virtual Report Suites](/help/components/vrs/vrs-about.md)oder einfach Ihre Adobe Analytics-Implementierung aktualisieren. Adobe empfiehlt VISTA-Regeln nur als letztes Mittel.

>[!IMPORTANT]
>
>VISTA-Regeln erfordern eine bezahlte Vereinbarung zwischen Ihrem Unternehmen und Adobe Professional Services. Wenden Sie sich an den Adobe Account Manager Ihres Unternehmens, wenn Sie eine VISTA-Regel erstellen oder aktualisieren möchten.

## Erstellen einer VISTA-Regel

Sie müssen mit Adobe Professional Services zusammenarbeiten, um eine VISTA-Regel zu erstellen. Wenden Sie sich an den Adobe Account Manager Ihres Unternehmens, wenn Sie eine VISTA-Regel erstellen möchten.

## Siehe Vorhandene VISTA-Regeln .

Adobe bietet keine Benutzeroberfläche zum Anzeigen vorhandener VISTA-Regeln. Wenden Sie sich an den Kundenbetreuer oder die Kundenunterstützung Ihres Unternehmens, um eine Liste der bestehenden VISTA-Regeln mit der gewünschten Report Suite abzurufen.
