---
description: Zu einer erfolgreichen DFA-Implementierung gehört auch ein optimierter Wert für s.maxDelay auf Ihrer entsprechenden Site.
keywords: DFA
seo-description: Zu einer erfolgreichen DFA-Implementierung gehört auch ein optimierter Wert für s.maxDelay auf Ihrer entsprechenden Site.
seo-title: Abstimmung von s.maxDelay
solution: Analytics
title: Abstimmung von s.maxDelay
topic: Data Connectors
uuid: 7640 af 26-6 ac 6-427 e -9 cfc -932 c 86 ccf 5 ab
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Abstimmung von s.maxDelay{#tuning-s-maxdelay}

Zu einer erfolgreichen DFA-Implementierung gehört auch ein optimierter Wert für s.maxDelay auf Ihrer entsprechenden Site.

Die Entscheidung zum Erhöhen oder Senken *`s.maxDelay`* enthält im Allgemeinen einen Kompromiss zwischen dem Abrufen weiterer DFA-Besucherdaten und dem Risiko der Erfassung von Adobe-Besucherdaten. Increasing *`s.maxDelay`* obtains more DFA visitor data, but (placed excessively high) could endanger the collection of Adobe visitor data. Senken Sie s.maxDelay, ist die Erfassung von Adobe-Besucherdaten gewährleistet, aber es können DFA-Besucherdaten verloren gehen.

*`s.maxDelay`* beinhaltet mehr als nur die Zeit für die Netzwerkkommunikation zur Kontaktaufnahme mit DFA. Dieser Wert stellt auch Browserverzögerungen dar, die das JavaScript auslösen und evaluieren, auf dem diese Kommunikation basiert. Das liegt daran, dass das Integrate-Modul den *`s.maxDelay`* Timer beginnt, nachdem das HTML-Element in das DOM eingefügt wurde, das die Daten vom DFA Floodlight-Server abruft. Die Zeit, die der Browser zur tatsächlichen Initiierung der auf diesem neuen HTML-Element basierenden HTTP-Abfrage benötigt, ist abhängig von anderen Bildern oder JavaScript-Dateien, die gleichzeitig geladen werden, der Geschwindigkeit des Besuchercomputers sowie spezifischen Browserimplementationen. Bei Abfrage der JSON-Daten vom DFA Floodlight-Server muss außerdem JavaScript vom Browser evaluiert werden. Dieser Vorgang wird wiederum vollständig vom Browser gesteuert und kann verzögert werden, wenn gleichzeitig eine große Menge an JavaScript-Code ausgeführt wird oder viele asynchrone JavaScript-Abfragen vorliegen.

Beachten Sie diese Informationen und legen Sie den Wert für *`s.maxDelay`* also auf Grundlage der Komplexität der Landingpage und der Netzwerkverzögerungen bei DFA fest. Auf einigen Seiten können Sie die Komplexität unter anderem dadurch reduzieren, dass der Adobe-Erfassungscode schon früh im Ladeprozess der Seite ausgelöst wird. So muss der Browser weniger Daten verarbeiten, wenn der Floodlight-Server kontaktiert wird.

Die Timeoutvariable ist bei der Abstimmung von *`s.maxDelay`*, da es bei jedem Erreichen des Timeout für s. maxdelay erhöht wird. Bei der Entscheidung, ob wir zu einem Anstieg oder einer Verringerung *`s.maxDelay`* entscheiden möchten, empfehlen wir dieses Verfahren:

1. Sammeln Sie mehrere Tage mit Daten, die *`s.maxDelay`* auf einen bestimmten Wert eingestellt sind.
1. Führen Sie einen [!DNL Daily Unique Visitors Report] für den Zeitraum aus.
1. Run the [!DNL Timeout Event Report] to check the number of timeouts that are coming through. Bedenken Sie, dass Timeouts nur einmal pro Besucher gezählt werden.

Verwenden Sie anhand dieser Informationen nun

```
Timeout Percentage = [Step 3] / [Step 2] * 100
```

Unter „Timeout Percentage“ (Timeoutprozentsatz) werden alle Besucher der Site berücksichtigt. Einige davon haben keinerlei Bezug zu DFA, daher ist der Timeoutwert irreführend. To improve this computation, another analysis could consider only unique visitors to pages with the `clickThroughParam` set (for example, `?CID=1`). Dadurch erhalten Sie genauere Ergebnisse.

Liegt der Timeoutprozentsatz sehr niedrig, sollten Sie *`s.maxDelay`*. Liegt er sehr hoch, erhöhen Sie *`s.maxDelay`*. When decreasing *`s.maxDelay`*, you will want to rerun the [!DNL Timeout Report] to ensure that timeouts have not dramatically increased. When increasing *`s.maxDelay`*, you will want to run a [!DNL Page Views Report] to make sure page views aren’t falling out due to lost data. Each time *`s.maxDelay`* is changed observe the data for several days in order to ensure that the data represents a trend, and not just a day-to-day fluctuation.

The optimal setting for *`s.maxDelay`* is the point at which the timeout percentage is minimized while Page Views do not drop off.

Wenn Sie zu Version 2.0 der Integration wechseln, wird die Anzahl der Timeouts voraussichtlich abnehmen, da die 302-Weiterleitungen wegfallen. Erste Ergebnisse von Beta-Kunden zeigen einen gleichmäßigen Rückgang der Timeouts, wodurch mehr DFA-Daten erfasst werden können.
