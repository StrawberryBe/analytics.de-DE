---
title: Unterschiede in der Verarbeitung und Architektur zwischen Analytics-Plattformen
description: Erfahren Sie, wie einige Daten zwischen Plattformen wie Adobe Analytics und Google Analytics unterschiedlich erfasst und angezeigt werden.
translation-type: tm+mt
source-git-commit: 757cea821bae49fabe819a65b921797070d328fc

---


# Unterschiede in der Verarbeitung und Architektur zwischen Analytics-Plattformen

Obwohl Adobe Analytics und Google Analytics beide Analytics-Tools sind, ist die Art und Weise, wie Daten zwischen Plattformen erfasst und verarbeitet werden, sehr unterschiedlich. Verwenden Sie diese Seite, um einige der wichtigsten Unterschiede bei der Erfassung bestimmter Dimensionen und Metriken zu verstehen und zu verstehen, warum sie in ähnlichen Berichten möglicherweise unterschiedliche Zahlen anzeigen.

## Absprungrate

Die Absprungrate ist ein häufig verwendeter KPI, mit dem die Effektivität und Relevanz der Einstiegsseiten in den meisten Analysetools gemessen werden kann. Dies wird normalerweise definiert als Besuche, die auf die Website gelangen, aber keinen Klick auf eine andere Seite beinhalten.

* In Adobe Analytics wird die Absprungrate anhand der Formel **Absprünge dividiert durch Einstiege** berechnet.
* In Google Analytics wird die Absprungrate anhand der Formel **Einseitige Sitzungen dividiert durch Sitzungen** berechnet.

Wenn auf beiden Plattformen bei demselben Besuch oder derselben Sitzung mehrere Treffer gesendet werden, wird dies nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und relativ häufig, wodurch verhindert werden kann, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet normalerweise nicht mehr als eine Datenanforderung auf derselben Seite.

Um eine bessere Parität zwischen den Berichterstellungs-Tools zu erreichen, verwenden Sie die Metrik Einzelseitenbesuche in Adobe Analytics anstelle von Absprüngen als Teil einer berechneten Metrik. Die Metrik Einzelseitenbesuche enthält die Gesamtanzahl der Besuche, bei denen nur ein Seitenaufruf oder Besuche auf der Website stattgefunden haben, die aber keinen Klick auf eine andere Seite beinhalten.

Weitere Informationen finden Sie in der Metrik " [Absprungrate](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) "im Komponenten-Benutzerhandbuch.

## Besuche und Sitzungen

Besuche (in Google Analytics als Sitzungen bezeichnet) sind eine Gruppe von Seitenansichten, die ein und derselbe Benutzer in kurzer Zeit anzeigt. Besuche auf beiden Plattformen laufen in der Regel nach 30 Minuten Inaktivität ab. Beide Plattformen ermöglichen die Anpassung bei Ablauf eines Besuchs. Es gibt mehrere Szenarien, die Unterschiede auf jeder Plattform verursachen können.

* **** Ende des Tages: Alle Sitzungen in Google Analytics laufen nach 23:59 Uhr an einem bestimmten Tag ab. Wenn der Benutzer nach 12 Uhr noch auf Ihrer Site aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics führt Besuche am folgenden Tag im Rahmen desselben Besuchs fort.
* **** Verschiedene Kampagnen: Eine neue Sitzung in Google Analytics wird gestartet, wenn sich die Kampagnenquelle eines Benutzers ändert. Wenn ein neuer Trackingcode-Wert in Adobe Analytics angezeigt wird, wird er als Teil desselben Besuchs betrachtet.
* **** Manuelle Sitzungsüberschreibungen: Eine neue Sitzung in Google Analytics wird gestartet, wenn Sie eine Sitzung manuell starten oder beenden `sessionControl` möchten. Besuche können nicht manuell in Adobe Analytics beendet werden.
* **** Ausreißerbesuchserkennung in Adobe Analytics: Ein neuer Besuch in Adobe Analytics beginnt automatisch, wenn ein Benutzer innerhalb von 100 Sekunden 12 Stunden kontinuierlicher Aktivität, 2500 Treffer oder 100 Treffer erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

Weitere Informationen finden Sie in der Metrik [Besuche](/help/components/c-variables/c-metrics/metrics-visit.md) im Komponenten-Benutzerhandbuch.
