---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 205d86b13046bd17e321734904bf57435ef6e106
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 33%

---

# Seitenereignisse

Die &quot;Seitenereignisse&quot; [Metrik](overview.md) zeigt an, wie oft ein Linktracking-Aufruf ausgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

So kann ein Besucher beispielsweise auf einer typischen Journey einer E-Commerce-Site mehrere Interaktionen auf einer Seite haben. Bei einer typischen Analytics-Implementierung sind diese Interaktionen als Linktracking konfiguriert ([`tl()`](/help/implement/vars/functions/tl-method.md)) aufrufen, während eine Seitenansicht ([`t()`](/help/implement/vars/functions/t-method.md)) ist für das erste Laden der Seite reserviert. Diese Implementierungsmethode bietet eine erweiterte Ereignisverfolgung, die Aufschluss darüber gibt, welche Interaktionen stattfinden, bevor ein Besucher seine Journey fortsetzt.

## Berechnung dieser Metrik

Diese Metrik zählt alle Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) in einer Report Suite. Alle Linktypen sind in dieser Metrik enthalten, insbesondere [Benutzerspezifische Links](../dimensions/custom-link.md), [Downloadlinks](../dimensions/download-link.md), und [Exitlinks](../dimensions/exit-link.md). Sie enthält keine Seitenansichtsaufrufe ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse vs. [Seitenansichten](page-views.md)**: Seitenereignisse zählen die Anzahl der Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und schließen Seitenansichts-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)). Seitenansichten sind das Gegenteil. Sie zählt die Anzahl der Seitenansicht-Tracking-Aufrufe und schließt Links aus.
