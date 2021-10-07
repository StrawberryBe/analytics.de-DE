---
description: Verwenden Sie Schnellsegmente in Analysis Workspace.
title: Schnellsegmente
feature: Workspace Basics
role: User, Admin
source-git-commit: 533c58f3bcc3974dafab1d6b7dd3e239ad80831b
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%

---


# Schnellsegmente

Sie können innerhalb eines Projekts schnelle Segmente erstellen, um die Komplexität des vollständigen [Segment Builders](/help/components/segmentation/segmentation-workflow/seg-build.md) zu umgehen. Schnellsegmente

* Gilt nur für Projekte, in denen sie erstellt wurden (Sie können dies ändern).
* Für bis zu 3 Regeln.
* Sie dürfen keine verschachtelten Container oder sequenziellen Regeln aufnehmen.
* Arbeiten Sie in Projekten mit mehreren Report Suites.

Einen Vergleich dessen, was Schnellsegmente im Vergleich zu vollständigen Komponentensegmenten tun können, finden Sie unter [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

>[!IMPORTANT]
> Schnellsegmente werden derzeit nur eingeschränkt getestet und sind ab dem 21. Oktober 2021 allgemein verfügbar.

## Voraussetzungen

Jeder kann ein [!UICONTROL Schnellsegment] erstellen. Sie benötigen jedoch die Berechtigung [!UICONTROL Segmenterstellung] in [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=en#analytics-tools), um in der Lage zu sein, Schnellsegmente zu speichern oder sie im [!UICONTROL Segmentaufbau] zu öffnen.

## Schnellsegmente erstellen

Klicken Sie in einer Freiformtabelle auf das Symbol filter+ in der Bedienfeldüberschrift:

![](assets/quick-seg1.png)

Konfigurieren Sie das Schnellsegment aus dieser leeren Tabelle:

![leeres Schnellsegment](assets/qs-blank-slate.png)

| Einstellung | Beschreibung |
| --- | --- |
| Name | Der Standardname eines Segments ist eine Kombination der Regelnamen im Segment. Sie können das Segment umbenennen. |
| Ein-/Ausschließen | Sie können Komponenten in Ihrer Segmentdefinition entweder ein- oder ausschließen, aber nicht in beidem. |
| Treffer-/Besuchs-/Besucherbehälter | Schnellsegmente enthalten nur einen [Segmentcontainer](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=en#section_AF2A28BE92474DB386AE85743C71B2D6) , mit dem Sie eine Dimension/Metrik/einen Datumsbereich in das Segment einbeziehen (oder daraus ausschließen) können.  Besucher enthält übergreifende Daten, die für den Besucher über Besuche und Seitenansichten hinweg spezifisch sind. Mit einem [!UICONTROL Besuchsbehälter] können Sie Regeln festlegen, mit denen die Besucherdaten auf der Grundlage von Besuchen aufgeschlüsselt werden, und einen [!UICONTROL Trefferbehälter] , mit dem die Besucherinformationen auf der Grundlage einzelner Seitenansichten aufgeschlüsselt werden. Der Standardcontainer ist [!UICONTROL Hit]. |
| Komponenten (Dimension/Metrik/Datumsbereich) | Definieren Sie bis zu 3 Regeln, indem Sie Komponenten (Dimensionen und/oder Metriken und/oder Datumsbereiche) und deren Werte hinzufügen. Es gibt 3 Möglichkeiten, die richtige Komponente zu finden:<ul><li>Beginnen Sie mit der Eingabe und der [!UICONTROL Schnellsegment]-Builder findet automatisch die entsprechende Komponente.</li><li>Verwenden Sie die Dropdownliste, um die Komponente zu finden.</li><li>Ziehen Sie Komponenten per Drag-and-Drop aus der linken Leiste.</li></ul> |
| Operator | Verwenden Sie das Dropdown-Menü, um Standardoperatoren und [!UICONTROL Unique Count]-Operatoren zu finden. [Weitere Infos](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-operators.html?lang=en) |
| Pluszeichen (+) | Eine weitere Regel hinzufügen |
| UND/ODER-Kennzahlen | Sie können den Regeln &quot;AND&quot;- oder &quot;OR&quot;-Kennungen hinzufügen, aber Sie können &quot;AND&quot;und &quot;OR&quot;nicht in einer Segmentdefinition kombinieren. |
| Übernehmen | Wenden Sie dieses Segment auf das Bedienfeld an. Wenn das Segment keine Daten enthält, werden Sie gefragt, ob Sie fortfahren möchten. |
| Builder öffnen | Öffnet den Segment Builder. Nachdem Sie das Segment im Segmentaufbau gespeichert oder angewendet haben, wird es nicht mehr als &quot;Schnellsegment&quot;betrachtet. Sie wird Teil der Segmentbibliothek der Komponentenliste. |
| Abbrechen | Abbrechen dieses Schnellsegments - wenden Sie es nicht an. |
| Datumsbereich | Der Validator verwendet den Datumsbereich des Bedienfelds für die Datensuche. Jeder Datumsbereich, der in einem Schnellsegment angewendet wird, überschreibt jedoch den Datumsbereich des Bedienfelds oben im Bedienfeld. |
| Vorschau (oben rechts) | Hiermit können Sie sehen, ob Sie über ein gültiges Segment verfügen und wie breit das Segment ist. Stellt die Aufschlüsselung des Datensatzes dar, den Sie bei Anwendung dieses Segments erwarten können. Möglicherweise erhalten Sie einen Hinweis, der anzeigt, dass dieses Segment über keine Daten verfügt. In diesem Fall können Sie die Segmentdefinition fortsetzen oder ändern. |

Hier ist ein Beispiel für ein Segment, das Dimensionen und Metriken kombiniert:

![](assets/quick-seg2.png)

Das Segment wird oben angezeigt. Die Seitenleiste mit blauen Streifen unterscheidet sich von der blauen Seitenleiste für Segmente auf Komponentenebene in der Segmentbibliothek auf der linken Seite.

![](assets/quick-seg5.png)

## Schnellsegmente bearbeiten

1. Bewegen Sie den Mauszeiger über das Schnellsegment und wählen Sie das Stiftsymbol aus.
1. Bearbeiten Sie die Segmentdefinition und/oder den Segmentnamen.
1. Klicken Sie auf [!UICONTROL Übernehmen].

## Schnellsegmente speichern

>[!IMPORTANT]
>Nachdem Sie das Segment gespeichert oder angewendet haben, können Sie es nicht mehr im Quick Segment Builder bearbeiten, sondern nur noch im regulären Segment Builder.

1. Sobald Sie das Schnellsegment angewendet haben, halten Sie den Mauszeiger darüber und wählen Sie das Infosymbol (&quot;i&quot;) aus.

   ![](assets/quick-seg6.png)

1. Klicken Sie auf **[!UICONTROL Verfügbar machen für alle Projekte und fügen Sie Ihrer Komponentenliste]** hinzu.
1. (Optional) Benennen Sie das Segment um.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Beachten Sie, dass sich die Seitenleiste des Segments von gestreiftem Blau in Blau ändert. Er wird jetzt in der Komponentenliste in der linken Leiste angezeigt.

## Was sind reine Projektsegmente?

Nur-Projekt-Segmente sind entweder Schnellsegmente oder Ad-hoc-Workspace-Projektsegmente. Beim Bearbeiten/Öffnen in [!UICONTROL Segment Builder] wird das Feld &quot;Nur Projekt&quot;angezeigt. Wenn Sie ein kurzes Segment im Builder anwenden, aber das Kontrollkästchen &quot;Verfügbar machen&quot;nicht aktivieren, ist es weiterhin ein reines Projekt-Segment, kann jedoch nicht mehr im [!UICONTROL Quick Segment Builder] geöffnet werden.

![Nur Projekt deaktiviert](assets/project-only-unchecked.png)

Wenn Sie das Kontrollkästchen aktivieren und auf **[!UICONTROL SAVE]** klicken, handelt es sich jetzt um ein Komponentensegment.

![Nur Projekt aktiviert](assets/project-only-checked.png)
