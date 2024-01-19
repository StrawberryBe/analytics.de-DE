---
description: So können Sie in Report Builder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.
title: Segmente verwalten (Report Builder)
feature: Report Builder
role: User, Admin
exl-id: c4ad89e0-91c9-47e1-a226-69d82fdb8918
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 74%

---

# Segmente verwalten

So können Sie in Report Builder Adobe Analytics-Segmente hinzufügen, bearbeiten, anwenden und filtern.

Report Builder bietet in Schritt 1 des Anforderungs-Assistenten einen Segmentierungsbereich, mit dem Sie Segmente erstellen und verwalten können.

![Screenshot mit den Segmentoptionen zum Hinzufügen, Bearbeiten oder Löschen von Segmenten und Hervorhebung der Symbole Kontrolle, Filter und Aktualisieren.](assets/seg_dialog.png)

## Hinzufügen oder Bearbeiten von Segmenten {#section_B2BC136F9A53498D90C7C2ECC5DB892B}

>[!NOTE]
>
>Um Segmente hinzuzufügen oder zu bearbeiten, wird über die Report Builder-Schnittstelle für Segmente in einem Microsoft Internet Explorer-Fenster der Analytics-Segment-Builder gestartet. Ihre Report Builder-Sitzung bleibt aktiv. Andere Browser (außer Internet Explorer) werden für diesen Vorgang nicht unterstützt.

1. Klicken Sie im Segmentfenster von Schritt 1 des Anforderungs-Assistenten auf **[!UICONTROL Hinzufügen]**.
1. Ein Internet Explorer-Fenster mit der Benutzeroberfläche des Analytics-Segment-Builder wird geöffnet. Informationen zum Erstellen von Segmenten finden Sie unter [Analytics-Segmentierung](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de).
1. Nachdem Sie das Segment definiert und gespeichert haben, gehen Sie zurück zum Anforderungs-Assistenten.
1. Klicken Sie auf das Aktualisierungssymbol, um die Segmentliste zu aktualisieren.

>[!IMPORTANT]
>
>Diese Liste wird zwischengespeichert und das neu erstellte Segment wird erst nach einer Aktualisierung angezeigt.

## Erstellen von kontextabhängigen Segmenten {#section_6DD2C663B2854469AA1075438F907678}

Möglicherweise verfügen Sie über bestimmte Kombinationen an Berichtsdimensionen, die Sie in ein Segment umwandeln möchten. Solche Segmente können Sie über die Report Builder-Schnittstelle erstellen. Wählen Sie zum Beispiel einige Seiten aus einer Seitenanforderungsausgabe aus und erstellen Sie auf Basis dieser Werte ein Segment.

1. Wählen Sie die Berichtausgabeelemente aus, die in ein Segment umgewandelt werden sollen.
1. Klicken Sie mit der rechten Maustaste, um **[!UICONTROL In-Context-Segment erstellen in]** auszuwählen und legen Sie den rechten Container fest (Container für Seitenaufrufe, Container für Besuche, Container für Besucher).

   ![Screenshot mit der Option In-Context-Segment erstellen in ausgewählten und verfügbaren Containeroptionen.](assets/seg_in_context.png)

   Weitere Informationen zu Containern finden Sie unter [Segmentierungsleitfaden](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de).

1. Die Segment-Builder-UI wird nun im Internet Explorer gestartet. Die Segment-Builder-UI wird mit dem von Ihnen festgelegten Container und Filter initialisiert.
1. Nachdem Sie dem Segment einen Namen und eine Beschreibung hinzugefügt haben, speichern Sie es.
1. Kehren Sie zu Report Builder zurück und klicken Sie auf das Symbol Aktualisieren , um die Segmentliste zu aktualisieren.
1. Nun können Sie dieses Segment anwenden.

## Segmente suchen und anwenden  {#search}

Alle Segmente, die in Reports &amp; Analytics (jetzt Ende der Unterstützung), Report Builder oder Data Warehouse erstellt wurden, werden in dieser Segmentliste angezeigt. Um die Liste zu aktualisieren, klicken Sie auf das Symbol Aktualisieren . ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg).

Sie können bei allen Anforderungen eines oder mehrere Segmente anwenden. Dies beinhaltet auch sequentielle Segmente.

1. Wechseln Sie in der Dropdown-Liste zu **[!UICONTROL Segment]** und klicken Sie im Feld **[!UICONTROL Segment auswählen]** auf den kleinen Pfeil nach unten, um alle Segmente anzuzeigen.

1. Aktivieren Sie die Segmente, die Sie anwenden möchten.

   ![Screenshot mit ausgewählten Segmenten.](assets/seg_list.png)

>[!NOTE]
>
>Unabhängig davon, ob Sie ein Administrator oder kein Administrator sind, können Sie im Report Builder nur die Segmente sehen, deren Inhaber Sie sind, sowie die Segmente, die für Sie freigegeben wurden.

## Filtern von Segmenten {#filter}

**Filter** Segmente durch Klicken auf das Filtersymbol:  ![Filtersymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg)

Folgende Filter stehen zur Verfügung:

