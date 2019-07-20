---
description: Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.
seo-description: Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.
seo-title: Statistische Verfahren, die in der Beitragsanalyse verwendet werden
title: Statistische Verfahren, die in der Beitragsanalyse verwendet werden
uuid: f 77 eb 4 e 4-4 fd 6-4397-b 8 a 8-a 063 f 199 b 676
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Statistische Verfahren, die in der Beitragsanalyse verwendet werden

Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.

Die Beitragsanalyse erreicht dies durch Ausführung eines zweiteiligen Algorithmus für jedes einzelne Dimensionselement, das für den Beitragsanalysebericht des Benutzers verfügbar ist. Dabei geht der Algorithmus in der folgenden Reihenfolge vor:

1. Er berechnet für jede Dimension die V-Test-Statistik nach Cramer. Im folgenden Beispiel sehen Sie eine Kontingenztabelle mit Seitenansichten nach Ländern über zwei Zeitperioden:

   ![](assets/contingency_table.png)

   In Tabelle 1 kann mit Cramers V der Zusammenhang zwischen den Seitenansichten nach Ländern für den Zeitraum 1 (z. B. historische Daten) und den Zeitraum 2 (z. B. der Tag, an dem die Anomalie aufgetreten ist) gemessen werden. Ein niedriger Wert für Cramers V bedeutet einen niedrigen Grad an Zusammenhang. Werte für Cramers V liegen zwischen 0 (kein Zusammenhang) und 1 (vollständiger Zusammenhang). Die Cramer-V-Statistik kann wie folgt berechnet werden:

   ![](assets/cramers-v.png)

1. Für jedes Dimensionselement wird der PR-Wert (Person’s Residual, Restwert der Person) verwendet, um den Zusammenhang zwischen der anormalen Metrik und den einzelnen Dimensionselementen zu messen. Da der PR-Wert einer gewöhnlichen Normalverteilung folgt, kann der Algorithmus die PRs von zwei zufälligen Variablen miteinander vergleichen, selbst wenn die Abweichungen nicht vergleichbar sind. In der Praxis ist der Fehler nicht bekannt und wird mittels finiter Stichprobenkorrektur abgeschätzt.

   In der vorherigen Beispieltabelle 1 wird der PR mittels finiter Stichprobenkorrektur für das Land i und den Zeitraum 2 angegeben durch

   ![](assets/persons-residual.png)

   Hier,

   ![](assets/pr-example.png)

   (Eine ähnliche Formel kann für den Zeitraum 1 genommen werden.)

   Für die Endergebnisse wird die Bewertung von jedem Dimensionselement dann mit dem Cramer-V-Messwert gewichtet und in einen Wert zwischen 0 und 1 skaliert, um dessen Beitragsbewertung zu erhalten.

