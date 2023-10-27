---
description: Schnellsegmente in Analysis Workspace verwenden
title: Schnellsegmente
feature: Segmentation
role: User, Admin
exl-id: 680e7772-10d3-4448-b5bf-def3bc3429d2
source-git-commit: d64f6687dd6e6f688d332926e6d90fa699cac968
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 39%

---

# Schnellsegmente

Schnellsegmente ermöglichen es Ihnen, Daten innerhalb eines Projekts einfach zu untersuchen, ohne ein komplexeres Komponentensegment in der [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md).

Beachten Sie beim Erstellen von Schnellsegmenten Folgendes:

* Schnellsegmente gelten nur für das Projekt, in dem sie erstellt wurden. Sie sind nicht in anderen Projekten verfügbar und können nicht für andere Benutzer freigegeben werden.
* Es sind maximal 3 Regeln zulässig.
* Verschachtelte Container oder sequenzielle Regeln werden nicht unterstützt.

Das folgende Video zeigt die Verwendung von Schnellsegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/341466/?quality=12&learn=on)

## Schnellsegment erstellen

Jeder Benutzer in Analysis Workspace kann ein schnelles Segment erstellen.

So erstellen Sie ein Schnellsegment:

1. Wählen Sie eine der folgenden Methoden, um mit der Erstellung des Schnellsegments zu beginnen:

   * **Ad Hoc (Drag &amp; Drop):** Ziehen Sie eine Komponente aus der linken Leiste in die Dropzone neben dem **Segment** Symbol in der Bedienfeldüberschrift und wählen Sie dann die **Bearbeiten** -Symbol, um das Segment anzupassen.

     ![Bearbeiten von Ad-hoc-Segmenten](assets/filter-adhoc-edit.png)

     >[!NOTE]
     >
     > Beachten Sie beim Erstellen eines Schnellsegment Ad Hoc (Drag &amp; Drop) Folgendes:
     > * Die folgenden Komponententypen werden nicht unterstützt: berechnete Metriken und Dimensionen sowie Metriken, aus denen Sie keine Segmente erstellen können.
     > * Bei vollständigen Dimensionen und Ereignissen erstellt Analysis Workspace Hit-Segmente mit „vorhanden“. Beispiele: `Hit where eVar1 exists` oder `Hit where event1 exists`.
     > * Wenn &quot;nicht angegeben&quot;oder &quot;keine&quot;in der Segment-Dropzone abgelegt werden, wird sie automatisch in ein Segment &quot;nicht vorhanden&quot;konvertiert, damit es in Segmenten korrekt behandelt wird.


   * **Verwenden des Segmentsymbols:** Wählen Sie in einer Freiformtabelle die **Segment** in der Bedienfeldüberschrift.

     ![Segmentfilter](assets/quick-seg1.png)

