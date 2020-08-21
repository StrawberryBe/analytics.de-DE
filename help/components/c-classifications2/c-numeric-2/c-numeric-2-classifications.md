---
description: Numerisch 2 Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Experience Cloud importieren können.
subtopic: Classifications
title: Numerisch 2 Classifications – Übersicht
topic: Admin tools
uuid: cbea7cd1-3a92-4e9d-b671-646e9add1ee6
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '328'
ht-degree: 100%

---


# Numerisch 2 Classifications – Übersicht

Numerisch 2 Classifications stellen benutzerdefinierte, flexible Metriken bereit, die Sie mit dem Importer in Adobe Experience Cloud importieren können.

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juli 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert, und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Workflow exportiert werden und sind weiterhin in Berichten verfügbar.

>[!NOTE]
>
>Nach der Analytics-Wartungsversion vom 10. Mai 2018 schränkte Adobe die Funktion für datumsaktivierte und numerische Classifications ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und Numerisch-Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

Eine gängige Verwendung von Numerisch 2 Classifications sind numerische Variablen, die sich im Laufe der Zeit für verschiedene Elemente verändern, z. B. die Kosten verkaufter Waren. In Admin können Sie auf der Seite [!UICONTROL Konversion-Classification] Classifications erstellen und dann mithilfe des Importeurs eine Datei exportieren, Bearbeitungen vornehmen und anschließend die Datei wieder in Adobe zurückimportieren. Nach dem Datenimport können Sie die numerischen Classifications beim Erstellen berechneter Metriken nutzen.

>[!IMPORTANT]
>
>Analysis Workspace und Ad Hoc Analysis unterstützen keine Numerisch 2 Classifications.

In der folgenden Tabelle werden die Unterschiede zwischen den Classification-Typen erläutert:

| FUNKTION | TEXT | NUMERISCH 1.0 | NUMERISCH 2.0 |
|---|---|---|---|
| Wird als Bericht angezeigt | Ja | Nein | Nein |
| Kann als Metrik verwendet werden | Nein | Ja | Ja |
| Kann zum Basisbericht erstellt werden | Ja | Nein | Ja |
| Wird ereignisbasiert berechnet | Nein | Ja | Ja |
| Mehrere Zeilen pro Schlüssel | Nein | Nein | Ja |
| Kann für verschiedene Zeiträume unterschiedliche Werte aufweisen | Nein | Nein | Ja |
| Kann in berechneten Metriken verwendet werden | Nein | Ja | Ja |

