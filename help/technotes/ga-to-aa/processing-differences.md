---
title: Unterschiede bei der Verarbeitung und Architektur von Analytics-Plattformen
description: Hier erfahren Sie, wie einige Daten gesammelt und auf unterschiedliche Weise zwischen Plattformen wie Adobe Analytics und Google Analytics angezeigt werden.
translation-type: tm+mt
source-git-commit: a5f612ba5e8446a56bc2bd252a8781e8ab1de403

---


# Unterschiede bei der Verarbeitung und Architektur von Analytics-Plattformen

Obwohl Adobe Analytics und Google Analytics beide Analytics-Tools sind, unterscheidet sich die Art und Weise, wie Daten zwischen Plattformen gesammelt und verarbeitet werden, sehr unterschiedlich. Auf dieser Seite können Sie einige der Hauptunterschiede in Bezug darauf verstehen, wie bestimmte Dimensionen und Metriken erfasst werden und warum sie in ähnlichen Berichten möglicherweise verschiedene Zahlen anzeigen.

## Absprungrate

Die Absprungrate ist ein häufig verwendeter KPI, mit dem die Effektivität und Relevanz von Einstiegsseiten in den meisten Analysetools gemessen werden. Dies wird häufig als Besuche definiert, die die Website besuchen, aber keinen Klick auf eine andere Seite enthalten.

* In Adobe Analytics, Bounce Rate is calculated using the formula **Bounces divided by Entries**.
* In Google Analytics, Bounce Rate is calculated using the formula **Single-page sessions divided by Sessions**.

Wenn mehrere Treffer auf beiden Plattformen an denselben Besuch oder dieselbe Sitzung gesendet werden, wird sie nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und allgemein allgemein, die verhindern, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet in der Regel nicht mehr als eine Datenanforderung auf derselben Seite.

Um eine bessere Gleichheit zwischen den Berichtstools zu erzielen, verwenden Sie die Metrik Einzelseitenbesuche in Adobe Analytics anstelle von Absprünge als Teil einer berechneten Metrik. Die Metrik "Einzelseitenbesuche" enthält die Gesamtzahl der Besuche, die nur eine Seitenansicht enthalten, oder Besuche, die die Website besuchen, aber keinen Klick zu einer anderen Seite enthalten.

See the [Bounce Rate](../../components/c-variables/c-metrics/metrics-bounce-rate.md) metric in the Components user guide for more information.

## Besuche und Sitzungen

Besuche (als Sitzungen in Google Analytics bezeichnet) sind eine Gruppe von Seitenansichten, die denselben Benutzer in kurzer Zeit aufrufen. Besuche auf beiden Plattformen laufen normalerweise nach 30 Minuten Inaktivität ab. Beide Plattformen ermöglichen die Anpassung eines Besuchs. Es gibt verschiedene Szenarien, die Unterschiede auf jeder Plattform verursachen können.

* **Enddatum:** Alle Sitzungen in Google Analytics laufen nach 12.59 PM an einem bestimmten Tag ab. Wenn der Benutzer nach 12 Uhr noch aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics besucht als Teil desselben Besuchs die Besuche am folgenden Tag.
* **Verschiedene Kampagnen:** Eine neue Sitzung in Google Analytics beginnt, wenn sich die Kampagnenquelle eines Benutzers ändert. Wenn in Adobe Analytics ein neuer Rückverfolgungscode-Wert angezeigt wird, gilt er als Teil desselben Besuchs.
* **Manuelle Sitzung überschreiben:** Eine neue Sitzung in Google Analytics beginnt, wenn Sie eine `sessionControl` Sitzung manuell starten oder beenden. Besuche können nicht manuell in Adobe Analytics beendet werden.
* **Ausreißer-Besucherkennung in Adobe Analytics:** Ein neuer Besuch in Adobe Analytics beginnt automatisch, wenn ein Benutzer 12 Stunden andauernder Aktivität, 2500 Hits oder 100 Treffer innerhalb von 100 Sekunden erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

See the [Visits](../../components/c-variables/c-metrics/metrics-visit.md) metric in the Components user guide for more information.