1. Passen Sie eine der folgenden Einstellungen an:

   | Einstellung | Beschreibung |
   | --- | --- |
   | [!UICONTROL Name] | Der Standardname eines Segments besteht aus der Kombination der Regelnamen im Segment. Sie können das Segment in einen benutzerfreundlicheren Namen umbenennen. |
   | [!UICONTROL Ein-/Ausschließen] | Sie können Komponenten in Ihrer Segmentdefinition entweder ein- oder ausschließen, aber nicht beides. |
   | [!UICONTROL Treffer-/Besuchs-/Besucher-Container] | Schnellsegmente enthalten nur einen [Segment-Container](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=de#section_AF2A28BE92474DB386AE85743C71B2D6), mit dem Sie eine Dimension/eine Metrik/einen Datumsbereich in das Segment einbeziehen (oder daraus ausschließen) können. [!UICONTROL Besucher] enthält für den Besucher spezifische übergreifende Daten zu allen Besuchen und Seitenansichten. Mit dem Container [!UICONTROL Besuch] können Sie Regeln für die Aufschlüsselung der Besucherdaten auf der Grundlage der Besuche festlegen und mit dem Container [!UICONTROL Treffer] können Sie die Besucherinformationen anhand der einzelnen Seitenaufrufe aufschlüsseln. Der Standard-Container ist [!UICONTROL Treffer]. |
   | [!UICONTROL Komponenten] (Dimension/Metrik/Datumsbereich) | Definieren Sie bis zu 3 Regeln, indem Sie Komponenten (Dimensionen, Metriken, Datumsbereiche oder Dimensionswerte) hinzufügen. Es gibt 3 Möglichkeiten, die richtige Komponente zu finden:<ul><li>Beginnen Sie mit der Eingabe und der schnelle Segment-Builder findet automatisch die entsprechende Komponente.</li><li>Verwenden Sie die Dropdown-Liste, um die Komponente zu finden.</li><li>Per Drag-and-Drop aus der der linken Leiste ziehen.</li></ul> |
   | [!UICONTROL Operator] | Verwenden Sie das Dropdown-Menü, um Standardoperatoren und Operatoren des Typs [!UICONTROL Distinct Count] zu finden. Siehe [Segmentoperatoren](/help/components/segmentation/seg-reference/seg-operators.md). |
   | Plus (+)-Zeichen | Eine weitere Regel hinzufügen |
   | AND/OR-Kennzeichung | Sie können den Regeln „AND“ oder „OR“ hinzufügen, aber Sie können „AND“ und „OR“ aber nicht in einer Segmentdefinition kombinieren. |
   | [!UICONTROL Übernehmen] | Dieses Segment auf das Panel anwenden. Wenn das Segment keine Daten enthält, werden Sie gefragt, ob Sie fortfahren möchten. |
   | [!UICONTROL Builder öffnen] | Öffnet Segment Builder. Nachdem Sie das Segment im Segmentaufbau gespeichert oder angewendet haben, wird es nicht mehr als &quot;Schnellsegment&quot;betrachtet. Es wird Teil der Segmentbibliothek der Komponentenliste. <p>Um die Komponente für alle Projekte und in der linken Leiste verfügbar zu machen, wählen Sie die Option [!UICONTROL **Dieses Segment für alle Projekte verfügbar machen und es zu Ihrer Komponentenliste hinzufügen**].</p><p>Weitere Informationen finden Sie im Abschnitt . [Schnellsegment als Komponentensegment speichern](#save-a-quick-segment-as-a-component-list-segment) in diesem Artikel.</p><p>**Hinweis:** Nur Benutzer mit der Berechtigung Segmenterstellung im [Adobe Admin Console](/help/admin/admin-console/permissions/analytics-tools.md) kann den Segment Builder öffnen.</p> |
   | [!UICONTROL Abbrechen] | Abbrechen dieses Schnellsegments (wenden Sie es nicht an). |
   | [!UICONTROL Datumsbereich] | Der Validator verwendet den Datumsbereich des Panels für die Datensuche. Doch jeder in einem Schnellsegment angewendete Datumsbereich überschreibt den Datumsbereich des Panels im oberen Bereich des Panels. |
   | Vorschau (oben rechts) | Ermöglicht festzustellen, ob ein gültiges Segment vorhanden ist und wie groß es ist. Stellt eine Aufschlüsselung des Datensatzes dar, der bei der Anwendung dieses Segments zu erwarten ist. Möglicherweise erhalten Sie den Hinweis, dass dieses Segment über keine Daten verfügt. In diesem Fall können Sie die Segmentdefinition fortsetzen oder ändern. |

1. Auswählen [!UICONTROL **Anwenden**] , um Ihre Änderungen zu speichern.

## Schnellsegmente bearbeiten

1. Bewegen Sie den Mauszeiger über das Schnellsegment und wählen Sie die **Bearbeiten** Symbol.

   ![Ad-hoc-Filter bearbeiten](assets/filter-adhoc-edit.png)

1. Bearbeiten Sie die Segmentdefinition und/oder den Segmentnamen.

1. Wählen Sie [!UICONTROL **Anwenden**] aus.

## Schnellsegmente als Komponentensegment speichern

>[!IMPORTANT]
>
> Beachten Sie beim Speichern eines Schnellsegments Folgendes:
> 
> * Um ein Schnellsegment zu speichern, benötigen Sie die Berechtigung Segmenterstellung im [Adobe Admin Console](/help/admin/admin-console/permissions/analytics-tools.md).
> 
> * Nachdem Sie das Segment gespeichert oder angewendet haben, kann es nicht mehr im Quick Segment Builder bearbeitet werden. Stattdessen müssen Sie den regulären Segment Builder verwenden.

Sie können Schnellsegmente als Komponentensegmente speichern. Vorteile von Komponenten-Listensegmenten:

* Verfügbarkeit aller Workspace-Projekte
* Unterstützung komplexerer Segmente sowie sequenzieller Segmente

Sie können Segmente entweder im Segment-Schnellaufbau oder im [!UICONTROL Filter Builder].

### Speichern im Schnellsegment-Builder {#save2}

1. Nachdem Sie das Schnellsegment angewendet haben, halten Sie den Mauszeiger darüber und wählen Sie das Infosymbol (&quot;i&quot;) aus.
1. Auswählen **[!UICONTROL Bereitstellen für alle Projekte und Hinzufügen zur Komponentenliste]**.
1. Optional: Benennen Sie das Segment um.
1. Wählen Sie **[!UICONTROL Speichern]** aus.

   Das Segment wird nun in der Komponentenliste in der linken Leiste angezeigt. Beachten Sie außerdem, dass sich die Seitenleiste des Segments von hellblau in dunkelblau ändert und damit angibt, dass es im Quick Segment Builder nicht mehr bearbeitet oder geöffnet werden kann.

### Im Segment Builder speichern {#save3}

1. Nachdem Sie das Schnellsegment angewendet haben, halten Sie den Mauszeiger darüber und wählen Sie das Infosymbol (&quot;i&quot;) aus.
1. Auswählen **[!UICONTROL Segment speichern]**
1. (Optional) Benennen Sie das Segment um und wählen Sie [!UICONTROL **Anwenden**].

   Gehen Sie zurück zu Workspace und beachten Sie, dass sich die Seitenleiste des Segments von hellblau in dunkelblau ändert, was bedeutet, dass das Segment nicht mehr im Schnellsegment-Builder bearbeitet oder geöffnet werden kann. Und durch Speichern wird er Teil der Komponentenliste.

Nachdem Sie das Segment angewendet haben, können Sie es Ihrer Segmentkomponentenliste hinzufügen und für alle Ihre Projekte verfügbar machen.

1. Bewegen Sie den Mauszeiger über das gespeicherte Segment und wählen Sie das Stiftsymbol aus.

1. Auswählen [!UICONTROL **Open Builder**].

1. Beachten Sie oben im Segment Builder die [!UICONTROL **Nur Projekt-Segment**] dialog:

   ![Dialogfeld &quot;Nur Projekt-Segment&quot;](assets/project-only-segment-dialog.png)

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Alle Projekte verfügbar machen und der Komponentenliste hinzufügen]**.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

   Das Segment wird jetzt in Ihrer Segmentkomponentenliste für alle Ihre Projekte angezeigt.
Sie können auch [Segment freigeben](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de#concept_4A9726927E7C44AFA260E2BB2721AFC6) mit anderen Personen in Ihrer Organisation.

## Schnellsegmentbeispiel

Im folgenden Beispiel eines Segments werden Dimensionen und Metriken kombiniert:

![](assets/quick-seg2.png)

## Bekanntes Problem

1. Erstellen Sie ein Schnellsegment mit zwei Einträgen und **[!UICONTROL speichern]** Sie es als „Test1“.
1. Klicken Sie auf **[!UICONTROL Speichern unter]** und speichern Sie dieses Schnellsegment als „Test2“.
1. Bearbeiten Sie das Schnellsegment „Test2“ und speichern Sie es erneut als „Test2“.
Beachten Sie, dass das Schnellsegment „Test1“ durch „Test2“ geändert wird.
