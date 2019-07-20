---
description: Die Pre-Spalte enthält die Daten, wie sie an die Datenerfassung gesendet wurden. Die Post-Spalte enthält den Wert nach der Verarbeitung.
keywords: Datenfeed; job; pre column; Post-Spalte; Groß-/Kleinschreibung
seo-description: Die Pre-Spalte enthält die Daten, wie sie an die Datenerfassung gesendet wurden. Die Post-Spalte enthält den Wert nach der Verarbeitung.
seo-title: Pre- und Post-Spalten
solution: Analytics
title: Pre- und Post-Spalten
topic: Reports and Analytics
uuid: a 415327 b -6151-4 d 08-b 8 b 9-5 aaa 2348 eb 0 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pre- und Post-Spalten

Die Pre-Spalte enthält die Daten, wie sie an die Datenerfassung gesendet wurden. Die Post-Spalte enthält den Wert nach der Verarbeitung.

So kann sich der finale Wert für eine Variable, der in der Post-Spalte angezeigt wird, beispielsweise durch Variablenpersistenz, Verarbeitungsregeln, VISTA-Regeln und Wechselkurskonversionen ändern. Für die meisten Berechnungen verwenden Sie normalerweise die Post-Spalte, es sei denn, Sie wenden benutzerspezifische Geschäftslogik an (z. B. Anwendung einer benutzerdefinierten Formel zur Bestimmung der Zuordnung).

Wenn für eine Spalte keine Pre- oder Post-Version vorliegt (z. B. bei `visit_num`), kann die Spalte als Post-Spalte betrachtet werden. Columns prefixed with " `pre_`" typically contain data that was populated by Adobe and not sent by your implementation. For example, `pre_browser` is populated by Adobe, but `evar1` is populated by your implementation. Both of these columns have a " `post_`" column ( `post_browser`, `post_evar1`), which contains the value used by reporting.

## Unterscheidung zwischen Groß- und Kleinschreibung bei Werten {#section_F979E099BFAB4AFEBEA2D7E228963CE8}

Bei den meisten Analysevariablen wird für Zwecke der Berichterstellung nicht zwischen Groß- und Kleinschreibung unterschieden. Das bedeutet, dass verschiedene Varianten als gleicher Wert gelten („snow“, „Snow“, „SNOW“ und „sNow“ gelten alle als gleicher Wert). Zu Anzeigezwecken wird die Groß- und Kleinschreibung jedoch beibehalten, da die meisten Kunden es vorziehen, sowohl Groß- als auch Kleinbuchstaben zur Anzeige in Berichten zu senden.

Bei der Verarbeitung des Datenfeeds können Sie zu Vergleichszwecken die Kleinschreibung bei Werten verwenden. Zu Anzeigezwecken empfiehlt sich hingegen unter Umständen die Beibehaltung von Groß- und Kleinschreibung.

Wenn Sie verschiedene Schreibweisen für den gleichen Wert in den Pre- und Post-Spalten sehen können (z. B. „snow“ in der Pre-Spalte und „Snow“ in der Post-Spalte), deutet dies darauf hin, dass Sie für den gleichen Wert auf Ihrer Website sowohl Groß- als auch Kleinschreibungsvarianten einreichen. Die Variante in der Post-Spalte wurde entweder zuvor eingereicht und ist in einem virtuellen Cookie gespeichert, oder sie wurde etwa zur selben Zeit für diese Report Suite verarbeitet. Beispiel:

Treffer 1: s.list1="Tabby,Persian,Siamese";

Treffer 2: s.list1="tabby,persian,siamese";

Wenn Treffer 2 im Datenfeed berichtet wird, berücksichtigt die Pre-Spalte genau die eingereichte Groß- und Kleinschreibung (tabby,persian,siamese), jedoch wird wahrscheinlich der Wert für Treffer 1 für diesen Besuch beibehalten und an die Post-Spalte berichtet (Tabby,Persian,Siamese), da Treffer 1 und 2 den genau gleichen Wert enthalten, wenn ein Vergleich ohne Berücksichtigung von Groß- und Kleinschreibung ausgeführt wird.
