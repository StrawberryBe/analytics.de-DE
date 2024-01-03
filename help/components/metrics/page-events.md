---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: a7434f72159a575f9ad7bf29644cb17777382df7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 40%

---

# Seitenereignisse

Die &quot;Seitenereignisse&quot; [Metrik](overview.md) zeigt an, wie oft ein Linktracking-Aufruf ausgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

## Berechnung dieser Metrik

Diese Metrik zählt alle [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) in einer Report Suite. Alle Linktypen sind in dieser Metrik enthalten, insbesondere [Benutzerspezifische Links](../dimensions/custom-link.md), [Downloadlinks](../dimensions/download-link.md), und [Exitlinks](../dimensions/exit-link.md). Sie umfasst nicht [Seitenansichts-Tracking-Aufrufe (`t()`)](/help/implement/vars/functions/t-method.md).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse vs. [Seitenansichten](page-views.md)**: Seitenereignisse zählen die Anzahl der Linktracking-Aufrufe (`tl()`) und schließen Seitenansichts-Tracking-Aufrufe (`t()`). Seitenansichten sind das Gegenteil. Sie zählt die Anzahl der Seitenansicht-Tracking-Aufrufe und schließt Links aus.
