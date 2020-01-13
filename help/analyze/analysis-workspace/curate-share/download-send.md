---
description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
title: PDF- oder CSV-Dateien herunterladen
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# PDF- oder CSV-Dateien herunterladen

Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.

Der Name der PDF- oder CSV-Datei entspricht dem aktuellen Projektnamen. Bei ungespeicherten Projekten sind die nicht gespeicherten Änderungen am Projekt in der heruntergeladenen Datei enthalten. Beachten Sie, dass Sie ungespeicherte Projekte im PDF- oder CSV-Format nicht planen können.

> [!NOTE] Wir unterstützen auch die Fallout-Visualisierung im CSV-Format.

> [!NOTE] Wenn ein Projekt in eine PDF gerendert wird, dann wird nur der Seiteninhalt gerendert. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.

1. Erstellen oder öffnen Sie ein Projekt.
1. Klicken Sie auf **[!UICONTROL Projekt]** &gt; **[!UICONTROL CSV herunterladen (bzw. PDF herunterladen)]**.

Am 11. April 2019 wurden mehrere Änderungen an **[!CSV Downloads]** (und **[!CIn Zwischenablage kopieren]**) in Analysis Workspace vorgenommen, um die Formatierung aus den exportierten Daten zu entfernen.
* Das Tausendertrennzeichen ist nicht mehr enthalten. (Das Dezimaltrennzeichen wird weiterhin enthalten sein und dem unter **[!UICONTROL Komponenten &gt; Berichtseinstellungen &gt; Tausendertrennzeichen]** definierten Format entsprechen.)
* Es werden keine Währungssymbole angezeigt.
* Es werden keine Prozentzeichen angezeigt.
* Prozentsätze sind dezimal; 75 % wird beispielsweise als 0,75 angezeigt.
* Die Zeit wird in Sekunden angezeigt.
* Kohortentabellen zeigen nur Rohwerte an. Prozentwerte wurden entfernt.
* Wenn eine Zahl ungültig ist, wird eine leere Zelle angezeigt.

>[!NHinweis:]
>
> Numerische Werte, die ein Komma als Dezimaltrennzeichen verwenden, werden weiterhin in der exportierten CSV angegeben.
