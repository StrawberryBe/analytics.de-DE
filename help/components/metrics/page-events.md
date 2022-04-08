---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '143'
ht-degree: 100%

---

# Seitenereignisse

Die Metrik „Seitenereignisse“ gibt an, wie oft ein Linktracking-Aufruf ausgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

## Berechnung dieser Metrik

Diese Metrik zählt alle Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) in einer Report Suite. Alle Link-Typen sind enthalten (benutzerspezifische Links, Downloadlinks und Exitlinks). Sie enthält keine Tracking-Aufrufe für Seitenansichten ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse im Vergleich zu [Seitenansichten](page-views.md)**: „Seitenereignisse“ zählt die Anzahl der Linktracking-Tracking-Aufrufe (`tl()`) und schließen Seitenansicht-Tracking-Aufrufe (`t()`) aus. „Seitenansichten“ im Gegensatz dazu zählt die Anzahl der Seitenansicht-Tracking-Aufrufe und schließt Links aus.
