---
description: Sie können Daten von Analysis Workspace durch Kopieren oder in PDF- und CSV-Formaten herunterladen.
title: PDF- oder CSV-Dateien herunterladen
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
feature: Kuratieren und Freigeben
role: Business Practitioner, Administrator
exl-id: 085013dc-8263-4fc8-9492-99f0ecadf14b
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '990'
ht-degree: 100%

---

# PDF- oder CSV-Dateien herunterladen

Es gibt verschiedene Möglichkeiten, Daten aus Analysis Workspace zu exportieren, je nachdem, welcher Datensatz außerhalb des Tools analysiert werden soll und wer die Informationen erhalten muss. Exportierte Daten können in Form kopierter Daten, CSV- oder PDF-Dateien vorliegen. Eine PDF-Datei wird in der Regel bevorzugt, wenn Sie in der Datei enthaltene Visualisierungen verwenden möchten, während eine CSV-Datei (oder kopierte Daten) bevorzugt wird, wenn Sie einfach Daten im Klartext benötigen.

## Projekt als CSV oder PDF herunterladen {#download-project}

Sie können ein vollständiges Projekt unter **[!UICONTROL Projekt > Als PDF herunterladen (oder als CSV)]** herunterladen. Die heruntergeladene Datei enthält alle angezeigten (sichtbaren) Tabellen und Visualisierungen im Projekt. Eine PDF-Datei wird in der Regel bevorzugt, wenn Sie in der Datei enthaltene Visualisierungen verwenden möchten, während eine CSV-Datei bevorzugt wird, wenn Sie einfach Daten mit reinem Text wünschen.

![](assets/download-project.png)

Beachten Sie beim Herunterladen von Projekten Folgendes:

* Die Anforderung von Projekt-Downloads kann mit oder ohne Speicherung eines Projekts erfolgen.  Es können jedoch nur gespeicherte Projekte [geplant](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/t-schedule-report.html) sein.
* Der Export von im Browser heruntergeladenen PDF-Dateien kann mehrere Minuten dauern, da das Projekt auf den Adobe-Servern erneut ausgeführt wird, bevor es im PDF-Format ausgegeben wird. Wir empfehlen, das Projekt nicht zu verlassen, bis die PDF-Datei in Ihren Browser heruntergeladen wurde. Sie können jedoch beim Warten weiterhin Änderungen am Projekt vornehmen. Wenn die Ausgabe einer PDF-Datei länger als 5 Minuten dauert, werden Sie aufgefordert, diese stattdessen per E-Mail zu erhalten.
* PDF-Downloads werden als einzelne Seite ohne Seitenumbruch gerendert.
* Bei der PDF-Ausgabe eines Projekts wird das gerendert, was sich auf der Seite befindet. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.

## Daten in die Zwischenablage kopieren (Hotkey: Strg+C) {#copy-data}

Mit der Rechtsklick-Option **[!UICONTROL In Zwischenablage kopieren]** können Sie Daten schnell aus Workspace kopieren und an einer anderen Stelle einfügen.

* Wenn die angezeigte Tabelle kopiert werden soll, klicken Sie mit der rechten Maustaste auf die Tabellenkopfzeile und wählen Sie **Daten in die Zwischenablage kopieren**.
* Wenn Sie möchten, dass nur ein Teil der Daten kopiert wird, wählen Sie die Tabelle aus, und klicken Sie dann mit der rechten Maustaste auf **Auswahl in Zwischenablage kopieren**.

Außerdem kopiert der Hotkey `Ctrl+C` Ihre Auswahl in die Zwischenablage. Nach dem Kopieren können Sie zu einem anderen Tool wechseln und die Informationen einfügen (oder `Ctrl+V` drücken).

![](assets/copy-selection.png)

## Daten als CSV herunterladen {#download-data}

Mit der Rechtsklick-Option **[!UICONTROL Daten als CSV herunterladen]** können Sie eine Datentabelle oder die Datenquelle einer beliebigen Visualisierung als CSV herunterladen.

* Klicken Sie in der Kopfzeile einer Tabelle oder Visualisierung mit der rechten Maustaste auf **[!UICONTROL Daten als CSV herunterladen]**. Dadurch werden die in der Tabelle angezeigten Daten oder die zugrunde liegende Datenquelle für eine Visualisierung als CSV heruntergeladen. Hinweis: Diese Option wird von der Map-Visualisierung nicht unterstützt.
* Wenn eine Auswahl in der Tabelle vorgenommen wird, lautet die Option **[!UICONTROL Auswahl als CSV herunterladen]**. Mit dieser Option wird nur die Auswahl heruntergeladen, nicht die vollständige, angezeigte Tabelle.

