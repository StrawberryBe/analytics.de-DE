---
title: Browser-Export
description: Mit dem Browser-Export können Sie Ihre Classification-Daten in eine tabulatorgetrennte Datei exportieren.
source-git-commit: 8a5c7309b5d4061b2e3241219d9bdb1521294535
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 74%

---


# Browser-Export

Mit dem Browser-Export können Sie Ihre Classification-Daten in eine tabulatorgetrennte Datei exportieren.

Admin > Classification Importer

Der Datensatz ist eine tabulatorgetrennte Datendatei (Dateierweiterung .tab), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.

>[!NOTE]
>Browser-Exporte sind auf 30 Spalten beschränkt.

## Feldbeschreibungen

| Element | Beschreibungen |
| --- | --- |
| Report Suite auswählen | Wählen Sie die Report Suite aus, aus der Sie die Berichtdaten exportieren möchten. |
| Datensatz, der klassifiziert werden soll | Wählen Sie aus dem Dropdown-Menü den Datensatz aus, den Sie klassifizieren möchten. |
| Zeilenanzahl auswählen | Geben Sie die Anzahl der zu exportierenden Datenzeilen an.<ul><li>Wählen Sie **[!UICONTROL Alle]**, um alle Berichtdaten (bis zu 50.000 Zeilen) herunterzuladen. </li><li>Wählen Sie **[!UICONTROL Datenzeilen beschränken auf]**, wenn Sie eine bestimmte Anzahl von Zeilen zum Download festlegen möchten.</li></ul>Wenn Sie mehr als 50.000 Datenzeilen herunterladen möchten, verwenden Sie die FTP-Download-Option. |
| Filtern nach Empfangsdatum | (Optional) Filtern Sie die Daten nach dem Empfangsdatum. Legen Sie den Datumsbereich fest, für den Sie Daten herunterladen möchten. |
| Datenfilter anwenden | (Optional) Filtern Sie den Datensatz nach Datenkriterien. Sie können den Download so filtern, dass Datenzeilen mit spezifischen Werten oder nicht zugewiesenen Spalten- (Classification-) Werten einbezogen werden. Berücksichtigen Sie beim Anwenden von Datenfiltern die folgenden Punkte:<ul><li>Beim Definieren des Datenfilters können Sie Platzhalter verwenden. Verwenden Sie ein Sternchen, um null oder mehr Zeichen zuzuordnen, und ein Fragezeichen `?`, um genau ein Zeichen zuzuordnen. Verwenden Sie `?*`, um ein oder mehrere Zeichen abzugleichen.</li><li>Wenn beide Datenfilter auf einen Download angewandt werden, werden üblicherweise nur die Zeilen heruntergeladen, die beide Regeln erfüllen. Es gibt jedoch folgende Ausnahmen:<ul><li>Wenn die Bedingung Zeilen mit leerer Spalte = Alle Spalten gilt, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen Spalte auf ihren leeren Gehalt überprüft. Mit dieser Ausnahme wird sichergestellt, dass das System jede Zeile mit einer Spalte herunterlädt, die die erste Regel erfüllt, gleichzeitig aber sonst nur über leere Spalten verfügt.</li><li>Beim Herunterladen von Datenzeilen auf Grundlage leerer Spalten werden alle Spalten mit Ausnahme der in der ersten Regel festgelegten auf leeren Gehalt überprüft.</li><li>Wurde dieselbe Spalte für beide Filterregeln angegeben (es ist fast unmöglich, beide Kriterien zu erfüllen), werden nur Zeilen heruntergeladen, die die erste Regel erfüllen.</li></ul></ul> |
| Datenfilter | (Optional) Filtern Sie die Daten nach Kampagnendaten. Sie können festlegen, dass nur Daten aus aktiven Kampagnen exportiert werden, oder Sie können Kampagnen auswählen, die in einem bestimmten Datumsbereich anfingen (oder endeten).<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |

