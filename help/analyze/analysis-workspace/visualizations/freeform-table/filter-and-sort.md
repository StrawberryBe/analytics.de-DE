---
description: Dokumentation, in der beschrieben wird, wie Tabellen in Analysis Workspace gefiltert und sortiert werden.
title: Filtern und Sortieren von Tabellen
feature: Freeform Tables
role: User, Admin
exl-id: 15fea9e2-f8d8-4489-9a44-e74a351b8f36
source-git-commit: 7f5fca4f7c3641d47e5d1d929a196d5e380c1e6b
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 77%

---

# Filtern und Sortieren von Tabellen

Freiformtabellen in Analysis Workspace bilden die Grundlage für die interaktive Datenanalyse. Daher können sie Tausende von Informationszeilen enthalten. Das Filtern und Sortieren der Daten kann ein wichtiger Teil der effizienten Aufdeckung der wichtigsten Informationen sein.

## Filtern von Tabellen

Mit Filtern in Analysis Workspace können Sie die wichtigsten Informationen aufdecken.

>[!NOTE]
>
> Nur dynamische Dimensionselemente können wie in diesem Abschnitt beschrieben gefiltert werden. Statische Dimensionselemente können nicht gefiltert werden. Weitere Informationen finden Sie unter [Dynamische im Vergleich zu statischen Dimensionselementen in Freiformtabellen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).

### Schnelles Ausschließen bestimmter Zeilen aus einer Tabelle

Sie können bestimmte Zeilen schnell aus der Tabelle ausschließen, ohne das Dialogfeld Filter öffnen zu müssen.

>[!NOTE]
>
>Wenn Sie Zeilen ausschließen, wie in diesem Abschnitt beschrieben, wird ein [!UICONTROL **Ist nicht gleich**] -Regel wird automatisch im [**[!UICONTROL Erweiterte Filter]**](#apply-a-simple-or-advanced-filter) angezeigt.

So schließen Sie bestimmte Zeilen schnell aus einer Freiformtabelle aus:

1. Bewegen Sie den Mauszeiger über die Zeile, die Sie ausschließen möchten, und wählen Sie dann das Symbol x aus.

   Halten Sie die Umschalttaste gedrückt, um Bereichszeilen auszuwählen, oder halten Sie die Befehlstaste (Mac) oder die Strg-Taste (Windows) gedrückt, um mehrere Zeilen auszuwählen.

### Anwenden eines einfachen oder erweiterten Filters auf eine Tabelle

So filtern Sie Daten in Freiformtabellen:

1. Bewegen Sie den Mauszeiger über die Spalte, die die zu filternden Daten enthält. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. Wählen Sie das **Filtersymbol** aus, wenn es angezeigt wird.

   ![Filtersymbol in einer Tabelle](assets/table-filter-icon.png)

   Die folgenden Optionen sind verfügbar:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Suchbegriff oder -satz**] | Geben Sie ein Wort oder eine Wortgruppe an, nach dem/der Sie filtern möchten. Es werden nur Zeilen angezeigt, die das Wort oder die exakte Phrase enthalten. |
   | [!UICONTROL **Nicht spezifizierte einschließen (keine)**] | Aktivieren Sie diese Option, um Daten in der Tabelle anzuzeigen, die nicht zu einer Dimension der Tabelle gehören. <!--what is this?--> |

