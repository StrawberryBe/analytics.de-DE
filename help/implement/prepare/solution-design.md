---
title: Erstellen eines Lösungsdesigndokuments
seo-title: Erstellen eines Lösungsdesigndokuments
description: Erfahren Sie, was ein Lösungsdesigndokument ist und wie Sie es in Ihrem Unternehmen verwenden können.
seo-description: Erfahren Sie, was ein Lösungsdesigndokument ist und wie Sie es in Ihrem Unternehmen verwenden können.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# Erstellen eines Lösungsdesigndokuments

Ein Dokument des Lösungsdesigners (auch als Referenz- oder Geschäftsanforderungen bezeichnet) ist im Grunde genommen das Blueprint Ihrer Analytics-Implementierung. Es definiert die Kriterien, die von den Stakeholdern innerhalb Ihres Unternehmens identifiziert wurden, und übersetzt diese in Variablen in Adobe Analytics. Ohne einen Unternehmen haben Organisationen eine schwierige Zeit, die Berichterstattungsbedürfnisse zu koordinieren und die Erfassung wichtiger Daten zu vernachlässigen.

## Voraussetzungen

[Validieren Ihrer Analytics-Implementierung und Veröffentlichung in der Produktion](../implement-with-launch/validate-publish-prod.md) - Obwohl nicht direkt erforderlich, empfiehlt Adobe, eine Basisimplementierung vorzunehmen, damit wichtige Daten erfasst werden, während zusätzliche Geschäftsanforderungen erstellt und implementiert werden.

## Eigentum und Speicherort des Designdokuments

* **Bestimmen Sie, wer in Ihrer Organisation für die Wartung des Dokuments für das Lösungsdesign verantwortlich sein wird.** Diese Rolle kann entweder ein einzelner Benutzer oder ein Team sein. Stellen Sie sicher, dass die Aufrechterhaltung des Lösungsentwurfs auch über Rollenänderungen oder Strukturierung von Organisationen beibehalten wird. Es ist ein Live-Dokument und muss ordnungsgemäß gepflegt werden.
* **Legen Sie fest, wo sich Ihr Lösungsdokument befindet.** Es gibt keinen einzelnen Ort für die Lösung von Lösungsdesigndokumenten, sie befinden sich jedoch meist in einem allgemein zugänglichen internen Ort. Beispiele sind eine freigegebene Tabelle oder ein Arbeitsbereich für Zusammenarbeit wie sharepoint oder ein interner Wiki. Sie muss für jeden nicht bearbeitet werden, es ist jedoch nützlich für diejenigen, die auf Berichte zugreifen können, um sie zumindest anzuzeigen.

## Geschäftsanforderungen definieren

Bei der Bestimmung der zu erfassenden Daten ist es einfach, "Alles" zu sagen, was jedoch schnell zu einer unbrauchbaren Verwaltung führt und sogar weniger Werte liefert als die Erfassung präziser Datenmengen.

1. **Bestimmen Sie die wichtigen Leistungsindikatoren.** Was sollen Besucher letztendlich tun? Die Antwort auf diese Frage variiert je nach Branche und vertikal und kann mehrere Dinge umfassen. Beispiele sind Käufe, Registrierungen oder Anzeigenklicks.
1. **Finden Sie heraus, welche wichtigen Daten gesammelt werden sollen.** Fragen Sie Geschäftsfragen, auf die Sie spezifische Antworten wünschen. Antworten auf diese Fragen bieten einen Einblick in die Verbesserung Ihrer Kpis.
1. **Nehmen Sie diese Fragen vor und legen Sie fest, wie Ihre Verfolgung benötigt wird.** Gruppieren Sie sie in Dimensionen und Metriken.
   * Dimensionen sind Variablen, die Text enthalten. Beispiele wären interne Suchbegriffe, Produktkategorien oder der Name eines Bereichs, auf den ein Besucher geklickt hat.
   * Metriken sind spezifische Ereignisse, die ein Besucher ausführen soll. Wenn sie eine Aktion durchführen, die Sie wünschen, wird die Zahl um 1 erhöht. Beispiele wären die Übermittlung einer Bestellung, das Abonnieren eines Newsletters oder das Senden einer Umfrageantwort.