![](assets/download-data-viz.png)

## Objekte als CSV herunterladen {#download-items}

Wenn Sie mehr als die 400 sichtbaren Zeilen mit Daten in einer Tabelle analysieren möchten, klicken Sie mit der rechten Maustaste auf die Tabellenkopfzeile oder eine beliebige Zeile und wählen Sie **Elemente als CSV herunterladen (Dimensionsname)**. Diese Option exportiert bis zu 50.000 Dimensionselemente (basierend auf der Tabellensortierung) für die ausgewählte Dimension, wobei Filter und Segmente angewendet werden. Wenn Sie diese Option oben in der Tabelle auswählen, wird die erste Dimension in der Tabelle exportiert. Obwohl in Freiformtabellen keine Beschränkungen gelten, wird empfohlen, die Option zum Herunterladen von Elementen in Tabellen mit weniger als 20 Spalten zu verwenden, um optimale Leistung sicherzustellen.

>[!TIP]
>
> Wenn Ihre Dimension 50.000 Elemente überschreitet, laden Sie die Datei mit unterschiedlichen Sortierkriterien herunter oder wenden Sie einen Filter an. Sortieren Sie z. B. absteigend nach Besuchen in einem Download und dann aufsteigend nach Besuchen in einem zweiten Download. Dieser Tipp hilft Ihnen beim Abrufen von längeren Elementen.

Während eines Downloads können Sie mehrere Aufgaben im Projekt ausführen und sogar zu einem neuen Workspace-Projekt auf derselben Registerkarte navigieren. Der Download wird angehalten, wenn Sie eine neue Browser-Registerkarte öffnen. Der Download wird abgebrochen, wenn Sie Workspace vollständig verlassen oder die Browser-Registerkarte schließen.

![](assets/download-items.png)

### Datei mit heruntergeladenen Elementen

Die Eigenschaften der Tabelle werden wie folgt auf die heruntergeladene Datei angewendet:

* Alle Bedienfeldsegmente werden als Filter angewendet.
* Aufschlüsselungen **oberhalb** der ausgewählten Dimension in der Tabelle werden als Filter über jeder einzelnen Spalte angezeigt.
* Aufschlüsselungen **unterhalb** der ausgewählten Dimension in der Tabelle werden entfernt.

Im obigen Beispiel werden Page-Elemente mit dem Bedienfeldsegment („New Visitor Customers“) heruntergeladen und die darüber liegenden Komponenten („Marketing Channel = Email“) als Filter angewendet, während die darunter liegenden Komponenten („Mobile Device Type“) aus der heruntergeladenen CSV entfernt werden.

![](assets/downloaded-file.png)

### Download-Benachrichtigungen

Beim Herunterladen der Datei wird eine Benachrichtigung mit dem Fortschritt angezeigt. Sie können den Download jederzeit abbrechen, indem Sie auf **[!UICONTROL Download abbrechen]** klicken. Durch Schließen des Popups wird der Download **nicht** abgebrochen.

Sobald die Datei abgeschlossen ist, wird eine Benachrichtigung angezeigt und die Datei wird in Ihren Browser heruntergeladen.

Wenn Sie mehrere Downloads gleichzeitig anfordern, erhalten Sie eine Benachrichtigung, dass jeder weitere Download in die Warteschlange gestellt wird, bis der vorherige Download abgeschlossen ist.

![](assets/toast.png)

## Häufig gestellte Fragen {#faq}

| Frage | Antwort |
| --- | --- |
| Warum besteht meine heruntergeladene PDF-Datei aus einer Seite? | In Workspace werden heruntergeladene PDFs derzeit nicht in Seiten unterteilt. |
| Kann ich mehr als 50.000 Elemente mit der Option „Elemente als CSV herunterladen“ exportieren? | Während jeder Download bis zu 50.000 Dimensionselemente enthalten kann, können Sie die Sortierung der Tabelle ändern, um längere Elemente abzurufen, oder einen Filter anwenden, um spezifischere Elemente herunterzuladen. |
| Beschreibung der Funktion **[!UICONTROL Visualisierung kopieren]** | **[!UICONTROL Visualisierung kopieren]** ist keine Exportoption. Damit können Sie eine Visualisierung oder ein Bedienfeld von einem Bereich in Workspace in einen anderen kopieren. Beispielsweise von einem Bedienfeld in ein anderes im selben Projekt oder von einem Projekt in ein anderes. [Intra-linking-Video](https://docs.adobe.com/content/help/de-DE/analytics-learn/tutorials/analysis-workspace/visualizations/intra-linking-in-analysis-workspace.html) |
