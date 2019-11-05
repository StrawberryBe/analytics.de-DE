---
description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
keywords: Best Practices;Fehler;Timeout;Fehlerbehebung
seo-description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
seo-title: Bewährte Methoden für Data Warehouse
solution: Analytics
title: Bewährte Methoden für Data Warehouse
topic: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
translation-type: tm+mt
source-git-commit: bc46011a48aa18e33ba6f1912223857f5a664f35

---


# Bewährte Methoden für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.



| Richtlinie | Beschreibung |
|--- |--- |
| Ausführen von Seitenansichten, Besuchen, Besuchern und anderen Standardberichten in Reports &amp; Analysen | Bevor Sie einen Data Warehouse-Bericht erstellen, prüfen Sie, ob die gesuchten Informationen bereits in Berichten verfügbar sind. In diesem Fall wird der Bericht aufgrund der Vorverarbeitung, die von Reports &amp; Analysen für häufig verwendete Metriken durchgeführt wird, viel schneller bereitgestellt. |
| Einschätzen der angeforderten Datenmenge | Bei einem mehrere Jahre umspannenden Bericht für eine umfangreiche Report Suite kann die Anzahl der Datenzeilen durchaus im zweistelligen Milliardenbereich liegen. Die Verarbeitung und Auswertung dieser Tage kann Tage oder gar Wochen dauern. Stellen Sie fest, wie der Bericht genutzt werden soll, und ermitteln Sie anhand dieser Informationen, ob ein Teil der Mehrjahresdaten verfügbar ist oder ob der Bericht in mehrere Anforderungen unterteilt werden kann. |
| Anpassen des Berichtszeitraums an die Granularität | Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden. |
| Bericht über abgeschlossene Datumsbereiche | Data Warehouse-Berichte werden nach Abschluss des angeforderten Datumsbereichs generiert. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erstellen von Pfadsetzungsberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Absprünge usw.) stehen in Data Warehouse nicht zur Verfügung. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. |
