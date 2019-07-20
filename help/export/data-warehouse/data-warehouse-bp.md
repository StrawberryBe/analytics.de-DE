---
description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
keywords: Best Practices; Fehler; timeout; Fehlerbehebung
seo-description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
seo-title: Best Practices für Data Warehouse
solution: Analytics
title: Best Practices für Data Warehouse
topic: Data Warehouse
uuid: d 71 c 9138-22 d 9-4 f 92-885 e -593 f 83 f 2 bb 59
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Best Practices für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.



| Richtlinie | Beschreibung |
|--- |--- |
| Ausführen von Seitenansichten, Besuchen, Besuchern und anderen Standardberichten in Reports &amp; Analysen | Bevor Sie einen Data Warehouse-Bericht erstellen, lesen Sie, ob die gesuchten Informationen bereits in den Berichten verfügbar sind. Wenn dies der Fall ist, wird der Bericht viel schneller bereitgestellt, da von Reports &amp; Analysen die Vorverarbeitung für häufig verwendete Metriken durchgeführt wird. |
| Einschätzen der angeforderten Datenmenge | Bei einem mehrere Jahre umspannenden Bericht für eine umfangreiche Report Suite kann die Anzahl der Datenzeilen durchaus im zweistelligen Milliardenbereich liegen. Die Verarbeitung und Auswertung dieser Tage kann Tage oder gar Wochen dauern. Stellen Sie fest, wie der Bericht genutzt werden soll, und ermitteln Sie anhand dieser Informationen, ob ein Teil der Mehrjahresdaten verfügbar ist oder ob der Bericht in mehrere Anforderungen unterteilt werden kann. |
| Anpassen des Berichtszeitraums an die Granularität | Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden. |
| Bericht über abgeschlossene Datumsbereiche | Data Warehouse-Berichte werden generiert, wenn der angeforderte Datumsbereich vollständig ist. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erstellen von Pfadsetzungsberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Absprünge usw.) stehen in Data Warehouse nicht zur Verfügung. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. |