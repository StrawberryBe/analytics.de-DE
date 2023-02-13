---
title: Vergleich von Implementierungsmethoden
description: Erfahren Sie mehr über die Vorteile jeder Methode zum Datenversand an Adobe Analytics.
source-git-commit: 96a5daaf9d8358e4a5222a20f64c381cb8340ab1
workflow-type: ht
source-wordcount: '273'
ht-degree: 100%

---

# Vergleich von Implementierungsmethoden

Hier finden Sie einen Vergleich der Implementierungsmethoden von Adobe Analytics. Diese Tabelle hilft Ihnen, für Ihr Unternehmen die optimale Methode zum Datenversand an Adobe zu finden.

|  | AppMeasurement | Adobe Analytics-Erweiterung | Web SDK | Web SDK-Erweiterung |
| --- | --- | --- | --- | --- |
| Implementierungsanforderungen | Referenzieren Sie `AppMeasurement.js` auf jeder Seite, definieren Sie Variablen, senden Sie Daten mit `s.t()` | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um Variablen zu definieren und Daten an Adobe zu senden. | Referenzieren Sie `Alloy.js` auf jeder Seite, verwenden Sie `alloy("sendEvent",{})` zum Senden eines JSON-Objekts, das die gewünschten Daten enthält | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um das JSON-Objekt zum Senden von Daten festzulegen. |
| Datenziel | Direkt an Adobe Analytics gesendet | Direkt an Adobe Analytics gesendet | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Website-Code muss nur einmal geändert werden, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden. | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Website-Code muss nur einmal geändert werden, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden. |
| Handhabung von A4T | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Handhabung von Referrern |