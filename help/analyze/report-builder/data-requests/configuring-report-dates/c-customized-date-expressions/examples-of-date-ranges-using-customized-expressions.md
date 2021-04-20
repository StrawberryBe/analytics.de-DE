---
description: Beispiele, Hinweise und Syntaxhinweise zur Verwendung von Datumsbereichen in benutzerdefinierten Ausdrücken.
title: Beispiele für Datumsbereiche mit benutzerdefinierten Ausdrücken
uuid: 3f46816d-9eee-4b2d-83be-bf1c9fb97fcf
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 99%

---


# Beispiele für Datumsbereiche mit benutzerdefinierten Ausdrücken

Beispiele, Hinweise und Syntaxhinweise zur Verwendung von Datumsbereichen in benutzerdefinierten Ausdrücken.

In der Tabelle wird als heutiges Datum Montag, der 10. November 2011 im Gregorianischen Kalender angenommen.

| Beispiel | Datumsbereich | Ausdruck anpassen | Datumsbereich des Berichts |
|---|---|---|---|
|  |  | **Von** | **Bis** |  |
| 1 | Vor zwei Wochen | cw-2w | cw-1w-1d | 26. Okt. bis 1. Nov. |
| 2 | Die ersten 3 Tage des fünften Monats des letzten Jahres | cy-1y+4m | cy-1y+4m+2d | 1. Mai bis 3. Mai 2010 |
| 3 | Eine ganze Woche, ab dem Datum vor vier Wochen | cw-4w | cw-3w-1d | 12. Okt. bis 18. Okt. |
| 4 | Die letzte Woche des vergangenen Jahres | cw-53w | cw-52w-1d | 1. Nov. bis 9. Nov. 2010 |
| 5 | Ein Monat ab dem Datum vor zwei Monaten | cm-2m | cm-1m-1d | 1. Sept. bis 30. Sept. |
| 6 | Vor 12 Monaten im vergangenen Jahr | cm-12m | cm-11m-1d | 1. Nov. bis 30. Nov. 2010 |

## Hinweise zu den Beispielen {#section_37801B0D6D364ABAA8DCE3A4C0123B2C}

**Beispiel 1**

Wenn heute Montag, der 10. November 2011 ist, das aktuelle Datum nehmen und eine Woche abziehen, um die letzte volle Woche im Oktober zu erhalten.

**Beispiel 2**

Dem Beginn des Jahres (dem Monat Januar) vier Monate hinzufügen, um den Mai zu erhalten; dem ersten Tag des Monats zwei Tage hinzufügen, um den dritten Tag des Monats zu erhalten.

## Syntaxhinweise {#section_555D6563B2D94FA3BDD801DC0B8C289D}

Benutzerdefinierte Ausdrücke für die Abdeckung eines Großteils aller möglichen Datumsbereiche können erstellt werden, indem zwei Terme mit einem Operator verknüpft werden. Ein Term besteht aus einem ganzzahligen Multiplikator und der Abkürzung für einen Zeitraum. Ein Beispiel für einen Term ist 18d, ein Beispiel für einen Operator ist +.

* Zwischen Operatoren und Termen sind keine Leerzeichen zulässig.
* Verwenden Sie nur diese Abkürzungen: cd, cw, cm, cq, cy, d, w, m, q, y
* Die Best Practice ist, denselben Datumsverweis im Start- und im Enddatum zu verwenden: cd, cd oder cw, cw oder cy, cy. Die Verwendung verschiedenartiger Abkürzungen kann an bestimmten Tagen des Jahres zu fehlerhaften Ergebnissen führen.
* Gültige Vielfache der Abkürzungen d w m q y werden durch ganze Zahlen (1 2 3 ... ) gebildet, die Abkürzung vorangestellt werden, z. B. 53d 3w 5q 9m 2y
* Nicht-ganzzahlige Werte sind nicht zulässig.
* Stellen Sie einer Abkürzung keine Null voran. Beispielsweise ist 0w nicht zulässig.
* Die folgenden Operatoren werden verwendet, um Abkürzungen zu verknüpfen: + -
* Da Datumsbereiche relativ zum aktuellen Zeitraum betrachtet werden müssen, beginnt der erste Term eines Ausdrucks immer mit einem c.

