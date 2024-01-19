---
description: Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Anhand dieser Richtlinien vermindern Sie den Zeitaufwand für das Abrufen der Daten.
keywords: Best Practices; Fehler; Zeitüberschreitung; Fehlerbehebung
title: Best Practices für Data Warehouse
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 87%

---

# Best Practices für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Verwenden Sie die folgenden Richtlinien, um die zum Abrufen von Daten benötigte Zeit zu verkürzen:

| Richtlinie | Beschreibung |
|--- |--- |
| Einschätzen der angeforderten Datenmenge | Bei einem mehrere Jahre umspannenden Bericht für eine umfangreiche Report Suite kann die Anzahl der Datenzeilen durchaus im zweistelligen Milliardenbereich liegen. Die Verarbeitung und Auswertung dieser Daten kann Tage oder gar Wochen dauern. Stellen Sie fest, wie der Bericht genutzt werden soll, und ermitteln Sie anhand dieser Informationen, ob ein Teil der Mehrjahresdaten verfügbar ist oder ob der Bericht in mehrere Anforderungen unterteilt werden kann. |
| Anpassen des Berichtszeitraums an die Granularität | Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden. |
| Bericht über abgeschlossene Datumsbereiche | Die Data Warehouse-Berichte werden erst dann erzeugt, wenn der angeforderte Datumsbereich abgeschlossen ist. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erstellen von Pfadberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Absprünge usw.) in Data Warehouse nicht verfügbar sind. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. |

