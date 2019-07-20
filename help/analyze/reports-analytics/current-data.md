---
description: Mit der Option „Aktuelle Daten einschließen“ in Reports & Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. Die aktuellen Daten zeigen die meisten Metriken in Minutenschnelle und liefern so relevante Daten für die rasche Entscheidungsfindung.
seo-title: Aktuelle Daten
solution: Analytics
subtopic: Aktuelle Daten
title: Aktuelle Daten
topic: 'Berichte    '
uuid: 601 d 3695-be 13-4 b 7 f -9 df 0-de 01 c 8 bd 64 ee
translation-type: tm+mt
source-git-commit: 1fdd14497171dbf5850ec1b1d873a06931d58435

---


# Aktuelle Daten

Mit der Option „Aktuelle Daten einschließen“ in Reports &amp; Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. Die aktuellen Daten zeigen die meisten Metriken in Minutenschnelle und liefern so relevante Daten für die rasche Entscheidungsfindung.

Es ist als Teil der Einstellungen eines Berichts sichtbar:

![Screenshot für aktuelle Daten](assets/current_data.png)

„Aktuelle Daten“ ist standardmäßig für alle Berichte aktiviert, die diese Funktion unterstützen. Wenn Sie alle Metriken lieber nach der vollständigen Verarbeitung der Daten anzeigen würden, gibt es mehrere Optionen:

* Verwenden Sie den Analysis Workspace, der vollständig verarbeitete Daten verwendet.
* Klicken Sie in der aktuellen Datenberichtseinstellung auf "Nein" , um nur vollständig verarbeitete Daten zu verwenden.
* Entfernen Sie das Berechtigungselement "Aktuelle Daten" aus einem Produktprofil in der Admin-Konsole, um zu verhindern, dass Benutzer diese Option sehen. See [Analytics Tools permission items](../../admin/admin-console/permissions/analytics-tools.md) in the Admin user guide for more information.

Aufgrund der Priorisierung der Datenverfügbarkeit können aktuelle Daten derzeit nicht mit Segmenten, Classifications, Aufschlüsselungen, Pfaden und einigen Metriken verwendet werden. Wenn eine dieser Funktionen verwendet wird, werden die aktuellen Daten im Bericht erzwungen und ein gelbes Hinweis zeigt an, warum aktuelle Daten nicht verfügbar sind.

![Aktuelle Datenbenachrichtigung](assets/current_data_notice.png)

## Typische Latenz aktueller Daten

Die Metriken werden in einem der drei nachfolgenden Zeitrahmen dargestellt. Mit dem Uhrensymbol neben dem Umschalter „Aktuelle Daten einschließen“ rufen Sie den tatsächlichen Latenzwert für die einzelnen Metriken in einem Bericht ab.

| Zeitrahmen | Metriken |
| --- | --- |
| Unter 10 Minuten | Instanzen und Seitenansichten in Traffic-Variablen |
| Zwischen 10 und 35 Minuten | Konversionsereignisse, Instanzen und Seitenansichten in Konversionsvariablen |
| Zwischen 45 und 120 Minuten | Alle anderen Daten, z. B. Besuche, Unique Visitors und Beitrag |

Da einige der Daten, die in der Ansicht der aktuellen Datenansicht angezeigt werden, nicht vollständig verarbeitet wurden, können Sie einen Unterschied zwischen den Werten sehen, die in der Ansicht der aktuellen Datenansicht und der endgültigen Ansicht gemeldet wurden. Bei Trendberichten liegt die Datenabweichung in der Regel bei maximal 1 %.

## Berechnete Metriken

Die berechneten Metriken können anhand von Metriken mit abweichenden Latenzen erstellt werden. Daher wird ein Teil der jüngsten Werte u. U. anhand von unvollständigen Daten in der Anzeige der aktuellen Daten berechnet.

For example, you create the calculated metric 'Page Views per Visit using the formula `Page Views divided by Visits`. Seitenansichten werden in der Regel innerhalb von 10 Minuten angezeigt und Besuche innerhalb von 2 Stunden werden gewöhnlich angezeigt. Berechnete Metriken innerhalb dieses Latenzfensters werden mit unvollständigen Metriken berechnet. Wenn Sie eine neue Seite posten, die 4000 Treffer aus 4000 verschiedenen Besuchen über einen Zeitraum von 2 Stunden erhält, kann die Latenzdifferenz zwischen diesen Metriken zu unvollständigen Berechnungen führen.

Dieser Datenunterschied ist bei der Berichterstellung zu neuen Werten oder bei kurzen Zeitbildern am deutlichsten. Wenn ein Bericht längere Datumsbereiche verwendet, haben die Latenzunterschiede, die in den letzten Stunden der Berichterstellung auftreten, keine nennenswerten Auswirkungen auf berechnete Metriken.

Wenn Sie über berechnete Metriken verfügen, die durch diese Unterschiede beeinflusst werden, sollten Sie die aktuellen Daten deaktivieren oder Metriken mit demselben Latenzfenster verwenden.

## Heruntergeladene Berichte

Wenn Sie einen Bericht herunterladen und dabei die Anzeige der aktuellen Daten aktiviert ist, wird der Bericht in die Warteschlange eingestellt, erzeugt und dann an den Browser zurückgegeben. Wenn Daten während der Generierung des Berichts gesammelt werden, werden diese Daten im Bericht angezeigt. Dieses Zeitfenster kann dazu führen, dass der heruntergeladene Bericht etwas mehr Daten enthält.
