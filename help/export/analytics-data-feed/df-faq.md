---
description: Häufig gestellte Fragen zu Datenfeeds
keywords: Data Feed;job;pre column;post column;case sensitivity
solution: Analytics
title: Häufig gestellte Fragen zu Datenfeeds
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Häufig gestellte Fragen zu Datenfeeds

Häufig gestellte Fragen zu Datenfeeds.

## Was ist der Unterschied zwischen Spalten mit einem `post_` Präfix und Spalten ohne `post_` Präfix?

Spalten ohne `post_` Präfix enthalten Daten, die exakt so sind, wie sie an die Datenerfassung gesendet wurden. Spalten mit `post_` Präfix enthalten den Wert nach der Verarbeitung. Beispiele, die einen Wert ändern können, sind Variablenpersistenz, Verarbeitungsregeln, VISTA-Regeln, Währungsumrechnung oder andere serverseitige Logik, die Adobe anwendet. Adobe empfiehlt, nach Möglichkeit die `post_` Version einer Spalte zu verwenden.

If a column does not contain a `post_` version (for example, `visit_num`), then the column can be considered a post column.

## Wie geht Data Feeds mit der Groß-/Kleinschreibung um?

In Adobe Analytics wird bei den meisten Variablen bei der Berichterstellung nicht zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise werden "Schnee", "Schnee", "SCHNEE"und "Jetzt"alle als gleicher Wert betrachtet. Die Groß-/Kleinschreibung wird in Datenfeeds beibehalten.

Wenn Sie unterschiedliche Schreibweisen desselben Werts zwischen Nicht-Post- und Post-Spalten sehen (z. B. "Schnee"in der Pre-Spalte und "Schnee"in der Post-Spalte), verwendet Ihre Implementierung auf Ihrer Site sowohl Groß- als auch Kleinbuchstaben. Die Variante in der Post-Spalte wurde entweder zuvor eingereicht und ist in einem virtuellen Cookie gespeichert, oder sie wurde etwa zur selben Zeit für diese Report Suite verarbeitet.