---
title: Unterschiede bei Verarbeitung und Architektur von Analyseplattformen
description: Erfahren Sie, wie einige Daten auf unterschiedlichen Plattformen wie Adobe Analytics und Google Analytics auf verschiedene Weise erfasst und angezeigt werden.
translation-type: tm+mt
source-git-commit: 6fc8145d9a94427ec942d55776b6029f7dd6f79c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 66%

---


# Unterschiede bei Verarbeitung und Architektur von Analyseplattformen

Obwohl Adobe Analytics und Google Analytics beide Analysetools sind, unterscheidet sich die Art und Weise, wie Daten erfasst und verarbeitet werden, zwischen den beiden Plattformen stark. Verwenden Sie diese Seite, um einige der wichtigsten Unterschiede bei der Erfassung bestimmter Dimensionen und Metriken zu verstehen und herauszufinden, warum sie in ähnlichen Berichten möglicherweise unterschiedliche Zahlen anzeigen.

## [!UICONTROL Absprungrate]

[!UICONTROL Die Absprungrate ist eine häufig verwendete KPI, mit der in den meisten Analysetools die Effektivität und Relevanz der Landingpages gemessen werden kann. ] Dies wird normalerweise definiert als Besuche, die auf die Website gelangen, aber keinen Klick auf eine andere Seite beinhalten.

* In Adobe Analytics wird [!UICONTROL Absprungrate] mit der Formel **Absprünge dividiert durch Einstiege** berechnet.
* In Google Analytics wird [!UICONTROL Absprungrate] mit der Formel **Einseitige Sitzungen dividiert durch Sitzungen** berechnet.

Wenn auf beiden Plattformen bei demselben Besuch oder derselben Sitzung mehrere Treffer gesendet werden, wird dies nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und relativ häufig, wodurch verhindert werden kann, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet normalerweise nicht mehr als eine Datenanfrage auf derselben Seite.

Um eine bessere Parität zwischen den Berichte-Tools zu erzielen, verwenden Sie die Metrik [!UICONTROL Einzelseitenbesuche] in Adobe Analytics anstelle von [!UICONTROL Absprünge] als Teil einer berechneten Metrik. Die Metrik [!UICONTROL Einzelseitenbesuche] enthält die Gesamtanzahl der Besuche, bei denen nur eine einseitige Ansicht oder Besuche auf der Website eingingen, die jedoch keinen Klick auf eine andere Seite beinhalten.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Absprungrate](/help/components/metrics/bounce-rate.md) im Benutzerhandbuch zu Komponenten.

## [!UICONTROL Besuche und Sitzungen]

[!UICONTROL Besuche]  (auch als Sitzungen in Google Analytics bezeichnet) sind eine Gruppe von Ansichten, die ein Benutzer innerhalb kurzer Zeit vornimmt. [!UICONTROL Besuche auf beiden Plattformen laufen in der Regel nach 30 Minuten Inaktivität ab. ] Beide Plattformen ermöglichen eine Anpassung bei Ablauf eines [!UICONTROL Besuchs]. Es gibt mehrere Szenarien, die Unterschiede auf den verschiedenen Plattformen verursachen können.

* **Tagesende:** Alle Sitzungen in Google Analytics laufen um 23:59 Uhr jeden Tages ab. Wenn der Anwender nach 00:00 Uhr noch auf Ihrer Site aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics führt Besuche am Folgetag im Rahmen desselben Besuchs fort.
* **Verschiedene Kampagnen:** In Google Analytics wird eine neue Sitzung gestartet, wenn sich die Kampagnenquelle eines Anwenders ändert. Wenn in Adobe Analytics ein neuer Wert [!UICONTROL Rückverfolgungscode] angezeigt wird, wird er als Teil desselben Besuchs betrachtet.
* **Manuelle Sitzungsüberschreibungen:** In Google Analytics wird eine neue Sitzung gestartet, wenn Sie `sessionControl` verwenden, um eine Sitzung manuell zu starten oder zu beenden. [!UICONTROL In Adobe Analytics können Besuche nicht manuell beendet werden.]
* **Erkennung von Außenbesuchen in Adobe Analytics:** Ein neuer Adobe Analytics-  Besuch wird automatisch Beginn, wenn ein Benutzer innerhalb von 100 Sekunden 12 Stunden dauerhafter Aktivität, 2500 Treffer oder 100 Treffer erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Besuche](/help/components/metrics/visits.md) im Benutzerhandbuch zu Komponenten.
