---
description: So können Sie in ReportBuilder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.
seo-description: So können Sie in ReportBuilder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.
seo-title: Segmente verwalten
solution: Analytics
title: Segmente verwalten
topic: ReportBuilder
uuid: 4 e 4 edc 39-ed 93-498 f -913 d -7 b 231 b 10 e 7 a 0
translation-type: tm+mt
source-git-commit: d75c58caf1220031fa36483a0ad50ea6f7be7c39

---


# Segmente verwalten

So können Sie in ReportBuilder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.

Im Schritt 1 des Anforderungs-Assistenten von ReportBuilder gibt es ein Segmentierungsfenster, mit dem Sie folgende Aufgaben ausführen können: Segmente erstellen und verwalten.

![](assets/seg_dialog.png)

## Segmente hinzufügen oder bearbeiten {#section_B2BC136F9A53498D90C7C2ECC5DB892B}

>[!NOTE]
>
>Um Segmente hinzuzufügen oder zu bearbeiten, startet die Reportbuilder-Schnittstelle für die Berichterstellung den Analytics-Segment-Builder in einem Microsoft Internet Explorer-Fenster. Ihre ReportBuilder-Sitzung bleibt dabei aktiv. Andere Browser (außer Internet Explorer) werden für diesen Vorgang nicht unterstützt.

