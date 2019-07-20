---
description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
seo-description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
seo-title: PDF- oder CSV-Dateien herunterladen
title: PDF- oder CSV-Dateien herunterladen
uuid: 8 af 5 f 3 d 7-5870-4 ed 6-8 a 9 f-ef 290 a 48 ef 5 f
translation-type: tm+mt
source-git-commit: b9e57162fae605719d7d85aad52a29165cb63fe4

---


# PDF- oder CSV-Dateien herunterladen

Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.

Der Name der PDF- oder CSV-Datei entspricht dem aktuellen Projektnamen. Bei ungespeicherten Projekten sind die nicht gespeicherten Änderungen am Projekt in der heruntergeladenen Datei enthalten. Beachten Sie, dass Sie ungespeicherte Projekte im PDF- oder CSV-Format nicht planen können.

>[!NOTE]
>
>Wir unterstützen auch die Fallout-Visualisierung im CSV-Format.

>[!NOTE]
>
>Wenn wir ein Projekt in PDF wiedergeben, rendert es einfach die Seite. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.

1. Erstellen oder öffnen Sie ein Projekt.
1. Click **[!UICONTROL Project]** &gt; **[!UICONTROL Download CSV (or Download PDF).]**

On April 11, 2019, several changes were made to **[!CSV downloads]** (and **[!Copy to Clipboard]**) from Analysis Workspace to remove formatting from exported data.
* Das Tausendertrennzeichen ist nicht mehr enthalten. (The decimal separator will continue to be included, and will adhere to the format defined under **[!UICONTROL Components &gt; Report Settings &gt; Thousands Separator]**).
* Es werden keine Währungssymbole angezeigt.
* Es werden keine Prozentsymbole angezeigt.
* Prozentsätze sind Dezimalzeichen. Beispielsweise wird 75% als 0,75 dargestellt.
* Die Zeit wird in Sekunden angezeigt.
* Kohortentabellen zeigen nur Rohwerte an; Prozentwerte entfernt.
* Wenn eine Zahl ungültig ist, wird eine leere Zelle angezeigt.

>[!Note:]
>
> Numerische Werte, die ein Komma als Dezimaltrennzeichen verwenden, werden weiterhin in der exportierten CSV-Datei angerechnet.