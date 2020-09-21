---
title: Übersicht über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die an Adobe gesendeten Daten aufnehmen können, um die Berichterstellung zu verbessern.
keywords: appmeasurement,variables,vars,configuration,page,implementation
translation-type: ht
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: ht
source-wordcount: '318'
ht-degree: 100%

---


# Übersicht über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die normalerweise direkt in Berichten verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars` und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet` und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionselemente.
* **Funktionen und Methoden** sind Code-Abschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den gebräuchlichen Funktionen gehören `t()`, `tl()` und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe bietet mehrere Möglichkeiten, Adobe Analytics zu implementieren. Jede Seite enthält einen Abschnitt zur Implementierung der Variablen mit Launch und AppMeasurement für JavaScript.

## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Website eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. Weitere Informationen finden Sie unter [Datenschicht](../prepare/data-layer.md).
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. Wenn Sie Launch verwenden, ist diese Aufgabe einfach zu bewältigen, indem Sie Datenelemente verwenden und dann das Datenelement einer Variablen zuweisen. Siehe [Datenelemente](https://docs.adobe.com/content/help/de-DE/launch/using/reference/manage-resources/data-elements.html) im Launch-Benutzerhandbuch.
3. Rufen Sie die Tracking-Funktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()`-Methode, doch einige mobile SDKs verwenden `track()`. Wenn die Tracking-Funktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Zeilenumschalter (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die [`products`](page-vars/products.md)-Variable behält beispielsweise Semikolons und Kommas vor, um separate Produkte und Kategorien zu trennen.
