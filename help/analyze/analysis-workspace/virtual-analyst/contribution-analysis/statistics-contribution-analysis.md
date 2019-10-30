---
description: Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.
seo-description: Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.
seo-title: In der Beitragsanalyse verwendete statistische Verfahren
title: In der Beitragsanalyse verwendete statistische Verfahren
uuid: f77eb4e4-4fd6-4397-b8a8-a063f199b676
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# In der Beitragsanalyse verwendete statistische Verfahren

Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. Damit soll dem Benutzer geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysieren viel schneller zu identifizieren.

Die Beitragsanalyse erreicht dies, indem sie einen zweiteiligen Algorithmus zu jedem einzelnen Dimensionselement durchführt, das dem Beitragsanalysebericht des Benutzers zur Verfügung steht. Dabei geht der Algorithmus in der folgenden Reihenfolge vor:

1. Für jede Dimension wird die V-Teststatistik von Cramer berechnet. Im folgenden Beispiel sehen Sie eine Kontingenztabelle mit Seitenansichten nach Ländern über zwei Zeitperioden:

   ![](assets/contingency_table.png)

   In Tabelle 1 kann Cramers V verwendet werden, um den Zusammenhang zwischen den Seitenansichten nach Ländern für den Zeitraum 1 (z. B. historisch) und den Zeitraum 2 (z. B. den Tag, an dem die Anomalie aufgetreten ist) zu messen. Ein niedriger Wert für Cramers V impliziert eine niedrige Assoziation. Cramers V liegt zwischen 0 (kein Zusammenhang) und 1 (vollständiger Zusammenhang). Die Cramer V-Statistik kann berechnet werden:

   ![](assets/cramers-v.png)

1. Für jedes Dimensionselement wird der PR-Wert (Person's Residual, Restwert der Person) verwendet, um die Verbindung zwischen der anormalen Metrik und jedem Dimensionselement zu messen. Da der PR-Wert einer gewöhnlichen Normalverteilung folgt, kann der Algorithmus die PRs von zwei zufälligen Variablen miteinander vergleichen, selbst wenn die Abweichungen nicht vergleichbar sind. In der Praxis ist der Fehler nicht bekannt und wird mittels finiter Stichprobenkorrektur abgeschätzt.

   In der vorherigen Beispieltabelle 1 wird der PR mittels finiter Stichprobenkorrektur für das Land i und den Zeitraum 2 angegeben durch

   ![](assets/persons-residual.png)

   Hier,

   ![](assets/pr-example.png)

   (Eine ähnliche Formel kann für den Zeitraum 1 genommen werden.)

   Für die Endergebnisse wird das Ergebnis für jedes Dimensionselement durch die Cramer-V-Messung gewichtet und auf eine Zahl zwischen 0 und 1 skaliert, um den Beitragswert zu ermitteln.

