---
description: Informationen
title: Metriktyp und Attribution
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 75%

---

# Metriktyp und Attribution

Wann [Erstellen einer berechneten Metrik](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)können Sie den Metriktyp und das Attributionsmodell angeben.

## Metriktyp

So legen Sie den Metriktyp beim Erstellen einer berechneten Metrik fest:

1. Wählen Sie das Zahnradsymbol neben der Metrik aus, deren Typ Sie auswählen möchten.

   ![](assets/cm_type_alloc.png)

1. Wählen Sie aus den folgenden Optionen:

   | Metriktyp | Definition |
   |---|---|
   | Standard | Diese Metriken sind dieselben, die auch in der Standard-[!DNL Analytics]-Berichterstellung verwendet werden. Wenn eine Formel aus einer einzelnen Standardmetrik besteht, zeigt sie die gleichen Daten wie das nicht berechnete Metrikgegenstück an. Standardmetriken eignen sich zum Erstellen berechneter Metriken, die speziell für die einzelnen Einzelposten gelten. Beispiel: [Bestellungen]/[Besuche] teilt die Bestellungen für diesen Einzelposten durch die Anzahl der Besuche für den Posten. |
   | Gesamtsumme | Verwenden Sie in jedem Zeileneintrag die Gesamtsumme für den Berichtszeitraum. Wenn eine Formel aus einer einzelnen Gesamtmetrik bestand, wird für jeden Zeileneintrag dieselbe Gesamtanzahl angezeigt. Gesamtmetriken sind nützlich für die Erstellung berechneter Metriken, die mit den Gesamtdaten der Site vergleichen. Beispiel: [Bestellungen]/[Gesamtbesuche] zeigt den Anteil der Bestellungen für ALLE Site-Besuche und nicht nur die Besuche für den speziellen Zeileneintrag. |

## Funktionsweise der linearen Zuordnung

[Attribution](/help/analyze/analysis-workspace/attribution/overview.md) gibt an, wie Zuordnungsmodelle in berechneten Metriken ausgewertet werden.

Eine vollständige Liste der nicht standardmäßigen Attributionsmodelle und unterstützten Lookback-Fenster finden Sie unter [Attributionsmodelle und Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md).

Das folgende Beispiel zeigt, wie berechnete Metriken mit linearen Zuordnungen in Berichten funktionieren:

| | Treffer 1 | Treffer 2 | Treffer 3 | Treffer 4 | Treffer 5 | Treffer 6 | Treffer 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Eingereichte Daten | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |
| Letztkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | 10$ |
| Erstkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | 10$ |
| Beispieleigenschaft | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |

In diesem Beispiel wurden die Werte A, B und C in eine Variable für die Treffer 1, 3, 4 und 6 gesendet, bevor ein Kauf in Höhe von 10 USD bei Treffer 7 getätigt wurde. In der zweiten Zeile werden dieses Werte bei Treffern auf Grundlage von Letztkontaktbesuchen gespeichert. In der dritten Zeile wird das Speichern auf Grundlage des Erstkontaktbesuchs dargestellt. Zu guter Letzt stellt die letzte Zeile dar, wie Daten aus einer Eigenschaft aufgezeichnet würden, bei denen kein Speichern vorgesehen ist.

## Unterschiede in der Funktionsweise der linearen Zuordnung in Reports &amp; Analytics im Vergleich zu Workspace

Es gibt einige Unterschiede in der Funktionsweise der linearen Attribution zwischen diesen beiden Tools:

* In Reports &amp; Analytics ist die (verarbeitete) lineare Attribution immer besuchsbasiert, während sie in Workspace besuchs- oder besuchsbasiert sein kann.
* Wenn in Reports &amp; Analytics beim ersten Treffer eines Besuchs kein Wert übergeben wurde, bleibt der (anfängliche) Wert des vorherigen Besuchs erhalten. Dies ist in Workspace NICHT der Fall (Attribution). Wenn beim ersten Treffer eines Besuchs kein Wert übergeben wird, ist „Keine“ der Ausgangswert.
