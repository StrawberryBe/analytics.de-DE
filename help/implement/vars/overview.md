---
title: Übersicht über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die an Adobe gesendeten Daten aufnehmen können, um die Berichterstellung zu verbessern.
keywords: Appmeasurement;Variablen;Vars;Konfiguration;Seite;Implementierung
feature: Variables
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
source-git-commit: 1516a1353c1b0a3b7365c3e3f10ce74ae1255696
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 70%

---

# Übersicht über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die normalerweise direkt in Berichten verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars` und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet` und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionselemente.
* **Funktionen und Methoden** sind Code-Abschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den gebräuchlichen Funktionen gehören `t()`, `tl()` und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe bietet mehrere Möglichkeiten, Adobe Analytics zu implementieren. Jede Seite enthält einen Abschnitt zur Implementierung der Variablen mithilfe des Web SDK, mithilfe der Adobe Analytics-Erweiterung und mithilfe von AppMeasurement für JavaScript.

Hier finden Sie ein Video zum Konfigurieren von Variablen in Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/28755/?quality=12)

## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Website eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. Beispiel: Sie füllen `adobeDataLayer.page.title` mit dem Seitentitel. Weitere Informationen finden Sie unter [Datenschicht](../prepare/data-layer.md).
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. <br/>Wenn Sie Tags in Adobe Experience Platform verwenden, erfolgt dies durch die Verwendung von Datenelementen dazwischen. Datenelemente werden mit Werten aus der Datenschicht gefüllt. Beispiel für ein Datenelement `Page Title` ruft den Wert aus der Datenschichtvariablen ab `adobeDataLayer.page.title`. <br/>Anschließend können Sie das Datenelement verwenden, um Analytics-Variablen zu füllen. Beispiel `eVar4` ruft den Wert aus dem Datenelement ab `Page Title`. <br/>Weitere Informationen finden Sie unter [Datenelemente](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=de), [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md)und [Tag-Datenelemente Analytics-Variablen zuordnen](../launch/elements-to-variable.md)
3. Rufen Sie schließlich die Tracking-Funktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()`-Methode, doch einige mobile SDKs verwenden `track()`. Wenn die Tracking-Funktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Zeilenumschalter (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die [`products`](page-vars/products.md)-Variable behält beispielsweise Semikolons und Kommas vor, um separate Produkte und Kategorien zu trennen.
