---
title: Unterschiede bei Verarbeitung und Architektur von Analyseplattformen
description: Erfahren Sie, wie einige Daten auf unterschiedlichen Plattformen wie Adobe Analytics und Google Analytics auf verschiedene Weise erfasst und angezeigt werden.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 66%

---


# Unterschiede bei Verarbeitung und Architektur von Analyseplattformen

Obwohl Adobe Analytics und Google Analytics beide Analysetools sind, unterscheidet sich die Art und Weise, wie Daten erfasst und verarbeitet werden, zwischen den beiden Plattformen stark. Verwenden Sie diese Seite, um einige der wichtigsten Unterschiede bei der Erfassung bestimmter Dimensionen und Metriken zu verstehen und herauszufinden, warum sie in ähnlichen Berichten möglicherweise unterschiedliche Zahlen anzeigen.

## [!UICONTROL Absprungrate]

[!UICONTROL Die Absprungrate ist eine häufig verwendete KPI, mit der in den meisten Analysetools die Effektivität und Relevanz der Landingpages gemessen werden kann. ] Dies wird normalerweise definiert als Besuche, die auf die Website gelangen, aber keinen Klick auf eine andere Seite beinhalten.

* In Adobe Analytics, [!UICONTROL Bounce Rate] is calculated using the formula **Bounces divided by Entries**.
* In Google Analytics, [!UICONTROL Bounce Rate] is calculated using the formula **Single-page sessions divided by Sessions**.

Wenn auf beiden Plattformen bei demselben Besuch oder derselben Sitzung mehrere Treffer gesendet werden, wird dies nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und relativ häufig, wodurch verhindert werden kann, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet normalerweise nicht mehr als eine Datenanfrage auf derselben Seite.

To achieve better parity between reporting tools, use the [!UICONTROL Single Page Visits] metric in Adobe Analytics instead of [!UICONTROL Bounces] as part of a calculated metric. The [!UICONTROL Single Page Visits] metric includes the total number of visits that only included one-page view, or visits that enter the website but do not include a click to another page.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Absprungrate](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) im Benutzerhandbuch zu Komponenten.

## [!UICONTROL Besuche und Sitzungen]

[!UICONTROL Besuche] (in Google Analytics als Sitzungen bezeichnet) sind eine Gruppe von Ansichten, die ein Benutzer innerhalb kurzer Zeit vornimmt. [!UICONTROL Besuche auf beiden Plattformen laufen in der Regel nach 30 Minuten Inaktivität ab. ] Both platforms allow customization on when a [!UICONTROL Visit] expires. Es gibt mehrere Szenarien, die Unterschiede auf den verschiedenen Plattformen verursachen können.

* **Tagesende:** Alle Sitzungen in Google Analytics laufen um 23:59 Uhr jeden Tages ab. Wenn der Anwender nach 00:00 Uhr noch auf Ihrer Site aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics führt Besuche am Folgetag im Rahmen desselben Besuchs fort.
* **Verschiedene Kampagnen:** In Google Analytics wird eine neue Sitzung gestartet, wenn sich die Kampagnenquelle eines Anwenders ändert. If a new [!UICONTROL Tracking Code] value is seen in Adobe Analytics, it is considered part of the same visit.
* **Manuelle Sitzungsüberschreibungen:** In Google Analytics wird eine neue Sitzung gestartet, wenn Sie `sessionControl` verwenden, um eine Sitzung manuell zu starten oder zu beenden. [!UICONTROL In Adobe Analytics können Besuche nicht manuell beendet werden.]
* **Ausreißerbesuchserkennung in Adobe Analytics:** Ein neuer [!UICONTROL Besuch] in Adobe Analytics wird automatisch Beginn, wenn ein Benutzer innerhalb von 100 Sekunden 12 Aktivitäten, 2500 Treffer oder 100 Treffer erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Besuche](/help/components/c-variables/c-metrics/metrics-visit.md) im Benutzerhandbuch zu Komponenten.
