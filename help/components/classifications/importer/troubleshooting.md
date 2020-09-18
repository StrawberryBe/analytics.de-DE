---
title: Fehlerbehebung beim Classification Importer
description: Häufige Upload-Probleme bei der Verwendung des Classification Importers.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 12%

---


# Fehlerbehebung beim Classification Importer

Die häufigsten Probleme beim Hochladen von Classification-Daten in die Adobe.

## Falsche(s) Dateiformat oder -erweiterung

Classifications erfordern einen bestimmten Dateityp und ein bestimmtes Format, um erfolgreich hochgeladen werden zu können. Wenn sie nicht im richtigen Format gespeichert wurden, verursacht dies einen Fehler und es werden keine Zeilen verarbeitet. Häufig wird der Fehler *&quot;Erste Spalte muss der Schlüssel sein&quot;* zurückgegeben, kann aber auch eine beliebige Anzahl von Fehlern sein. Überprüfen Sie Folgendes:

* **Hochladen einer Tabelle (.xlsx) anstelle einer .tab- oder .txt-Datei**: Sie können die Fehlermeldung *&quot;Die erste Spalte muss der Schlüssel&quot;* erhalten, wenn Sie Classification-Dateien in einem falschen Format hochladen. Der Classification Importer kann keine .xls- oder .xlsx-Dateien verarbeiten. Legen Sie im Excel-Dialogfeld &quot;Speichern unter&quot;den richtigen Dateityp fest:
   * Unter Windows verwenden Sie das Dateiformat `Text (Tab delimited) (*.txt)`
   * Verwenden Sie unter Mac das Dateiformat `Windows Formatted Text`.
* **Ändern der Dateinamenerweiterung nach dem Speichern als Arbeitsmappe**: Beim Versuch, eine Dateierweiterung direkt umzubenennen, wird eine ungültige Arbeitsmappe generiert. Verwenden Sie nur die Excel-Funktion Speichern unter oder bearbeiten Sie Classifications in einem Texteditor wie Notepad++.
* **Verwenden von Großbuchstabenerweiterungen**: Erweiterungen in Großbuchstaben (z. B. `fileupload.TXT`) funktionieren nicht. Rename the file to a lowercase extension (`fileupload.txt`).
* **Nicht übereinstimmende Zeichenkodierung**: Stellen Sie sicher, dass die Kodierung des gespeicherten Classification-Uploads mit der ursprünglichen Kodierung übereinstimmt, wenn die Vorlage heruntergeladen wurde. Wenn Sie eine UTF-16-Datei hochladen, während sie ursprünglich in UTF-8 kodiert war, führen Uploads zu unerwarteten Ergebnissen. Adobe empfiehlt das Hochladen von Dateien mit UTF-8 ohne Byte-Bestellzeichen.

## Ungültige Dateiinhalte

Wenn die hochgeladene Datei richtig formatiert ist, versucht der Uploader, möglichst viele gültige Reihen zu importieren. Einige häufig auftretende Probleme mit Classification-Daten:

