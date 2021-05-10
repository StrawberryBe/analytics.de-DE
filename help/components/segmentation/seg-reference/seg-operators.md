---
description: Mit dem Segmentaufbau können Sie Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
title: Vergleichsoperatoren für Segmente
feature: Segmentierung
uuid: 02ad814c-2c7c-4833-9bb2-4113dcf9475d
exl-id: 1ec1ff05-03a9-4151-8fcb-a72ebbce87dd
translation-type: tm+mt
source-git-commit: af3e4fc64085e94ec5616b8b6851a823e4954b36
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 99%

---

# Vergleichsoperatoren für Segmente

Mit dem Segmentaufbau können Sie Werte mithilfe ausgewählter Operatoren vergleichen und beschränken. Es gibt drei Kategorien von Operatoren: Standard, Data Warehouse und Distinct Count.

Das einzige unterstützte Platzhalterzeichen ist das Sternchen: *. Wenn Sie nach „*“ suchen müssen, können Sie dieses mit einem Backslash schützen.

**Beispiel**: Angenommen, Sie haben einen Seitennamen „My cool product“. Die Segmentregel „Seitenname entspricht My*product“ entspricht dem obigen Seitennamen. Die Regel „Seitenname entspricht My\\*product“ entspricht hingegen nur dem Seitennamen „My*Product“.

## Standardoperatoren

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
|--- |--- |
| gleich | Gibt Elemente mit einer exakten Entsprechung für numerische oder Zeichenfolgenwerte wieder. Hinweis: Nutzen Sie bei Verwendung von Platzhalterzeichen den Operator „stimmt überein mit“. |
| ist nicht gleich | Gibt alle Elemente zurück, die keine exakte Übereinstimmung mit dem eingegebenen Wert enthalten.  Hinweis: Nutzen Sie bei Verwendung von Platzhalterzeichen den Operator „stimmt nicht überein mit“. |
| entspricht einem der folgenden Werte | Gibt Elemente zurück, die exakt mit einem beliebigen Wert im Eingabefeld übereinstimmen (bis zu 500 Elemente). Wenn Sie beispielsweise „Suchergebnisse, Homepage“ mit diesem Operator eingeben, werden „Suchergebnisse“ und „Homepage“ abgeglichen und zählen als 2 Elemente. Das Eingabefeld für diesen Operator ist kommagetrennt. |
| entspricht keinem der folgenden Werte | Identifiziert Elemente, die exakt mit einem beliebigen Wert im Eingabefeld übereinstimmen, (bis zu 500 Elemente) und gibt dann nur Elemente ohne diese Werte zurück. Wenn Sie beispielsweise „Suchergebnisse, Homepage“ mit diesem Operator eingeben, werden „Suchergebnisse“ und „Homepage“ identifiziert und von den zurückgegebenen Elementen ausgeschlossen. Dieses Beispiel würde als 2 Elemente zählen. Das Eingabefeld für diesen Operator ist kommagetrennt. |
| enthält | Gibt Elemente zurück, die mit den Unterzeichenfolgen der eingegebenen Werte vergleichbar sind. Wenn die Regel für „Seite“ z. B. „Suche“ enthält, stimmt dies mit allen Seiten überein, die die Unterzeichenfolge „Suche“ enthalten, z. B. „Suchergebnisse“, „Suche“ und „Suchen“. |
| „Enthält nicht“ | Gibt das Gegenteil der Regel „enthält“ zurück. Insbesondere werden alle Elemente, die mit dem eingegebenen Wert übereinstimmen, aus den eingegebenen Werten ausgeschlossen. Wenn die Regel für „Seite“ z. B. „Suche“ nicht enthält, stimmt dies mit keiner Seite überein, die die Unterzeichenfolge „Suche“ enthält, z. B. „Suchergebnisse“, „Suche“ und „Suchen“. Diese Werte werden aus den Ergebnissen ausgeschlossen. |
| enthält alle von | Gibt Elemente zurück, die mit den Unterzeichenfolgen vergleichbar sind, einschließlich mehrerer miteinander verbundener Werte. Wenn z. B. „Suchergebnisse“ mit diesem Operator eingegeben wird, stimmen „Suchergebnisse“ und „Ergebnisse der Suche“ überein, „Suche“ oder „Ergebnisse“ als unabhängige Werte jedoch nicht. Eine Übereinstimmung liegt vor, wenn „Suche“ UND „Ergebnisse“ gemeinsam gefunden werden. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| enthält nicht alle von | Ermittelt Elemente, die mit Unterzeichenfolgen verglichen werden – einschließlich mehrfacher miteinander verbundener Werte –, und gibt anschließend lediglich Elemente ohne diese Werte zurück. Beispielsweise werden bei der Eingabe von „Suchergebnisse“ mit diesem Operator „Suchergebnisse“ und „Ergebnisse der Suche“ ermittelt (jedoch nicht „Suche“ oder „Ergebnisse“ als unabhängige Werte) und anschließend ausgenommen. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| enthält beliebige von | Gibt Elemente zurück, die mit den Unterzeichenfolgen vergleichbar sind, einschließlich mehrerer miteinander verbundener oder unabhängig erkannter Werte. Wenn z. B. „Suchergebnisse“ mit diesem Operator eingegeben wird, stimmen „Suchergebnisse“, „Ergebnisse der Suche“, „Suche“ und „Ergebnisse“ überein. Eine Übereinstimmung liegt vor, wenn entweder „Suche“ ODER „Ergebnisse“ zusammen oder unabhängig voneinander gefunden werden. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| enthält keinen von | Ermittelt Elemente basierend auf Unterzeichenfolgen und gibt Werte zurück, die diese Zeichenfolgen nicht enthalten. Kann mehrfache zusammengefasste Werte oder unabhängig ermittelte Werte umfassen. Wenn z. B. „Suchergebnisse“ eingegeben wird, stimmen „Suchergebnisse“, „Ergebnisse der Suche“, „Suche“ und „Ergebnisse“ überein, wobei sowohl „Suche“ als auch „Ergebnisse“ zusammen oder unabhängig voneinander gefunden werden. Anschließend würden die Elemente ausgenommen, die diese Unterzeichenfolgen enthalten. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| beginnt mit | Gibt Elemente zurück, die mit dem Zeichen oder der Zeichenfolge des eingegebenen Werts beginnen. |
| beginnt nicht mit | Gibt alle Elemente zurück, die nicht mit dem Zeichen oder der Zeichenfolge der eingegebenen Werte beginnen. Dies ist das Gegenteil des Operators „beginnt mit“. |
| endet mit | Gibt Elemente zurück, die mit dem Zeichen oder der Zeichenfolge des eingegebenen Werts enden. |
| endet nicht mit | Gibt alle Elemente zurück, die nicht mit dem Zeichen oder der Zeichenfolge der eingegebenen Werte enden. Dies ist das Gegenteil des Operators „endet mit“. |
| stimmt überein mit | Gibt Elemente mit einer exakten Entsprechung für gegebene numerische oder Zeichenfolgenwerte wieder. Hinweis: Nutzen Sie diesen Operator bei der Verwendung von Platzhalterfunktionen (Globbing). |
| stimmt nicht überein mit | Gibt alle Elemente zurück, die keine exakte Übereinstimmung mit dem eingegebenen Wert enthalten. Hinweis: Nutzen Sie diesen Operator bei der Verwendung von Platzhalterfunktionen (Globbing). |
| vorhanden | Gibt die Anzahl der vorhandenen Elemente zurück. Wenn Sie z. B. die Dimension „Seiten nicht gefunden“ mithilfe des Operators „vorhanden“ auswerten, wird die Anzahl der vorhandenen Fehlerseiten zurückgegeben. |
| nicht vorhanden | Gibt alle nicht vorhandenen Elemente zurück. Wenn Sie zum Beispiel die Dimension „Seiten nicht gefunden“ mithilfe des Operators „nicht vorhanden“ auswerten, wird die Anzahl der Seiten zurückgegeben, bei denen diese Fehlerseite nicht vorhanden war. |

