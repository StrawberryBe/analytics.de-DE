---
title: Personen
description: Die Anzahl der Einzelanwender, üblicherweise mit mehreren Geräten.
feature: Metrics
exl-id: 0136b843-2a1e-44d5-b5a6-e0fb03b7b995
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 100%

---

# Personen

Es gibt zwei Versionen der Metrik für Personen.

Bei Mitgliedern der [Gerätekooperation](https://experienceleague.adobe.com/docs/device-co-op/using/data/people.html?lang=de), die nicht [geräteübergreifende Analysen](../cda/overview.md) verwenden, ist die Metrik für Personen die statistisch abgeleitete Anzahl der Personen, die im Bericht repräsentiert sind. Es ist die Anzahl der Besucher-IDs, die durch die Gerätekooperation identifiziert werden, zuzüglich der Anzahl der Geräte, die nicht durch die Kooperation identifiziert werden.

Bei der Metrik „Personen“ in einer Virtual Report Suite in [Cross-Device Analytics](../cda/overview.md) handelt es sich um keine statistische Ableitung. Stattdessen wird unter „Personen“ die Summe der Einzelanwender zusammengefasst, die im Bericht identifiziert wurden, zuzüglich der Anzahl der Geräte, die nicht als zu einer Person gehörend identifiziert wurden.

Wird ein Besucher während eines Besuchs identifiziert, kann dieser Besucher als zwei Personen gezählt werden (1 nicht identifizierte Person und 1 identifizierte Person). Durch [Wiederholen](/help/components/cda/replay.md) kann diese doppelte Zählung abhängig vom Berichtsfenster, von der Häufigkeit der Wiederholung und von der Erfolgsrate verhindert werden. Weitere Informationen finden Sie unter [Eindeutige Geräte](unique-devices.md).
