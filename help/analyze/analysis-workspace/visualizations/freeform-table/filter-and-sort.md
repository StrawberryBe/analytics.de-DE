---
description: Video über Paginierung, Filterung und Sortierung
title: Paginierung, Filtern und Sortieren von Tabellen
feature: Freeform Tables
role: User, Admin
exl-id: 15fea9e2-f8d8-4489-9a44-e74a351b8f36
source-git-commit: 08dd9724efa105d0d9efd25223f72b2ae8e9a487
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 3%

---

# Tabellen filtern und sortieren

Freiformtabellen in Analysis Workspace bilden die Grundlage für die interaktive Datenanalyse. Daher können sie Tausende von Informationszeilen enthalten. Das Filtern und Sortieren der Daten kann ein wichtiger Teil der effizienten Aufdeckung der wichtigsten Informationen sein.

## Tabellen filtern

Mit Filtern in Analysis Workspace können Sie die wichtigsten Informationen aufdecken.

So filtern Sie Daten in Freiformtabellen:

1. Bewegen Sie in einer Freiformtabelle den Mauszeiger über die Spalte, die die Daten enthält, die Sie filtern möchten. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. Wählen Sie die **Filter** angezeigt.

   ![Filtersymbol in einer Tabelle](assets/table-filter-icon.png)

1. Im [!UICONTROL **Suchbegriff oder -satz**] ein Wort oder eine Wortgruppe angeben, nach dem/der Sie filtern möchten. Es werden nur Zeilen angezeigt, die das Wort oder den exakten Satz enthalten, die angegeben sind.

1. (Optional) Um nach verschiedenen Kriterien oder nach mehreren Kriterien zu filtern, wählen Sie [!UICONTROL **Erweitert anzeigen**].

   Die folgenden Optionen sind verfügbar

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Nicht angegeben einschließen (keine)**] | Aktivieren Sie diese Option, um Daten in der Tabelle anzuzeigen, die nicht in eine der Dimensionen der Tabelle fallen. <!--what is this?--> |
   | [!UICONTROL **Übereinstimmung**] | <p>Auswählen [!UICONTROL **Wenn alle Kriterien erfüllt sind**] um nur Daten anzuzeigen, die alle angegebenen Kriterien erfüllen. Diese Option führt normalerweise zu verfeinerten Daten.</p> <p>Auswählen [!UICONTROL **Wenn ein Kriterium erfüllt ist**] um Daten anzuzeigen, die eines der von Ihnen angegebenen Filterkriterien erfüllen. Diese Option führt normalerweise zu weniger detaillierten Daten.</p> |
   | [!UICONTROL **Kriterien**] | <p>Wählen Sie aus den folgenden Filteroptionen aus:</p><p>(Auswahl [!UICONTROL **Zeile hinzufügen**] , um mehrere Filterkriterien hinzuzufügen. Die Option, die Sie im [!UICONTROL **Übereinstimmung**] bestimmt, ob alle oder eines der hinzugefügten Kriterien erfüllt sein müssen.)</p><ul><li><p>[!UICONTROL **Enthält die Wortgruppe**]: Nur Daten, die den von Ihnen angegebenen Satz enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen in der im Feld [!UICONTROL **Suchbegriff- oder Satzfeld**].<p>Dies ist die Standardeinstellung bei einer einfachen Suche.</p></p></li><li><p>[!UICONTROL **Enthält beliebige Begriffe**]: Nur Daten, die ein oder mehrere Wörter aus der von Ihnen angegebenen Wortgruppe enthalten, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Enthält alle Begriffe**]: Nur Daten, die alle Wörter aus dem von Ihnen angegebenen Satz enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen nicht in der im Feld [!UICONTROL **Suchbegriff- oder Satzfeld**].</p></li><li><p>[!UICONTROL **Enthält keinen Begriff**]: Nur Daten, die keines der Wörter aus der von Ihnen angegebenen Wortgruppe enthalten, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Enthält keine Wortgruppe**]: Nur Daten, die nicht den von Ihnen angegebenen genauen Wortlaut enthalten, werden in die gefilterten Ergebnisse aufgenommen. Die Wörter müssen in der im Feld [!UICONTROL **Suchbegriff- oder Satzfeld**].</p></li><li><p>[!UICONTROL **Gleich**]: Nur Daten, die genau mit der von Ihnen angegebenen Wortgruppe übereinstimmen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Ist nicht gleich**]: Nur Daten, die nicht genau mit der von Ihnen angegebenen Wortgruppe übereinstimmen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Beginnt mit**]: Nur Daten, die mit dem von Ihnen angegebenen Wort oder exakten Satz beginnen, werden in die gefilterten Ergebnisse aufgenommen. </p></li><li><p>[!UICONTROL **Endet in**]: Nur Daten, die mit dem von Ihnen angegebenen Wort oder exakten Satz enden, werden in die gefilterten Ergebnisse aufgenommen. </p></li></ul> |
   | [!UICONTROL **Elemente immer ausschließen**] | Geben Sie den Namen der Elemente an, die Sie aus den gefilterten Daten ausschließen möchten. |

1. Auswählen [!UICONTROL **Anwenden**] , um die Daten zu filtern.

   Die **Filter** icon ![Gefilterte Tabelle mit blauem Filtersymbol](assets/table-filter-blue-icon.png) blauer wird angezeigt, wenn ein Filter auf die Tabelle angewendet wird.

## Tabellen sortieren

Sie können die Daten einer Freiformtabelle nach einer der in Analysis Workspace verfügbaren Spalten sortieren.

Symbol für einen Abwärtspfeil ![Symbol mit Abwärtspfeil Sortierte Tabellenspalte](assets/table-sort-arrow-icon.png) ist in der Kopfzeile der Spalte sichtbar, nach der die Daten derzeit sortiert werden.

So sortieren Sie die Daten in einer Freiformtabelle nach einer bestimmten Spalte:

1. Bewegen Sie den Mauszeiger über den Spaltentitel, nach dem die Daten sortiert werden sollen.

1. Wählen Sie das Symbol mit dem Abwärtspfeil aus, wenn es angezeigt wird.

   ![Symbol mit Abwärtspfeil Sortierte Tabellenspalte](assets/table-sort.png)

   Die Tabellendaten werden nach der von Ihnen ausgewählten Spalte sortiert.