## Data Warehousen

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
| --- | --- |
| kleiner als | Gibt Elemente zurück, deren numerische Anzahl kleiner als der eingegebene Wert ist. |
| kleiner als oder gleich | Gibt Elemente zurück, deren numerische Anzahl kleiner als der eingegebene Wert ist oder damit übereinstimmt. |
| größer als | Gibt Elemente zurück, deren numerische Anzahl größer als der eingegebene Wert ist. |
| größer als oder gleich | Gibt Elemente zurück, deren numerische Anzahl größer als der eingegebene Wert ist oder damit übereinstimmt. |

## Operatoren für bestimmte Zähler

Sie können nach einer bestimmten Anzahl von Elementen innerhalb einer Dimension segmentieren. Beispiele: „Besucher, die mehr als 5 verschiedene Produkte angesehen haben“ oder „Besuche, bei denen mehr als 5 verschiedene Seiten angesehen wurden.“

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
| --- | --- |
| gleich | Gibt Dimensionselemente zurück, deren eindeutige Anzahl dem eingegebenen Wert entspricht. |
| ist nicht gleich | Gibt Dimensionselemente zurück, deren eindeutige Anzahl nicht dem eingegebenen Wert entspricht. |
| größer als | Gibt Dimensionselemente zurück, deren eindeutige Anzahl größer als der eingegebene Wert ist. |
| kleiner als | Gibt Dimensionselemente zurück, deren eindeutige Anzahl kleiner als der eingegebene Wert ist. |
| größer als oder gleich | Gibt Dimensionselemente zurück, deren eindeutige Anzahl größer als der eingegebene Wert ist oder damit übereinstimmt. |
| kleiner als oder gleich | Gibt Dimensionselemente zurück, deren eindeutige Anzahl kleiner als der eingegebene Wert ist oder damit übereinstimmt. |
