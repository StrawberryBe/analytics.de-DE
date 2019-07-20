---
description: Nummerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Marketing Cloud importieren können.
seo-description: Nummerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Marketing Cloud importieren können.
seo-title: Übersicht über Nummerisch 2 Klassifizierungen
solution: Analytics
subtopic: Classifications
title: Übersicht über Nummerisch 2 Klassifizierungen
topic: Admin Tools
uuid: cbea 7 cd 1-3 a 92-4 e 9 d-b 671-646 e 9 add 1 ee 6
translation-type: tm+mt
source-git-commit: 49e149fe57d5d66b8eda22b1bdf60e7c6200761c

---


# Übersicht über Nummerisch 2 Klassifizierungen

Nummerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Marketing Cloud importieren können.

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juli 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

>[!NOTE]
>
>In der Analytics Maintenance Release vom 10. Mai 2018 wurde Adobe gestartet, um die Funktionalität von datumsaktivierten und numerischen Klassifizierungen zu beschränken. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und Numerisch-Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

Eine gängige Verwendung von Nummerisch-2-Classifications sind nummerische Variablen, die sich im Laufe der Zeit für verschiedene Elemente verändern, z. B. die Kosten verkaufter Waren. In Admin können Sie auf der Seite [!UICONTROL Konversion-Classification] Classifications erstellen und dann mithilfe des Importeurs eine Datei exportieren, Bearbeitungen vornehmen und anschließend die Datei wieder in Adobe zurückimportieren. Nach dem Datenimport können Sie die nummerischen Classifications beim Erstellen berechneter Metriken nutzen.

>[!IMPORTANT]
>
>Analysis Workspace und Ad-hoc-Analysen unterstützen keine Nummerisch 2 Klassifizierungen.

In der folgenden Tabelle werden die Unterschiede zwischen den Classification-Typen erläutert:

| FUNKTION | TEXT | NUMMERISCH 1.0 | NUMMERISCH 2.0 |
|---|---|---|---|
| Wird als Bericht angezeigt | Ja | Nein | Nein |
| Kann als Metrik verwendet werden | Nein | Ja | Ja |
| Kann zum Basisbericht erstellt werden | Ja | Nein | Ja |
| Wird ereignisbasiert berechnet | Nein | Ja | Ja |
| Mehrere Zeilen pro Schlüssel | Nein | Nein | Ja |
| Kann für verschiedene Zeiträume unterschiedliche Werte aufweisen | Nein | Nein | Ja |
| Kann in berechneten Metriken verwendet werden | Nein | Ja | Ja |

