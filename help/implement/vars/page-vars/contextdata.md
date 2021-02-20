---
title: contextData
description: Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 100%

---


# contextData

Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können. Anstatt Analytics-Variablen explizit Werte in Ihrem Code zuzuweisen, können Sie Daten in Kontextdatenvariablen senden. Verarbeitungsregeln nehmen dann Kontextdatenvariablenwerte auf und übergeben sie an die entsprechenden Analytics-Variablen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md).

Kontextdatenvariablen sind für Entwicklungsteams hilfreich, um Daten in benannten Elementen, statt in nummerierten Variablen zu erfassen. Anstatt beispielsweise anzufordern, dass Entwicklungsteams den Autor der Seite `eVar10` zuweisen, können Sie sie stattdessen auffordern, ihn `s.contextData["author"]` zuzuweisen. Ein Analytics-Administrator in Ihrem Unternehmen kann dann Verarbeitungsregeln erstellen, um Kontextdatenvariablen Analysevariablen für die Berichterstellung zuzuordnen. Entwicklungsteams würden sich letztlich nur um Kontextdatenvariablen kümmern, nicht um die vielen Seitenvariablen, die Adobe anbietet.

## Kontextdatenvariablen in Adobe Experience Platform Launch

Es gibt keine spezielle Stelle in Launch, um Kontextdatenvariablen festzulegen. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.contextData in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.contextData`-Variable nimmt keinen Wert direkt an. Setzen Sie stattdessen die Eigenschaften dieser Variable auf eine Zeichenfolge.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Gültige Kontextdatenvariablen enthalten nur alphanumerische Zeichen, Unterstriche und Punkte. Adobe garantiert die Datenerfassung in den Verarbeitungsregeln nicht, wenn Sie andere Zeichen, wie z. B. Bindestriche, einfügen.
* Starten Sie Kontextdatenvariablen nicht mit `"a."`. Dieses Präfix ist reserviert und wird von Adobe verwendet. Verwenden Sie zum Beispiel nicht `s.contextData["a.InstallEvent"]`.
* Bei Kontextdatenvariablen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Variablen `s.contextData["example"]` und `s.contextData["EXAMPLE"]` sind identisch.

## Verwenden von Verarbeitungsregeln zum Ausfüllen von Analytics-Variablen

>[!IMPORTANT]
>
>Kontextdatenvariablen werden nach Ausführung der Verarbeitungsregeln verworfen. Wenn keine Verarbeitungsregeln aktiv sind, die Werte in Variablen platzieren, gehen diese Daten dauerhaft verloren!

1. Aktualisieren Sie Ihre Implementierung, um Kontextdatenvariablennamen und -werte festzulegen.
2. Melden Sie sich bei Adobe Analytics an und gehen Sie zu „Admin“ > „Report Suites“.
3. Wählen Sie die gewünschte Report Suite aus und gehen Sie dann zu „Einstellungen bearbeiten“ > „Allgemein“ > „Verarbeitungsregeln“.
4. Erstellen Sie eine Verarbeitungsregel, die eine Analytics-Variable auf den Wert der Kontextdatenvariablen setzt.
5. Speichern Sie die Änderungen.

Verarbeitungsregeln werden sofort nach dem Speichern wirksam. Sie gelten nicht für historische Daten.

## Senden von Kontextdaten in einem Linktracking-Aufruf

Schließen Sie die Kontextdatenvariable als Eigenschaft von `contextData` in [`s.linkTrackVars`](../config-vars/linktrackvars.md) ein:

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```

## Ereignisse mithilfe von Kontextdatenvariablen erhöhen

Beim Erstellen von Verarbeitungsregeln können Sie Ereignissen Kontextdatenvariablen zuweisen.

* Enthält eine Kontextdatenvariable einen Textt, wird das Ereignis um 1 inkrementiert.
* Wenn eine Kontextdatenvariable eine Ganzzahl enthält, wird das Ereignis um diesen ganzzahligen Betrag inkrementiert.

```js
// Assigning this context data variable to an event increments it by one
s.contextData["example_text"] = "Text value";

// Assigning this context data variable to an event increments it by four
s.contextData["example_number"] = "4";
```
