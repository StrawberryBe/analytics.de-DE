---
description: Die Analytics-Implementierung erfolgt in drei Hauptschritten.
keywords: Analytics-Implementierung
seo-description: Die Analytics-Implementierung erfolgt in drei Hauptschritten.
seo-title: Überblick über die Optimierung
solution: Analytics
subtopic: Fehlerbehebung
title: Überblick über die Optimierung
topic: Entwickler und Implementierung
uuid: 8e8ecc5b-d4b1-4d13-8525-39e4924df247
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Überblick über die Optimierung

Die Analytics-Implementierung erfolgt in drei Hauptschritten.

1. Zuerst werden in jede Seite (oder Seitenvorlage) einer Website einige Zeilen HTML-Code eingefügt. Dieser HTML-Codeausschnitt ist sehr klein (400 bis 1.000 Byte) und enthält JavaScript-Variablen und andere Bezeichner, die eine Datenerfassung ermöglichen.
1. Der Codeausschnitt ruft eine Datei mit einer JavaScript-Bibliothek auf, die spezielle JavaScript-Funktionen für die Erfassung von Metriken durch Analytics enthält. Wenn der Analytics-Code korrekt implementiert ist, wird die JavaScript-Bibliotheksdatei im Browser beinahe im Handumdrehen ausgeführt.

1. Die Bibliotheksdatei richtet eine Bildanforderung an den Adobe-Datenerfassungsserver. Der Server erfasst die Daten, die übermittelt werden, und gibt ein transparentes Bild im Format 1x1 Pixel an den Browser des Besuchers zurück. Durch diesen dritten Schritt wird die Gesamtdauer für den Seitendownload nur unwesentlich verlängert.

> [!NOTE] Kunden können noch weitere Schritte durchführen, um den mit Analytics verbundenen Verwaltungsaufwand zu minimieren.

