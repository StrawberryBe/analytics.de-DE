---
title: hier
description: Implementieren Sie Hierarchievariablen in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# hier

Hierarchievariablen sind benutzerdefinierte Variablen, mit denen Sie die Struktur einer Site sehen können.

Bei Sites mit mehr als drei Ebenen in der Sitestruktur ist diese Variable besonders nützlich. So kann zum Beispiel eine Mediensite über vier Ebenen im Abschnitt „Sport“ verfügen: Sport, Lokaler Sport, Fußball, Bayern München. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ widergegeben.

Es sind fünf [!UICONTROL hierarchy]-Variablen verfügbar, die vom Adobe-Kundendienst aktiviert werden müssen. Bei Aktivierung der hierarchy-Variablen müssen Sie festlegen, welches Trennzeichen verwendet werden soll und über wie viele Ebenen die Hierarchie maximal verfügen soll. Wenn beispielsweise ein Komma als Trennzeichen dient, wird die Sporthierarchie wie folgt dargestellt.

```js
s.hier1="Sports,Local Sports,Baseball"
```

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn zum Beispiel einer Ihrer Abschnitte „Trainer Heynckes, Jupp“ heißt, sollten Sie kein Komma als Trennzeichen festlegen. Jeder Hierarchieabschnitt ist auf 255 Byte beschränkt, wobei das Limit für die Variable insgesamt 255 Byte beträgt. Nach Auswahl des Trennzeichens (zum Zeitpunkt der Erstellung der Hierarchie) ist eine spätere Änderung nicht so einfach möglich.

Wenden Sie sich an den Adobe-Kundendienst, wenn Sie bei einer vorhandenen Hierarchie das Trennzeichen ändern möchten. Trennzeichen können auch aus mehreren Zeichen bestehen (z. B. || oder /|\), bei denen es unwahrscheinlich ist, dass sie in Namen von Hierarchieabschnitten enthalten sind.

## Syntax und mögliche Werte

Zwischen den einzelnen Trennzeichen darf kein Leerzeichen stehen. Im folgenden Syntaxbeispiel steht „N“ für eine Ziffer zwischen 1 und 5.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

Setzen Sie das Trennzeichen nur ein, um die Ebenen der Hierarchie voneinander zu trennen. Als Trennzeichen sind ein oder mehrere beliebige Zeichen Ihrer Wahl erlaubt.

## Beispiele

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

## Probleme, Fragen und Tipps

* Das Trennzeichen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden. Wenn Sie bei Ihrer Hierarchie das Trennzeichen ändern müssen, wenden Sie sich an den Adobe-Kundendienst.
* Die Anzahl der Ebenen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden.

> [!NOTE] Änderungen an Hierarchien können dazu führen, dass eine kostenpflichtige Serviceleistung berechnet wird.
