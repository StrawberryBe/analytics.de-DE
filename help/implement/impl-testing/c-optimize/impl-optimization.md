---
description: Die Analytics-Implementierung erfolgt in drei Hauptschritten.
keywords: Analytics-Implementierung
seo-description: Die Analytics-Implementierung erfolgt in drei Hauptschritten.
seo-title: Optimierungsübersicht
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Optimierungsübersicht
topic: Entwickler und Implementierung
uuid: 8 e 8 ecc 5 b-d 4 b 1-4 d 13-8525-39 e 4924 df 247
translation-type: tm+mt
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# Optimierungsübersicht

Die Analytics-Implementierung erfolgt in drei Hauptschritten.

1. Zuerst werden in jede Seite (oder Seitenvorlage) einer Website einige Zeilen HTML-Code eingefügt. Dieser HTML-Codeausschnitt ist sehr klein (400 bis 1.000 Byte) und enthält JavaScript-Variablen und andere Bezeichner, die eine Datenerfassung ermöglichen.
1. Der Codeausschnitt ruft eine Datei mit einer JavaScript-Bibliothek auf, die spezielle JavaScript-Funktionen für die Erfassung von Metriken durch Analytics enthält. Wenn der Analytics-Code korrekt implementiert ist, wird die JavaScript-Bibliotheksdatei im Browser beinahe im Handumdrehen ausgeführt.

1. Die Bibliotheksdatei richtet eine Bildanforderung an den Adobe-Datenerfassungsserver. Der Server erfasst die Daten, die übermittelt werden, und gibt ein transparentes Bild im Format 1x1 Pixel an den Browser des Besuchers zurück. Durch diesen dritten Schritt wird die Gesamtdauer für den Seitendownload nur unwesentlich verlängert.

>[!NOTE]
>
>Kunden können weitere Schritte ergreifen, um Analytics-Aufwand zu minimieren.