1. Klicken Sie im Segmentfenster von Schritt 1 des Anforderungs-Assistenten auf **[!UICONTROL Hinzufügen]**.
1. Ein Internet Explorer-Fenster mit der Benutzeroberfläche des Analytics-Segment-Builder wird geöffnet. Informationen zum Erstellen von Segmenten finden Sie unter [https://marketing.adobe.com/resources/help/de_DE/analytics/segment/](https://marketing.adobe.com/resources/help/en_US/analytics/segment/).
1. Nachdem Sie das Segment definiert und gespeichert haben, gehen Sie zurück zum Anforderungs-Assistenten.
1. Klicken Sie auf das Aktualisierungssymbol, um die Segmentliste zu aktualisieren.

>[!IMPORTANT]
>
>Diese Liste wird zwischengespeichert, und das neu erstellte Segment wird nur angezeigt, wenn Sie eine Aktualisierung vornehmen.

## In-Context-Segmente erstellen {#section_6DD2C663B2854469AA1075438F907678}

Möglicherweise verfügen Sie über bestimmte Kombinationen an Berichtsdimensionen, die Sie in ein Segment umwandeln möchten. Solche Segmente können Sie über die ReportBuilder-Schnittstelle erstellen. Wählen Sie zum Beispiel einige Seiten aus einer Seitenanforderungsausgabe aus und erstellen Sie auf Basis dieser Werte ein Segment.

1. Wählen Sie die Berichtausgabeelemente aus, die in ein Segment umgewandelt werden sollen.
1. Klicken Sie mit der rechten Maustaste, um **[!UICONTROL In-Context-Segment erstellen in]auszuwählen und legen Sie den rechten Container fest (Container für Seitenaufrufe, Container für Besuche, Container für Besucher).**

   ![](assets/seg_in_context.png)

   Weitere Informationen zu Containern finden Sie unter [Segmentierungsleitfaden](https://marketing.adobe.com/resources/help/en_US/analytics/segment/).

1. Die Segment-Builder-UI wird nun im Internet Explorer gestartet. Die Segment-Builder-UI wird mit dem von Ihnen festgelegten Container und Filter initialisiert.
1. Nachdem Sie dem Segment einen Namen und eine Beschreibung hinzugefügt haben, speichern Sie es.
1. Gehen Sie zurück zum ReportBuilder und klicken Sie auf das Aktualisierungssymbol, um die Segmentliste zu aktualisieren.
1. Nun können Sie dieses Segment anwenden.

## Segmente suchen und anwenden {#section_CACA269B48E94CFD91C2D5A15E9C77B7}

Alle Segmente, die in Reports &amp; Analysen, Ad-hoc-Analysen, ReportBuilder oder Data Warehouse erstellt wurden, werden in dieser Segmentliste angezeigt. Klicken Sie zum Aktualisieren der Liste auf das Aktualisierungssymbol ( ![](assets/refresh_icon.png).

Sie können bei allen Anforderungen eines oder mehrere Segmente anwenden. Dies beinhaltet auch sequentielle Segmente.

1. Go to the **[!UICONTROL Segment]** drop-down list and click the small down arrow in the **[!UICONTROL Choose Segment]**box to display all the segments.

   ![](assets/seg_list.png)

1. Aktivieren Sie die Segmente, die Sie anwenden möchten.

>[!NOTE]
>
>Unabhängig davon, ob Sie Administrator oder Nicht-Administrator sind, können Sie in Reportbuilder nur die Segmente sehen, deren Inhaber Sie sind, sowie diejenigen, die für Sie freigegeben wurden. (Auf der Benutzeroberfläche von Marketing Reports &amp; Analysen können Administratoren alle Segmente der Organisation anzeigen.)

## Segmente filtern {#section_376E986D3E684999A7CDB08E53854159}

**Filtern** Sie Segmente, indem Sie auf das Filtersymbol klicken: ![.](assets/segment_filter.png)

Folgende Filter stehen zur Verfügung:

| Filtername | Beschreibung |
|---|---|
| Tags | Filtern Sie Segmente mit bestimmten Tags. Beachten Sie, dass Tagfilter mit dem Operator UND arbeiten. Wenn Sie zwei Tags aktivieren, werden im rechten Fenster Segmente angezeigt, die mit **beiden** Tags versehen wurden. |
| Inhaber | Filtern Sie Segmente nach Inhaber. Beachten Sie, dass Inhaberfilter mit dem Operator ODER arbeiten. Wenn Sie zwei Inhaber aktivieren, werden im rechten Fenster Segmente angezeigt, die **beiden** Inhabern gehören. |
| Weitere Filter &gt; Nur *Name der Report Suite* | If you apply the "Only *report suite name*" filter in the Segment Builder in [!DNL marketing reports & analytics], and then display the Advanced Filter in [!DNL report builder], the Advanced filter will display the segment for the selected report suite only. |
| Weitere Filter &gt; Meine | Zeigt alle Segmente an, deren Inhaber Sie sind. |
| Weitere Filter &gt; Für mich freigegeben | Es werden alle Segmente angezeigt, die für Sie freigegeben wurden. |
| Weitere Filter &gt; Favoriten | Es werden alle Segmente angezeigt, die Sie als Favoriten markiert haben. |
| Weitere Filter &gt; Genehmigt | Es werden alle offiziell genehmigten Segmente angezeigt. |

## Segmentsteuerelement zu einer Arbeitsmappe hinzufügen {#section_E3E5149A8464441FA5445A98DBD520AC}

Wenn Sie ein Segmentsteuerelement hinzufügen, können Sie innerhalb einer Arbeitsmappe zwischen Segmenten wechseln, anstatt hierfür zum Anforderungs-Assistenten wechseln zu müssen.

1. Click the Control icon ( ![](assets/control_icon.png)) next to the segment drop-down.

   ![](assets/seg_control.png)

1. Aktivieren Sie alle Segmente, die im Segmentsteuerelement angezeigt werden sollen oder aktivieren Sie **[!UICONTROL Alle auswählen]**.
1. Beachten Sie die Option **[!UICONTROL Verknüpfte Anforderungen bei Elementauswahl automatisch aktualisieren]**.

   * Wenn diese aktiviert ist, werden alle Anforderungen aktualisiert, die dieses Steuerelement verwenden.
   * Wenn sie nicht aktiviert ist, werden zwar die verknüpften Anforderungsparameter aktualisiert, jedoch nicht die Anforderungen selbst.

1. Legen Sie die Position für die obere linke Zelle des Steuerelements fest.
1. Klicken Sie auf **[!UICONTROL OK]. Das Segmentsteuerelement wird an der angegebenen Position angezeigt.**

   ![](assets/seg_control2.png)

## Segmentliste aktualisieren {#section_22E4A86789444B4A998532396B476EFB}

Any time you add a new segment or edit an existing one, you should click the Refresh icon ( ![](assets/refresh_icon.png) to refresh the cached list of segments.

## Anforderungsübergreifende Verwaltung von Segmenten {#section_C3D63FCBE1A94369A319243313B03C93}

Vor der Version v5.4 konnten Benutzer in ReportBuilder Segmente in mehreren Anforderungen ändern. Bei diesem Vorgang wurden jeweils die bestehenden Segmente ersetzt. Benutzer, die ein neues Segment zu einer einzelnen Anforderung hinzufügen wollten, konnten dies nicht tun, da durch Hinzufügen des Segments vorherige Segmente entfernt wurden, die der jeweiligen Anforderung bereits zugeordnet waren.

In ReportBuilder 5.4 ist das Hinzufügen, Entfernen und Ersetzen einzelner oder aller Segmente innerhalb mehrerer Anforderungen zulässig:

1. Wählen Sie mehrere Anforderungen in einer Arbeitsmappe aus.
1. Right-click and select **[!UICONTROL Edit Requests]** &gt; **[!UICONTROL By Segment]**.

   ![](assets/edit_by_segment.png)

1. Wählen Sie im Dialog „Gruppe bearbeiten“ eine der folgenden vier Optionen aus:

   | Option | Beschreibung |
   |---|---|
   | Segment hinzufügen | Sie können eines oder mehrere Segmente auswählen und der Liste der aktuellen Segmente hinzufügen. |
   | Segment(e) ersetzen | Sie können auswählen, welche(s) Segment(e) Sie durch ein Segment bzw. mehrere Segmente ersetzen möchten. |
   | Alle Segmente ersetzen nach | Sie können eines oder mehrere Segmente auswählen und damit vorhandene Segmente ersetzen. |
   | Segment(e) entfernen | Sie können Segmente aus Anforderungen entfernen. |

