---
description: Information zur .txt-Vorlage von Datenquelle.
subtopic: Data sources
title: Importdatei-Referenz
topic: Developer and implementation
uuid: cc58f8d8-cb6e-4908-846f-0a41c6da805d
translation-type: ht
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: ht
source-wordcount: '430'
ht-degree: 100%

---


# Importdatei-Referenz

Information zur .txt-Vorlage von Datenquelle.

Verwenden Sie den Data Sources-Assistenten, um eine Importvorlage zu erstellen. Die Data Sources-Importdatei enthält die folgenden Daten:

* Ein Nummernzeichen (#) kennzeichnet die Zeile als Kommentar.
* Sie können bei Bedarf der Datei weitere Kommentare hinzufügen.
* Ein Kommentar, in dem der Titel der Vorlagendatei aufgeführt wird.
* Ein Kommentar, in dem die Namen von externen Metriken und Datendimensionen aufgeführt werden, die im [!UICONTROL Datenquelle-Aktivierungsassistenten angegeben werden].

Mithilfe von Spaltenüberschriften werden die Daten in jeder Spalte der Datenquelle-Datei identifiziert. Es gibt drei Arten von Spaltenüberschriften:

**Datum**: (Erforderlich) Ein Zeitstempel für jede Datenzeile in der Datei, im `m/d/yyyy`-Format.

**Variablen**: Die Namen der Berichterstellungsvariablen, die den Datendimensionen der Datenquelle zugeordnet sind.

**Ereignisse**: Die Namen der Ereignisse, die den Metriken der Datenquellen zugeordnet sind.

Verwenden Sie die Datenquelle-Vorlage, um eine Data Sources-Datei zu erstellen, die Daten enthält, die Sie hochladen möchten. Beachten Sie beim Erstellen einer Data Sources-Datei Folgendes:

* Jede Zeile in der Data Sources-Datei enthält im Grunde einen Datensatz, wobei jeder Datensatz aus mehreren Tabulator-getrennten Feldern besteht. Die Spaltenüberschriften in der Datenquelle-Vorlage definieren die Reihenfolge dieser Felder. Beispiel:

   ```
     #Sample data file for mycorp_report_suite 
     #Imported data for ad impressions applied to Event 6
     Date     Tracking Code      Event 6 
     1/1/2009     NYT8453A      8754
     1/1/2009     WSJ4453B      9492
     1/1/2009     BHG44563      10553
     1/2/2009     NYT8453A      6452
     1/2/2009     WSJ4453B      7237
     1/2/2009     BHG44563      9031
   ```

* Wenn Sie mehrere Datendateien hochladen, lädt Data Sources sie in alphabetischer Reihenfolge. Die Dateien, die chronologisch verarbeitet werden müssen, müssen derart benannt sein, dass die alphabetische Reihenfolge auch der chronologischen Reihenfolge entspricht. Beispiel:

   ```
   log_2009-01-01_13:00.txt
   log_2009-01-01_13:15.txt
   log_2009-01-01_13:30.txt
   ```

* Um die Verarbeitung der Data Sources-Datei zu beschleunigen, empfiehlt Adobe die Erfassung von Ereignisdaten (Metriken) in einer einzelnen Zeile pro Datum.

   Wenn Ihre Data Sources-Datei beispielsweise Anzeigenimpressionsdaten dem Ereignis 6 zuordnet, erstellen Sie eine einzelne Datenzeile, die die Gesamtanzahl an Anzeigenimpressionen für jeden Tag umfasst, anstatt einen eigenen Datenzeileneintrag für jede Anzeigenimpression zu erstellen, die an einem bestimmten Tag aufgetreten ist.
* Wenn Sie Daten mit einem Datum vor dem Erstellungsdatum der Report Suite hochladen müssen, wenden Sie sich an Ihren Kundenbetreuer, um das älteste Datum zu ändern, für das Sie Berichte ausführen können.

**.FIN-Datei**

Wenn Sie die Datenquellendatei gefüllt haben, können Sie sie über FTP in Analytics laden. Es ist jedoch eine weitere Datei erforderlich, damit Ihre Daten verarbeitet werden können. Sie müssen eine leere Textdatei mit demselben Namen wie Ihre Datendatei erstellen und die Erweiterung [!DNL .fin] verwenden.

Wenn Sie zum Beispiel eine (tabulatorgetrennte) Datendatei mit dem Namen [!DNL myproductdata.txt] hochladen, müssen Sie außerdem eine leere Textdatei mit dem Namen [!DNL myproductdata.fin] hochladen. Ohne diese [!DNL .fin]-Datei können die Daten nicht verarbeitet werden.
