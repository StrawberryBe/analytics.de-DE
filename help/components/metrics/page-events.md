---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 5e70a84c7793b516c0eca2776d8bbfd3ea3fc02b
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 60%

---

# Seitenereignisse

Die Metrik „Seitenereignisse“ gibt an, wie oft ein Linktracking-Aufruf ausgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

## Berechnung dieser Metrik

Diese Metrik zählt alle [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) in einer Report Suite. Alle Link-Typen sind enthalten (benutzerspezifische Links, Downloadlinks und Exitlinks). Sie umfasst nicht [Seitenansichts-Tracking-Aufrufe (`t()`)](/help/implement/vars/functions/t-method.md).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse vs. [Seitenansichten](page-views.md)**: Seitenereignisse zählen die Anzahl der Linktracking-Aufrufe (`tl()`) und schließen Seitenansichts-Tracking-Aufrufe (`t()`). Seitenansichten sind das Gegenteil. Sie zählt die Anzahl der Seitenansicht-Tracking-Aufrufe und schließt Links aus.
