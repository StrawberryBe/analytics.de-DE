---
description: Schnellsegmente in Analysis Workspace verwenden
title: Schnellsegmente
feature: Segmentation
role: User, Admin
exl-id: 680e7772-10d3-4448-b5bf-def3bc3429d2
source-git-commit: d64f6687dd6e6f688d332926e6d90fa699cac968
workflow-type: ht
source-wordcount: '1153'
ht-degree: 100%

---

# Schnellsegmente

Schnellsegmente ermöglichen es Ihnen, Daten innerhalb eines Projekts einfach zu untersuchen, ohne ein komplexeres Komponentenlisten-Segment in [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) erstellen zu müssen.

Beachten Sie beim Erstellen von Schnellsegmenten Folgendes:

* Schnellsegmente gelten nur für das Projekt, in dem sie erstellt wurden. Sie sind nicht in anderen Projekten verfügbar und können nicht für andere Benutzende freigegeben werden. 
* Es sind maximal 3 Regeln zulässig.
* Verschachtelte Container oder sequenzielle Regeln werden nicht unterstützt.

Das folgende Video zeigt, wie Schnellsegmente verwendet werden:

>[!VIDEO](https://video.tv.adobe.com/v/341466/?quality=12&learn=on)

## Erstellen eines Schnellsegments

Alle Analysis Workspace-Benutzenden können ein Schnellsegment erstellen.

So erstellen Sie ein Schnellsegment:

1. Wählen Sie eine der folgenden Methoden, um ein Schnellsegment zu erstellen:

   * **Ad hoc (Drag-and-Drop):** Ziehen Sie eine Komponente aus der linken Leiste in den Ablagebereich neben dem Symbol **Segment** in der Bedienfeldüberschrift und wählen Sie dann das Symbol **Bearbeiten** aus, um das Segment anzupassen.

     ![Ad-hoc-Bearbeitung von Segmenten](assets/filter-adhoc-edit.png)

     >[!NOTE]
     >
     > Beachten Sie bei der Ad-hoc-Erstellung eines Schnellsegments (per Drag-and-Drop) Folgendes:
     > * Die folgenden Komponententypen werden nicht unterstützt: berechnete Metriken und Dimensionen sowie Metriken, aus denen Sie keine Segmente erstellen können.
     > * Bei vollständigen Dimensionen und Ereignissen erstellt Analysis Workspace Treffersegmente mit „vorhanden“. Beispiele: `Hit where eVar1 exists` oder `Hit where event1 exists`.
     > * Wenn „nicht angegeben“ oder „keine“ im Segmentablagebereich abgelegt wird, werden sie automatisch in ein Segment „nicht vorhanden“ umgewandelt, damit sie bei der Segmentierung korrekt gehandhabt werden.


   * **Verwenden des Segmentsymbols:** Wählen Sie in einer Freiformtabelle das Symbol **Segment** in der Bedienfeldüberschrift aus.

     ![Segmentfilter](assets/quick-seg1.png)

1. Passen Sie die folgenden Einstellungen an:

   | Einstellung | Beschreibung |
   | --- | --- |
   | [!UICONTROL Name] | Der Standardname eines Segments besteht aus der Kombination der Regelnamen im Segment. Sie können für das Segment einen benutzerfreundlicheren Namen wählen. |
   | [!UICONTROL Ein-/Ausschließen] | Sie können Komponenten in Ihrer Segmentdefinition entweder ein- oder ausschließen, aber nicht beides. |
   | [!UICONTROL Treffer-/Besuchs-/Besucher-Container] | Schnellsegmente enthalten nur einen [Segment-Container](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=de#section_AF2A28BE92474DB386AE85743C71B2D6), mit dem Sie eine Dimension/eine Metrik/einen Datumsbereich in das Segment einbeziehen (oder daraus ausschließen) können. [!UICONTROL Besucher] enthält für den Besucher spezifische übergreifende Daten zu allen Besuchen und Seitenansichten. Mit dem Container [!UICONTROL Besuch] können Sie Regeln für die Aufschlüsselung der Besucherdaten auf der Grundlage der Besuche festlegen und mit dem Container [!UICONTROL Treffer] können Sie die Besucherinformationen anhand der einzelnen Seitenaufrufe aufschlüsseln. Der Standard-Container ist [!UICONTROL Treffer]. |
   | [!UICONTROL Komponenten] (Dimension/Metrik/Datumsbereich) | Definieren Sie bis zu 3 Regeln, indem Sie Komponenten (Dimensionen, Metriken, Datumsbereiche oder Dimensionswerte) hinzufügen. Es gibt 3 Möglichkeiten, die richtige Komponente zu finden:<ul><li>Beginnen Sie mit der Eingabe. Der Schnellsegment-Builder findet automatisch die entsprechende Komponente.</li><li>Verwenden Sie die Dropdown-Liste, um die Komponente zu finden.</li><li>Per Drag-and-Drop aus der der linken Leiste ziehen.</li></ul> |
   | [!UICONTROL Operator] | Verwenden Sie das Dropdown-Menü, um Standardoperatoren und Operatoren des Typs [!UICONTROL Distinct Count] zu finden. Siehe [Segmentoperatoren](/help/components/segmentation/seg-reference/seg-operators.md). |
   | Plus (+)-Zeichen | Eine weitere Regel hinzufügen |
   | AND/OR-Kennzeichung | Sie können den Regeln „AND“ oder „OR“ hinzufügen, aber Sie können „AND“ und „OR“ aber nicht in einer Segmentdefinition kombinieren. |
   | [!UICONTROL Anwenden] | Wenden Sie dieses Segment auf das Bedienfeld an. Wenn das Segment keine Daten enthält, werden Sie gefragt, ob Sie fortfahren möchten. |
   | [!UICONTROL Builder öffnen] | Öffnet Segment Builder. Nachdem Sie das Segment in Segment Builder gespeichert oder übernommen haben, ist es kein „Schnellsegment“ mehr. Es wird Teil der Segmentbibliothek der Komponentenliste. <p>Um die Komponente für alle Projekte und in der linken Leiste verfügbar zu machen, wählen Sie die Option [!UICONTROL **Dieses Segment für alle Projekte verfügbar machen und der Komponentenliste hinzufügen**] aus.</p><p>Weitere Informationen finden Sie in diesem Artikel unter [Speichern eines Schnellsegments als Komponentenlisten-Segment](#save-a-quick-segment-as-a-component-list-segment).</p><p>**Hinweis:** Nur Benutzende mit der Berechtigung „Segmenterstellung“ in der [Adobe Admin Console](/help/admin/admin-console/permissions/analytics-tools.md) können Segment Builder öffnen.</p> |
   | [!UICONTROL Abbrechen] | Verwirft das entsprechende Schnellsegment. Es wird nicht angewendet. |
   | [!UICONTROL Datumsbereich] | Der Validator verwendet den Datumsbereich des Panels für die Datensuche. Doch jeder in einem Schnellsegment angewendete Datumsbereich überschreibt den Datumsbereich des Panels im oberen Bereich des Panels. |
   | Vorschau (oben rechts) | Ermöglicht festzustellen, ob ein gültiges Segment vorhanden ist und wie groß es ist. Stellt eine Aufschlüsselung des Datensatzes dar, der bei der Anwendung dieses Segments zu erwarten ist. Möglicherweise erhalten Sie den Hinweis, dass dieses Segment über keine Daten verfügt. In diesem Fall können Sie weiterarbeiten oder aber die Segmentdefinition ändern. |

1. Wählen Sie [!UICONTROL **Übernehmen**] aus, um Ihre Änderungen zu speichern.

## Schnellsegmente bearbeiten

1. Bewegen Sie den Mauszeiger über das Schnellsegment und wählen Sie das Symbol **Bearbeiten** aus.

   ![Ad-hoc-Bearbeitung von Filtern](assets/filter-adhoc-edit.png)

1. Bearbeiten Sie die Segmentdefinition und/oder den Segmentnamen.

1. Wählen Sie [!UICONTROL **Anwenden**] aus.

## Speichern eines Schnellsegments als Komponentenlisten-Segment

>[!IMPORTANT]
>
> Beachten Sie beim Speichern eines Schnellsegments Folgendes:
> 
> * Um ein Schnellsegment zu speichern, benötigen Sie die Berechtigung „Segmenterstellung“ in der [Adobe Admin Console](/help/admin/admin-console/permissions/analytics-tools.md).
> 
> * Nachdem Sie das Segment gespeichert oder angewendet haben, kann es nicht mehr im Schnellsegment-Builder bearbeitet werden. Stattdessen müssen Sie den standardmäßigen Segment Builder verwenden.

Sie können Schnellsegmente als Komponentenlisten-Segmente speichern. Zu den Vorteilen von Komponentenlisten-Segmenten gehören:

* Verfügbarkeit über alle Arbeitsbereich-Projekte hinweg
* Unterstützung komplexerer Segmente sowie sequenzieller Segmente

Sie können Segmente entweder über den Schnellsegment-Builder oder über den [!UICONTROL Filter-Builder] speichern.

### Speichern im Schnellsegment-Builder {#save2}

1. Nachdem Sie das Schnellsegment angewendet haben, bewegen Sie den Mauszeiger darüber und wählen Sie das Infosymbol („i“) aus.
1. Wählen Sie **[!UICONTROL Für alle Projekte verfügbar machen und Ihrer Komponentenliste hinzufügen]** aus.
1. Optional: Benennen Sie das Segment um.
1. Wählen Sie **[!UICONTROL Speichern]** aus.

   Das Segment wird nun in der Komponentenliste in der linken Leiste angezeigt. Außerdem ändert sich die Seitenleiste des Segments von hellblau in dunkelblau. Dies bedeutet, dass das Segment nicht mehr im Schnellsegment-Builder bearbeitet oder geöffnet werden kann.

### Speichern im Segment Builder {#save3}

1. Nachdem Sie das Schnellsegment angewendet haben, bewegen Sie den Mauszeiger darüber und wählen Sie das Infosymbol („i“) aus.
1. Wählen Sie **[!UICONTROL Segment speichern]** aus.
1. (Optional) Benennen Sie das Segment um und wählen Sie [!UICONTROL **Anwenden**] aus.

   Gehen Sie zurück zum Arbeitsbereich. Sie werden bemerken, dass sich die Seitenleiste des Segments von hellblau in dunkelblau ändert. Das bedeutet, dass das Segment nicht mehr im Schnellsegment-Builder bearbeitet oder geöffnet werden kann. Und durch Speichern wird es Teil der Komponentenliste.

Nachdem Sie das Segment angewendet haben, können Sie es Ihrer Liste der Segmentkomponenten hinzufügen und für alle Ihre Projekte verfügbar machen.

1. Bewegen Sie den Mauszeiger über das gespeicherte Segment und wählen Sie das Stiftsymbol aus.

1. Wählen Sie [!UICONTROL **Builder öffnen**] aus.

1. Oben in Segment Builder ist das Dialogfeld für projektbasierte Segmente [!UICONTROL ****] zu sehen:

   ![Dialogfeld für projektbasierte Segmente](assets/project-only-segment-dialog.png)

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Für alle Projekte verfügbar machen und Ihrer Komponentenliste hinzufügen]**.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

   Das Segment wird jetzt in der Liste der Segmentkomponenten für alle Ihre Projekte angezeigt.
Sie können das Segment auch für andere Personen in Ihrer Organisation [freigeben](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de#concept_4A9726927E7C44AFA260E2BB2721AFC6).

## Beispiel für ein Schnellsegment

In dem folgenden Beispiel für ein Segment werden Dimensionen und Metriken kombiniert:

![](assets/quick-seg2.png)

## Bekanntes Problem

1. Erstellen Sie ein Schnellsegment mit zwei Einträgen und **[!UICONTROL speichern]** Sie es als „Test1“.
1. Klicken Sie auf **[!UICONTROL Speichern unter]** und speichern Sie dieses Schnellsegment als „Test2“.
1. Bearbeiten Sie das Schnellsegment „Test2“ und speichern Sie es erneut als „Test2“.
Beachten Sie, dass das Schnellsegment „Test1“ durch „Test2“ geändert wird.
