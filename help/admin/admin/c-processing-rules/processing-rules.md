---
description: Verarbeitungsregeln erleichtern die Datenerfassung und ermöglichen die Verwaltung der Inhalte, die an die Berichterstellung gesendet wurden.
subtopic: Processing rules
title: Übersicht über Verarbeitungsregeln
feature: Admin Tools
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 68%

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

Administratoren haben standardmäßig die Berechtigung, Verarbeitungsregeln **zu verwenden.** Administratoren können diese Rechte über die Admin Tools-Benutzeroberfläche auch Benutzern ohne Administratorstatus gewähren. Eine Anleitung finden Sie unter []

![](assets/processing-rules.png)

>[!IMPORTANT]
>
>Da Verarbeitungsregeln dauerhafte Auswirkungen auf Analytics-Daten haben, empfiehlt Adobe dringend, dass Verarbeitungsregeladministratoren eine Zertifizierungsschulung in Adobe Analytics erhalten und mit allen Datenquellen für Ihre Report Suites (Standard-Websites, mobile Sites, mobile Apps, Dateneinfüge-API usw.) vertraut sein sollten. Kenntnisse der Kontextdatenvariablen sowie der Standardvariablen, die in verschiedenen Plattformen enthalten sind, tragen dazu bei, ein versehentliches Löschen oder Ändern von Daten zu vermeiden.

## Vereinfachung der Datenerfassung durch Kontextdaten  {#section_09EEA03612D24C15839631AA9E9668D8}

Kontextdatenvariablen sind Variablentypen, die nur für Verarbeitungsregeln verfügbar sind. Für die Verwendung von Kontextdatenvariablen werden Schlüssel-Wert-Datenpaare durch unsere Implementierung eingereicht, und es werden Verarbeitungsregeln angewendet, um diese Werte in Standard-Analytics-Variablen zu erfassen. So müssen Programmierer nicht immer genau wissen, welche Prop und/oder eVar welchen Wert enthalten muss.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

Nach der Einstellung im Code können Sie Verarbeitungsregeln festlegen, um Variablen Werte zuzuweisen. Beispiel:

1. Ordnen Sie `author` zu `eVar2` zu
2. Ordnen Sie `section` zu `prop1` und `eVar3` zu
3. Wenn `author` und `section` vorhanden sind, setzen Sie `event5`

Weitere Informationen finden Sie unter [contextData](/help/implement/vars/page-vars/contextdata.md) im Benutzerhandbuch für die Implementierung.

## Verwenden von Verarbeitungsregeln zum Korrigieren von Daten und zum Auslösen von Ereignissen   {#section_8284E72E999244E091CD7FB1A22342B6}

Mit Verarbeitungsregeln können eingehende Werte überwacht werden. Dabei werden gängige Schreibfehler korrigiert und Ereignisse auf Basis der Berichtsdaten festgelegt. Props können in eVars kopiert werden, Werte lassen sich zu Berichtzwecken miteinander verketten, und Ereignisse können festgelegt werden.

## Verwenden von Kontextdatenvariablen in Berichten   {#section_BD098BC503024A0B8703596628071134}

Sobald in Ihrer Implementierung Kontextdatenvariablen definiert sind, müssen diese in Variablen wie eVars kopiert werden, damit sie in Berichten verwendet werden können.

Weitere Informationen finden Sie unter [Kopieren einer Kontextdatenvariablen in eine eVar](processing-rules-examples/processing-rules-copy-context-data.md) und [Festlegen eines Ereignisses mithilfe einer Kontextdatenvariablen](processing-rules-examples/processing-rules-copy-context-data-event.md).
