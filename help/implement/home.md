---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 100%

---

# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Im Folgenden finden Sie eine Videoübersicht zu Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Adobe benötigt Code auf Ihrer Website oder in Ihrer App, um Daten an die Adobe-Datenerfassungs-Server zu senden. Die folgenden Schritte zeigen die Funktionsweise einer typischen Implementierung.

1. Wenn ein Besucher Ihre Site aufruft, erfolgt eine Anfrage an Ihren Web-Server.
2. Der Web-Server Ihrer Site sendet die Informationen zum Seiten-Code, und die Seiten wird im Browser angezeigt.
3. Die Seite wird geladen, und der Analytics JavaScript-Code wird ausgeführt.
Der JavaScript-Code sendet eine Bildanforderung an die Adobe-Datenerfassungs-Server. Die Seitendaten, die Sie in Ihrer Implementierung definiert haben, werden als Teil einer Abfragezeichenfolge in dieser Bildanforderung gesendet.

4. Adobe gibt ein transparentes Pixelbild zurück.
5. Adobe-Server speichern erfasste Daten in einer oder mehreren *Report Suites*.
6. Report Suite-Daten erscheinen in den Berichten, auf die Sie in einem Webbrowser zugreifen können.

   Die JavaScript Code-Ausführung erfolgt schnell und hat keine größeren Auswirkungen auf die Seitenladezeiten. Dieser Ansatz ermöglicht es Ihnen, Seiten zu zählen, die angezeigt wurden, wenn ein Besucher zum Erreichen einer Seite auf **[!UICONTROL Neu laden]** oder **[!UICONTROL Zurück]** klickt, da das JavaScript auch dann ausgeführt wird, wenn die Seite aus dem Cache abgerufen wird.

Adobe Analytics benötigt Code in Ihrer Website, App oder anderen Anwendung, um Daten an die Datenerfassungs-Server zu senden. Abhängig von der Plattform und den Anforderungen Ihres Unternehmens gibt es verschiedene Methoden, um diesen Code zu implementieren.

* **Web SDK**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics. Installieren Sie die Web SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, verwenden Sie auf jeder Seite ein Lader-Tag und senden Sie Daten an Adobe Experience Platform Edge in einem für Ihr Unternehmen geeigneten Format. Experience Edge leitet eingehende Daten im richtigen Format an Adobe Analytics weiter.
* **Adobe Analytics-Erweiterung**: Installieren Sie die Adobe Analytics-Erweiterung in der Datenerfassung von Adobe Experience Platform. Platzieren Sie ein Lader-Tag auf jeder Seite und verwenden Sie die Analytics-Erweiterung, um zu bestimmen, wie jede Variable definiert wird.
* **Legacy JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Führt Variablen und Einstellungen auf, die in einer Implementierung verwendet werden. Dies kann für ta-Implementierungen hilfreich sein, bei denen Regeln mit benutzerdefiniertem Code verwendet werden.
* **Mobile SDK**: Spezifische Bibliotheken zum einfachen Senden von Daten aus Ihrer App an Adobe.

## Wichtige Artikel zur Analytics-Implementierung

* [Übernahme einer bestehenden Adobe Analytics-Implementierung](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Erstellen einer Tag-Eigenschaft in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)

## Weitere Benutzerhandbücher für Analytics

[Analytics-Benutzerhandbücher](https://experienceleague.adobe.com/docs/analytics.html?lang=de)

## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://experienceleague.adobe.com/?support-solution=Analytics&amp;lang=de#support)
* [Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Adobe Analytics-Ressourcen](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/adobe-analytics-resources/m-p/276666?profile.language=de)
* [Experience League](https://experienceleague.adobe.com/?lang=de#home)
