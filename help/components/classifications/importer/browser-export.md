---
title: Browser-Export
description: Mit dem Browser-Export können Sie die Klassifizierungsdaten in eine mit Tabulatoren getrennte Datei exportieren.
source-git-commit: d522303de5beb6a10d95ad2da523774ea595ae2d
workflow-type: ht
source-wordcount: '627'
ht-degree: 100%

---


# Browser-Export

Mit dem Browser-Export können Sie die Klassifizierungsdaten in eine mit Tabulatoren getrennte Datei exportieren.

[!UICONTROL Admin] > [!UICONTROL Classification Importer]

Die Datensatzdatei ist eine tabulatorgetrennte Datendatei (Dateierweiterung.tab), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.

>[!NOTE]
>Browser-Exporte sind auf 30 Spalten beschränkt.

## Feldbeschreibungen

| Element | Beschreibungen |
| --- | --- |
| Report Suite auswählen | Wählen Sie die Report Suite aus, aus der Sie die Berichtsdaten exportieren möchten. |
| Datensatz, der klassifiziert werden soll | Wählen Sie aus dem Dropdown-Menü den Datensatz aus, den Sie klassifizieren möchten. |
| Zeilenanzahl auswählen | Geben Sie die Anzahl der zu exportierenden Datenzeilen an.<ul><li>Wählen Sie **[!UICONTROL Alle]**, um alle Berichtsdaten (bis zu 50.000 Zeilen) herunterzuladen. </li><li>Wählen Sie **[!UICONTROL Datenzeilen beschränken auf]**, wenn Sie eine bestimmte Anzahl von Zeilen zum Download festlegen möchten.</li></ul>Wenn Sie mehr als 50.000 Datenzeilen herunterladen möchten, verwenden Sie die FTP-Download-Option. |
| Filtern nach Empfangsdatum | (Optional) Filtern Sie die Daten nach dem Empfangsdatum. Legen Sie den Datumsbereich fest, für den Sie Daten herunterladen möchten. |
| Datenfilter anwenden | (Optional) Filtern Sie den Datensatz nach Datenkriterien. Sie können den Download so filtern, dass Datenzeilen mit spezifischen Werten oder nicht zugewiesenen Spalten-Werten (Classification-Werten) einbezogen werden. Berücksichtigen Sie beim Anwenden von Datenfiltern die folgenden Punkte:<ul><li>Beim Definieren des Datenfilters können Sie Platzhalter verwenden. Verwenden Sie ein Sternchen als Platzhalter für null oder mehr Zeichen und ein Fragezeichen `?` für genau ein Zeichen. Für ein oder mehrere Zeichen können Sie `?*` eingeben.</li><li>Wenn beide Datenfilter auf einen Download angewandt werden, werden üblicherweise nur die Zeilen heruntergeladen, die beide Regeln erfüllen. Es gibt jedoch folgende Ausnahmen:<ul><li>Wenn die Bedingung „Zeilen mit leerer Spalte = Alle Spalten“ gilt, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen Spalte auf ihren leeren Gehalt überprüft. Mit dieser Ausnahme wird sichergestellt, dass das System jede Zeile mit einer Spalte herunterlädt, die die erste Regel erfüllt, gleichzeitig aber sonst nur über leere Spalten verfügt.</li><li>Beim Herunterladen von Datenzeilen auf Grundlage leerer Spalten werden alle Spalten mit Ausnahme der in der ersten Regel festgelegten auf leeren Gehalt überprüft.</li><li>Wurde dieselbe Spalte für beide Filterregeln angegeben (es ist fast unmöglich, beide Kriterien zu erfüllen), werden nur Zeilen heruntergeladen, die die erste Regel erfüllen.</li></ul></ul> |
| Datenfilter | (Optional) Filtern Sie die Daten nach Kampagnendaten. Sie können festlegen, dass nur Daten aus aktiven Kampagnen exportiert werden, oder Sie können Kampagnen auswählen, die in einem bestimmten Datumsbereich anfingen (oder endeten).<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Export von Numerisch 2 | Mit dem Importer können Sie Numerisch-2-Classifications in das System importieren. Numerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im Marketing-Kanal-Bericht. Im Abschnitt „Numerisch-2-Classifications“ finden Sie Informationen zum Hochladen von Daten mithilfe von Numerisch-2-Classifications. |
| Kodierung | Wählen Sie die Zeichenkodierung für die Datendatei aus. Das Standardcodierungsformat ist entweder UTF-8 oder ISO-8859-1, basierend auf der für die Classification hochgeladenen Codierung. Mit „UTF-8 zu UTF-16“ können Sie UTF-8-codierte Classifications in UTF-16-Codierung konvertieren. Mit „ISO-8859-1 zu UTF-16“ können Sie ISO-8859-1-kodierte Classifications in UTF-16-Kodierung konvertieren.<br>**Hinweis:** Wenn Sie die Konvertierung in UTF-16 auswählen, muss die Quellkodierung mit der Kodierung des Original-Uploads übereinstimmen. Andernfalls kann es zu unerwarteten Ergebnissen kommen. Es wird empfohlen, alle hochgeladenen Dateien in UTF-8 ohne BOM zu kodieren. |
| Anführungszeichenausgabe | Gibt Version 2.1 für die Classification-Datei an. Bei dieser Einstellung werden Sonderzeichen in Anführungszeichen gesetzt, um sicherzustellen, dass Exporte in Excel funktionieren, wenn die eVar-Werte einen Zeilenumbruch aufweisen. Sie können ermitteln, ob eine Classification-Datei die Version 2.1 hat, indem Sie die heruntergeladene Datei öffnen. Im Header wird v2.1 angezeigt. Beispiel: `## SC SiteCatalyst SAINT Import File v:2.1` |

## Exportieren von Classification-Daten über den Browser

1. Klicken Sie auf [!UICONTROL Admin] > [!UICONTROL Classification Importer].
1. Klicken Sie auf die Registerkarte [!UICONTROL Browser-Export].
1. Spezifizieren Sie die Datensatzdetails.
1. Klicken Sie auf [!UICONTROL Datei exportieren].
1. Speichern Sie den Datensatz auf Ihrem lokalen System.
