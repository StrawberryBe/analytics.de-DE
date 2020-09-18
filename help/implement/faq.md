---
title: Häufig gestellte Fragen zur Implementierung
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 48%

---


# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

## Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID?

Der Identitätsdienst weist eine eindeutige, beständige ID zu, die von den anderen Lösungen in Experience Cloud gemeinsam genutzt werden kann. Die Analytics-Besucher-ID wird nur von Analytics verwendet. Adobe empfiehlt, den Experience Cloud-Besucher-ID-Dienst in Ihrer Implementierung zu verwenden.

## Wie wird Heartbeat-Video-Tracking implementiert?

Weitere Informationen finden Sie unter [Messen von Audio und Video in Adobe Analytics](https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html).

## Kann eine Dienstunterbrechung bei Adobe die Performance beeinträchtigen?

Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf Ihre AppMeasurement-Bibliothek auswirkt. Wenn Sie Adobe Experience Platform Launch verwenden, wird die JavaScript-Datei von Akamai oder von einem von Ihrem Unternehmen bestimmten Server-Standort gehostet.

## Kann das Senden von Daten vom Browser an die Adobe-Dienste die Performance beeinträchtigen?

AppMeasurement erstellt innerhalb der HTML-Seite ein Bildobjekt, das der Browser dann von den Adobe-Datenerfassungs-Servern anfordert. Falls der Datenerfassungs-Server sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Bildes verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Bildern durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten.

## Wie kann ich eine Analytics-Implementierung ungültig machen oder entfernen?

Manchmal möchte ein Unternehmen eine Implementierung aufgrund des Vertragsablaufs entfernen oder die Anzahl der Serveraufrufe verringern.

* **Implementierungen mit Start**: Deaktivieren oder deinstallieren Sie die Adobe Analytics-Erweiterung auf der Registerkarte &quot; [!UICONTROL Erweiterungen] &quot;und veröffentlichen Sie dann die Veröffentlichung.
* **Ältere AppMeasurement-Implementierungen**: Ersetzen Sie den gesamten Inhalt Ihrer `s_code.js` Datei durch die folgende Codezeile:

```js
var s = new Object();
```

>[!WARNING]
>
>Nicht anwenden:
>
>* Ändern Sie die Report Suite in einen ungültigen Wert, da dies zu unnötiger Belastung auf den Servern der Adobe führt.
>* Entfernen Sie die `s_code.js` Datei ganz, es sei denn, Sie entfernen alle Verweise auf die Datei auf jeder Seite.
>* Ändern Sie die `trackingServer` Variable so, dass sie von der Adobe abweicht. AppMeasurement sendet weiterhin Bildanforderungen, die 404-Fehler zurückgeben.


## Ich habe AppMeasurement über einen Code-Analyzer ausgeführt und seine Verwendung als potenzielles Sicherheitsrisiko markiert `Math.random()` . Wird mit vertraulichen Daten `Math.random()` verwendet?

Nein. Die Zahlen, die verwendet `Math.random()` werden, werden nicht zum Maskieren, Senden oder Empfangen sensibler Daten verwendet. Daten, die an Datenerfassungsserver der Adobe gesendet werden, hängen von der Sicherheit der zugrunde liegenden HTTPS-Verbindung ab. <!-- AN-173590 -->

AppMeasurement verwendet `Math.random()` drei Schlüsselbereiche:

* **Probenahme**: Je nach Implementierung können einige Informationen für nur einen kleinen Prozentsatz der Besucher Ihrer Site gesammelt werden. `Math.random()` bestimmt, ob ein Besucher Daten senden soll. Bei den meisten Implementierungen wird kein Sampling verwendet.
* **Fallback-Besucher-ID**: Wenn die Besucher-ID nicht aus Cookies abgerufen werden kann, wird eine zufällige Besucher-ID generiert. Dieser Teil von AppMeasurement verwendet zwei Aufrufe an `Math.random()`.
* **Cache-Busting**: Am Ende der Bildanforderungs-URLs wird eine Zufallszahl hinzugefügt, um die Zwischenspeicherung im Browser zu verhindern.