1. **Dimensionen und Metriken in einer Seite oder Tabelle zuordnen.** Diese Seite oder Tabelle wird letztendlich zu Ihrem Lösungsdesigndokument. Einige hilfreiche Spalten oder Aufzählungspunkte für die Einbeziehung:
   * Implementierungsstatus: Geplante, aktive, inaktive, Probleme usw. Dadurch werden die Viewer des jeweiligen Variablenstatus, falls dieser implementiert wurde, oder Probleme mit der Datenerfassung beschrieben.
   * Variablenname: Beispiel: "Interne Suchbegriffe" . Dieser Wert wird von Analysten bei der Arbeit in Analytics angezeigt.
   * Analytics-Variable zugeordnet zu: Welche standardmäßige oder benutzerdefinierte Analytics-Variable, dem Sie Werte zuweisen möchten Dimensionen fallen normalerweise unter evars, während Metriken unter Ereignisse fallen.
   * Logik: Eine Beschreibung der Art und Weise, wie die Variable festgelegt wird und deren Wert bestimmt wird. Beispiel: "Nur auf internen Suchseiten eingestellt. Akzeptiert den Wert des Abfragezeichenfolgenparameters q. «
   * Alle anderen Hinweise, die in die Variable einbezogen werden sollen

## Zusätzliche Ressourcen

Das Definieren eines Lösungsdesigndokuments ist ein ziemlich komplexer Projekt, insbesondere für Organisationen, die noch keine erstellt haben. Wenn zusätzliche Hilfe gewünscht wird, bietet Adobe spezialisierte Beratung an, um Ihre Organisation mit Adobe Analytics zu versorgen. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie die Professional Services von Adobe auflisten möchten. A [Technical pre-implementation questionnaire](assets/technical-pre-implementation-questionnaire.pdf) can be filled out so Adobe knows exactly how to help based on your organization's needs.

Es gibt auch verschiedene Adobe-Partner, die sich für die Erstellung eines Lösungsdesigndokuments sowie für die Implementierung von Adobe Analytics auf Ihrer Site spezialisieren.

> [!NOTE] Obwohl Mitglieder der Analytics-Community die folgenden Links hilfreich gefunden haben, befinden sie sich nicht von Adobe. Beachten Sie diese Hinweise bei der Anzeige ihres Inhalts.

* [7 Schritte zum Einrichten Ihres Webanalyselösungsdesigns](https://resources.observepoint.com/blog/7-steps-solution-design-data-governance) nach observepoint
* [Ein Framework für Digital Analytics-Prozess](https://analyticsdemystified.com/analytics-strategy/framework-digital-analytics-process/) mit demystisiertem Analytics
* [Die Lösungsdesignreferenz ist eigentlich Ihr BFF](http://numericanalytics.com/why-a-simple-piece-of-documentation-is-the-key-to-analytics-success-the-solution-design-reference-is-actually-your-bff/) nach numerischen Analysen.
* [Tagging von](http://www.anttikoski.fi/how-to-make-adobe-analytics-tagging-map-aka-solution-design-requirements-for-sitecatalyst-implementation/) Adobe Analytics durch Antti Koski
* [Die Wichtigkeit des Lösungsdesigndokuments](https://www.ebiquity.com/news-insights/analytics/the-importance-of-the-solution-design-document) nach Ebiquity

## Nächste Schritte

Implementieren Sie die Variablen in Ihrem Lösungsdesigndokument.

* Einführung in evars: Erfahren Sie, was eine evar ist, wie sie funktioniert und wie sie sie in Ihrer Implementierung einsetzen.
* Einführung in Ereignisse: Erfahren Sie, was ein Erfolgsereignis ist, wie es funktioniert und wie es in Ihrer Implementierung verwendet wird.
