---
title: Lösungsdesigndokument erstellen
description: Erfahren Sie, was ein Lösungsdesigndokument ist und wie Sie es in Ihrem Unternehmen verwenden können.
translation-type: ht
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707
workflow-type: ht
source-wordcount: '696'
ht-degree: 100%

---


# Lösungsdesigndokument erstellen

Ein Dokument zum Lösungsentwurf (auch als Referenz zum Lösungsentwurf oder als Dokument zu Geschäftsanforderungen bezeichnet) ist im Wesentlichen der Entwurf Ihrer Analytics-Implementierung. Es definiert Kriterien, die von Interessenträgern in Ihrer gesamten Organisation identifiziert werden, und übersetzt diese in Variablen in Adobe Analytics. Ohne eine Lösung haben Unternehmen Schwierigkeiten, die Berichtserfordernisse zu koordinieren, und neigen dazu, das Erfassen wichtiger Daten zu übersehen.

## Voraussetzungen

[Überprüfen Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie in der Produktion](../launch/validate-publish-prod.md) - Adobe empfiehlt, eine Basisimplementierung einzurichten, damit wichtige Daten gesammelt werden, während zusätzliche Geschäftsanforderungen festgelegt und implementiert werden.

## Eigentum und Speicherort des Entwurfspapiers

* **Stellen Sie fest, wer in Ihrem Unternehmen für die Verwaltung des Lösungsentwurfsdokuments verantwortlich ist.** Diese Rolle kann entweder eine Einzelperson oder ein Team innehaben. Stellen Sie sicher, dass der Lösungsentwurf auch durch Rollenänderungen oder Organisationsänderungen erhalten bleibt. Es handelt sich um ein lebendiges Dokument, das ordnungsgemäß aufbewahrt werden muss.
* **Stellen Sie fest, wo sich Ihr Lösungsdokument befindet.** Es gibt keinen einzigen idealen Ort, an dem sich Lösungsdesigndokumente befinden, aber sie befinden sich normalerweise an einem gut zugänglichen internen Ort. Beispiele sind eine freigegebene Tabelle oder ein gemeinsamer Arbeitsbereich wie SharePoint oder ein internes Wiki. Sie müssen nicht für jeden bearbeitbar sein, aber es ist hilfreich, wenn zumindest die Anzeige möglich ist,

## Geschäftsanforderungen definieren

Bei der Ermittlung der zu erfassenden Daten ist es leicht, „alles“ zu sagen, was jedoch schnell schwer zu handhaben sein kann und sogar weniger Wert bieten kann als die Erfassung präziserer Datenmengen.

1. **Bestimmen Sie die wichtigen Leistungsindikatoren.** Was sollen die Besucher letztendlich tun? Die Antwort auf diese Frage variiert je nach Branche und kann mehrere Dinge umfassen. Beispiele sind Käufe, Registrierungen oder Anzeigenklicks.
1. **Ermittlung der wichtigsten zu erfassenden Daten.** Stellen Sie Geschäftsfragen, auf die Sie spezifische Antworten erhalten möchten. Antworten auf diese Fragen würden Einblicke in die Verbesserung der KPIs geben.
1. **Nehmen Sie diese Fragen auf und bestimmen Sie, was Sie für das Tracking benötigen.** Gruppieren Sie sie in Dimensionen und Metriken.
   * Dimensionen sind Variablen, die Text enthalten. Beispiele wären der interne Suchbegriff, die Produktkategorie oder der Name eines Bereichs, auf den ein Besucher geklickt hat.
   * Metriken sind spezifische Ereignisse, die ein Besucher ausführen soll - wenn er eine gewünschte Aktion durchführt, steigt die Zahl um 1. Beispiele wären das Senden einer Bestellung, das Abonnieren eines Newsletters oder das Senden einer Umfrageantwort.
1. **Ordnen Sie Dimensionen und Metriken einer Seite oder Tabelle zu.** Diese Seite oder Tabelle wird letztendlich zu Ihrem Lösungsdesigndokument. Einige hilfreiche Spalten oder Aufzählungspunkte, die eingeschlossen werden sollen:
   * Implementierungsstatus: Geplant, aktiv, inaktiv, Probleme usw. Dadurch werden die Betrachter über den Status des Dokuments informiert, wenn die Variable implementiert wurde oder Probleme mit der Datenerfassung auftreten.
   * Variablenname: Beispiel: „Interne Suchbegriffe“. Dieser Wert ist der Wert, den Analysten bei der Arbeit in Analytics sehen.
   * Zugeordnete Analytics-Variable: welcher standardmäßigen oder benutzerdefinierten Analytics-Variable Werte zugewiesen werden sollen. Dimensionen fallen normalerweise unter eVars, während Metriken unter Ereignisse fallen.
   * Logik: Eine Beschreibung, wie die Variable festgelegt wird und was deren Wert bestimmt. Beispiel: „Nur auf internen Suchseiten eingestellt. Übernimmt den Wert des Abfragezeichenfolgenparameters q.“
   * Sonstige Hinweise zur Variablen.

## Zusätzliche Ressourcen

Die Definition eines Lösungsdesigndokuments ist ein ziemlich komplexes Projekt, besonders für Unternehmen, die noch kein Projekt erstellt haben. Wenn Sie weitere Unterstützung benötigen, bietet Adobe eine spezielle Beratung an, um Ihr Unternehmen bei der Einführung von Adobe Analytics zu unterstützen. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie die professionellen Services von Adobe nutzen möchten. Es kann ein [technischer Fragenkatalog](assets/technical-pre-implementation-questionnaire.pdf) zur Implementierung ausgefüllt werden, damit Adobe anhand der Anforderungen Ihres Unternehmens genau weiß, wie Sie dabei unterstützt werden können.

Es gibt auch mehrere Adobe-Partner, die sich auf die Unterstützung bei der Erstellung eines Lösungsdesigndokuments sowie die Implementierung von Adobe Analytics auf Ihrer Site spezialisiert haben.

## Nächste Schritte

Implementieren Sie die Variablen in Ihr Lösungsdesigndokument.

[Erstellen Sie eine Datenschicht](data-layer.md): Übersetzen Sie Variablen in Ihrem Design-Dokument in JavaScript-Variablen auf Ihrer Site.
