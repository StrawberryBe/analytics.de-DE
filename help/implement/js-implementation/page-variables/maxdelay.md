---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# maxDelay

Die Variable „s.maxDelay“ dient hauptsächlich in Genesis DFA-Integrationen zur Bestimmung der Timeout-Zeitdauer beim Herstellen von Verbindungen zum DFA-Host. Wenn Adobe innerhalb des in der „“-Variablen festgelegten Zeitraums keine Antwort von DFA-Servern erhält, wird die Verbindung abgebrochen und die Daten werden normal verarbeitet. Diese Variable implementieren Sie, wenn es bei den DFA-Antwortzeiten der einzelnen Seiten zu Problemen kommt. Es empfiehlt sich, diesen Wert versuchsweise zu ändern, um einen optimalen Timeout-Wert zu finden.


<!-- 

maxDelay.xml

 -->

**Implementierungsbeispiel**

```
s.maxDelay="750";
```

**Eigenschaften**

* Diese Variable ist eine optionale Ereignismetrik, die über das auf Ihrer Site implementierte JavaScript aufgefüllt wird.
* Wenn der DFA-Host nicht innerhalb der angegebenen Zeitdauer antwortet, wird das für Timeouts vorgesehene Ereignis (das per Genesis-Integrations-Assistenten zugewiesen wird) ausgelöst.
* Die Variable darf nur einen numerischen Wert enthalten.
* Die Zeitdauer wird in Millisekunden angegeben.
* Wenn Sie die Wartezeit erhöhen, können mehr DFA-Daten gesammelt werden, es steigt aber auch das Risiko, Analytics-Trefferdaten zu verlieren.

   Der Verlust von Analytics-Trefferdaten würde auftreten, wenn der Benutzer während des *`s.maxDelay`*-Zeitraums von der Seite weg navigiert.

* Bei einer niedrigeren Wartezeit sinkt das Risiko, Analytics-Trefferdaten zu verlieren, dabei kann es jedoch auch zu einer Verringerung der mit den Trefferdaten gesendeten DFA-Daten kommen.

   Das Löschen von DFA-Integrationsdaten erfolgt, wenn der *`s.maxDelay`*-Zeitraum nicht genügend Zeit für die Reaktion des DFA-Hosts bietet.

> [!NOTE] Adobe hat keine Kontrolle über die Antwortzeiten von DFA. Sollten bei Ihnen Probleme auftreten, die auch nach einer (vernünftigen) Anhebung der maximalen Wartezeit nicht verschwinden, wenden Sie sich an den DFA-Konto-Administrator Ihrer Organisation.
