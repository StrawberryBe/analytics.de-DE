---
description: Verarbeitungsregeln erleichtern die Datenerfassung und ermöglichen die Verwaltung der Inhalte, die an die Berichterstellung gesendet wurden.
subtopic: Processing rules
title: Übersicht über Verarbeitungsregeln
feature: Processing Rules
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: ht
source-wordcount: '373'
ht-degree: 100%

---

# Übersicht über Verarbeitungsregeln

Verarbeitungsregeln erleichtern die Datenerfassung und ermöglichen die Verwaltung der Inhalte, die an die Berichterstellung gesendet wurden. Verarbeitungsregeln vereinfachen die Interaktion mit IT-Gruppen und Web-Entwicklern, da sie eine Schnittstelle für folgende Aufgaben bereitstellen:

* Festlegen eines Ereignisses auf der Seite mit der Produktübersicht
* Auffüllen von Kampagnen mit einem Abfragezeichenfolgenparameter
* Verketten von Kategorien und Seitennamen in einer Prop zur leichteren Berichterstellung
* Anzeigen von Pfaden durch das Kopieren von eVars in Props
* Korrigieren von Fehlschreibungen bei Sitebereichen
* Extrahieren von Suchbegriffen oder Kampagnen-IDs aus der Abfragezeichenfolge in eine eVar

>[!VIDEO](https://video.tv.adobe.com/v/26124/?quality=12&learn=on)

## Berechtigungen für Verarbeitungsregeln {#section_8A4846688050453784DAE4D89355169A}

Administratoren sind **standardmäßig** dazu berechtigt, Verarbeitungsregeln zu verwenden. Administratoren können diese Rechte über die Admin Tools-Benutzeroberfläche auch Benutzern ohne Administratorstatus gewähren. Eine Anleitung finden Sie unter []

![Verarbeitungsregeln](assets/processing-rules.png)

## Vereinfachung der Datenerfassung durch Kontextdaten  {#section_09EEA03612D24C15839631AA9E9668D8}

Kontextdatenvariablen sind ein Variablentyp, der nur für Verarbeitungsregeln zur Verfügung steht. Für die Verwendung von Kontextdatenvariablen werden Schlüssel-Wert-Datenpaare durch unsere Implementierung eingereicht, und es werden Verarbeitungsregeln angewendet, um diese Werte in Standard-Analytics-Variablen zu erfassen. So müssen Programmierer nicht immer genau wissen, welche Prop und/oder eVar welchen Wert enthalten muss.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

Sobald sie in einem Code verfügbar sind, können Sie Verarbeitungsregeln festlegen, um Variablen Werte zuzuweisen. Beispiel:

1. Zuordnung von `author` nach `eVar2`
2. Zuordnung von `section` nach `prop1` und `eVar3`
3. Wenn `author` und `section` vorhanden sind, legen Sie `event5` fest

Weitere Informationen finden Sie unter [contextData](/help/implement/vars/page-vars/contextdata.md) im Implementierungshandbuch.

## Verwenden von Verarbeitungsregeln zum Transformieren von Trefferdaten und zum Auslösen von Ereignissen  {#section_8284E72E999244E091CD7FB1A22342B6}

Mit Verarbeitungsregeln können eingehende Werte überwacht werden. Dabei werden gängige Schreibfehler korrigiert und Ereignisse auf Basis der Berichtsdaten festgelegt. Props können in eVars kopiert werden, Werte lassen sich zu Berichtzwecken miteinander verketten, und Ereignisse können festgelegt werden.

## Verwenden von Kontextdatenvariablen in Berichten  {#section_BD098BC503024A0B8703596628071134}

Nachdem in Ihrer Implementierung Kontextdatenvariablen definiert sind, müssen diese in Variablen wie eVars kopiert werden, damit sie in Berichten verwendet werden können.

Siehe [Kontextdatenvariable in eine eVar kopieren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) und [Ereignis mit einer Kontextdatenvariablen festlegen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md) für weitere Informationen.

## Bekannte Einschränkungen

**Verwendung von Karat (^) in Verarbeitungsregeln.** Wenn Sie in Verarbeitungsregeln Karat als Trennzeichen oder für andere Zwecke verwenden möchten, muss jedes einzelne Karat durch zwei Karat dargestellt werden. Stellen Sie beispielsweise einen einzelnen Karat mit ^^ dar, einen doppelten Karat mit ^^^^ etc.