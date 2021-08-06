---
title: Export von Classification-Daten über FTP
description: Der FTP-Export bietet mehr Flexibilität beim Herunterladen von Datensätzen, einschließlich des Herunterladens von Daten aus mehreren Report Suites und des Herunterladens von Datensatzdateien mit mehr als 50.000 Datenzeilen.
source-git-commit: 32196fc76b2743679516a00f86c4912fac0bb3cf
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 76%

---


# Export von Classification-Daten über FTP

Die FTP-Option bietet mehr Flexibilität beim Herunterladen von Datensätzen, z. B. die Fähigkeit, Daten aus mehreren Report Suites oder Datensatzdateien mit über 50.000 Datenzeilen herunterzuladen. Erstellen Sie vor dem Herunterladen von Classification-Daten via FTP ein FTP-Konto.

Berücksichtigen Sie beim Anwenden von Datenfiltern die folgenden Punkte:

* Beim Definieren des Datenfilters können Sie Platzhalter verwenden. Verwenden Sie ein Sternchen `*`, um null oder mehr Zeichen zuzuordnen, und ein Fragezeichen `?`, um genau ein Zeichen zu entsprechen. Verwenden Sie `?*`, um ein oder mehrere Zeichen abzugleichen.
* Wenn beide Datenfilter auf einen Download angewandt werden, werden üblicherweise nur die Zeilen heruntergeladen, die beide Regeln erfüllen. Es gibt jedoch folgende Ausnahmen:
   * Wenn die Bedingung Zeilen mit leerer Spalte = Alle Spalten gilt, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen Spalte auf ihren leeren Gehalt überprüft. Mit dieser Ausnahme wird sichergestellt, dass das Tool jede Zeile mit einer Spalte herunterlädt, die die erste Regel erfüllt, gleichzeitig aber sonst nur über leere Spalten verfügt.
   * Beim Herunterladen von Datenzeilen auf Grundlage leerer Spalten werden alle Spalten mit Ausnahme der in der ersten Regel festgelegten auf leeren Gehalt überprüft.
   * Wurde dieselbe Spalte für beide Filterregeln angegeben (es ist fast unmöglich, beide Kriterien zu erfüllen), werden nur Zeilen heruntergeladen, die die erste Regel erfüllen.
   * FTP-Exporte sind auf 30 Spalten begrenzt.

## Exportieren von Classifications per FTP

In diesen Schritten wird beschrieben, wie Sie Classifications per FTP aus Adobe Analytics exportieren (herunterladen).

1. Erstellen Sie ein FTP-Konto.
1. Gehen Sie zu [!UICONTROL Admin] > [!UICONTROL Classification Importer].
1. Klicken Sie auf die Registerkarte **[!UICONTROL FTP-Import]** .
1. Konfigurieren Sie die Felder für den FTP-Export.
1. Klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Speichern Sie den Datensatz auf Ihrem lokalen System.

## Feldbeschreibungen

| Element | Beschreibungen |
| --- | --- |
| [!UICONTROL Report Suite auswählen] | Wählen Sie die Report Suite aus, aus der Sie die Berichtdaten exportieren möchten. |
| [!UICONTROL Datensatz, der klassifiziert werden soll] | Wählen Sie aus dem Dropdown-Menü den Datensatz aus, den Sie klassifizieren möchten. |
| [!UICONTROL Zeilenanzahl auswählen] | Geben Sie die Anzahl der zu exportierenden Datenzeilen an.<ul><li>Wählen Sie **[!UICONTROL Alle]**, um alle Berichtdaten herunterzuladen.</li><li>Wählen Sie **[!UICONTROL Datenzeilen beschränken auf]**, wenn Sie eine bestimmte Anzahl von Zeilen zum Download festlegen möchten.</li></ul> |
| [!UICONTROL Filtern nach Empfangsdatum] | (Optional) Filtern Sie die Daten nach dem Empfangsdatum. Legen Sie den Datumsbereich fest, für den Sie Daten herunterladen möchten. |
| [!UICONTROL Datenfilter anwenden] | (Optional) Filtern Sie den Datensatz nach Datenkriterien. Sie können den Download so filtern, dass Datenzeilen mit spezifischen Werten oder nicht zugewiesenen Spalten- (Classification-) Werten einbezogen werden. |
| [!UICONTROL Datumsfilter] | (Optional) Filtern Sie die Daten nach Kampagnendaten. Sie können nur Daten aus aktiven Kampagnen herunterladen oder Kampagnen auswählen, die innerhalb eines bestimmten Datumsbereichs beginnen (oder enden). |
| [!UICONTROL Nummerisch exportieren 2] | Mit dem Importer können Sie Nummerisch-2-Classifications in das System importieren. Nummerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im Marketingkanal bericht. |
| [!UICONTROL FTP-Konto] | Geben Sie die Informationen zum FTP-Server, auf den Adobe die Datendatei herunterladen soll, inklusive Hostnamen und Port, Pfad des Zielverzeichnisses, Benutzername und Kennwort an. |
| [!UICONTROL Benachrichtigung] | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen zu diesem FTP-Download gesendet werden sollen. |
| [!UICONTROL Kodierung] | Wählen Sie die Zeichenkodierung für die Datendatei aus. Das Standardkodierungsformat ist entweder UTF-8 oder ISO-8859-1, basierend auf der für die Classification hochgeladenen Kodierung. Mit „UTF-8 zu UTF-16“ können Sie UTF-8-kodierte Classifications in UTF-16-Kodierung konvertieren. Mit „ISO-8859-1 zu UTF-16“ können Sie ISO-8859-1-kodierte Classifications in UTF-16-Kodierung konvertieren.<br>**Hinweis:** Wenn Sie die Konvertierung in UTF-16 auswählen, muss die Quellkodierung mit der Kodierung des Original-Uploads übereinstimmen. Andernfalls kann es zu unerwarteten Ergebnissen kommen. Es wird empfohlen, alle hochgeladenen Dateien in UTF-8 ohne BOM zu kodieren. |

