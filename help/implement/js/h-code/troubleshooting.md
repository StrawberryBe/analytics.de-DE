---
title: Fehlerbehebung bei H-Code-Implementierungen
description: Erfahren Sie mehr über einige häufige Probleme bei älteren JavaScript-Implementierungen.
translation-type: tm+mt
source-git-commit: 69138bdedb42b66449426fee39822520ee4b1198

---


# Fehlerbehebung bei H-Code-Implementierungen

Im Folgenden finden Sie Anweisungen zur Fehlerbehebung, die spezifisch für H-Code-Implementierungen gelten.

## Analytics-Code im Head-Tag platzieren

> [!NOTE] Bei H-Code-Implementierungen muss im Tag auf Code verwiesen werden, bei anderen Implementierungen (z. B. beim Einsatz von Adobe Experience Platform Launch) muss im Tag auf Code verwiesen werden `<body>` , der `<head>` verwendet wird.

Analytics-Code erstellt ein unsichtbares 1x1-Pixelbild. Zuvor bestand eine gängige Implementierungsmethode darin, den `s_code.js` Verweis in das `<head>` -Tag zu setzen. Die Platzierung des Codes hier verhinderte, dass das Bild das Seitenlayout in irgendeiner Weise beeinflusst. Es wird auch früher ausgeführt, sodass Sie Seitenansichten für teilweise Seitenladevorgänge effizienter zählen können.

However, certain elements of the code require the existence of the `<body>` object. Wenn sich der Analytics-JavaScript-Code im Tag befindet, wird er ausgeführt, bevor das `<head>` Objekt vorhanden `<body>` ist. As a result, your implementation does not collect [!UICONTROL ClickMap] data, automatic tracking of file downloads or exit links, or connection type data. Die Platzierung des Skriptverweises `s_code.js` im `<head>` -Tag funktioniert, aber das Ergebnis ist eine sehr begrenzte Version von Analytics.

The Analytics code can be placed anywhere inside the `<body>` tag of a well-formed HTML page. Adobe empfiehlt, Analytics-Code so nah wie möglich am Anfang des `<body>` Tags zu platzieren. Stellen Sie sicher, dass alle Seitenvariablen festgelegt werden, nachdem die `s_code.js` Datei geladen wurde.

> [!TIP] Wenn Sie Adobe Analytics in Adobe Target integrieren möchten, muss die JavaScript-Include-Datei unten auf der Seite platziert werden.
