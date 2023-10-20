---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
source-git-commit: b157674adf67fa6ef0f2e75775d0ec888cff3cba
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 55%

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

* **Web SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics für neue Kundinnen und Kunden. Fügen Sie die **Adobe Experience Platform Web SDK-Erweiterung** in der Adobe Experience Platform-Datenerfassung **Tags** und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten an die Adobe Experience Platform **Edge Network**, der diese Daten an Adobe Analytics weiterleitet.
  ![Web SDK-Erweiterung](./assets/websdk-extension-implementation.png)
Siehe [Implementieren von Adobe Analytics mithilfe der Adobe Experience Platform Web SDK-Erweiterung.](./aep-edge/overview.md) für weitere Informationen.

* **Web SDK**: Wenn Sie nicht die Datenerfassung von Adobe Experience Platform verwenden möchten, können Sie die Web SDK-Bibliotheken auch manuell auf Ihre Site laden. Verweisen Sie auf jeder Seite auf die Web SDK-Bibliothek (`alloy.js`) und senden Sie die gewünschten Tracking-Aufrufe an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format. Das Edge-Netzwerk leitet diese Daten an Adobe Analytics weiter.
  ![Web SDK](./assets/websdk-implementation.png)
Siehe [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK](./aep-edge/overview.md) für weitere Informationen.

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in der Adobe Experience Platform-Datenerfassung **Tags**und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten direkt an Adobe Analytics. Verwenden Sie diese Implementierungsmethode, wenn Sie den Komfort von Tags wünschen, aber nicht die Edge-Netzwerkinfrastruktur verwenden möchten.
  ![Adobe Analytics-Erweiterung](./assets/analytics-extension-implementation.png)
Siehe [Implementieren von Adobe Analytics mithilfe der Analytics-Erweiterung](launch/overview.md) für weitere Informationen.

* **Legacy-JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Referenzieren Sie die AppMeasurement-Bibliothek (`AppMeasurement.js`) auf jeder Seite und legen Sie dann Variablen und Einstellungen in JavaScript fest.
  ![Implementieren von Adobe Analytics mit Legacy JavaScript](./assets/appmeasurement-implementation.png)
Diese Implementierungsmethode kann für Implementierungen mit benutzerdefiniertem Code nützlich sein und eignet sich ideal für Implementierungstypen, die andernorts nicht angeboten werden, z. B. für [AMP-Seiten](other/amp.md).

Der folgende Entscheidungsfluss kann Ihnen bei der Auswahl einer Implementierungsmethode helfen:

![Eine Entscheidungsstruktur zur Auswahl einer Implementierungsmethode, wie in diesem Abschnitt beschrieben.](./assets/decision-tree.png)


>[!TIP]
>
>Wenden Sie sich an Ihr Adobe Account-Team, um Ratschläge und Best Practices zur Implementierung zu erhalten, die auf Ihrer aktuellen Situation basieren.

## Implementierungsmethoden für Mobile Apps

Für Ihre **Mobile App** sind die folgenden Implementierungsmethoden verfügbar:

* **Mobile SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics in Ihrer App. Verwenden Sie spezifische Bibliotheken, um Daten aus Ihrer App ganz einfach an Adobe zu senden. Fügen Sie die **Adobe Experience Platform Mobile SDK-Erweiterung** in der Adobe Experience Platform-Datenerfassung **Tags** und implementieren Sie dann die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Senden von Daten an die Adobe Experience Platform **Edge Network**; Edge leitet diese Daten dann an Adobe Analytics weiter.
  ![Mobile SDK-Erweiterung](./assets/mobilesdk-extension.png)

  Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK](../implement/aep-edge/mobile-sdk/overview.md).

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in der Adobe Experience Platform-Datenerfassung **Tags**und implementieren Sie die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Diese Implementierungsmethode sendet Daten direkt an Adobe Analytics. Es wird empfohlen, wenn Sie den Komfort der Adobe Experience Platform-Datenerfassung wünschen, aber keine Adobe Experience Platform Edge-Netzwerkinfrastruktur verwenden möchten.
  ![Analytics-Erweiterung](./assets/mobilesdk-analytics-extension.png)

  Weitere Informationen finden Sie unter [Implementieren von Adobe Analytics mit der Analytics-Erweiterung](../implement/aep-edge/mobile-sdk/overview.md).


>[!CAUTION]
>
>Die Unterstützung für Mobile SDKs Version 4 endete am 31. August 2021. Weitere Informationen finden Sie in den [Häufig gestellten Fragen zum Ende der Unterstützung für Mobile SDKs Version 4](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/v4-faq/).

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
