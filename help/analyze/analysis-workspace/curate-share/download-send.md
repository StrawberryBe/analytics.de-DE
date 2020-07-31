---
description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
title: PDF- oder CSV-Dateien herunterladen
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: ht
source-git-commit: 422b69a9f671bbd3c4e8f033916296cbdf7f27d9
workflow-type: ht
source-wordcount: '363'
ht-degree: 100%

---


# PDF- oder CSV-Dateien herunterladen

Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.

Der Name der PDF- oder CSV-Datei entspricht dem aktuellen Projektnamen. Bei ungespeicherten Projekten sind die nicht gespeicherten Änderungen am Projekt in der heruntergeladenen Datei enthalten. Beachten Sie, dass Sie ungespeicherte Projekte im PDF- oder CSV-Format nicht planen können.

Beachten Sie:

* Wir unterstützen auch die Fallout-Visualisierung im CSV-Format.
* Wenn ein Projekt in eine PDF gerendert wird, wird nur der Seiteninhalt gerendert. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.
* Der Export von in den Browser heruntergeladenen PDFs kann einige Minuten dauern. Das liegt daran, dass wir das gesamte Projekt auf unseren Servern erneut ausführen müssen, bevor wir es im PDF-Format wiedergeben können. Wir empfehlen, das Projekt nicht zu verlassen, bis die PDF-Datei in Ihren Browser heruntergeladen wurde. Sie können jedoch beim Warten weiterhin Änderungen am Projekt vornehmen.
* Derzeit werden die PDFs sehr langer Workspace-Projekte als eine einzige riesige Seite und nicht als paginiertes Dokument exportiert. Wir arbeiten an einer Verbesserung des PDF-Exports von Workspace, die eine Paginierung ermöglicht.

1. Erstellen oder öffnen Sie ein Projekt.
1. Klicken Sie auf **[!UICONTROL Projekt]** > **[!UICONTROL CSV herunterladen (bzw. PDF herunterladen).]**

Am 11. April 2019 wurden mehrere Änderungen an **[!UICONTROL CSV-Downloads]** (und **[!UICONTROL In Zwischenablage kopieren]**) in Analysis Workspace vorgenommen, um die Formatierung aus den exportierten Daten zu entfernen.
* Das **[!UICONTROL Tausendertrennzeichen]** ist nicht mehr enthalten. (Das Dezimaltrennzeichen wird weiterhin enthalten sein und dem unter **[!UICONTROL Komponenten > Berichtseinstellungen > Tausendertrennzeichen]** definierten Format entsprechen.)
* Es werden keine Währungssymbole angezeigt.
* Es werden keine Prozentzeichen angezeigt.
* Prozentsätze sind dezimal; 75 % wird beispielsweise als 0,75 angezeigt.
* Die Zeit wird in Sekunden angezeigt.
* Kohortentabellen zeigen nur Rohwerte an. Prozentwerte wurden entfernt.
* Wenn eine Zahl ungültig ist, wird eine leere Zelle angezeigt.
* Es wird keine Rundung angewendet (auch wenn diese in der berechneten Metrik angegeben ist) – es werden die Rohwerte angezeigt.

>[!NHinweis:]
>
> Numerische Werte, die ein Komma als Dezimaltrennzeichen verwenden, werden weiterhin in der exportierten CSV angegeben.
