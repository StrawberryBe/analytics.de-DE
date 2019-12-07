---
description: Die Analytics-Implementierung erfolgt in drei Hauptschritten.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Überblick über die Optimierung
topic: Developer and implementation
uuid: 8e8ecc5b-d4b1-4d13-8525-39e4924df247
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Überblick über die Optimierung

Die Analytics-Implementierung erfolgt in drei Hauptschritten.

1. Zuerst werden in jede Seite (oder Seitenvorlage) einer Website einige Zeilen HTML-Code eingefügt. Dieser HTML-Codeausschnitt ist sehr klein (400 bis 1.000 Byte) und enthält JavaScript-Variablen und andere Bezeichner, die eine Datenerfassung ermöglichen.
1. Der Codeausschnitt ruft eine Datei mit einer JavaScript-Bibliothek auf, die spezielle JavaScript-Funktionen für die Erfassung von Metriken durch Analytics enthält. Wenn der Analytics-Code korrekt implementiert ist, wird die JavaScript-Bibliotheksdatei im Browser beinahe im Handumdrehen ausgeführt.

1. Die Bibliotheksdatei richtet eine Bildanforderung an den Adobe-Datenerfassungsserver. Der Server erfasst die Daten, die übermittelt werden, und gibt ein transparentes Bild im Format 1x1 Pixel an den Browser des Besuchers zurück. Durch diesen dritten Schritt wird die Gesamtdauer für den Seitendownload nur unwesentlich verlängert.

> [!NOTE] Kunden können noch weitere Schritte durchführen, um den mit Analytics verbundenen Verwaltungsaufwand zu minimieren.

