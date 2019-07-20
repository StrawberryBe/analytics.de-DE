---
description: Neben den in Excel über Format > Zellen formatieren (Strg+1) verfügbaren Standard-Zellformatierungsoptionen können Sie mit ReportBuilder bestimmte Formatierungen auf Zellbereiche anwenden. Die möglichen Formatierungen hängen von der gewählten Metrik ab.
seo-description: Neben den in Excel über Format > Zellen formatieren (Strg+1) verfügbaren Standard-Zellformatierungsoptionen können Sie mit ReportBuilder bestimmte Formatierungen auf Zellbereiche anwenden. Die möglichen Formatierungen hängen von der gewählten Metrik ab.
seo-title: Datum formatieren
solution: Analytics
title: Datum formatieren
topic: ReportBuilder
uuid: 5211 db 30-07 b 3-4413-97 c 3-e 40 e 6 ff 223 cd
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Datum formatieren

Neben den in Excel über Format &gt; Zellen formatieren (Strg+1) verfügbaren Standard-Zellformatierungsoptionen können Sie mit ReportBuilder bestimmte Formatierungen auf Zellbereiche anwenden. Die möglichen Formatierungen hängen von der gewählten Metrik ab.

After you [add dimensions](../../../analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md#task_E3F520C020F64C5A96DC5C96FEF71FC4) to the Row Labels grid, click **[!UICONTROL Format]**.

Klicken Sie im Menü **[!UICONTROL Format]** auf **Benutzerdefiniertes Format], um ähnlich wie beim Voranstellen oder Anhängen benutzerdefinierte Formate anzuwenden.[!UICONTROL ** Beispielsweise können Sie Text eingeben, der immer nach dem Datum angezeigt werden soll (z. B. „A.D.“, „B.C.E.“, „A.H.“ usw.). Sie können Text vor dem Datum einfügen, z. B. [!UICONTROL Startdatum] und [!UICONTROL Start- und Enddatum]. Darüber hinaus können Sie einen eigenen Datumsausdruck mit Hilfe von Abkürzungen für Tag, Monat und Jahr erstellen und benutzerdefinierte Trennzeichen zwischen den Datumsbestandteilen verwenden. Alle Datumsformate müssen aus drei Abkürzungen bestehen, die nur in Klammern eingeschlossen werden dürfen.

In der folgenden Tabelle wird beschrieben, wie Datumsabkürzungen im Feld [!UICONTROL Benutzerdefiniertes Format] verwendet werden können:

| Abkürzung | Beschreibung | Beispiel   Verwendung von Mittwoch, 14. März 2012 |
|--- |--- |--- |
| MM/dd/yyy | Volles numerisches Datum | 03/14/2012 |
| M | Monatsnummer | 3 |
| MM | Monatsnummer mit vorangestellter 0 für Monate &lt; 10 | 03 |
| MMM | Kurzname des Monats | Mär |
| MMMM | Langname des Monats | März |
| D | Langname des Datums | Mittwoch, 14. März 2012 |
| d | Tagesnummer | 14 |
| dd | Tagesnummer mit vorangestellter 0 für Tage &lt; 10 | 01 - 09 |
| ddd | Kurzname des Tages | Mit |
| dddd | Langname des Tags | Mittwoch |
| yy | Jahr (zweistellig) | 10 |
| yyyy | Jahr (vierstellig) | 2012 |