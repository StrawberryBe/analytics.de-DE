---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
source-git-commit: d2c291f7db465034ffadc4a2c1caf9639caf2a1d
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 79%

---

# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Im Folgenden finden Sie eine Videoübersicht zu Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Adobe benötigt Code auf Ihrer Website oder in Ihrer App, um Daten an die Adobe-Datenerfassungs-Server zu senden. Die folgenden Schritte zeigen die Funktionsweise einer typischen Implementierung.

1. Wenn ein Besucher Ihre Site aufruft, erfolgt eine Anfrage an Ihren Web-Server.
2. Der Web-Server Ihrer Site sendet die Informationen zum Seiten-Code, und die Seiten wird im Browser angezeigt.
3. Die Seite wird geladen, und der Analytics JavaScript-Code wird ausgeführt.
4. Der JavaScript-Code sendet eine Bildanforderung von 1 x 1 Pixel an die Datenerfassungsserver von Adobe. Die Seitendaten, die Sie in Ihrer Implementierung definiert haben, werden als Teil einer Abfragezeichenfolge in dieser Bildanforderung gesendet.
5. Die Datenerfassungsserver der Adobe geben das angeforderte Bild zurück.
6. Adobe-Server analysieren und speichern die erfassten Daten in einer Report Suite.
7. Report Suite-Daten erscheinen in den Berichten, auf die Sie in einem Webbrowser zugreifen können.


Adobe bietet je nach Plattform und den Anforderungen Ihres Unternehmens verschiedene Methoden zur Implementierung dieses Codes.

* **Web SDK-Erweiterung**: Die aktuelle, standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics. Installieren Sie die Web SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, verwenden Sie auf jeder Seite ein Lader-Tag und senden Sie Daten an Adobe Experience Platform Edge in einem für Ihr Unternehmen geeigneten Format. Experience Edge leitet eingehende Daten im richtigen Format an Adobe Analytics weiter.
* **Web SDK**: Wenn Sie keine Tags verwenden möchten, können Sie die Web SDK-Bibliotheken manuell auf Ihre Site laden. Verweisen Sie auf jeder Seite auf die Web SDK-Bibliothek und senden Sie die gewünschten Tracking-Aufrufe an Adobe Experience Edge.
* **Adobe Analytics-Erweiterung**: Installieren Sie die Adobe Analytics-Erweiterung in der Datenerfassung von Adobe Experience Platform. Platzieren Sie ein Lader-Tag auf jeder Seite und verwenden Sie die Analytics-Erweiterung, um zu bestimmen, wie jede Variable definiert wird.
* **Veraltetes JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Führt Variablen und Einstellungen auf, die in einer Implementierung verwendet werden. Dies kann für Implementierungen hilfreich sein, bei denen Regeln mit benutzerdefiniertem Code verwendet werden.
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
* [Experience League](https://experienceleague.adobe.com/?lang=de#dashboard/learning)
