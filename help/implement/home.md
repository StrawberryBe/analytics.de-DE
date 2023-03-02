---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
source-git-commit: d9a5d8a15b9e108af795cdfb7ed5481d51311328
workflow-type: ht
source-wordcount: '885'
ht-degree: 100%

---

# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Adobe benötigt Code auf Ihrer Website oder in Ihrer App, um Daten an die Adobe-Datenerfassungs-Server zu senden. Die folgenden Schritte zeigen die Funktionsweise einer typischen Implementierung.

1. Wenn ein Besucher Ihre Site aufruft, erfolgt eine Anfrage an Ihren Web-Server.
2. Der Web-Server Ihrer Site sendet die Informationen zum Seiten-Code, und die Seiten wird im Browser angezeigt.
3. Die Seite wird geladen, und der Analytics JavaScript-Code wird ausgeführt.
Der JavaScript-Code sendet eine Bildanforderung an die Datenerfassungs-Server von Adobe. Die Seitendaten, die Sie in Ihrer Implementierung definiert haben, werden als Teil einer Abfragezeichenfolge in dieser Bildanforderung gesendet.

4. Adobe gibt ein transparentes Pixelbild zurück.
5. Adobe-Server speichern erfasste Daten in einer oder mehreren *Report Suites*.
6. Report Suite-Daten erscheinen in den Berichten, auf die Sie in einem Webbrowser zugreifen können.

Die JavaScript Code-Ausführung erfolgt schnell und hat keine größeren Auswirkungen auf die Seitenladezeiten. Dieser Ansatz ermöglicht es Ihnen, Seiten zu zählen, die angezeigt wurden, wenn ein Besucher zum Erreichen einer Seite auf **[!UICONTROL Neu laden]** oder **[!UICONTROL Zurück]** klickt, da das JavaScript auch dann ausgeführt wird, wenn die Seite aus dem Cache abgerufen wird.

Adobe Analytics benötigt Code in Ihrer Website, App oder anderen Anwendung, um Daten an die Datenerfassungs-Server zu senden. Abhängig von der Plattform und den Anforderungen Ihres Unternehmens gibt es verschiedene Methoden, um diesen Code zu implementieren.

## Website-Implementierungsmethoden

Für Ihre **Website** sind die folgenden Implementierungsmethoden verfügbar:

* **Web SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics für neue Kundinnen und Kunden. Installieren Sie die **AEP Web SDK-Erweiterung** in **Datenerfassungs-Tags** von Adobe Experience Platform, verwenden Sie auf jeder Seite ein Loader-Tag und senden Sie Daten an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format. Das Edge Network leitet eingehende Daten im richtigen Format an Adobe Analytics weiter.
   ![Web SDK-Erweiterung](./assets/websdk-extension-implementation.png)
Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit der Adobe Experience Platform Web SDK-Erweiterung](./aep-edge/overview.md).

* **Web SDK**: Wenn Sie nicht die Datenerfassung von Adobe Experience Platform verwenden möchten, können Sie die Web SDK-Bibliotheken auch manuell auf Ihre Site laden. Verweisen Sie auf jeder Seite auf die Web SDK-Bibliothek (`alloy.js`) und senden Sie die gewünschten Tracking-Aufrufe an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format. Das Edge Network leitet eingehende Daten im richtigen Format an Adobe Analytics weiter.
   ![Web SDK](./assets/websdk-implementation.png)
Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK](./aep-edge/overview.md).


* **Analytics-Erweiterung**: Installieren Sie die **Adobe Analytics-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform. Platzieren Sie ein Loader-Tag auf jeder Seite und verwenden Sie die Adobe Analytics-Erweiterung, um zu bestimmen, wie jede Variable definiert wird. Nutzen Sie diese Implementierungsmethode, wenn Sie Tags, aber nicht die Edge Network-Infrastruktur verwenden möchten.
   ![Adobe Analytics-Erweiterung](./assets/analytics-extension-implementation.png)
Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit der Analytics-Erweiterung](launch/overview.md).

