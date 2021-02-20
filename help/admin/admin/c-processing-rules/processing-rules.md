---
description: Verarbeitungsregeln erleichtern die Datenerfassung und ermöglichen die Verwaltung der Inhalte, die an die Berichterstellung gesendet wurden.
subtopic: Processing rules
title: Übersicht über Verarbeitungsregeln
topic: Admin tools
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
translation-type: tm+mt
source-git-commit: 4cacd06d268c501ade05487c594bc68aa22e9f4c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 80%

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

## Vereinfachung der Datenerfassung durch Kontextdaten   {#section_09EEA03612D24C15839631AA9E9668D8}

Kontextdatenvariablen sind Variablentypen, die nur für Verarbeitungsregeln verfügbar sind. Für die Verwendung von Kontextdatenvariablen werden Schlüssel-Wert-Datenpaare durch unsere Implementierung eingereicht, und es werden Verarbeitungsregeln angewendet, um diese Werte in Standard-Analytics-Variablen zu erfassen. So müssen Programmierer nicht immer genau wissen, welche Prop und/oder eVar welchen Wert enthalten muss.

![](assets/evar-context-map.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/contextdata.html) in der Implementierungshilfe.

## Verwenden von Verarbeitungsregeln zum Korrigieren von Daten und zum Auslösen von Ereignissen   {#section_8284E72E999244E091CD7FB1A22342B6}

Mit Verarbeitungsregeln können eingehende Werte überwacht werden. Dabei werden gängige Schreibfehler korrigiert und Ereignisse auf Basis der Berichtsdaten festgelegt. Props können in eVars kopiert werden, Werte lassen sich zu Berichtzwecken miteinander verketten, und Ereignisse können festgelegt werden.

## Verwenden von Kontextdatenvariablen in Berichten   {#section_BD098BC503024A0B8703596628071134}

Sobald in Ihrer Implementierung Kontextdatenvariablen definiert sind, müssen diese in Variablen wie eVars kopiert werden, damit sie in Berichten verwendet werden können.

Weitere Informationen finden Sie  [hier](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) und [hier](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md).
