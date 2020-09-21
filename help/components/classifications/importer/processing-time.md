---
title: Verarbeitungszeit von Classification Importer
description: Verstehen Sie den Zeitrahmen, in dem Adobe Classification-Dateien verarbeitet, und wie Sie die Verarbeitungszeit minimieren.
translation-type: ht
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: ht
source-wordcount: '416'
ht-degree: 100%

---


# Verarbeitungszeit von Classification Importer

Die Verarbeitungszeit für eine Classification-Datei hängt von der Größe der Datei und der Gesamtzahl der von Adobe verarbeiteten Dateien ab. Klassifizierungen dauern in der Regel nicht länger als 72 Stunden. In Unternehmen, die Adobe Analytics einsetzen, kann es jedoch vorkommen, dass Dateien in Zeiten starker Nutzung der Classification länger als 72 Stunden benötigen. Adobe verzeichnet in den Monaten vor der Weihnachtssaison eine starke Nutzung von Classifications.

Wenn Sie sehen möchten, ob eine Classification-Datei fertig ist, gehen Sie wie folgt vor:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Wählen Sie die betreffende Report Suite und den betreffenden Datensatz aus.
3. Wenn die Verarbeitung noch nicht abgeschlossen ist, wird eine der folgenden Meldungen angezeigt:

   * ![Hinweis](assets/icon_notice_notice.gif) Der ausgewählte Bericht enthält einen Classification-Import, der verarbeitet wird.
   * ![Hinweis](assets/icon_notice_notice.gif) Der ausgewählte Bericht enthält Classification-Daten, die noch nicht alle Server erreicht haben.

Wenn Sie die Importzeit für Classifications minimieren möchten, empfiehlt Adobe dringend die Einhaltung der folgenden Richtlinien:

* **Verwenden Sie nach Möglichkeit den Classification Rule Builder**: Der Classification Rule Builder verarbeitet Daten anders als der herkömmliche Klassifizierungs-Importer . Wenn die Classification-Daten bestimmten Mustern folgen, wird die Verwendung dieser Funktion dringend empfohlen.
* **Nur geänderte Zeilen hochladen**: Durch diese Vorgehensweise wird die Zeit für die Verarbeitung von Classification-Dateien erheblich reduziert, da unveränderte Zeilen nicht sortiert werden. Adobe empfiehlt dringend, nur geänderte Zeilen hochzuladen.
* **Vorausplanen**: Beginnen Sie so bald wie möglich mit dem Hochladen von Classification-Daten, insbesondere wenn diese Daten während der Weihnachtssaison verwendet werden.
* **Classification-Dateien nach Möglichkeit kombinieren**: Wenn eine Variable mehrere Classifications hat, laden Sie eine einzige Datei mit allen zutreffenden Classification hoch. Vermeiden Sie das Hochladen mehrerer Klassifizierungen für dieselbe Variable.
* **Hochladen von Dateien über 500 MB vermeiden**: Bei großen Mengen an Classification-Daten empfiehlt Adobe, Dateien in Dateien mit 100 MB bis 500 MB aufzuteilen.
* **Hochladen großer Dateimengen auf FTP vermeiden**: Wenn Sie vorhaben, dieselben Dateien über FTP in viele Report Suites hochzuladen, begrenzen Sie die Anzahl der gleichzeitig hochgeladenen Dateien. Adobe empfiehlt, dass die Anzahl der Dateien multipliziert mit der Anzahl der Report Suites weniger als 1000 beträgt. Wenn das Hochladen von 100 Dateien in 100 Report Suites erforderlich ist, beträgt die Gesamtanzahl der Dateien 10.000. Anstatt alle 100 Dateien gleichzeitig hochzuladen, teilen Sie sie in 10 Gruppen zu je 10 Dateien auf.
* **Kleine Dateien über den Browser-Importer hochladen**: Wenn Sie eine Datei mit einer Größe von weniger als 1 MB (weniger als 50.000 Zeilen) haben, empfiehlt Adobe die Verwendung des Browser-Importers. Browser-Importe sind fast immer schneller als FTP-Importe.
