---
title: Vergleich von Implementierungsmethoden
description: Erfahren Sie mehr über die Vorteile jeder Methode zum Datenversand an Adobe Analytics.
source-git-commit: 2e69321404237213c6929f3fb0c330575d8a90db
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 76%

---

# Vergleich von Implementierungsmethoden

Hier finden Sie einen Vergleich der Implementierungsmethoden von Adobe Analytics. Diese Tabelle hilft Ihnen, für Ihr Unternehmen die optimale Methode zum Datenversand an Adobe zu finden.

|  | AppMeasurement | Adobe Analytics-Erweiterung | Web SDK | Web SDK-Erweiterung |
| --- | --- | --- | --- | --- |
| Implementierungsanforderungen | Referenzieren Sie `AppMeasurement.js` auf jeder Seite, definieren Sie Variablen, senden Sie Daten mit `s.t()` | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um Variablen zu definieren und Daten an Adobe zu senden. | Referenzieren Sie `Alloy.js` auf jeder Seite, verwenden Sie `alloy("sendEvent",{})` zum Senden eines JSON-Objekts, das die gewünschten Daten enthält | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um das JSON-Objekt zum Senden von Daten festzulegen. |
| Datenziel | Direkt an Adobe Analytics gesendet | Direkt an Adobe Analytics gesendet | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Loader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Loader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden |
| Handhabung von A4T | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Kontextdaten | Verwenden Sie `s.contextData`. | Verwendung `s.contextData` in benutzerspezifischen Codeblöcken | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen. | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen. |

{style=&quot;table-layout:auto&quot;}
