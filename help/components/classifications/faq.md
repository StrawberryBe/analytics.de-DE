---
title: Häufig gestellte Fragen zu Klassifizierungen
description: Häufig gestellte Fragen zur Verwendung von Klassifizierungen
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '344'
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

## Kann ich mit dem Classification Importer Dimensionselemente klassifizieren, die noch nicht vorhanden sind?

Ja, dabei wird *jedoch jedes Dimensionselement als abrechnungsfähiger Serveraufruf gezählt.*

* Dimensionen, die bereits vorhanden sind, verursachen keine zusätzlichen Kosten.
* Die Verwendung des Classification Rule Builders klassifiziert nicht vorhandene Elemente nicht und verursacht daher keine zusätzlichen Kosten.

## Wie klassifiziere ich Werte, die Sonderzeichen enthalten?

Die Verwendung von Sonderzeichen wie Kommas oder Dubletten-Anführungszeichen in Berichte wird in der Regel nicht empfohlen. In einigen Fällen ist ihre Verwendung jedoch erforderlich. Wenn Ihre Berichte solche Zeichen enthalten, die Sie klassifizieren möchten, gehen Sie wie folgt vor:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Click the **[!UICONTROL Browser export]** tab.
3. Konfigurieren Sie die Exporteinstellungen und stellen Sie sicher, dass &quot;Anführungszeichenausgabe&quot;NICHT ausgewählt ist.
4. Klicken Sie auf Datei **[!UICONTROL exportieren]** und öffnen Sie die heruntergeladene Datei in einem Tabelleneditor.
5. Suchen Sie in Zeile 1 die Zelle C1, die den Wert enthält `v:2.0`. Ändern Sie den Wert in `v:2.1` und wenden Sie die gewünschten Klassifizierungen auf die Arbeitsmappe an.
6. Laden Sie die Datei wie jede andere Klassifizierung hoch.

## Was sind Nummerisch-2-Klassifizierungen?

Mit Nummerisch-2-Klassifizierungen können Sie Dimensionselemente als zeitbasierte Metriken klassifizieren. Sie wurden im Juli 2019 von der Benutzeroberfläche von Analytics eingestellt.
