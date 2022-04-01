---
title: Ausschließen spezifischer Daten in der Analyse
description: Tipps zum Ausschließen von Datumsangaben oder Datumsbereichen, wenn Sie sie nicht in Berichte aufnehmen möchten.
exl-id: 744666c0-17f3-443b-9760-9c8568bec600
source-git-commit: d03206b127e16cbb98d1318b0acc6c304f91ca48
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 2%

---

# Ausschließen spezifischer Daten in der Analyse

Wenn Sie Daten haben [von einem Ereignis beeinflusst](overview.md)können Sie ein Segment verwenden, um alle Datumsbereiche auszuschließen, die Sie nicht in Ihre Berichte aufnehmen möchten. Die Segmentierung ereignisbetroffener Daten kann verhindern, dass Ihr Unternehmen Entscheidungen zu partiellen Daten trifft.

## Betroffene Tage isolieren {#isolate}

Erstellen Sie ein Segment, das den betroffenen Tag oder Datumsbereich isoliert. Dieses Segment ist nützlich, wenn Sie sich nur auf die Problemtage konzentrieren möchten, um mehr Informationen über die Auswirkungen zu erhalten.

1. Öffnen Sie den Segment Builder, indem Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Segmente]** Klicken Sie auf **[!UICONTROL Hinzufügen]**.
2. Ziehen Sie die Dimension &quot;Tag&quot;auf die Arbeitsfläche der Definition und legen Sie sie auf den Tag fest, den Sie isolieren möchten.
3. Wiederholen Sie den obigen Schritt für jeden Tag, den Sie in Ihrem Bericht isolieren möchten.

![Betroffenes Tagessegment](assets/affected_days.jpg)

>[!TIP]
>
>Um die Anweisung OR in eine AND-Anweisung zu ändern, klicken Sie auf den Pfeil nach unten neben OR und wählen Sie AND aus.

Adobe empfiehlt die Verwendung der orangefarbenen Dimensionskomponenten und nicht der lilafarbenen Datumsbereichskomponenten. Wenn Sie lilafarbene Datumsbereichskomponenten verwenden, überschreiben sie den Kalenderbereich des Projekts:

![Segmenttag ausschließen](assets/exclude_segment_day_type.jpg)

## Betroffene Tage ausschließen {#exclude}

Erstellen Sie ein Segment, das den betroffenen Tag oder Datumsbereich ausschließt. Dieses Segment ist nützlich, wenn Sie die Tage ausschließen möchten, an denen Probleme aufgetreten sind, um die Auswirkungen auf die Gesamtberichterstattung zu minimieren.

1. Öffnen Sie den Segment Builder, indem Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Segmente]** Klicken Sie auf **[!UICONTROL Hinzufügen]**.
2. Klicken Sie oben rechts auf der Arbeitsfläche für die Segmentdefinition auf **[!UICONTROL Optionen]** > **[!UICONTROL Ausschließen]**.
3. Ziehen Sie die Dimension &quot;Tag&quot;auf die Arbeitsfläche der Definition und legen Sie sie auf den Tag fest, den Sie entfernen möchten.
4. Wiederholen Sie den obigen Schritt für jeden Tag, den Sie in Ihrem Bericht entfernen möchten.

![Betroffene Tage ausschließen](assets/exclude_affected_days.jpg)

## Verwenden Sie diese Segmente in Berichten

Nachdem Sie das Ausschlusssegment erstellt haben, können Sie es genau so verwenden, wie Sie andere Segmente verwenden würden.

### Segmente in einem Trendbericht vergleichen {#compare}

Sie können sowohl das Segment &quot;Betroffene Tage&quot;als auch das Segment &quot;Betroffene Tage ausschließen&quot;in einem Bericht anwenden, um ihn nebeneinander zu vergleichen. Ziehen Sie beide Segmente über oder unter eine Metrik, um sie zu vergleichen:

![Beide Segmente](assets/affected_and_exclude.png)

Wenn Sie keine Nullen in Ihrer Tabelle oder Ihren Visualisierungen anzeigen möchten (wodurch Dips verursacht werden), aktivieren Sie **[!UICONTROL Null als keinen Wert auffassen]** unter Spalteneinstellungen.

![Null interpretieren](assets/interpret_zero.png)

Wenn Sie keine Nullen in Ihrer Tabelle oder Ihren Visualisierungen anzeigen möchten (wodurch Dips verursacht werden), aktivieren Sie **[!UICONTROL Null als keinen Wert auffassen]** unter Spalteneinstellungen.

![Null interpretieren](assets/interpret_zero.png)

### Anwenden des Ausschlusssegments auf ein Projekt {#apply}

Sie können das Segment &quot;Betroffene Tage ausschließen&quot;auf ein Workspace-Projekt anwenden. Ziehen Sie das Ausschlusssegment in den Arbeitsbereich-Arbeitsbereich mit der Bezeichnung *Segment hier ablegen*.

>[!TIP]
>
>Fügen Sie einen Hinweis zu ausgeschlossenen Daten in die Beschreibung des Bedienfelds ein, um denjenigen zu helfen, die den Bericht anzeigen. Klicken Sie mit der rechten Maustaste auf den Titel eines Bedienfelds und klicken Sie dann auf **[!UICONTROL Beschreibung bearbeiten]**.

![Auf ein Bedienfeld angewendetes Segment](assets/exclude_segment_panel.jpg)

### Verwenden des Ausschlusssegments in einer Virtual Report Suite {#use-vrs}

Sie können das Segment in einem [Virtual Report Suite](/help/components/vrs/vrs-about.md) um die Daten leichter auszuschließen. Diese Option ist optimal, da Sie nicht daran denken müssen, das Segment auf jeden Bericht anzuwenden, der den betroffenen Datumsbereich enthält. Wenn Sie Virtual Report Suites bereits als primäre Datenquelle verwenden, können Sie das Segment zu einer vorhandenen VRS hinzufügen.

1. Navigieren Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Virtual Report Suites]**.
2. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
3. Geben Sie den gewünschten Namen und die Beschreibung für die Virtual Report Suite ein.
4. Ziehen Sie das Ausschlusssegment in den Bereich mit der Bezeichnung **[!UICONTROL Segment hinzufügen]**.
5. Klicken **[!UICONTROL Weiter]** oben rechts und klicken Sie dann auf **[!UICONTROL Speichern]**.

![Auf VRS angewendetes Segment](assets/exclude_segment_vrs.png)
