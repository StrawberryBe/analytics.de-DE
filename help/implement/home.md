---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
translation-type: ht
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb
workflow-type: ht
source-wordcount: '382'
ht-degree: 100%

---


# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Adobe benötigt Code auf Ihrer Website oder in Ihrer App, um Daten an die Adobe-Datenerfassungs-Server zu senden. Die folgenden Schritte zeigen die Funktionsweise einer typischen Implementierung.

1. Wenn ein Besucher Ihre Site aufruft, erfolgt eine Anfrage an Ihren Web-Server.
2. Der Web-Server Ihrer Site sendet die Informationen zum Seiten-Code, und die Seiten wird im Browser angezeigt.
3. Die Seite wird geladen, und der Analytics JavaScript-Code wird ausgeführt.
Der JavaScript-Code sendet eine Bildanforderung an die Adobe-Datenerfassungs-Server. Die Seitendaten, die Sie in Ihrer Implementierung definiert haben, werden als Teil einer Abfragezeichenfolge in dieser Bildanforderung gesendet.

4. Adobe gibt ein transparentes Pixelbild zurück.
5. Die Adobe-Server speichern die erfassten Daten in einer *Report Suite*.
6. Report Suite-Daten erscheinen in den Berichten, auf die Sie in einem Webbrowser zugreifen können.

   Die JavaScript Code-Ausführung erfolgt schnell und hat keine größeren Auswirkungen auf die Seitenladezeiten. Dieser Ansatz ermöglicht es Ihnen, Seiten zu zählen, die angezeigt wurden, wenn ein Besucher zum Erreichen einer Seite auf **[!UICONTROL Neu laden]** oder **[!UICONTROL Zurück]** klickt, da das JavaScript auch dann ausgeführt wird, wenn die Seite aus dem Cache abgerufen wird.

Adobe Analytics benötigt Code in Ihrer Website, App oder anderen Anwendung, um Daten an die Datenerfassungs-Server zu senden. Abhängig von der Plattform und den Anforderungen Ihres Unternehmens gibt es verschiedene Methoden, um diesen Code zu implementieren.

* **Adobe Experience Platform Launch**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics. Platzieren Sie ein Loader-Tag auf jeder Seite und definieren Sie die einzelnen Variablen über die Benutzeroberfläche von Launch.
* **Dynamic Tag Management**: Der Vorgänger von Launch. DTM verwendet eine ähnliche Benutzeroberfläche zur Implementierung von Analytics, wird jedoch nicht mehr aktualisiert und ist weniger flexibel. Adobe empfiehlt Launch zum Implementieren von Adobe Analytics.
* **Legacy JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Führt Variablen und Einstellungen auf, die für eine Implementierung verwendet werden. Dies kann für Launch-Implementierungen hilfreich sein, bei denen benutzerdefinierter Code verwendet wird.
* **Mobile SDK**: Spezifische Bibliotheken zum einfachen Senden von Daten aus Ihrer App an Adobe.

## Wichtige Artikel zur Analytics-Implementierung

* [Adobe Debugger](validate/debugger.md)
* [Erstellen einer Eigenschaft in Experience Platform Launch](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)

## Weitere Benutzerhandbücher für Analytics

[Analytics-Benutzerhandbücher](/help/landing/home.md)

## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://helpx.adobe.com/de/contact/enterprise-support.ec.html)
* [Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Adobe Analytics-Ressourcen](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
