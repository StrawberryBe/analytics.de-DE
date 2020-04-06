---
title: maxDelay
description: Stellen Sie fest, wie lange AppMeasurement maximal auf eine Antwort von DFA wartet, bevor eine Bildanforderung gesendet wird.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# maxDelay

Die Variable `s.maxDelay` wird im DFA-Data Connector zur Bestimmung der Timeout-Zeitdauer beim Herstellen von Verbindungen zum DFA-Host verwendet. Wenn Adobe innerhalb des in der Variablen festgelegten Zeitraums keine Antwort von DFA-Servern erhält, wird die Verbindung abgebrochen und die Daten werden normal verarbeitet. Fügen Sie diese Variable in Ihre Implementierung ein, wenn es bei den DFA-Antwortzeiten der einzelnen Seiten zu Problemen kommt. Adobe empfiehlt, mit diesem Wert zu experimentieren, um den optimalen Timeout-Zeitraum zu ermitteln.

Diese Variable wird nur in Implementierungen mit dem DFA-Data Connector verwendet. Auch bei Implementierungen mit DFA ist diese Variable optional.

## Max. Verzögerung bei Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerspezifischen Code-Editor entsprechend der AppMeasurement-Syntax.

## s.maxDelay in AppMeasurement und im benutzerspezifischem Launch-Codeeditor

Die Variable `s.maxDelay` ist eine Ganzzahl, welche in Millisekunden angibt, wie lange AppMeasurement auf eine Antwort von DFA wartet. Wenn AppMeasurement nicht rechtzeitig eine Antwort von DFA erhält, wird eine Bildanforderung ohne DFA-Daten an Adobe gesendet.

```js
s.maxDelay = 750;
```

## Eigenschaften

* Wenn Sie die Wartezeit erhöhen, können mehr DFA-Daten gesammelt werden, es steigt aber auch das Risiko, Analytics-Trefferdaten zu verlieren. Analytics-Trefferdaten gehen verloren, wenn der Benutzer während des `s.maxDelay`-Zeitraums von der Seite weg navigiert.
* Bei einer niedrigeren Wartezeit sinkt das Risiko, Analytics-Trefferdaten zu verlieren, dabei kann es jedoch auch zu einer Verringerung der mit den Trefferdaten gesendeten DFA-Daten kommen.
* DFA-Integrationsdaten werden gelöscht, wenn der `s.maxDelay`-Zeitraum nicht genügend Zeit für die Reaktion des DFA-Hosts bietet.

>[!NOTE] Adobe hat keine Kontrolle über die Antwortzeiten von DFA. Sollten bei Ihnen Probleme auftreten, die auch nach einer (vernünftigen) Anhebung der maximalen Wartezeit nicht verschwinden, wenden Sie sich an den DFA-Kontoadministrator Ihrer Organisation.
