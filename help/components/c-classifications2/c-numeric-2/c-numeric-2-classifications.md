---
description: Nummerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Experience Cloud importieren können.
seo-description: Nummerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Experience Cloud importieren können.
seo-title: Numerisch-2-Klassifizierungen – Übersicht
solution: Analytics
subtopic: Classifications
title: Numerisch-2-Klassifizierungen – Übersicht
topic: Admin Tools
uuid: cbea7cd1-3a92-4e9d-b671-646e9add1ee6
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Numerisch-2-Klassifizierungen – Übersicht

Numerisch-2-Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Experience Cloud importieren können.

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juli 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

>[!NOTE]
>
>In der Analytics Maintenance-Version vom 10. Mai 2018 hat Adobe begonnen, die Funktionalität datumsaktivierter und numerischer Klassifizierungen zu beschränken. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und Numerisch-Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

Eine gängige Verwendung von Nummerisch-2-Classifications sind nummerische Variablen, die sich im Laufe der Zeit für verschiedene Elemente verändern, z. B. die Kosten verkaufter Waren. In Admin können Sie auf der Seite [!UICONTROL Konversion-Classification] Classifications erstellen und dann mithilfe des Importeurs eine Datei exportieren, Bearbeitungen vornehmen und anschließend die Datei wieder in Adobe zurückimportieren. Nach dem Datenimport können Sie die nummerischen Classifications beim Erstellen berechneter Metriken nutzen.

>[!IMPORTANT]
>
>Analysis Workspace und Ad-hoc-Analysen unterstützen keine Nummerisch-2-Klassifizierungen.

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

