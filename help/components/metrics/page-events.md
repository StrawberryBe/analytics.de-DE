---
title: Ereignisse der Seite
description: Die Anzahl der ausgelösten Linkverfolgungsaktionen.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Ereignisse der Seite

Die Metrik &quot;Ereignisse der Seite&quot;zeigt an, wie oft ein Link-Verfolgungsaufruf durchgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion durchführen kann, ohne zu einer neuen Seite zu navigieren.

## Berechnung dieser Metrik

Diese Metrik zählt alle Link-Verfolgungsaufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) in einer Report Suite. Alle Linktypen sind enthalten (benutzerspezifische Links, Downloadlinks und Exitlinks). Es enthält keine Verfolgungsaufrufe für die Ansicht von Seiten ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergleichen mit ähnlichen Metriken

* **Seiten-Ereignis oder[Seiten-Ansichten](page-views.md)**: Seitenaufrufe zählen die Anzahl der Linktracking-Ereignis (`tl()`) und schließen Seitenverfolgungsaufrufe (`t()`) aus. Die Ansichten der Seite sind umgekehrt. Es zählt die Anzahl der Seitenverfolgungsaufrufe und schließt Links aus.
