---
title: Neue Interaktionen
description: Die Häufigkeit, mit der ein Erstkontakt-Kanal eingestellt wird.
feature: Metrics
exl-id: a419d048-9715-4d7b-9c24-d34129755371
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 83%

---

# Neue Interaktionen

Die &quot;neuen Interaktionen&quot; [Metrik](overview.md) zeigt an, wie oft ein Besucher im Interaktionszeitraum des Besuchers zum ersten Mal mit einem Marketing-Kanal übereinstimmt. Diese Metrik ist nützlich, wenn Sie eine beliebige Dimension mit einem Besucher vergleichen möchten, der zum ersten Mal mit einer Verarbeitungsregel für einen Marketing-Kanal übereinstimmt.

## Berechnung dieser Metrik

Während der Datenverarbeitung durchläuft jeder Treffer die [Verarbeitungsregeln für Marketing-Kanäle](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md). Wenn ein Treffer mit einer Marketing-Kanal-Verarbeitungsregel übereinstimmt und der Besucher noch keinen Erstkontakt-Kanal hat, handelt es sich bei dem Treffer um eine neue Interaktion. Wenn ein Treffer nicht mit den Verarbeitungsregeln für Marketing-Kanäle übereinstimmt oder wenn der Besucher bereits über einen Erstkontakt-Kanal verfügt, handelt es sich bei dem Treffer nicht um eine neue Interaktion.

Besucher können über mehr als eine neue Interaktion verfügen, wenn sie ihre Interaktionszeit ablaufen lassen.
