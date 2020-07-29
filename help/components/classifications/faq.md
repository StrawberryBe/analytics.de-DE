---
title: Häufig gestellte Fragen zu Klassifizierungen
description: Häufig gestellte Fragen zur Verwendung von Klassifizierungen
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Häufig gestellte Fragen zu Klassifizierungen

Häufig gestellte Fragen zur Verwendung von Klassifizierungen

## Wie klassifiziere ich das Dimensionselement &quot;0&quot;?

Classification-Dateien, die mit einem Schlüsselwert oder einem Classification-Wert von null hochgeladen wurden (`0`), führen zu einem Fehler. Es enthält alle Werte, die nur Nullen (`00`, `000`usw.) enthalten. Es gibt mehrere Methoden, um dieses Problem zu beheben:

* **Implementieren Sie alternative Werte**: Die Verwendung eines anderen Textwerts als `"0"` der beste und einfachste Weg, dieses Problem zu lösen. Ändern Sie zum Beispiel `s.campaign = "0";` in Ihre Implementierung `s.campaign = "Zero";`.

* **Verarbeitungsregeln** verwenden: Sie können Dimensionselemente zwischen der Datenerfassung und ihrer Datenspeicherung in einer Report Suite ändern. Erstellen Sie die folgende Verarbeitungsregel:

   *Wenn die[Dimension]gleich ist`0`, überschreiben Sie den Wert der[Dimension]mit dem benutzerdefinierten Wert`Zero`.*

* **Eine VISTA-Regel** anfordern: Ein Engineering Services-Berater richtet für Sie eine serverseitige Regel gegen Aufpreis ein. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um eine VISTA-Regel anzufordern.

## Kann ich mit dem Uploader Dimensionselemente klassifizieren, die noch nicht vorhanden sind?

Ja, dabei wird *jedoch jedes Dimensionselement als abrechnungsfähiger Serveraufruf gezählt.*

* Dimensionen, die bereits vorhanden sind, verursachen keine zusätzlichen Kosten.
* Die Verwendung des Classification Rule Builders klassifiziert nicht vorhandene Elemente nicht und verursacht daher keine zusätzlichen Kosten.
