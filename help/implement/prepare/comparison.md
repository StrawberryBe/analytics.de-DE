---
title: Vergleich von Implementierungsmethoden
description: Erfahren Sie mehr über die Vorteile jeder Methode zum Datenversand an Adobe Analytics.
exl-id: 19353255-6356-4426-a2ef-5a2672a00eca
feature: Implementation Basics
source-git-commit: 61264d9f4ff2f1e961a613b81461efa826bc3d23
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 46%

---

# Vergleich von Implementierungsmethoden

Hier finden Sie einen Vergleich der Implementierungsmethoden von Adobe Analytics. Sie können diese Tabellen verwenden, um Ihr Unternehmen bei der Ermittlung der optimalen Methode zum Senden von Daten an Adobe zu unterstützen. Klicken Sie auf jede Spalte, um genauere Informationen zu erhalten.

## Web

| | [AppMeasurement](/help/implement/js/overview.md) | [Adobe Analytics-Erweiterung](/help/implement/launch/overview.md) | [Web SDK](/help/implement/aep-edge/web-sdk/overview.md#web-sdk) | [Web SDK-Erweiterung](/help/implement/aep-edge/web-sdk/overview.md#web-sdk-extension) |
| --- | --- | --- | --- | --- |
| Implementierungsanforderungen | Referenzieren Sie `AppMeasurement.js` auf jeder Seite, definieren Sie Variablen, senden Sie Daten mit `s.t()` zu Adobe Analytics | Referenzieren Sie Tag-Lader auf jeder Seite über die Datenerfassungs-Benutzeroberfläche, um Variablen zu definieren und Daten an Adobe Analytics zu senden. | Referenz `Alloy.js` Verwenden Sie auf jeder Seite `alloy("sendEvent",{})` , um XDM-Objekte zu erstellen und die gewünschten Daten über Edge Network an Adobe Analytics zu senden. | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden. |
| Datenziel | Direkt an Adobe Analytics gesendet | Direkt an Adobe Analytics gesendet | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden. | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden. |
| Handhabung von A4T | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Kontextdaten | Verwenden Sie `s.contextData`. | Verwendung `s.contextData` in benutzerspezifischen Codeblöcken | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen. | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen. |

{style="table-layout:auto"}

## Mobile u. a.

>[!CAUTION]
>
>Die Unterstützung für Mobile SDKs Version 4 endete am 31. August 2021. Weitere Informationen finden Sie in den [Häufig gestellten Fragen zum Ende der Unterstützung für Mobile SDKs Version 4](https://developer.adobe.com/client-sdks/documentation/v4-end-of-life-faq/).


| | [Mobile SDK](/help/implement/aep-edge/mobile-sdk/overview.md) | [Server-API](/help/implement/aep-edge/server-api/overview.md) |
| --- | --- | --- |
| Implementierungsanforderungen | Verweisen Sie in der App auf Tag-Lader und verwenden Sie dann direkte API-Aufrufe oder -Regeln in der Datenerfassungs-Benutzeroberfläche, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden. | Verwenden Sie Edge Network Server-APIs, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden. |
| Datenziel | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Ändern Sie den App-Code, in dem direkte API-Aufrufe durchgeführt werden, oder nehmen Sie Änderungen in der Datenerfassungs-Benutzeroberfläche vor. | Erfordert Zugriff auf App-Code für jede Implementierungsänderung |
| Handhabung von A4T | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Kontextdaten | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen. | Alle nicht zugeordneten Felder werden automatisch als `a.x.*` Kontextdatenvariablen |

{style="table-layout:auto"}
