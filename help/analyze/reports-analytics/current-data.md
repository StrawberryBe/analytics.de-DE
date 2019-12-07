---
description: Mit der Option „Aktuelle Daten einschließen“ in Reports & Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. Die aktuellen Daten zeigen die meisten Metriken in Minutenschnelle und liefern so relevante Daten für die rasche Entscheidungsfindung.
subtopic: Current Data
title: Aktuelle Daten
topic: Reports
uuid: 601d3695-be13-4b7f-9df0-de01c8bd64ee
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Aktuelle Daten

Mit der Option „Aktuelle Daten einschließen“ in Reports &amp; Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. Die aktuellen Daten zeigen die meisten Metriken in Minutenschnelle und liefern so relevante Daten für die rasche Entscheidungsfindung.

Es ist als Option im Rahmen der Berichtseinstellungen sichtbar:

![Screenshot "Aktuelle Daten"](assets/current_data.png)

„Aktuelle Daten“ ist standardmäßig für alle Berichte aktiviert, die diese Funktion unterstützen. Wenn Sie nach der vollständigen Verarbeitung der Daten lieber alle Metriken anzeigen möchten, stehen Ihnen mehrere Optionen zur Verfügung:

* Verwenden Sie den Analysis Workspace, der vollständig verarbeitete Daten verwendet.
* Klicken Sie in der aktuellen Berichtseinstellung auf "Nein", um nur vollständig verarbeitete Daten zu verwenden.
* Entfernen Sie das Berechtigungselement "Aktuelle Daten"aus einem Produktprofil in der Admin-Konsole, um zu verhindern, dass diese Option Benutzern ohne Administratorrechte angezeigt wird. Weitere Informationen finden Sie unter Berechtigungselemente[ zu ](/help/admin/admin-console/permissions/analytics-tools.md)Analytics-Tools im Admin-Benutzerhandbuch.

Aufgrund der Priorisierung der Datenverfügbarkeit können aktuelle Daten derzeit nicht mit Segmenten, Classifications, Unterteilungen, Pfaden und einigen Metriken verwendet werden. Wenn eine dieser Funktionen verwendet wird, werden die aktuellen Daten im Bericht auf "Nein"gesetzt und es wird ein gelber Hinweis angezeigt, der erklärt, warum aktuelle Daten nicht verfügbar sind.

![Aktuelle Datenmeldung](assets/current_data_notice.png)

## Typische Latenz aktueller Daten

Die Metriken werden in einem der drei nachfolgenden Zeitrahmen dargestellt. Mit dem Uhrensymbol neben dem Umschalter „Aktuelle Daten einschließen“ rufen Sie den tatsächlichen Latenzwert für die einzelnen Metriken in einem Bericht ab.

| Zeitrahmen | Metriken |
| --- | --- |
| Unter 10 Minuten | Instanzen und Seitenansichten in Traffic-Variablen |
| Zwischen 10 und 35 Minuten | Konversionsereignisse, Instanzen und Seitenansichten für Konversionsvariablen |
| Zwischen 45 und 120 Minuten | Alle anderen Daten, z. B. Besuche, individuelle Besucher und Teilnahme |

Da einige der Daten, die in der aktuellen Datenansicht angezeigt werden, nicht vollständig verarbeitet wurden, können Sie einen Unterschied zwischen den Werten sehen, die in der aktuellen Datenansicht und in der finalisierten Ansicht gemeldet werden. Bei Trendberichten liegt die Datenabweichung in der Regel bei maximal 1 %.

## Berechnete Metriken

Die berechneten Metriken können anhand von Metriken mit abweichenden Latenzen erstellt werden. Daher wird ein Teil der jüngsten Werte u. U. anhand von unvollständigen Daten in der Anzeige der aktuellen Daten berechnet.

Sie erstellen beispielsweise die berechnete Metrik "Seitenansichten pro Besuch"mit der Formel `Page Views divided by Visits`. Seitenansichten werden in der Regel innerhalb von 10 Minuten angezeigt, und Besuche werden in der Regel innerhalb von 2 Stunden angezeigt, berechnete Metriken innerhalb dieses Latenzfensters werden anhand unvollständiger Metriken berechnet. Wenn Sie eine neue Seite mit 4000 Treffern aus 4000 verschiedenen Besuchen innerhalb eines Zeitraums von 2 Stunden posten, kann die Latenzabweichung zwischen diesen Metriken unvollständige Berechnungen hervorrufen.

Dieser Datenunterschied ist am deutlichsten sichtbar, wenn über neue Werte oder kurze Zeitrahmen berichtet wird. Wenn ein Bericht längere Datumsbereiche verwendet, haben die Latenzunterschiede, die in den letzten Stunden der Berichterstellung auftreten, kaum merkliche Auswirkungen auf berechnete Metriken.

Wenn Sie berechnete Metriken haben, die von diesen Unterschieden betroffen sein könnten, deaktivieren Sie entweder die aktuellen Daten oder verwenden Sie Metriken mit derselben erwarteten Latenzzeit.

## Heruntergeladene Berichte

Wenn Sie einen Bericht herunterladen und dabei die Anzeige der aktuellen Daten aktiviert ist, wird der Bericht in die Warteschlange eingestellt, erzeugt und dann an den Browser zurückgegeben. Wenn Daten gesammelt werden, während der Bericht erstellt wird, werden diese Daten im Bericht angezeigt. Dieser Zeitfenster kann dazu führen, dass der heruntergeladene Bericht etwas mehr Daten enthält.
