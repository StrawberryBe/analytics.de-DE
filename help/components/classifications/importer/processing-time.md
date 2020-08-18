---
title: Verarbeitungszeit des Classification Importers
description: Verstehen Sie, wie Classification-Dateien in der Adobe des Zeitrahmens verarbeitet werden und wie Sie die Verarbeitungszeit minimieren.
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Verarbeitungszeit des Classification Importers

Die Verarbeitungszeit für eine Classification-Datei hängt von der Dateigröße und der Gesamtanzahl der Dateiprozesse ab, die bei der Adobe durchgeführt werden. Klassifizierungen dauern in der Regel nicht länger als 72 Stunden. Zeiträume, in denen Adobe Analytics verwendet wird, mit hoher Classification können jedoch dazu führen, dass Dateien länger als 72 Stunden dauern. Adobe sieht eine starke Klassifizierung in Monaten vor der Urlaubszeit.

Wenn Sie sehen möchten, ob eine Classification-Datei fertig ist, führen Sie die folgenden Schritte aus:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Wählen Sie die betreffende Report Suite und den betreffenden Datensatz aus.
3. Wenn die Verarbeitung noch nicht abgeschlossen ist, wird eine der folgenden Meldungen angezeigt:

   * ![Beachten Sie](assets/icon_notice_notice.gif) , dass der ausgewählte Bericht einen Classification-Import enthält, der verarbeitet wird.
   * ![Beachten Sie](assets/icon_notice_notice.gif) , dass der ausgewählte Bericht über Classification-Daten verfügt, die noch nicht an alle Server übertragen wurden.

Wenn Sie die Importzeit für Klassifizierungen minimieren möchten, empfiehlt Adobe dringend die Einhaltung der folgenden Richtlinien:

* **Verwenden Sie nach Möglichkeit** den Classification Rule Builder: Der Classification Rule Builder verarbeitet Daten anders als der herkömmliche Classification Importer. Wenn Classification-Daten bestimmten Mustern folgen, wird die Verwendung dieser Funktion dringend empfohlen.
* **Nur geänderte Zeilen** hochladen: Durch diese Vorgehensweise wird die Verarbeitungszeit für Classification-Dateien erheblich reduziert, da sie nicht durch unveränderte Zeilen sortiert wird. Adobe empfiehlt, nur geänderte Zeilen hochzuladen.
* **Vorausplanung**: Beginn laden so bald wie möglich Classification-Daten hoch, insbesondere wenn diese Daten während der Urlaubszeit verwendet werden.
* **Klassifizierungsdateien nach Möglichkeit** kombinieren: Wenn eine einzelne Variable mehrere Classifications enthält, laden Sie eine einzelne Datei mit allen entsprechenden Classifications hoch. Vermeiden Sie das Hochladen mehrerer Classifications für dieselbe Variable.
* **Vermeiden Sie das Hochladen von Dateien über 500 MB**: Bei großen Mengen an Classification-Daten empfiehlt Adobe, Dateien in 100 MB-500 MB-Dateien aufzuteilen.
* **Vermeiden Sie das Hochladen großer Dateimengen auf FTP**: Wenn Sie dieselben Dateien über FTP in viele Report Suites hochladen möchten, beschränken Sie die Anzahl der gleichzeitig hochgeladenen Dateien. Adobe empfiehlt, dass die Anzahl der Dateien, die mit der Anzahl der entsprechenden Report Suites multipliziert werden, unter 1000 liegt. Wenn das Hochladen von 100 Dateien in 100 Report Suites erforderlich ist, beträgt die Gesamtanzahl der Dateien 10.000. Statt alle 100 Dateien gleichzeitig hochzuladen, sollten Sie sie in 10 Gruppen von jeweils 10 Dateien unterteilen.
* **Kleine Dateien über den Browser-Importer** hochladen: Wenn Sie eine Datei mit einer Größe von weniger als 1 MB (weniger als 50.000 Zeilen) haben, empfiehlt Adobe die Verwendung des Browser-Importeurs. Browser-Importe sind fast immer schneller als FTP-Importe.
