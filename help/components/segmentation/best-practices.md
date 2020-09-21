---
title: Best Practices für die Segmentierung
description: Erstellen Sie optimale Segmente, die Daten effizient zurückgeben.
translation-type: ht
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: ht
source-wordcount: '296'
ht-degree: 100%

---


# Best Practices für die Segmentierung

Oft sind komplexe Segmente erforderlich, um die gewünschten Daten zu erhalten. Wenn komplexe Segmente ineffizient sind und in einer großen Report Suite verwendet werden, dauert die Ausführung von Berichten erheblich länger. Berücksichtigen Sie beim Erstellen oder Bearbeiten eines Segments die folgenden Ressourcen, um die Komplexität zu minimieren.

## Verwenden Sie den Operator „Enthält“ nur als letzten Ausweg.

Der Operator „Enthält“ ist eine der verarbeitungsintensivsten Funktionen bei der Segmentierung, da er den gesamten Inhalt jedes Werts analysieren muss. Erwägen Sie die Verwendung anderer Operatoren wie „Beginn mit“ oder „Endet mit“, wenn sich die gewünschten Werte am Anfang oder am Ende einer Zeichenfolge befinden.

Wenn ein Operator „Enthält“ in einem Segment eine große Anzahl von Ergebnissen zurückgibt, wird der Bericht typischerweise mit einer Zeitüberschreitung abgebrochen. Wenn Sie z. B. ein Segment erstellt haben, in dem `Referrer equals "."`, durchsucht das Segment den Inhalt jedes Werts. Verwenden Sie stattdessen den Operator „Existiert“.

## Verwenden Sie Klassifizierungen zum Gruppieren von Dimensionselementen.

Wenn Sie viele Segmentbedingungen haben, können diese die Segmentleistung schnell beeinträchtigen. Zum Beispiel wurde `Page equals X or Page equals Y or Page equals Z`mit Hunderten von verschiedenen Werten wiederholt. Anstatt diese Hunderte von Bedingungen aufzuschreiben, klassifizieren Sie alle gewünschten Werte in ein Segment und verwenden Sie dann den klassifizierten Wert in einem Segment.

1. Erstellen Sie eine Classification für die Variable, mit der Sie arbeiten.
2. Laden Sie die Classification-Vorlage herunter und öffnen Sie sie in der gewünschten Tabelle oder im Texteditor.
3. Weisen Sie jedem Dimensionselement, das Sie in Ihr Segment einbeziehen möchten, denselben Wert zu.
4. Verwenden Sie den Classification Importer, um die Tabelle wieder in Adobe Analytics zu importieren.
5. Nachdem die Classification verarbeitet wurde, erstellen Sie ein Segment mit dem klassifizierten Wert.

Diese Methode erhöht die Leistung drastisch und bietet eine einfache Möglichkeit, Segmentbedingungen zu ändern. Anstatt das Segment mit unterschiedlichen Werten zu bearbeiten, können Sie Dimensionselemente zur Klassifizierung hinzufügen oder daraus entfernen.
