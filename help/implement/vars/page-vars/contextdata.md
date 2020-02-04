---
title: contextData
description: Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# contextData

Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können. Anstatt Analytics-Variablen explizit Werte in Ihrem Code zuzuweisen, können Sie Daten in Kontextdatenvariablen senden. Verarbeitungsregeln nehmen dann Kontextdatenvariablenwerte auf und übergeben sie an die entsprechenden Analytics-Variablen. See [Processing rules](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) in the Admin user guide.

Kontextdatenvariablen sind für Entwicklungsteams hilfreich, um Daten in benannten Elementen statt in nummerierten Variablen zu erfassen. Anstatt zum Beispiel Entwicklungsteams anzufordern, den Autor der Seite zuzuweisen, können Sie `eVar10`anfordern, dass sie `s.contextData["author"]` stattdessen die Seite zuweisen. Ein Analytics-Administrator in Ihrem Unternehmen kann dann Verarbeitungsregeln erstellen, um Kontextdatenvariablen Analysevariablen für die Berichterstellung zuzuordnen. Entwicklungsteams würden sich letztlich nur um Kontextdatenvariablen kümmern, nicht um die vielen Seitenvariablen, die Adobe anbietet.

## Kontextdatenvariablen beim Start der Adobe Experience Platform

Launch verfügt nicht über einen speziellen Speicherort zum Festlegen von Kontextdatenvariablen. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.contextData in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `s.contextData` Variable nimmt keinen Wert direkt an. Legen Sie stattdessen die Eigenschaften dieser Variablen auf eine Zeichenfolge fest.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Gültige Kontextdatenvariablen enthalten nur alphanumerische Zeichen, Unterstriche und Punkte. Adobe übernimmt keine Garantie für die Datenerfassung in Verarbeitungsregeln, wenn Sie andere Zeichen wie z. B. Bindestriche einschließen.
* Starten Sie keine Kontextdatenvariablen mit `"a."`. Dieses Präfix ist von Adobe reserviert und wird verwendet. Verwenden Sie zum Beispiel nicht `s.contextData["a.InstallEvent"]`.
* Bei Kontextdatenvariablen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Variablen `s.contextData["example"]` und `s.contextData["EXAMPLE"]` sind identisch.

## Verwenden von Verarbeitungsregeln zum Ausfüllen von Analysevariablen

> [!IMPORTANT] Kontextdatenvariablen werden nach Ausführung der Verarbeitungsregeln verworfen. Wenn keine Verarbeitungsregeln aktiv sind, die Werte in Variablen platzieren, gehen diese Daten dauerhaft verloren!

1. Aktualisieren Sie Ihre Implementierung, um Kontextdatenvariablennamen und -werte festzulegen.
2. Melden Sie sich bei Adobe Analytics an und gehen Sie zu Admin > Report Suites.
3. Wählen Sie die gewünschte Report Suite aus und gehen Sie dann zu Einstellungen bearbeiten > Allgemein > Verarbeitungsregeln.
4. Erstellen Sie eine Verarbeitungsregel, die eine Analytics-Variable auf den Wert der Kontextdatenvariablen setzt.
5. Speichern Sie die Änderungen.

Verarbeitungsregeln werden sofort nach dem Speichern wirksam. Sie gelten nicht für historische Daten.

## Senden von Kontextdaten in einem Linkverfolgungsaufruf

Schließen Sie die Kontextdatenvariable als Eigenschaft von `contextData` in ein `s.linkTrackVars`:

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```
