---
title: Best Practices zur Segmentierung
description: Erstellen Sie optimale Segmente, die Daten effizient zurückgeben.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Best Practices zur Segmentierung

Komplexe Segmente sind häufig erforderlich, um die gewünschten Daten zu erhalten. Wenn komplexe Segmente ineffizient sind und in einer großen Report Suite verwendet werden, dauert die Ausführung von Berichten erheblich länger. Berücksichtigen Sie beim Erstellen oder Bearbeiten eines Segments die folgenden Ressourcen, um die Komplexität zu minimieren.

## Verwenden Sie nur den Operator &quot;Enthält&quot;als letzten Ausweg

Der Operator &#39;Enthält&#39; ist eine der am meisten verarbeitenden Funktionen in der Segmentierung, da er den gesamten Inhalt jedes Werts analysieren muss. Erwägen Sie die Verwendung anderer Operatoren wie &quot;Beginn mit&quot;oder &quot;Endet mit&quot;, wenn sich die gewünschten Werte am Anfang oder am Ende einer Zeichenfolge befinden.

Wenn ein &quot;Enthält&quot;-Operator in einem Segment eine große Anzahl von Ergebnissen zurückgibt, ist die Zeitüberschreitung im Bericht in der Regel zu erwarten. Wenn Sie z. B. ein Segment erstellt haben, in dem `Referrer equals "."`das Segment den Inhalt jedes Werts durchsucht. Verwenden Sie stattdessen den Operator &quot;Exists&quot;.

## Klassifizierungen zum Gruppieren von Dimensionselementen verwenden

Bei vielen Segmentbedingungen kann die Segmentleistung schnell beeinträchtigt werden. Beispiel: `Page equals X or Page equals Y or Page equals Z` Wird mit Hunderten von verschiedenen Werten wiederholt. Klassifizieren Sie statt diese Hunderte von Bedingungen zu schreiben alle gewünschten Werte in ein Segment und verwenden Sie dann den klassifizierten Wert in einem Segment.

1. Erstellen Sie eine Classification für die Variable, mit der Sie arbeiten.
2. Laden Sie die Classification-Vorlage herunter und öffnen Sie sie in der gewünschten Tabelle oder im Texteditor.
3. Weisen Sie jedem Dimensionselement, das Sie in Ihr Segment einbeziehen möchten, denselben Wert zu.
4. Verwenden Sie den Classification Importer, um die Tabelle wieder in Adobe Analytics zu importieren.
5. Nachdem die Classification verarbeitet wurde, erstellen Sie ein Segment mit dem klassifizierten Wert.

Diese Methode erhöht die Leistung drastisch und bietet eine einfache Möglichkeit, Segmentbedingungen zu ändern. Statt das Segment mit unterschiedlichen Werten zu bearbeiten, können Sie Dimensionselemente der Klassifizierung hinzufügen oder daraus entfernen.
