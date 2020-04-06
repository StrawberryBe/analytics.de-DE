---
description: So können Sie in Report Builder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.
title: Segmente verwalten
topic: Report builder
uuid: 4e4edc39-ed93-498f-913d-7b231b10e7a0
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Segmente verwalten

So können Sie in Report Builder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.

Im Schritt 1 des Anforderungs-Assistenten von Report Builder gibt es ein Segmentierungsfenster, mit dem Sie folgende Aufgaben ausführen können: Segmente erstellen und verwalten.

![](assets/seg_dialog.png)

## Segmente hinzufügen oder bearbeiten {#section_B2BC136F9A53498D90C7C2ECC5DB892B}

>[!NOTE] Um Segmente hinzuzufügen oder zu bearbeiten, wird über die Report Builder-Schnittstelle für Segmente in einem Microsoft Internet Explorer-Fenster der Analytics-Segment-Builder gestartet. Ihre ReportBuilder-Sitzung bleibt aktiv. Andere Browser als Internet Explorer werden für diesen Vorgang nicht unterstützt.

1. Klicken Sie im Segmentfenster von Schritt 1 des Anforderungs-Assistenten auf **[!UICONTROL Add]**.
1. Ein Internet Explorer-Fenster wird geöffnet, in dem die Benutzeroberfläche des Analytics-Segmentaufbaus geöffnet wird. Informationen zum Erstellen von Segmenten finden Sie unter [https://marketing.adobe.com/resources/help/en_US/analytics/segment/](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/).
1. Nachdem Sie das Segment definiert und gespeichert haben, gehen Sie zurück zum Anforderungs-Assistenten.
1. Klicken Sie auf das Symbol Aktualisieren, um die Segmentdatei zu aktualisieren.

>[!IMPORTANT]
>
>Diese Liste wird zwischengespeichert und das neu erstellte Segment wird erst nach einer Aktualisierung angezeigt.

## In-Context-Segmente erstellen {#section_6DD2C663B2854469AA1075438F907678}

Möglicherweise verfügen Sie über bestimmte Kombinationen an Berichtsdimensionen, die Sie in ein Segment umwandeln möchten. Solche Segmente können Sie über die Report Builder-Schnittstelle erstellen. Wählen Sie beispielsweise einige Seiten aus der Ausgabe einer Seitenanfrage aus und erstellen Sie ein Segment, das auf diesen Werten basiert.

1. Wählen Sie die Berichtausgabeelemente aus, die Sie in ein Segment umwandeln möchten.
1. Right-click to select **[!UICONTROL Create In-Context Segment in]** and specify the right container (Hits Container, Visits Container, Visitor Container).

   ![](assets/seg_in_context.png)

   Weitere Informationen zu Containern finden Sie im [Segmentierungshandbuch](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/).

1. Die Segment Builder-Benutzeroberfläche wird jetzt in Internet Explorer gestartet. Die Segment Builder-Benutzeroberfläche wird mit dem angegebenen Container und Filter initialisiert.
1. Nachdem Sie dem Segment einen Namen und eine Beschreibung hinzugefügt haben, speichern Sie es.
1. Gehen Sie zurück zum ReportBuilder und klicken Sie auf das Symbol Aktualisieren, um die Liste der Segmente zu aktualisieren.
1. Sie können dieses Segment jetzt anwenden.

## Segmente suchen und anwenden {#section_CACA269B48E94CFD91C2D5A15E9C77B7}

Alle Segmente, die in Reports &amp; Analytics, Ad Hoc Analysis, Report Builder oder Data Warehouse erstellt wurden, werden in dieser Segmentliste angezeigt. Klicken Sie zum Aktualisieren der Liste auf das Aktualisierungssymbol ![](assets/refresh_icon.png).

Sie können bei allen Anforderungen eines oder mehrere Segmente anwenden. Dies umfasst sequenzielle Segmente.

1. Go to the **[!UICONTROL Segment]** drop-down list and click the small down arrow in the **[!UICONTROL Choose Segment]** box to display all the segments.

   ![](assets/seg_list.png)

1. Aktivieren Sie die Segmente, die Sie anwenden möchten.

>[!NOTE] Unabhängig davon, ob Sie ein Benutzer mit oder ohne Administratorrechten sind, können Sie in Report Builder nur die Segmente anzeigen, die Ihnen gehören und die für Sie freigegeben wurden. (Auf der Benutzeroberfläche von Marketing Reports &amp; Analytics können Administratoren alle Segmente der Organisation anzeigen.)

## Segmente filtern {#section_376E986D3E684999A7CDB08E53854159}

**Filtern** Sie Segmente, indem Sie auf das Filtersymbol klicken: ![](assets/segment_filter.png).

Zu den verfügbaren Filtern gehören:

| Filtername | Beschreibung |
|---|---|
| Tags | Filtert Segmente nach bestimmten Tags. Beachten Sie, dass Tag-Filter den Operator AND verwenden. Wenn Sie zwei Tags aktivieren, werden im rechten Bereich Segmente angezeigt, die mit **beiden** Tags versehen wurden. |
| Eigentümer | Filtert Segmente nach Inhaber. Beachten Sie, dass Filter des Inhabers den Operator OR verwenden. Wenn Sie zwei Inhaber aktivieren, werden im rechten Bereich Segmente angezeigt, die **beiden** Inhabern gehören. |
| Andere Filter > Nur *Report Suite-Name* | Wenn Sie im Segment Builder in [!DNL marketing reports & analytics] den Filter „Nur *Name der Report Suite*“ anwenden und dann in [!DNL report builder] den erweiterten Filter anzeigen, zeigt der erweiterte Filter nur das Segment für die ausgewählte Report Suite an. |
| Weitere Filter > Meine | Zeigt alle Segmente an, deren Inhaber Sie sind. |
| Weitere Filter > Für mich freigegeben | Zeigt alle Segmente an, die andere für Sie freigegeben haben. |
| Weitere Filter > Favoriten | Zeigt alle Segmente an, die Sie als Favoriten gekennzeichnet haben. |
| Weitere Filter > Genehmigt | Zeigt alle offiziell genehmigten Segmente an. |

## Segmentsteuerelement zu einer Arbeitsmappe hinzufügen {#section_E3E5149A8464441FA5445A98DBD520AC}

Wenn Sie ein Segmentsteuerelement hinzufügen, können Sie innerhalb einer Arbeitsmappe zwischen Segmenten wechseln, anstatt hierfür zum Anforderungs-Assistenten wechseln zu müssen.

1. Klicken Sie neben dem Dropdown-Menü für Segmente auf das Steuerelementsymbol (![](assets/control_icon.png)).

   ![](assets/seg_control.png)

1. Markieren Sie alle Segmente, die im Segmentsteuerelement angezeigt werden sollen, oder aktivieren Sie **[!UICONTROL Select All]**.
1. Beachten Sie die Option **[!UICONTROL Automatically refresh linked requests upon item selection]**.

   * Wenn diese Option aktiviert ist, werden alle Anforderungen, die dieses Steuerelement verwenden, aktualisiert.
   * Wenn diese Option nicht aktiviert ist, werden die zugehörigen Anforderungsparameter aktualisiert, die Anforderungen werden jedoch nicht aktualisiert.

1. Geben Sie die Position der Zelle oben links im Segmentsteuerelement an.
1. Klicken Sie auf **[!UICONTROL OK]** und das Segmentsteuerelement wird an der angegebenen Position angezeigt.

   ![](assets/seg_control2.png)

## Segmentliste aktualisieren {#section_22E4A86789444B4A998532396B476EFB}

Jedes Mal, wenn Sie ein neues Segment hinzufügen oder ein vorhandenes bearbeiten, sollten Sie auf das Aktualisierungssymbol (![](assets/refresh_icon.png)) klicken, um die zwischengespeicherte Segmentliste zu aktualisieren.

## Anforderungsübergreifende Verwaltung von Segmenten {#section_C3D63FCBE1A94369A319243313B03C93}

Vor der Version v5.4 konnten Benutzer in Report Builder Segmente in mehreren Anforderungen ändern. Dieser Prozess hat jedoch immer die vorhandenen Segmente ersetzt. Benutzer, die jeder Anforderung ein neues Segment hinzufügen wollten, konnten dies nicht tun, da durch Hinzufügen des Segments der vorherige Satz von Segmenten entfernt wurde, der jeder Anforderung bereits zugewiesen war.

In Report Builder 5.4 ist das Hinzufügen, Entfernen und Ersetzen einzelner oder aller Segmente innerhalb mehrerer Anforderungen zulässig:

1. Wählen Sie mehrere Anforderungen in einer Arbeitsmappe aus.
1. Klicken Sie mit der rechten Maustaste und wählen Sie **[!UICONTROL Edit Requests]** > **[!UICONTROL By Segment]**.

   ![](assets/edit_by_segment.png)

1. Wählen Sie im Dialogfeld &quot;Gruppe bearbeiten&quot;eine der vier Optionen aus:

   | Option | Beschreibung |
   |---|---|
   | Fügen Sie Segment | Ermöglicht die Auswahl eines oder mehrerer Segmente, die zur Liste der aktuellen Segmente hinzugefügt werden sollen. |
   | Segment(e) ersetzen | Ermöglicht die Auswahl des/der Segmente, die durch ein oder mehrere Segmente ersetzt werden sollen. |
   | Alle Segmente ersetzen durch | Ermöglicht die Auswahl eines oder mehrerer Segmente, um das aktuelle Segment/die aktuellen Segmente zu ersetzen. |
   | Segment(e) entfernen | Ermöglicht das Entfernen von Segmenten aus den Anforderungen. |

