---
description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
seo-description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
seo-title: PDF- oder CSV-Dateien herunterladen
title: PDF- oder CSV-Dateien herunterladen
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# PDF- oder CSV-Dateien herunterladen

Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.

Der Name der PDF- oder CSV-Datei entspricht dem aktuellen Projektnamen. Bei ungespeicherten Projekten sind die nicht gespeicherten Änderungen am Projekt in der heruntergeladenen Datei enthalten. Beachten Sie, dass Sie ungespeicherte Projekte im PDF- oder CSV-Format nicht planen können.

> [!NOTE] Wir unterstützen auch die Fallout-Visualisierung im CSV-Format.

> [!NOTE] Wenn wir ein Projekt als PDF wiedergeben, geben wir einfach das auf der Seite. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.

1. Erstellen oder öffnen Sie ein Projekt.
1. Click **[!UICONTROL Project]** &gt; **[!UICONTROL Download CSV (or Download PDF).]**

On April 11, 2019, several changes were made to **[!CSV downloads]** (and **[!Copy to Clipboard]**) from Analysis Workspace to remove formatting from exported data.
* Das Tausendertrennzeichen ist nicht mehr enthalten. (The decimal separator will continue to be included, and will adhere to the format defined under **[!UICONTROL Components &gt; Report Settings &gt; Thousands Separator]**).
* Es werden keine Währungssymbole angezeigt.
* Es werden keine Prozentzeichen angezeigt.
* Prozentsätze sind dezimal; 75 % sind beispielsweise 0,75.
* Die Zeit wird in Sekunden angezeigt.
* Kohortentabellen zeigen nur Rohwerte an. Prozentwerte entfernt.
* Ist eine Zahl ungültig, wird eine leere Zelle angezeigt.

>[!NHinweis:]
>
> Numerische Werte, die ein Komma als Dezimaltrennzeichen verwenden, werden weiterhin in der exportierten CSV zitiert.