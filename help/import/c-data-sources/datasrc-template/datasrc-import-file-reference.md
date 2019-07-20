---
description: Information zur .txt-Vorlage von Datenquelle.
seo-description: Information zur .txt-Vorlage von Datenquelle.
seo-title: Dateireferenz importieren
solution: Analytics
subtopic: Datenquellen
title: Dateireferenz importieren
topic: Entwickler und Implementierung
uuid: cc 58 f 8 d 8-cb 6 e -4908-846 f -0 a 41 c 6 da 805 d
translation-type: tm+mt
source-git-commit: cce2c1c54f21244f856385aeaad811d89f2fda7f

---


# Dateireferenz importieren

Information zur .txt-Vorlage von Datenquelle.

Verwenden Sie den Data Sources-Assistenten, um eine Importvorlage zu erstellen. Die Data Sources-Importdatei enthält die folgenden Daten:

* Ein Nummernzeichen (#) kennzeichnet die Zeile als Kommentar.
* Sie können bei Bedarf der Datei weitere Kommentare hinzufügen.
* Ein Kommentar, in dem der Titel der Vorlagendatei aufgeführt wird.
* Ein Kommentar, in dem die Namen von externen Metriken und Datendimensionen aufgeführt werden, die im [!UICONTROL Datenquelle-Aktivierungsassistenten angegeben werden].

Mithilfe von Spaltenüberschriften werden die Daten in jeder  Spalte der Datenquelle-Datei identifiziert. Es gibt drei Arten von Spaltenüberschriften:

**Datum**: (Erforderlich) Ein Zeitstempel für jede Datenzeile in der Datei.

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

Wenn Sie die Datenquelle-Datei ausgefüllt haben, können Sie sie per FTP in Analytics einfügen. Es ist jedoch eine weitere Datei erforderlich, damit Ihre Daten verarbeitet werden können. You will need to upload an empty text file with the same name of your data file, but with a [!DNL .fin] extension.

For example, if you upload a (tab-delimited) data file called [!DNL myproductdata.txt], you would also need to upload an empty text file called [!DNL myproductdata.fin]. Without the [!DNL .fin] file, data would never be processed.
