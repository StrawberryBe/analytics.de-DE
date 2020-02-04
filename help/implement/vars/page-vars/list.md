---
title: befindet
description: Benutzerdefinierte Variablen, die mehrere Werte im selben Treffer enthalten.
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# befindet

Listenvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.

Vergewissern Sie sich, dass Sie aufzeichnen, wie Sie die einzelnen Listenvariablen und deren Logik in Ihrem [Lösungsdesigndokument](../../prepare/solution-design.md)verwenden.

> [!NOTE] Listenvariablen speichern die letzten 250 Werte pro Besucher. Wenn mehr als 250 individuelle Werte für einen bestimmten Besucher vorhanden sind, werden die ältesten Werte nicht den Metriken zugeordnet.

## Einrichten von Listenvariablen in den Report Suite-Einstellungen

Stellen Sie sicher, dass Sie jede Listenvariable in den Report Suite-Einstellungen konfigurieren, bevor Sie sie in Ihrer Implementierung verwenden. See [Conversion variables](/help/admin/admin/conversion-var-admin/list-var-admin.md) in the Admin guide.

## Variablen beim Starten der Adobe Experience Platform auflisten

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.list1 - s.list3 in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Jede Listenvariable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Sie haben keine maximale Bytezahl. Jeder einzelne Wert hat jedoch maximal 255 Byte. Das Trennzeichen, das Sie verwenden, wird beim Einrichten der Variablen in den Report Suite-Einstellungen festgelegt. Verwenden Sie keine Leerzeichen, wenn Sie mehrere Elemente trennen.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

> [!TIP] Wenn Sie im selben Treffer doppelte Werte festlegen, dedupliziert Adobe alle Instanzen dieser Werte. Wenn Sie z. B. eine Instanz festlegen, `s.list1 = "Example,Example";`wird eine Instanz in Berichten gezählt.

## Listen-Props mit Listenvariablen vergleichen

Listen-Props und Listenvariablen können im selben Treffer mehrere Werte enthalten. Zwischen diesen beiden Variablentypen gibt es jedoch einige wichtige Unterschiede.

* Jede Eigenschaftsvariable kann eine Listen-Prop werden. Sie können bis zu 75 Listen-Props haben, wenn jede Prop eine Listen-Prop ist. Es sind nur 3 Listenvariablen verfügbar.
* Listen-Props haben für die gesamte Variable einen Grenzwert von 100 Byte. Listenvariablen haben einen Grenzwert von 255 Byte pro Wert und keine Bytegrenze insgesamt.
* Listen-Props bleiben nicht über den Treffer hinaus erhalten, den sie festlegen. Für Listenvariablen gelten die gewünschten Ablaufeinstellungen. Bei der [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md)können Sie jedoch eine benutzerdefinierte Zuordnung sowohl auf Listen- als auch auf Listenvariablen anwenden.
