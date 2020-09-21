---
description: Häufig gestellte Fragen zu Daten-Feeds
keywords: Data Feed;job;pre column;post column;case sensitivity
title: Häufig gestellte Fragen zu Daten-Feeds
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 77%

---


# Häufig gestellte Fragen zu Daten-Feeds

Häufig gestellte Fragen zu Daten-Feeds.

## Was ist der Unterschied zwischen Spalten mit `post_`-Präfix und Spalten ohne `post_`-Präfix?

Spalten ohne `post_`-Präfix enthalten Daten, die exakt so sind, wie sie an die Datenerfassung gesendet wurden. Spalten mit `post_`-Präfix enthalten den Wert nach der Verarbeitung. Beispiele, die einen Wert ändern können, sind Variablenpersistenz, Verarbeitungsregeln, VISTA-Regeln, Währungsumrechnung oder andere serverseitige Logik, die Adobe anwendet. Adobe empfiehlt, nach Möglichkeit die `post_`-Version einer Spalte zu verwenden.

Wenn für eine Spalte keine `post_`-Version vorliegt (z. B. bei `visit_num`), kann die Spalte als Post-Spalte betrachtet werden.

## Wie gehen Daten-Feeds mit Groß-/Kleinschreibung um?

In Adobe Analytics wird bei den meisten Variablen beim Reporting nicht zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise werden „schnee“, „Schnee“, „SCHNEE“ und „sChnee“ alle als gleicher Wert betrachtet. Die Groß-/Kleinschreibung wird in Daten-Feeds beibehalten.

Wenn Sie unterschiedliche Schreibweisen desselben Werts zwischen Nicht-Post- und Post-Spalten sehen (z. B. „schnee“ in der Pre-Spalte und „Schnee“ in der Post-Spalte), verwendet Ihre Implementierung auf Ihrer Site sowohl Groß- als auch Kleinbuchstaben. Die Variante in der Post-Spalte wurde entweder zuvor eingereicht und ist in einem virtuellen Cookie gespeichert, oder sie wurde etwa zur selben Zeit für diese Report Suite verarbeitet.

## Enthalten Daten-Feeds Bots, die nach Admin Console-Bot-Regeln gefiltert wurden?

Daten-Feeds enthalten keine Bots, die nach [Admin Console-Bot-Regeln](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/bot-removal/bot-removal.html) gefiltert wurden.

## Warum werden mehrere `000` Werte in der Spalte `event_list` oder in der `post_event_list` Datenfeed-Spalte angezeigt?

Einige Tabelleneditoren, insbesondere Microsoft Excel, runden automatisch sehr große Zahlen ab. Die `event_list` Spalte enthält viele kommagetrennte Zahlen, wodurch Excel sie manchmal als große Zahl behandelt. Die letzten Ziffern werden gerundet `000`.

Adobe empfiehlt das automatische Öffnen von `hit_data.tsv` Dateien in Microsoft Excel. Verwenden Sie stattdessen das Excel-Dialogfeld &quot;Daten importieren&quot;und stellen Sie sicher, dass alle Felder als Text behandelt werden.
