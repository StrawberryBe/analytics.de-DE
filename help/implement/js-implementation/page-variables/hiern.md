---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---



# hierN

Die Variable [!UICONTROL hierarchy] bestimmt die Positionierung einer Seite in der Hierarchie der Site.


<!-- 

hierN.xml

 -->

Bei Sites mit mehr als drei Ebenen in der Sitestruktur ist diese Variable besonders nützlich. So kann zum Beispiel eine Mediensite über vier Ebenen im Abschnitt „Sport“ verfügen: Sport, Lokaler Sport, Fußball, Bayern München. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ widergegeben.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | H1-H5 | Hierarchie | "" |

Es sind fünf [!UICONTROL hierarchy]-Variablen verfügbar, die vom Adobe-Kundendienst aktiviert werden müssen. Bei Aktivierung der hierarchy-Variablen müssen Sie festlegen, welches Trennzeichen verwendet werden soll und über wie viele Ebenen die Hierarchie maximal verfügen soll. Wenn beispielsweise ein Komma als Trennzeichen dient, wird die Sporthierarchie wie folgt dargestellt.

```js
s.hier1="Sports,Local Sports,Baseball"
```

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn zum Beispiel einer Ihrer Abschnitte „Trainer Heynckes, Jupp“ heißt, sollten Sie kein Komma als Trennzeichen festlegen. Jeder Hierarchieabschnitt ist auf 255 Byte beschränkt, wobei das Limit für die Variable insgesamt 255 Byte beträgt. Nach Auswahl des Trennzeichens (zum Zeitpunkt der Erstellung der Hierarchie) ist eine spätere Änderung nicht so einfach möglich.

Wenden Sie sich an den Adobe-Kundendienst, wenn Sie bei einer vorhandenen Hierarchie das Trennzeichen ändern möchten. Trennzeichen können auch aus mehreren Zeichen bestehen (z. B. || oder /|\), bei denen es unwahrscheinlich ist, dass sie in Namen von Hierarchieabschnitten enthalten sind.

**Syntax und mögliche Werte** {#section_0739948A68A2420DAB1CBEA3115A5A66}

Zwischen den einzelnen Trennzeichen darf kein Leerzeichen stehen. Im folgenden Syntaxbeispiel steht „N“ für eine Ziffer zwischen 1 und 5.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

Setzen Sie das Trennzeichen nur ein, um die Ebenen der Hierarchie voneinander zu trennen. Als Trennzeichen sind ein oder mehrere beliebige Zeichen Ihrer Wahl erlaubt.

**Beispiele** {#section_38E0929F88DD45B6ACDF473DF155971D}

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

**Konfigurationseinstellungen** {#section_E823FB3CAD744D2480EBCE2DF9B134CC}

Keine

**Probleme, Fragen und Tipps** {#section_104E5BD320764BDEA5FA8D13A70C78E3}

* Das Trennzeichen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden. Wenn Sie bei Ihrer Hierarchie das Trennzeichen ändern müssen, wenden Sie sich an den Adobe-Kundendienst.
* Die Anzahl der Ebenen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden.

> [!NOTE] Änderungen an Hierarchien können dazu führen, dass eine kostenpflichtige Serviceleistung berechnet wird.