| Filtername | Beschreibung |
|---|---|
| Tags | Filtern Sie Segmente mit bestimmten Tags. Beachten Sie, dass Tagfilter mit dem Operator AND arbeiten. Wenn Sie zwei Tags aktivieren, werden im rechten Fenster Segmente angezeigt, die mit **beiden** Tags versehen wurden. |
| Inhaber | Filtert Segmente nach Inhaber. Beachten Sie, dass Inhaberfilter mit dem Operator OR arbeiten. Wenn Sie zwei Inhaber aktivieren, werden im rechten Fenster Segmente angezeigt, die **beiden** Inhabern gehören. |
| Weitere Filter > Nur *Name der Report Suite* | Wenn Sie &quot;Nur *Name der Report Suite*&quot;im Segmentaufbau in Adobe Analytics und zeigen Sie dann den erweiterten Filter in [!DNL Report Builder], zeigt der erweiterte Filter nur das Segment für die ausgewählte Report Suite an. |
| Weitere Filter > Meine | Zeigt alle Segmente an, deren Inhaber Sie sind. |
| Weitere Filter > Für mich freigegeben | Es werden alle Segmente angezeigt, die für Sie freigegeben wurden. |
| Weitere Filter > Favoriten | Es werden alle Segmente angezeigt, die Sie als Favoriten markiert haben. |
| Weitere Filter > Genehmigt | Es werden alle offiziell genehmigten Segmente angezeigt. |

## Hinzufügen eines Segmentsteuerelements zu einer Arbeitsmappe {#segment-control}

Wenn Sie ein Segmentsteuerelement hinzufügen, können Sie innerhalb einer Arbeitsmappe zwischen Segmenten wechseln, anstatt hierfür zum Anforderungs-Assistenten wechseln zu müssen.

1. Klicken Sie auf das Symbol Kontrolle . ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) neben der Dropdown-Liste &quot;Segment&quot;.

1. Aktivieren Sie alle Segmente, die im Segmentsteuerelement angezeigt werden sollen oder aktivieren Sie **[!UICONTROL Alle auswählen]**.

   ![Screenshot des Dialogfelds &quot;Kontrolleinstellungen&quot;mit allen ausgewählten Einstellungen.](assets/seg_control.png)

1. Beachten Sie die Option **[!UICONTROL Verknüpfte Anforderungen bei Elementauswahl automatisch aktualisieren]**.

   * Wenn diese aktiviert ist, werden alle Anforderungen aktualisiert, die dieses Steuerelement verwenden.
   * Wenn sie nicht aktiviert ist, werden zwar die verknüpften Anforderungsparameter aktualisiert, jedoch nicht die Anforderungen selbst.

1. Legen Sie die Position für die obere linke Zelle des Steuerelements fest.

1. Klicken Sie auf **[!UICONTROL OK]**. Das Segmentsteuerelement wird an der angegebenen Position angezeigt.

   ![Screenshot mit dem Dropdown-Feld Segment auswählen .](assets/seg_control2.png)

## Segmentliste aktualisieren  {#refresh}

Jedes Mal, wenn Sie ein neues Segment hinzufügen oder ein vorhandenes bearbeiten, sollten Sie auf das Symbol Aktualisieren klicken ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) , um die zwischengespeicherte Segmentliste zu aktualisieren.

## Verwalten von Segmenten in mehreren Anfragen {#manage}

Vor der Version v5.4 konnten Benutzer in Report Builder Segmente in mehreren Anforderungen ändern. Bei diesem Vorgang wurden jeweils die bestehenden Segmente ersetzt. Benutzer, die ein neues Segment zu einer einzelnen Anforderung hinzufügen wollten, konnten dies nicht tun, da durch Hinzufügen des Segments vorherige Segmente entfernt wurden, die der jeweiligen Anforderung bereits zugeordnet waren.

In Report Builder 5.4 ist das Hinzufügen, Entfernen und Ersetzen einzelner oder aller Segmente innerhalb mehrerer Anforderungen zulässig:

1. Wählen Sie mehrere Anforderungen in einer Arbeitsmappe aus.
1. Klicken Sie mit der rechten Maustaste und wählen Sie **[!UICONTROL Anforderungen bearbeiten]** > **[!UICONTROL Nach Segment]** aus.

   ![Screenshot mit den Optionen Anforderungen bearbeiten und Nach Segment ausgewählt.](assets/edit_by_segment.png)

1. Wählen Sie im Dialog „Gruppe bearbeiten“ eine der folgenden vier Optionen aus:

   | Option | Beschreibung |
   |---|---|
   | Segment hinzufügen | Sie können eines oder mehrere Segmente auswählen und der Liste der aktuellen Segmente hinzufügen. |
   | Segment(e) ersetzen | Sie können auswählen, welche(s) Segment(e) Sie durch ein Segment bzw. mehrere Segmente ersetzen möchten. |
   | Alle Segmente ersetzen nach | Sie können eines oder mehrere Segmente auswählen und damit vorhandene Segmente ersetzen. |
   | Segment(e) entfernen | Sie können Segmente aus Anforderungen entfernen. |
