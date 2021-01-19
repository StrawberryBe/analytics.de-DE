---
title: Häufig gestellte Fragen zu Klassifizierungen
description: Häufig gestellte Fragen zur Verwendung von Klassifizierungen
translation-type: ht
source-git-commit: a63b8ae3948ffd9a37058696aa1b1d4c923709ba
workflow-type: ht
source-wordcount: '345'
ht-degree: 100%

---


# Häufig gestellte Fragen zu Klassifizierungen

Häufig gestellte Fragen zur Verwendung von Klassifizierungen

## Wie klassifiziere ich das Dimensionselement „0“?

Klassifizierungsdateien, die mit einem Schlüsselwert oder einem Klassifizierungswert von null hochgeladen wurden (`0`), führen zu einem Fehler. Dies schließt alle Werte ein, die nur Nullen (`00`, `000` usw.) enthalten. Es gibt mehrere Methoden, um dieses Problem zu beheben:

* **Alternative Werte implementieren**: Die Verwendung eines anderen Textwerts als `"0"` ist der beste und einfachste Weg, dieses Problem zu lösen. Ändern Sie zum Beispiel `s.campaign = "0";` in Ihrer Implementierung in `s.campaign = "Zero";`.

* **Verarbeitungsregeln verwenden**: Sie können Dimensionselemente zwischen der Datenerfassung und ihrer Datenspeicherung in einer Report Suite ändern. Erstellen Sie die folgende Verarbeitungsregel:

   *Wenn die [Dimension] gleich `0` ist, überschreiben Sie den Wert der [Dimension] mit dem benutzerdefinierten Wert `Zero`.*

* **Eine VISTA-Regel anfordern**: Ein Engineering Services-Berater richtet gegen Aufpreis eine Server-seitige Regel für Sie ein. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um eine VISTA-Regel anzufordern.

## Kann ich mit Classification Importer Dimensionselemente klassifizieren, die noch nicht vorhanden sind?

Ja, dabei wird *jedoch jedes Dimensionselement als abrechnungsfähiger Server-Aufruf gezählt.*

* Dimensionen, die bereits vorhanden sind, verursachen keine zusätzlichen Kosten.
* Die Verwendung des Classification Rule Builders klassifiziert nicht vorhandene Elemente nicht und verursacht daher keine zusätzlichen Kosten.

## Wie klassifiziere ich Werte, die Sonderzeichen enthalten?

Die Verwendung von Sonderzeichen wie Kommas oder doppelten Anführungszeichen im Reporting wird normalerweise nicht empfohlen. In einigen Fällen ist ihre Verwendung jedoch erforderlich. Wenn Ihre Reporting-Werte solche Zeichen enthalten, die Sie klassifizieren möchten, gehen Sie wie folgt vor:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Browser-Export]**.
3. Konfigurieren Sie die Exporteinstellungen und stellen Sie sicher, dass „Anführungszeichenausgabe“ NICHT aktiviert ist.
4. Klicken Sie auf **[!UICONTROL Datei exportieren]** und öffnen Sie die heruntergeladene Datei in einem Tabellen-Editor.
5. Suchen Sie in Zeile 1 die Zelle C1, die den Wert `v:2.0` enthält. Ändern Sie den Wert in `v:2.1` und wenden Sie die gewünschten Klassifizierungen auf die Arbeitsmappe an.
6. Laden Sie die Datei wie jede andere Classification hoch.

## Was sind Nummerisch-2-Klassifizierungen?

Mit Nummerisch-2-Klassifizierungen können Sie Dimensionselemente als zeitbasierte Metriken klassifizieren. Sie wurden im Juli 2019 aus der Benutzeroberfläche von Adobe Analytics entfernt.
