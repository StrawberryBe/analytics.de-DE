---
title: Personen
description: Die Anzahl der Einzelanwender, üblicherweise mit mehreren Geräten.
exl-id: 0136b843-2a1e-44d5-b5a6-e0fb03b7b995
source-git-commit: 639897682c9a28df7dc642dd7c68ad992fde40a9
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 49%

---

# Personen

Es gibt zwei Versionen der Metrik für Personen.

Bei Mitgliedern der [Gerätekooperation](https://experienceleague.adobe.com/docs/device-co-op/using/data/people.html?lang=de), die nicht [geräteübergreifende Analysen](../cda/overview.md) verwenden, ist die Metrik für Personen die statistisch abgeleitete Anzahl der Personen, die im Bericht repräsentiert sind. Es ist die Anzahl der Besucher-IDs, die durch die Gerätekooperation identifiziert werden, zuzüglich der Anzahl der Geräte, die nicht durch die Kooperation identifiziert werden.

Innerhalb einer Virtual Report Suite [Cross-Device Analytics](../cda/overview.md) ist die Metrik &quot;Personen&quot;keine statistische Ableitung. Stattdessen handelt es sich um die Summe der Personen, die im Bericht identifiziert werden, plus die Anzahl der Geräte, die nicht als einer Person zugehörig identifiziert werden.

Wird ein Besucher während des Besuchs identifiziert, kann dieser Besucher als 2 Personen zählen (1 nicht identifizierte Person und 1 identifizierte Person). [](/help/components/cda/replay.md) Diese doppelte Zählung wird anhand des Berichtsfensters, der Häufigkeit der Wiederholungen und der Erfolgsrate reduziert. Weitere Informationen finden Sie unter [Eindeutige Geräte](unique-devices.md) .
