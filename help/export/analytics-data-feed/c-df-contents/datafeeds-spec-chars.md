---
description: Informationen zu Sonderzeichen, die im Daten-Feed verwendet werden.
keywords: Daten-Feed;Auftrag;Sonderzeichen;hit_data;Variablen mit mehreren Werten;events_list;products_list;mvvars
subtopic: data feeds
title: Sonderzeichen in Daten-Feeds
feature: Data Feeds
exl-id: b816ebc5-0b23-4420-aa8c-b88953d031e6
source-git-commit: 6e59ee3cb3eb59b025053603cd1357c5a2709d00
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 90%

---

# Sonderzeichen in Daten-Feeds

Adobe verwendet eine Escape-Logik, um sicherzustellen, dass die an Datenerfassungsserver gesendeten Werte keine Daten-Feed-Dateien beschädigen oder negativ beeinflussen. Diese Zeichen sind von Adobe für folgende Zwecke in `hit_data.tsv` reserviert.

## Sonderzeichen in einer beliebigen Spalte

| Zeichen | Beschreibung |
|--- |--- |
| `\t` | Steht für eine Registerkarte. Markiert das Ende einer Spalte oder eines Datenfelds. |
| `\n` | Steht für einen Zeilenumbruch. Markiert das Ende einer Zeile oder eines Treffers. |
| `\` | Umgekehrter Schrägstrich. Escape-Zeichen, wenn sie im Zuge der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein umgekehrter Schrägstrich vorangestellt wird, wurden sie als Teil der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `\\t` | Der Wert „`\t`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `\\n` | Der Wert „`\n`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `\\` | Der Wert „`\`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |

Beispiel: Ein Besucher Ihrer Site verwendet die interne Suche und sucht nach `"search\nstring"`. Sie füllen eVar 1 mit `"search\nstring"`und senden Sie diesen Wert an Adobe. Adobe erhält diesen Treffer und versieht den in der Zeichenfolge enthaltenen Zeilenumbruch mit einem Escape-Zeichen. Der tatsächliche Wert, der in den Rohdaten platziert wird, lautet `"search\\nstring"`.

## Sonderzeichen in Variablen mit mehreren Werten (events_list, products_list, mvvars)

Die folgenden Zeichen haben in Spalten, die mehrere Werte enthalten können, eine besondere Bedeutung.

| Zeichen | Beschreibung |
|--- |--- |
| `,` | Komma. Kennzeichnet das Ende eines einzelnen Werts. Trennt Produktzeichenfolgen, Ereignis-IDs oder andere Werte. |
| `;` | Semikolon. Kennzeichnet das Ende eines einzelnen Werts in `product_list`. Trennt Felder innerhalb einer einzelnen Produktzeichenfolge. |
| `=` | Gleich-Zeichen. Weist einem Ereignis in `product_list` einen Wert zu. |
| `^` | Caret. Escape-Zeichen, wenn sie im Zuge der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein Caret vorangeht, wurden sie im Zuge der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `^,` | Der Wert „`,`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^;` | Der Wert „`;`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^=` | Der Wert „`=`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^^` | Der Wert „`^`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
