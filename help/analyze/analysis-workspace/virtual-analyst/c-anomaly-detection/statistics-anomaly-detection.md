---
description: Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.
title: In der Anomalieerkennung verwendete statistische Verfahren
uuid: b6ef6a2e-0836-4c9a-bf7e-01910199bb92
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# In der Anomalieerkennung verwendete statistische Verfahren

Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.

Je nach der im Bericht verwendeten Datumsgranularität werden 3 verschiedene statistische Verfahren eingesetzt - insbesondere zur stündlichen, täglichen, wöchentlichen/monatlichen Anomalieerkennung. Die statistischen Verfahren werden nachfolgend beschrieben.

## Anomaly detection for daily granularity {#section_758ACA3C0A6B4D399563ECABFB8316FA}

Für Berichte mit täglicher Granularität berücksichtigt der Algorithmus verschiedene wichtige Faktoren, um Ergebnisse mit höchstmöglicher Genauigkeit bereitzustellen. Erstens bestimmt der Algorithmus, welcher Modelltyp auf der Grundlage der verfügbaren Daten angewendet werden soll, von denen wir zwischen einer von zwei Klassen wählen - einem zeitreihenbasierten Modell oder einem Ausreißererkennungsmodell (als funktionale Filterung bezeichnet).

Die Entscheidung für das zeitreihenbasierte Modell beruht auf den folgenden Kombinationen für den Typ ETS (Error, Trend and Seasonality = Fehler, Trend und Saisonabhängigkeit), wie von [Hyndman und Kollegen (2008)](https://www.springer.com/us/book/9783540719168) beschrieben. Dabei versucht der Algorithmus insbesondere die folgenden Kombinationen:

1. ANA (Additive error, No trend, Additive seasonality = Additiver Fehler, Kein Trend, Additive Saisonabhängigkeit)
1. AAA (Additive error, Additive trend, Additive seasonality = Additiver Fehler, Additiver Trend, Additive Saisonabhängigkeit)
1. MNM (Multiplicative error, No trend, Multiplicative seasonality = Multiplikativer Fehler, Kein Trend, Multiplikative Saisonabhängigkeit)
1. MNA (Multiplicative error, No trend, Additive seasonality = Multiplikativer Fehler, Kein Trend, Additive Saisonabhängigkeit)
1. AAN (Additive error, Additive trend, No seasonality = Additiver Fehler, Additiver Trend, Keine Saisonabhängigkeit)

Der Algorithmus testet die Tauglichkeit jeder dieser Kombinationen, indem er die Kombination mit dem besten MAPE-Wert (Mean Absolute Percentage Error, Mittlerer absoluter prozentualer Fehler) auswählt. Liegt jedoch der MAPE-Wert des besten Zeitreihenmodells über 15 %, wird funktionale Filterung angewendet. Bei einem Zeitreihenmodell passen meist Daten mit einem hohen Grad an Wiederholbarkeit am besten (z. B. von Woche zu Woche oder von Monat zu Monat).

Nach Auswahl des Modells passt der Algorithmus die Ergebnisse basierend auf Feiertagen und jährlicher Saisonalität an. Für Feiertage überprüft der Algorithmus, ob einer der folgenden Feiertage im Datumsbereich des Berichts vorhanden ist:

* Memorial Day (nur USA)
* 4. Juli (nur USA)
* Thanksgiving (nur USA)
* Black Friday (nur USA)
* Cyber Monday (nur USA)
* 24.–26. Dezember
* 1&amp;#46; Januar
* 31. Dezember

Diese Feiertage wurden auf der Grundlage umfangreicher statistischer Analysen über viele Kundendatenpunkte ausgewählt, um Feiertage zu identifizieren, die für die meisten Kundentrends am wichtigsten waren. Obwohl die Liste sicherlich nicht für alle Kunden oder Geschäftszyklen erschöpfend ist, haben wir festgestellt, dass die Anwendung dieser Feiertage die Leistung des Algorithmus insgesamt für fast alle Kundendatensätze deutlich verbessert hat.

Nach Auswahl des Modells und der Identifizierung der im Berichtszeitraum befindlichen Feiertage fährt der Algorithmus wie folgt fort:

1. Konzipieren Sie den abweichenden Berichtszeitraum - dies umfasst bis zu 35 Tage vor dem Berichtszeitraum und einen entsprechenden Datumsbereich im Vorjahr (unter Berücksichtigung von Schalttagen, falls erforderlich, und einschließlich aller anwendbaren Feiertage, die möglicherweise an einem anderen Kalendertag im Vorjahr stattgefunden haben).
1. Er testet, ob im aktuellen Zeitraum (außer dem Vorjahr) Feiertage vorhanden sind, die laut den aktuellsten Daten eine Anomalität darstellen.
1. Wenn der Feiertag im aktuellen Datumsbereich anormal ist, passen Sie den erwarteten Wert und das Konfidenzintervall des aktuellen Feiertags in Anbetracht des Feiertags des Vorjahres an (2 Tage vor und nach). Die Korrektur für den aktuellen Feiertag erfolgt auf Grundlage des niedrigsten MAPE-Wertes von:

   1. Additive Effekte
   1. Multiplikative Effekte
   1. Differenz zum Vorjahr

Beachten Sie die dramatische Verbesserung der Leistung am Weihnachten und Neujahr im folgenden Beispiel:

![](assets/anomaly_statistics.png)

## Anomaly detection for hourly granularity {#section_014C9E9209AF43F8A03D5D46E3B3AEE7}

Stündliche Daten basieren auf der gleichen Vorgehensweise des zeitreihenbasierten Algorithmus wie beim Algorithmus für tägliche Granularität: Allerdings setzt der Algorithmus hier primär auf zwei Trendmuster: den 24-Stunden-Zyklus sowie den Wochenende-Wochentag-Zyklus. Um diese beiden saisonalen Effekte zu erfassen, erstellt der stündliche Algorithmus zwei separate Modelle (für ein Wochenende und einen Wochentag), wobei er auf die gleiche Weise wie oben beschrieben vorgeht.

Das Trainingfenster für stündliche Trends basiert auf einem 336-Stunden rückwärts gerichteten Fenster.

## Anomaly detection for weekly and monthly granularities {#section_5D421576BFBC4B24A58DFCC0A6407545}

Da wöchentliche und monatliche Trends nicht die gleichen wöchentlichen oder täglichen Trends wie bei täglicher oder stündlicher Granularität aufweisen, wird ein separater Algorithmus verwendet. Für wöchentliche oder monatliche Granularität wird ein aus zwei Schritten bestehender Ausreißererkennungsalgorithmus eingesetzt, der als GESD-Test (Generalized Extreme Studentized Deviate, Generalisierte Extreme Studentisierte Abweichung) bezeichnet wird. Dieser Test betrachtet die maximale Anzahl der zu erwartenden Anomalien kombiniert mit dem angepassten Box-Plot-Ansatz (ein nichtparametrisches Verfahren zur Erkennung von Ausreißern), um die maximale Anzahl von Ausreißern zu ermitteln. Die beiden Schritte sehen wie folgt aus:

1. Angepasste Box-Plot-Funktion: Diese Funktion ermittelt die maximale Anzahl von Anomalien aus den eingegebenen Daten.
1. GESD-Funktion: Wird mit der Ausgabe aus Schritt 1 auf die eingegebenen Daten angewendet.

Der Schritt zur Ermittlung der Anomalie bei Feiertag und YoY-Saisonabhängigkeit zieht dann die Daten des letzten Jahres von den Daten dieses Jahres ab und iteriert dann die Daten erneut mithilfe des oben beschriebenen zweistufigen Prozesses, um zu überprüfen, ob Anomalien saisonbedingt angemessen sind. Jede dieser Datumsgranularitäten verwendet ein 15 Zeiträume zurückliegendes Zeitfenster, in dem der für den Bericht ausgewählte Datumsbereich liegt (entweder 15 Monate oder 15 Wochen), sowie einen entsprechenden Datumsbereich, der 1 Jahr vor dem Trainigszeitraum liegt.