* **Legacy-JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Verweisen Sie auf jeder Seite auf die AppMeasurement-Bibliothek (`AppMeasurement.js`) und beschreiben Sie dann die Variablen und Einstellungen, die in einer Implementierung verwendet werden.
   ![Legacy-JavaScript](./assets/appmeasurement-implementation.png)
Diese Implementierungsmethode kann für Implementierungen mit benutzerdefiniertem Code nützlich sein und wird weiterhin empfohlen, wenn Sie Folgendes verwenden (möchten):

   * [Activity Map-Daten auf Klickebene](../analyze/activity-map/activity-map.md),

   * [Messung von Streaming-Medien](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=de),

   * [Livestream-API oder Livestream-Trigger](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md),

   * [AMP-Seitenanalyse](./other/amp.md)
   Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit AppMeasurement für JavaScript](js/overview.md).

Der folgende Entscheidungsbaum kann Ihnen bei der Auswahl einer Implementierungsmethode helfen:

![Entscheidungsbaum](./assets/decision-tree.png)


>[!TIP]
>
>Wenden Sie sich an Adobe, um Hinweise und Best Practices zu erhalten, die Ihnen bei der Entscheidung helfen können, welche Implementierung Sie in Ihrer aktuellen Situation wählen sollten.

## Implementierungsmethoden für Mobile Apps

Für Ihre **Mobile App** sind die folgenden Implementierungsmethoden verfügbar:

* **Mobile SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics in Ihrer App. Verwenden Sie spezifische Bibliotheken, um Daten aus Ihrer App ganz einfach an Adobe zu senden. Installieren Sie die **Adobe Experience Platform Mobile SDK-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform und implementieren Sie den korrekten Code in Ihrer App, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Dadurch werden Daten an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format gesendet. Experience Edge leitet eingehende Daten im richtigen Format an Adobe Analytics weiter.
   ![Mobile SDK-Erweiterung](./assets/mobilesdk-extension.png)

   Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK](../implement/aep-edge/mobile-sdk/overview.md).

* **Analytics-Erweiterung**: Installieren Sie die **Adobe Analytics-Erweiterung** in **Datenerfassungs-Tags** von Adobe Experience Platform und implementieren Sie den richtigen Code in Ihrer Anwendung, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Verwenden Sie die Analytics-Erweiterung, um festzustellen, wie die einzelnen Variablen definiert sind. Verwenden Sie diese Implementierungsmethode, wenn Sie den Komfort der Adobe Experience Platform-Datenerfassung wünschen, aber nicht die Netzwerkinfrastruktur von Adobe Experience Platform Edge nutzen möchten.
   ![Analytics-Erweiterung](./assets/mobilesdk-analytics-extension.png)

   Weitere Informationen finden Sie unter [Implementieren von Adobe Analytics mit der Analytics-Erweiterung](../implement/aep-edge/mobile-sdk/overview.md).


>[!CAUTION]
>
>Die Unterstützung für Mobile SDKs Version 4 endete am 31. August 2021. Weitere Informationen finden Sie in den [Häufig gestellten Fragen zum Ende der Unterstützung für Mobile SDKs Version 4](https://developer.adobe.com/client-sdks/documentation/v4-end-of-life-faq/).

## Wichtige Artikel zur Analytics-Implementierung

* [Übernahme einer bestehenden Adobe Analytics-Implementierung](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Erstellen einer Tag-Eigenschaft in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)

## Weitere Benutzerhandbücher für Analytics

[Analytics-Benutzerhandbücher](https://experienceleague.adobe.com/docs/analytics.html?lang=de)

## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://experienceleague.adobe.com/?support-solution=Analytics&amp;lang=de#support)
* [Analytics-Forum](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?lang=de)
* [Adobe Analytics-Ressourcen](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/adobe-analytics-resources/m-p/276666?profile.language=de)
