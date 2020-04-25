---
title: Unterschiede bei Verarbeitung und Architektur von Analyseplattformen
description: Erfahren Sie, wie einige Daten auf unterschiedlichen Plattformen wie Adobe Analytics und Google Analytics auf verschiedene Weise erfasst und angezeigt werden.
translation-type: tm+mt
source-git-commit: 757cea821bae49fabe819a65b921797070d328fc

---


# Unterschiede bei Verarbeitung und Architektur von Analyseplattformen

Obwohl Adobe Analytics und Google Analytics beide Analysetools sind, unterscheidet sich die Art und Weise, wie Daten erfasst und verarbeitet werden, zwischen den beiden Plattformen stark. Verwenden Sie diese Seite, um einige der wichtigsten Unterschiede bei der Erfassung bestimmter Dimensionen und Metriken zu verstehen und herauszufinden, warum sie in ähnlichen Berichten möglicherweise unterschiedliche Zahlen anzeigen.

## Absprungrate

Die Absprungrate ist eine häufig verwendete KPI, mit der in den meisten Analysetools die Effektivität und Relevanz der Landingpages gemessen werden kann. Dies wird normalerweise definiert als Besuche, die auf die Website gelangen, aber keinen Klick auf eine andere Seite beinhalten.

* In Adobe Analytics wird die Absprungrate anhand der Formel **Absprünge dividiert durch Einstiege** berechnet.
* In Google Analytics wird die Absprungrate anhand der Formel **Einseitige Sitzungen dividiert durch Sitzungen** berechnet.

Wenn auf beiden Plattformen bei demselben Besuch oder derselben Sitzung mehrere Treffer gesendet werden, wird dies nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und relativ häufig, wodurch verhindert werden kann, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet normalerweise nicht mehr als eine Datenanfrage auf derselben Seite.

Um eine bessere Parität zwischen den Berichtswerkzeugen zu erreichen, verwenden Sie in Adobe Analytics anstelle von Absprüngen die Metrik „Einzelseitenbesuche“ als Teil einer berechneten Metrik. Die Metrik „Einzelseitenbesuche“ enthält die Gesamtanzahl der Besuche, bei denen nur ein Seitenaufruf stattfand oder die keinen Klick auf eine andere Seite beinhalteten.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Absprungrate](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) im Benutzerhandbuch zu Komponenten.

## Besuche und Sitzungen

Besuche (in Google Analytics als Sitzungen bezeichnet) sind eine Gruppe von Seitenansichten, die ein und derselbe Anwender in kurzer Zeit tätigt. Besuche auf beiden Plattformen laufen in der Regel nach 30 Minuten Inaktivität ab. Beide Plattformen ermöglichen die Anpassung der Bedingungen für den Ablauf eines Besuchs. Es gibt mehrere Szenarien, die Unterschiede auf den verschiedenen Plattformen verursachen können.

* **Tagesende:** Alle Sitzungen in Google Analytics laufen um 23:59 Uhr jeden Tages ab. Wenn der Anwender nach 00:00 Uhr noch auf Ihrer Site aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics führt Besuche am Folgetag im Rahmen desselben Besuchs fort.
* **Verschiedene Kampagnen:** In Google Analytics wird eine neue Sitzung gestartet, wenn sich die Kampagnenquelle eines Anwenders ändert. Wenn in Adobe Analytics ein neuer Trackingcode-Wert auftaucht, wird er als Teil desselben Besuchs betrachtet.
* **Manuelle Sitzungsüberschreibungen:** In Google Analytics wird eine neue Sitzung gestartet, wenn Sie `sessionControl` verwenden, um eine Sitzung manuell zu starten oder zu beenden. In Adobe Analytics können Besuche nicht manuell beendet werden.
* **Ausreißerbesuchserkennung in Adobe Analytics:** In Adobe Analytics beginnt automatisch ein neuer Besuch, wenn ein Anwender 12 Stunden kontinuierlicher Aktivität, 2.500 Treffer oder 100 Treffer in 100 Sekunden erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Besuche](/help/components/c-variables/c-metrics/metrics-visit.md) im Benutzerhandbuch zu Komponenten.
