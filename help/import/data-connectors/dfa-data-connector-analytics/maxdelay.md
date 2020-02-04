---
title: maxDelay
description: Stellen Sie fest, wie lange AppMeasurement auf eine Antwort von DFA wartet, bevor eine Bildanforderung gesendet wird.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# maxDelay

The `s.maxDelay` variable is used in the DFA data connector to determine the timeout period in contacting the DFA host. Wenn Adobe innerhalb des in dieser Variablen festgelegten Zeitraums keine Antwort von DFA-Servern erhält, wird die Verbindung abgebrochen und die Daten werden normal verarbeitet. Fügen Sie diese Variable in Ihre Implementierung ein, wenn Sie sich mit der Antwortzeit von DFA auf jeder Seite beschäftigen. Adobe empfiehlt, mit diesem Wert zu experimentieren, um den optimalen Timeout-Zeitraum zu ermitteln.

Diese Variable wird nur in Implementierungen mit dem DFA-Datenanschluss verwendet. Auch bei Implementierungen mit DFA ist diese Variable optional.

## Max. Verzögerung beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.maxDelay in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.maxDelay` Variable ist eine Ganzzahl, die die Anzahl der Millisekunden angibt, die AppMeasurement auf eine Antwort von DFA wartet. Wenn AppMeasurement nicht rechtzeitig eine Antwort von DFA erhält, wird eine Bildanforderung ohne DFA-Daten an Adobe gesendet.

```js
s.maxDelay = 750;
```

## Eigenschaften

* Wenn Sie die Wartezeit erhöhen, können mehr DFA-Daten gesammelt werden, es steigt aber auch das Risiko, Analytics-Trefferdaten zu verlieren. Losing Analytics hit data happens when the user navigates away from the page during the `s.maxDelay` period.
* Durch die Verkürzung der Wartezeit sinkt das Risiko, Analytics-Trefferdaten zu verlieren, kann jedoch die Menge der mit Trefferdaten gesendeten DFA-Daten reduziert werden.
* Losing DFA integration data happens when the `s.maxDelay` period does not accommodate enough time for the DFA host to respond.

> [!NOTE] Adobe hat keine Kontrolle über die Antwortzeiten von DFA. Sollten Sie selbst nach Anhebung der maximalen Wartezeit auf einen angemessenen Zeitraum konsistente Probleme feststellen, wenden Sie sich an den DFA-Kontoadministrator Ihres Unternehmens.