* **Bereits klassifizierte** Zeilen: Beim Versuch, Zeilen hochzuladen, die bereits mit demselben Wert klassifiziert sind, gibt der Importeur Zeilen zurück, die keine Auswirkung hatten. Dies ist so vorgesehen, da Classifications einen Schlüsselwert nicht erneut mit derselben Classification klassifizieren. Es handelt sich um eine Benachrichtigung anstelle eines Fehlers. Sie müssen sich also keine Gedanken darum machen, Zeilen innerhalb einer Exportdatei zu ändern. Adobe empfiehlt, nur geänderte Zeilen hochzuladen.
* **Die Kopfzeile stimmt nicht mit der hochgeladenen** Variablen überein: Wenn Sie eine Classification-Vorlage für die Dimension &quot;Trackingcode&quot;herunterladen und versuchen, sie in eine eVar-Classification hochzuladen, schlägt sie fehl. Verwenden Sie nur Exportdateien für die spezifischen Variablen, aus denen sie exportiert wurden.
* **Ein Schlüssel oder Classification-Wert enthält den Wert 0**: Klassifizierungen können den Wert 0 nicht von einer leeren Zelle unterscheiden, daher kann dieser Wert nicht klassifiziert werden. Siehe Häufig gestellte Fragen zu [Klassifizierungen](../faq.md).
* **Die Classification-Datei enthält Kommas oder Sonderzeichen**: Siehe Häufig gestellte Fragen zu [Klassifizierungen](../faq.md).
* **Zusätzliche Registerkarten in der hochgeladenen Datei**: Manchmal kann beim Bearbeiten von Classification-Dateien eine zusätzliche Registerkarte versehentlich eingeschlossen werden. Jede Zeile erfordert eine identische Anzahl von Tabs, damit sie richtig verarbeitet werden kann. Um zu überprüfen, ob die Datei über zusätzliche Registerkarten verfügt, markieren Sie den gesamten Text in einem Texteditor und stellen Sie sicher, dass am Ende keine Zeilen mehr Platz haben.
* **Duplikat-Schlüsselwerte sind in der Datei** vorhanden: Jeder Schlüsselwert kann nur eine Classification pro Spalte haben. Wenn Sie versuchen, denselben Wert mehrmals zu klassifizieren, gibt der Importeur einen Fehler aus.
* **Unterklassifizierungen sind vorhanden und falsch konfiguriert**: Wenn Unterklassifizierungen vorhanden sind, überprüfen Sie Folgendes:
   * Alle Subclassification-Werte müssen über einen übergeordneten Classification-Wert verfügen.
   * Es dürfen nicht mehrere Subclassifications auf denselben übergeordneten Classification-Wert verweisen.
* **Spaltenabweichung**: Sie können die Fehlermeldung *&quot;The key on line has too many columns&quot;* erhalten, wenn eine Zeile eine ungültige Spaltenanzahl enthält. Sie haben z. B. 3 Spalten in Ihrem Classification-Upload und die Variable hat nur eine Classification. Überprüfen Sie Ihre Hochladedatei, um sicherzustellen, dass die Anzahl der Spalten nicht größer ist als die Anzahl der für diese Variable konfigurierten Klassifizierungen.

## Fehlerbehebung bei FTP-Importen

Die folgenden Ursachen treten häufig bei FTP-Classifications auf, die keine hochgeladenen Dateien verarbeiten:

* **Fehlende .fin-Datei**: Erstellen Sie ein leeres Dokument auf Ihrem Desktop und benennen Sie die Dateinamenerweiterung von .txt in .fin um. Der Name dieser .fin-Datei muss mit dem Namen der betreffenden Classification-Datei übereinstimmen. Wenn Ihr FTP-Dateiname beispielsweise `fileupload.tab`lautet, geben Sie Ihrer .fin-Datei einen Namen `fileupload.fin`. Nach dem Hochladen der .fin-Datei werden beide Dateien ausgeblendet.
* **.fin-Datei vor der Classification-Datei** hochladen: Manchmal wird eine .fin-Datei erstellt, bevor der Upload der Classifications-Datei auf die FTP-Site abgeschlossen ist. Die Verarbeitung kann fehlschlagen, wenn Dateien nicht in der richtigen Reihenfolge hochgeladen werden. Entfernen Sie beide Dateien, fügen Sie zuerst die Classification-Datei hinzu und dann die .fin-Datei, nachdem die Classification-Datei vollständig hochgeladen wurde.
* **Die Dateigröße ist zu groß**: Adobe empfiehlt, die Größe der Classification-Dateien so gering wie möglich zu halten, um eine zügige Verarbeitung zu gewährleisten.
* **Vorhandene Dateien werden bereits verarbeitet**: Wenn mehrere Dateien für dieselbe Variable und dieselbe Report Suite hochgeladen werden, wird die Verarbeitung der alten Datei zugunsten der neuen Datei eingestellt. Wenn Sie Classifications mit mehreren Dateien hochladen, warten Sie auf die Bestätigung, dass die Verarbeitung der vorhandenen Dateien abgeschlossen ist, bevor Sie neue hochladen.
* **Hochgeladene Dateien, die nicht im Stammverzeichnis** gespeichert sind: Auf die FTP-Site der Adobe hochgeladene Dateien müssen im Stammverzeichnis abgelegt werden. Wenn Classification-Importdateien in Unterordnern abgelegt werden, werden sie nicht aufgenommen oder verarbeitet.

Wenn beim Hochladen einer Classification-Datei weiterhin Probleme auftreten, wenden Sie sich an den Kundendienst der Adobe.
