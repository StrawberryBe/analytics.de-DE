---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics auf Ihrer Site, Eigenschaft oder Anwendung.
translation-type: tm+mt
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Adobe benötigt Code auf Ihrer Site oder App, um Daten an die Datenerfassungsserver von Adobe zu senden. Die folgenden Schritte zeigen, wie eine typische Implementierung funktioniert.

1. Wenn ein Besucher Ihre Site aufruft, erfolgt eine Anfrage an Ihren Web-Server.
2. Der Web-Server Ihrer Site sendet die Informationen zum Seiten-Code, und die Seiten wird im Browser angezeigt.
3. Die Seite wird geladen, und der Analytics JavaScript-Code wird ausgeführt.
Der JavaScript-Code sendet eine Bildanforderung an Adobe-Datenerfassungsserver. Seitendaten, die Sie in Ihrer Implementierung definiert haben, werden als Teil einer Abfragezeichenfolge in dieser Bildanforderung gesendet.

4. Adobe gibt ein transparentes Pixelbild zurück.
5. Adobe-Server speichern erfasste Daten in einer *Report Suite*.
6. Report Suite-Daten erscheinen in den Berichten, auf die Sie in einem Webbrowser zugreifen können.

   Die JavaScript Code-Ausführung erfolgt schnell und hat keine größeren Auswirkungen auf die Seitenladezeiten. Dieser Ansatz ermöglicht es Ihnen, Seiten zu zählen, die angezeigt wurden, wenn ein Besucher zum Erreichen einer Seite auf **[!UICONTROL Neu laden]**oder**[!UICONTROL  Zurück]** klickt, da das JavaScript auch dann ausgeführt wird, wenn die Seite aus dem Cache abgerufen wird.

Adobe Analytics benötigt Code in Ihrer Website, mobilen App oder einer anderen Anwendung, um Daten an Datenerfassungsserver zu senden. Es gibt verschiedene Methoden, diesen Code zu implementieren, je nach Plattform und den Anforderungen Ihres Unternehmens.

* **Adobe Experience Platform Launch**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics. Platzieren Sie ein Loader-Tag auf jeder Seite und definieren Sie die einzelnen Variablen über die Benutzeroberfläche von Launch.
* **Dynamisches Tag-Management**: Der Vorgänger, der gestartet werden soll. DTM verwendet eine ähnliche Benutzeroberfläche zur Implementierung von Analytics, wird jedoch nicht mehr aktualisiert und ist weniger flexibel. Adobe empfiehlt Launch zum Implementieren von Adobe Analytics.
* **Legacy-JavaScript**: Die historische manuelle Methode zur Implementierung von Adobe Analytics. Führt Variablen und Einstellungen auf, die für eine Implementierung verwendet werden. Dies kann für Launch-Implementierungen hilfreich sein, bei denen benutzerdefinierter Code verwendet wird.
* **Mobile SDK**: Spezifische Bibliotheken zum einfachen Senden von Daten aus Ihrer mobilen App an Adobe.

## Wichtige Artikel zur Analytics-Implementierung

* [Adobe Debugger](validate/debugger.md)
* [Eigenschaft in Experience Platform Launch erstellen](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)

## Weitere Benutzerhandbücher für Analytics

[Analytics-Benutzerhandbücher](/help/landing/home.md)

## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://helpx.adobe.com/contact/enterprise-support.ec.html)
* [Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Adobe Analytics-Ressourcen](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
