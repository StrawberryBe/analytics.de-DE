---
description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
keywords: Best Practices;Fehler;Timeout;Fehlerbehebung
title: Best Practices für Data Warehouse
topic: Data warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 98%

---


# Best Practices für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.



| Richtlinie | Beschreibung |
|--- |--- |
| Ausführen der Berichte „Seitenansichten“, „Besuche“, „Besucher“ und weiterer Standardberichte in Reports &amp; Analytics | Bevor Sie einen Data Warehouse-Bericht erstellen, überprüfen Sie, ob die gewünschten Informationen bereits in den Berichten verfügbar sind. Falls ja, wird der Bericht deutlich schneller bereitgestellt, da von Reports &amp; Analytics eine Vorverarbeitung für häufig genutzte Metriken vorgenommen wird. |
| Einschätzen der angeforderten Datenmenge | Bei einem mehrere Jahre umspannenden Bericht für eine umfangreiche Report Suite kann die Anzahl der Datenzeilen durchaus im zweistelligen Milliardenbereich liegen. Die Verarbeitung und Auswertung dieser Daten kann Tage oder gar Wochen dauern. Stellen Sie fest, wie der Bericht genutzt werden soll, und ermitteln Sie anhand dieser Informationen, ob ein Teil der Mehrjahresdaten verfügbar ist oder ob der Bericht in mehrere Anforderungen unterteilt werden kann. |
| Anpassen des Berichtszeitraums an die Granularität | Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden. |
| Bericht über abgeschlossene Datumsbereiche | Die Data Warehouse-Berichte werden erst dann erzeugt, wenn der angeforderte Datumsbereich abgeschlossen ist. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erstellen von Pfadsetzungsberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Absprünge usw.) stehen in Data Warehouse nicht zur Verfügung. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. |
