---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
role: Admin, Developer, Leader, User
source-git-commit: e033f32fb3394bb9e2a9ec47766febfbe8d5bfd7
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 83%

---

# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Adobe Analytics benötigt Code in Ihrer Website, App oder anderen Anwendung, um Daten an die Datenerfassungs-Server zu senden. Abhängig von der Plattform und den Anforderungen Ihres Unternehmens gibt es verschiedene Methoden, um diesen Code zu implementieren.

## Website-Implementierungsmethoden

Für Ihre **Website** sind die folgenden Implementierungsmethoden verfügbar:

### Client-seitig

* **Web SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics für neue Kundinnen und Kunden. Fügen Sie die **Adobe Experience Platform Web SDK-Erweiterung** in den **Datenerfassungs-Tags** der Adobe Experience Platform hinzu und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten an das Adobe Experience Platform **Edge Network**, das diese Daten an Adobe Analytics weiterleitet.
  ![Web SDK-Erweiterung](./assets/websdk-extension-implementation.png)
Weitere Informationen finden Sie unter [So implementieren Sie Adobe Analytics mit der Adobe Experience Platform Web SDK-Erweiterung.](./aep-edge/overview.md) für weitere Informationen.

* **Web SDK**: Wenn Sie nicht die Datenerfassung von Adobe Experience Platform verwenden möchten, können Sie die Web SDK-Bibliotheken auch manuell auf Ihre Site laden. Verweisen Sie auf jeder Seite auf die Web SDK-Bibliothek (`alloy.js`) und senden Sie die gewünschten Tracking-Aufrufe an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format. Das Edge Network leitet die Daten an Adobe Analytics weiter.
  ![Web SDK](./assets/websdk-implementation.png)
Weitere Informationen finden Sie unter [So implementieren Sie Adobe Analytics mit dem Adobe Experience Platform Web SDK](./aep-edge/overview.md).

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten direkt an Adobe Analytics. Nutzen Sie diese Implementierungsmethode, wenn Sie Tags, aber nicht die Edge Network-Infrastruktur verwenden möchten.
  ![Adobe Analytics-Erweiterung](./assets/analytics-extension-implementation.png)
Weitere Informationen finden Sie unter [So implementieren Sie Adobe Analytics mit der Analytics-Erweiterung](launch/overview.md).

* **Legacy-JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Verweisen Sie auf jeder Seite auf die AppMeasurement-Bibliothek (`AppMeasurement.js`) und stellen Sie dann die Variablen und Einstellungen in JavaScript ein.
  ![So implementieren Sie Adobe Analytics mit Legacy JavaScript](./assets/appmeasurement-implementation.png)
Diese Implementierungsmethode kann für Implementierungen mit benutzerdefiniertem Code nützlich sein und eignet sich ideal für Implementierungstypen, die andernorts nicht angeboten werden, z. B. für [AMP-Seiten](other/amp.md).

Der folgende Entscheidungsfluss kann Ihnen bei der Auswahl einer clientseitigen Implementierungsmethode helfen:

![Ein Entscheidungsbaum zur Auswahl einer Implementierungsmethode, wie in diesem Abschnitt beschrieben.](./assets/decision-tree.png)


>[!TIP]
>
>Wenden Sie sich an das Adobe-Accountteam, um Hinweise und Best Practices zu erhalten, die Ihnen bei der Entscheidung helfen können, welche Implementierung Sie in Ihrer aktuellen Situation wählen sollten.

### Server-seitig

Zur serverseitigen Implementierung von Adobe Analytics stehen Ihnen die folgenden Optionen zur Verfügung:

* **Edge Server-API**: Sie implementieren Code auf dem Server, der die Adobe Experience Platform Edge Server-API verwendet, um über einen Datenspeicher mit Adobe Analytics zu kommunizieren.
  ![Serverseitige Implementierung](assets/edge-network-server-api.svg)
Siehe [Implementieren von Adobe Analytics mit der Adobe Experience Platform Edge Network Server-API](/help/implement/aep-edge/server-api/overview.md) für weitere Informationen.

* **(Bulk) Data Insertion API**: Sie verwenden die Adobe Analytics-Dateneinfüge-APIs (Bulk), um Daten Server-seitig direkt in Adobe Analytics zu erfassen.
  ![Dateneinfüge-APIs](assets/analytics-apis.png)
Siehe [Dateneinfüge-API](../import/c-data-insertion-api/c-data-insertion-api.md) für weitere Informationen.

## Implementierungsmethoden für Mobile Apps

Für Ihre **Mobile App** sind die folgenden Implementierungsmethoden verfügbar:

* **Mobile SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics in Ihrer App. Verwenden Sie spezifische Bibliotheken, um Daten aus Ihrer App ganz einfach an Adobe zu senden. Fügen Sie die **Adobe Experience Platform Mobile SDK-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und implementieren Sie dann die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Senden Sie Daten an das Adobe Experience Platform **Edge Network**. Edge leitet diese Daten dann an Adobe Analytics weiter.
  ![Mobile SDK-Erweiterung](./assets/mobilesdk-extension.png)

  Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK](../implement/aep-edge/mobile-sdk/overview.md).

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und implementieren Sie die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Diese Implementierungsmethode sendet Daten direkt an Adobe Analytics. Verwenden Sie diese Implementierungsmethode, wenn Sie den Komfort der Adobe Experience Platform-Datenerfassung wünschen, aber nicht die Netzwerkinfrastruktur von Adobe Experience Platform Edge nutzen möchten.
  ![Analytics-Erweiterung](./assets/mobilesdk-analytics-extension.png)

  Weitere Informationen finden Sie unter [Implementieren von Adobe Analytics mit der Analytics-Erweiterung](../implement/aep-edge/mobile-sdk/overview.md).


>[!CAUTION]
>
>Siehe Unterstützung für ältere Versionen von Adobe Mobile SDKs unter [Mitteilungen zum Ende der Unterstützung für SDKs](https://developer.adobe.com/client-sdks/resources/sdks-end-of-support/).

## Wichtige Artikel zur Analytics-Implementierung

* [Übernahme einer bestehenden Adobe Analytics-Implementierung](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Erstellen einer Tag-Eigenschaft in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)
* [Tutorial zum Einrichten von Adobe Analytics mit dem Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-analytics.html)
* [Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/overview.html?lang=de)


## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://experienceleague.adobe.com/?support-solution=Analytics&amp;lang=de#support)
* [Analytics-Forum](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?lang=de)
* [Adobe Analytics-Ressourcen](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/adobe-analytics-resources/m-p/276666?profile.language=de)
* [Neueste Versionshinweise](../release-notes/latest.md)
