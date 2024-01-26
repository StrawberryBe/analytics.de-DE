---
title: Häufig gestellte Fragen zur Implementierung
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
feature: Implementation Basics
exl-id: 4bab6d51-0077-42ce-8091-f75207d4c4db
role: Admin, Developer, Leader, User
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 100%

---

# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

## Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID?

Der Identitätsdienst weist eine eindeutige, beständige ID zu, die von den anderen Lösungen in Experience Cloud gemeinsam genutzt werden kann. Die Analytics-Besucher-ID wird nur von Analytics verwendet. Adobe empfiehlt, den Experience Cloud-Besucher-ID-Dienst in Ihrer Implementierung zu verwenden.

## Wie wird Heartbeat-Video-Tracking implementiert?

Weitere Informationen finden Sie unter [Messen von Audio und Video in Adobe Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=de).

## Kann eine Dienstunterbrechung bei Adobe die Performance beeinträchtigen?

Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf Ihre AppMeasurement-Bibliothek auswirkt. Wenn Sie Tags in Adobe Experience Platform verwenden, wird die JavaScript-Datei von Akamai oder an einem von Ihrem Unternehmen bestimmten Server-Speicherort gehostet.

## Kann das Senden von Daten vom Browser an die Adobe-Dienste die Performance beeinträchtigen?

AppMeasurement erstellt innerhalb der HTML-Seite ein Bildobjekt, das der Browser dann von den Adobe-Datenerfassungs-Servern anfordert. Falls der Datenerfassungs-Server sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Bildes verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Bildern durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten.

## Wie kann ich eine Analytics-Implementierung ungültig machen oder entfernen?

Manchmal möchte ein Unternehmen eine Implementierung aufgrund des Vertragsablaufs entfernen oder die Anzahl der Serveraufrufe verringern.

* **Implementierungen mit der Adobe Experience Platform-Datenerfassung**: Deaktivieren oder deinstallieren Sie die entsprechende Adobe Analytics-, Web SDK- oder Mobile SDK-Erweiterung im [!UICONTROL Erweiterungen] und veröffentlichen Sie dann.
* **Ältere AppMeasurement-Implementierungen**: Ersetzen Sie den gesamten Inhalt Ihrer `s_code.js`-Datei durch die folgende Codezeile:

```js
var s = new Object();
```

>[!WARNING]
>
>Beachten Sie Folgendes:
>
>* Ändern Sie die Report Suite nicht in einen ungültigen Wert, da dies die Server von Adobe unnötig belastet.
>* Entfernen Sie die `s_code.js`-Datei nicht vollständig, es sei denn, Sie entfernen alle Verweise auf die Datei auf jeder Seite.
>* Ändern Sie die `trackingServer`-Variable nicht von Adobe weg. AppMeasurement sendet weiterhin Bildanforderungen, die 404-Fehler zurückgeben.

## Ich habe AppMeasurement über einen Code Analyzer ausgeführt und die Verwendung von `Math.random()` wurde als potenzielles Sicherheitsrisiko gekennzeichnet. Wird `Math.random()` mit vertraulichen Daten verwendet?

Nein. Die Zahlen, die `Math.random()` verwenden, werden nicht zum Maskieren, Senden oder Empfangen sensibler Daten verwendet. Daten, die an Datenerfassungs-Server von Adobe gesendet werden, sind auf die Sicherheit der zugrunde liegenden HTTPS-Verbindung angewiesen. <!-- AN-173590 -->

AppMeasurement verwendet `Math.random()` in drei zentralen Bereichen:

* **Sampling**: Je nach Implementierung können einige Informationen für nur einen kleinen Prozentsatz der Besucher Ihrer Site gesammelt werden. `Math.random()` bestimmt, ob ein Besucher Daten senden soll. Bei den meisten Implementierungen wird kein Sampling verwendet.
* **Fallback-Besucher-ID**: Wenn die Besucher-ID nicht aus Cookies abgerufen werden kann, wird eine zufällige Besucher-ID generiert. Dieser Teil von AppMeasurement verwendet zwei Aufrufe von `Math.random()`.
* **Zwischenspeichern von Daten**: Am Ende der Bildanforderungs-URLs wird eine zufällig ausgewählte Zahl hinzugefügt, um die Zwischenspeicherung im Browser zu verhindern.
