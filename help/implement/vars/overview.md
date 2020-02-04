---
title: Übersicht über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die an Adobe gesendeten Daten aufnehmen können, um die Berichterstellung zu verbessern.
keywords: appmeasurement,variables,vars,configuration,page,implementation
translation-type: tm+mt
source-git-commit: 7a1c3c7ed0e509969e281e865e8ff2c969a18bcb

---


# Übersicht über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die normalerweise direkt in Berichten verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars`und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet`und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionswerte.
* **Funktionen und Methoden** sind Codeabschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den allgemeinen Funktionen gehören `t()`, `tl()`und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe bietet mehrere Möglichkeiten zur Implementierung von Adobe Analytics. Jede Seite enthält einen Abschnitt zur Implementierung der Variablen mit Launch und AppMeasurement für JavaScript.

## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Site eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. See [Data layer](../prepare/data-layer.md) for more information.
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. Wenn Sie Launch verwenden, ist diese Aufgabe einfach zu bewältigen, indem Sie Datenelemente verwenden und dann das Datenelement einer Variablen zuweisen. Siehe [Datenelemente](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html) im Benutzerhandbuch zum Starten.
3. Rufen Sie die Verfolgungsfunktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()` Funktion, jedoch einige mobile SDKs verwenden `track()`. Wenn die Verfolgungsfunktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Wagenrücklauf (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die `products` Variable behält beispielsweise Semikolons und Kommas vor, um separate Produkte und Kategorien zu trennen.
