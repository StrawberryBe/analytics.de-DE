---
title: Implementierungsmethoden vergleichen
description: Erfahren Sie mehr über die Vorteile jeder Methode, die Daten an Adobe Analytics sendet.
source-git-commit: 96a5daaf9d8358e4a5222a20f64c381cb8340ab1
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 3%

---

# Implementierungsmethoden vergleichen

Vergleichen Sie die Implementierungsmethoden von Adobe Analytics miteinander. Sie können diese Tabelle verwenden, um Ihr Unternehmen bei der Ermittlung der optimalen Methode zum Senden von Daten an Adobe zu unterstützen.

|  | AppMeasurement | Adobe Analytics-Erweiterung | Web SDK | Web SDK-Erweiterung |
| --- | --- | --- | --- | --- |
| Implementierungsanforderungen | Referenz `AppMeasurement.js` auf jeder Seite Variablen definieren, Daten senden mit `s.t()` | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um Variablen zu definieren und Daten an Adobe zu senden. | Referenz `Alloy.js` Verwenden Sie auf jeder Seite `alloy("sendEvent",{})` zum Senden eines JSON-Objekts, das die gewünschten Daten enthält | Verwenden Sie die Datenerfassungs-Benutzeroberfläche, um das JSON-Objekt zum Senden von Daten festzulegen. |
| Datenziel | Direkt an Adobe Analytics gesendet | Direkt an Adobe Analytics gesendet | An Adobe Experience Platform Edge gesendet, der Daten an Adobe Analytics weiterleitet | An Adobe Experience Platform Edge gesendet, der Daten an Adobe Analytics weiterleitet |
| Schwierigkeiten bei der Umsetzung | Erfordert Zugriff auf Website-Code für jede Implementierungsänderung | Website-Code muss nur einmal geändert werden, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden | Erfordert Zugriff auf Website-Code für jede Implementierungsänderung | Website-Code muss nur einmal geändert werden, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden |
| Handhabung von A4T | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Handhabung von Referrern |