1. (Optional) Um nach verschiedenen Kriterien oder nach mehreren Kriterien zu filtern, wählen Sie [!UICONTROL **Erweiterte Filter**].

   Die folgenden erweiterten Filteroptionen sind verfügbar:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Nicht spezifizierte einschließen (keine)**] | Aktivieren Sie diese Option, um Daten in der Tabelle anzuzeigen, die nicht zu einer Dimension der Tabelle gehören. <!--what is this?--> |
   | [!UICONTROL **Übereinstimmung**] | <p>Wählen Sie [!UICONTROL **Wenn alle Kriterien erfüllt sind**] aus, um nur Daten anzuzeigen, die alle angegebenen Kriterien erfüllen. Diese Option führt normalerweise zu verfeinerten Daten.</p> <p>Wählen Sie [!UICONTROL **Wenn ein Kriterium erfüllt ist**] aus, um Daten anzuzeigen, die eines der angegebenen Filterkriterien erfüllen. Diese Option führt normalerweise zu weniger verfeinerten Daten.</p> |
   | [!UICONTROL **Kriterien**] | <p>Treffen Sie eine Auswahl aus den folgenden Filteroptionen:</p><p>(Wählen Sie [!UICONTROL **Zeile hinzufügen**] aus, um mehrere Filterkriterien hinzuzufügen. Die Option, die Sie im Abschnitt [!UICONTROL **Übereinstimmung**] auswählen, bestimmt, ob alle oder eines der hinzugefügten Kriterien erfüllt sein müssen.)</p><ul><li><p>[!UICONTROL **Enthält die Phrase**]: Nur Daten, die die von Ihnen angegebene Phrase enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen in der Reihenfolge vorliegen, die im Feld [!UICONTROL **Nach Wort oder Phrase suchen**] angegeben ist.<p>Dies ist die Standardeinstellung bei einer einfachen Suche.</p></p></li><li><p>[!UICONTROL **Enthält einen der Begriffe**]: Nur Daten, die ein oder mehrere Wörter aus der angegebenen Phrase enthalten, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Enthält alle Begriffe**]: Nur Daten, die alle Wörter aus der angegebenen Phrase enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen nicht in der gleichen Reihenfolge wie im Feld [!UICONTROL **Nach Wort oder Phrase suchen**] vorliegen.</p></li><li><p>[!UICONTROL **Enthält keinen der Begriffe**]: Nur Daten, die keines der Wörter aus der angegebenen Phrase enthalten, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Enthält nicht die Phrase**]: Nur Daten, die nicht genau die angegebene Phrase enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen in der Reihenfolge vorliegen, die im Feld [!UICONTROL **Nach Wort oder Phrase suchen**] angegeben ist.</p></li><li><p>[!UICONTROL **Gleich**]: Nur Daten, die genau mit der angegebenen Phrase übereinstimmen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Ist nicht gleich**]: Nur Daten, die nicht genau mit der angegebenen Phrase übereinstimmen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Beginnt mit**]: Nur Daten, die mit dem angegebenen Wort oder der angegebenen Phrase beginnen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Endet mit**]: Nur Daten, die mit dem angegebenen Wort oder der angegebenen Phrase enden, werden in die gefilterten Ergebnisse aufgenommen. </p></li></ul> |
   | [!UICONTROL **Elemente immer ausschließen**] | Geben Sie den Namen aller Elemente an, die Sie aus den gefilterten Daten ausschließen möchten. |

1. Wählen Sie [!UICONTROL **Anwenden**] aus, um die Daten zu filtern.

   Das **Filtersymbol** ![Blaues Filtersymbol zur Filterung der Tabelle](assets/table-filter-blue-icon.png) wird angezeigt, wenn ein Filter auf die Tabelle angewendet wird.

## Sortieren von Tabellen

Sie können die Daten einer Freiformtabelle nach einer beliebigen Spalte in Analysis Workspace sortieren, die eine Metrik ist.

Ein Pfeil-nach-unten-Symbol ![Pfeil nach unten zur Sortierung einer Tabellenspalte](assets/table-sort-arrow-icon.png) ist in der Kopfzeile der Spalte sichtbar, nach der die Daten derzeit sortiert werden.

So sortieren Sie die Daten in einer Freiformtabelle nach einer bestimmten Spalte:

1. Bewegen Sie den Mauszeiger über den Spaltentitel, nach dem die Daten sortiert werden sollen.

1. Wählen Sie das Pfeil-nach-unten-Symbol aus, wenn es angezeigt wird.

   ![Pfeil nach unten zur Sortierung einer Tabellenspalte](assets/table-sort.png)

   Die Tabellendaten werden nach der von Ihnen ausgewählten Spalte sortiert.
