---
description: In diesem Abschnitt erhalten Sie Informationen zu Sonderzeichen, die im Datenfeed verwendet werden.
keywords: Data Feed;job;special characters;hit_data;multi-valued variables;events_list;products_list;mvvars
subtopic: data feeds
title: Sonderzeichen in Datenfeeds
topic: Reports and analytics
uuid: 5efe019b-39e6-4226-a936-88202a02f5e6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Sonderzeichen in Datenfeeds

Adobe verwendet Escape-Logik, um sicherzustellen, dass an Datenerfassungsserver gesendete Werte keine Daten-Feed-Dateien beschädigen oder negativ beeinflussen. Die folgenden Zeichen sind von Adobe für folgende Zwecke in `hit_data.tsv`reserviert.

## Sonderzeichen in einer beliebigen Spalte

| Zeichen | Beschreibung |
|--- |--- |
| `\t` | Stellt eine Registerkarte dar. Markiert das Ende einer Spalte oder eines Datenfelds. |
| `\n` | Stellt einen Zeilenumbruch dar. Markiert das Ende einer Zeile oder eines Treffers. |
| `\` | Umgekehrter Schrägstrich. Escape-Zeichen, wenn sie im Rahmen der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein umgekehrter Schrägstrich vorangestellt wird, wurden sie als Teil der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `\\t` | Der Wert '`\t`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
| `\\n` | Der Wert '`\n`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
| `\\` | Der Wert '`\`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |

Beispielsweise verwendet ein Besucher Ihrer Site die interne Suche und sucht nach "search\nstring". Sie füllen eVar1 mit "search\nstring"und senden diesen Wert an Adobe. Adobe erhält diesen Treffer und entgeht der in der Zeichenfolge enthaltenen Zeilenumbruchposition. Der tatsächliche Wert, der in Rohdaten platziert wird, ist "search\\nstring".

## Sonderzeichen in Variablen mit mehreren Werten (events_list, products_list, mvvars)

Die folgenden Zeichen haben eine besondere Bedeutung in Spalten, die mehrere Werte enthalten können.

| Zeichen | Beschreibung |
|--- |--- |
| `,` | Komma. Stellt das Ende eines einzelnen Werts dar. Trennt Produktzeichenfolgen, Ereignis-IDs oder andere Werte. |
| `;` | Semikolon. Stellt das Ende eines einzelnen Werts in `product_list`dar. Trennt Felder in einer einzelnen Produktzeichenfolge. |
| `=` | Gleich Zeichen. Assigns a value to an event in `product_list`. |
| `^` | Caret. Escape-Zeichen, wenn sie im Rahmen der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein Caret vorangeht, wurden sie als Teil der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `^,` | Der Wert '`,`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
| `^;` | Der Wert '`;`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
| `^=` | Der Wert '`=`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
| `^^` | Der Wert '`^`' wurde während der Datenerfassung gesendet, die von Adobe mit Escapezeichen versehen wurde. |
