---
description: Häufig gestellte Fragen zu Daten-Feeds
keywords: Datenfeed;Auftrag;Pre-Spalte;Post-Spalte;Groß-/Kleinschreibung
title: Häufig gestellte Fragen zu Daten-Feeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
translation-type: tm+mt
source-git-commit: c6d4095fdf86be52c7921aed84b9229ac3b27f82
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 58%

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

## Warum werden in der Datenfeed-Spalte `event_list` oder `post_event_list` mehrere `000`-Werte angezeigt?

Einige Tabelleneditoren, insbesondere Microsoft Excel, runden automatisch sehr große Zahlen ab. Die Spalte `event_list` enthält viele kommagetrennte Zahlen, was dazu führt, dass Excel sie manchmal als große Zahl behandelt. Die letzten Ziffern werden auf `000` gerundet.

Adobe empfiehlt, `hit_data.tsv`-Dateien nicht automatisch in Microsoft Excel zu öffnen. Verwenden Sie stattdessen das Excel-Dialogfeld &quot;Daten importieren&quot;und stellen Sie sicher, dass alle Felder als Text behandelt werden.

## Warum kann ich keine &quot;stündliche&quot;Dateien aus Daten extrahieren, die älter als 7 Tage sind?

Bei Daten, die älter als 7 Tage sind, werden die &quot;stündlich&quot;-Dateien eines Tages in einer einzigen &quot;täglichen&quot;Datei zusammengefasst.

Beispiel: Am 9. März 2021 wird ein neuer Datenfeed erstellt, und die Daten vom 1. Januar 2021 bis zum 9. März werden als &quot;stündlich&quot;bereitgestellt. Die &quot;Stündlich&quot;-Dateien vor dem 2. März 2021 werden jedoch in einer einzigen &quot;Täglich&quot;-Datei zusammengefasst. Sie können &quot;Stündliche&quot;Dateien nur aus Daten extrahieren, die weniger als 7 Tage nach dem Erstellungsdatum alt sind. In diesem Fall vom 2. März bis 9. März.
