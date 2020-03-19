---
title: Übersicht über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die Daten aufnehmen können, die Sie an Adobe senden, um den Berichte zu verbessern.
keywords: appmeasurement,variables,vars,configuration,page,implementation
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Übersicht über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die in der Regel direkt in Berichte verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars`und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet`und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionswerte.
* **Funktionen und Methoden** sind Codeabschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den allgemeinen Funktionen gehören `t()`, `tl()`und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe Angebots bietet mehrere Möglichkeiten zur Implementierung von Adobe Analytics. Auf jeder Seite wird ein Abschnitt zur Implementierung der Variablen mithilfe von Launch und AppMeasurement für JavaScript Angebot.

## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Site eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. See [Data layer](../prepare/data-layer.md) for more information.
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. Wenn Sie Launch verwenden, wird diese Aufgabe einfach mithilfe von Datenelementen durchgeführt und das Datenelement dann einer Variablen zugewiesen. See [Data elements](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html) in the Launch user guide.
3. Rufen Sie die Verfolgungsfunktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()` Methode, jedoch einige mobile SDKs verwenden `track()`. Wenn die Verfolgungsfunktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Wagenrücklauf (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die `products` Variable behält beispielsweise Semikolons und Kommas für die Trennung von einzelnen Produkten und Kategorien bei.
