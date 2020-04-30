---
description: Zeigt den Prozentsatz der Besuche mit einem einzelnen Hit an.
title: Absprungrate
topic: Metrics
uuid: 9a5aba33-c16a-47db-b8d3-f66be6eb65be
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Absprungrate

Zeigt den Prozentsatz der Besuche mit einem einzelnen Hit an.

Die Absprungrate verwendet die Metrik  [Absprünge](/help/components/c-variables/c-metrics/metrics-bounces.md) und wird wie folgt berechnet:

`Bounces divided by Entries`

Die Absprungrate beinhaltet keine Besuche, bei denen auf einer einzigen Seite mehrere Aktionen aufgetreten sind. Beispiel: Ein Besuch mit angeschautem Video auf einer Einzelseite gilt als Einzelzugriff, nicht als Absprung.

>[!NOTE] Bestehende Implementierungen können manchmal eine berechnete Metrik enthalten, die von der Analytics-Standard-Metrik abweicht. Prüfen Sie die Definition der berechneten Metrik, um sicherzustellen, dass es keine Abweichungen gibt.

Weitere Informationen finden Sie in diesem [Knowledge Base-Artikel](https://helpx.adobe.com/analytics/kb/comparing-bounces-and-single-access.html).
