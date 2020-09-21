---
description: Sie können das Segment für Marketingaktivitäten in der Zielgruppenbibliothek, in der Target-Komponente und im Audience Manager verwenden.
title: Veröffentlichen von Segmenten in Experience Cloud
topic: Segments
uuid: e5ce20c0-ce43-423b-a29f-ba66e9e24d27
translation-type: tm+mt
source-git-commit: 82cf5ddfd4d18af09c2dbedba20514e4b643a94b
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 100%

---


# Veröffentlichen von Segmenten in Experience Cloud

Durch das Veröffentlichen eines Adobe Analytics-Segments in Experience Cloud können Sie das Segment für die Marketing-Aktivität in [!DNL Audience Manager] und in anderen Aktivierungskanälen verwenden, einschließlich [!DNL Advertising Cloud], [!DNL Target] und [!DNL Campaign] von Adobe. Die neuesten Updates haben den Publishing-Workflow erheblich optimiert. Sie können Analytics-Segmente jetzt in weniger als 8 Stunden in Experience Cloud veröffentlichen. Verwenden Sie diese Segmente, um Zielgruppen-Manager in Audience Manager für alle nachfolgenden Ziele zu aktivieren.

Außerdem haben wir die maximale Anzahl an publizierbaren Adobe Analytics-Segmenten von 20 auf 75 erhöht. Sie können veröffentlichte Segmente unter [!UICONTROL Analytics > Komponenten > Segmente] anzeigen.

>[!NOTE]
>
>Adobe Campaign (Classic und Standard) verhält sich anders, da es zusätzlich zur 8-Stunden-Latenz eine 24-Stunden-Latenz gibt.


## Voraussetzungen

* Stellen Sie sicher, dass die Report Suite, in der Sie dieses Segment speichern, [für die Experience Cloud aktiviert](https://docs.adobe.com/content/help/de-DE/core-services/interface/audiences/t-publish-audience-segment.html) ist. Andernfalls können Sie sie nicht in der Experience Cloud veröffentlichen.
* Vergewissern Sie sich, dass Sie an einer Report Suite arbeiten, die [Ihrer Experience Cloud-Organisation zugeordnet](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html) ist.
* Stellen Sie sicher, dass Ihre Organisation Experience Cloud IDs verwendet.
* Bevor Sie Segmente veröffentlichen können, muss Ihr Administrator einem Produktprofil die Berechtigung für die [!UICONTROL Segmentveröffentlichung] in der [Admin Console](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html) zuweisen und Sie zum Produktprofil hinzufügen.


## Zu beachten

* **Report Suite-Beschränkungen**: Sie können bis zu 75 Segmente pro Report Suite veröffentlichen. Diese Beschränkung wird erzwungen. Wenn Sie bereits 75 Segmente veröffentlicht haben, können Sie keine weiteren Segmente veröffentlichen, bis Sie die Veröffentlichung für genügend Segmente aufheben, um unter den Schwellenwert von 75 Segmenten zu gelangen.
* **Mitgliedschaftsbeschränkungen**: Zielgruppen, die von [!DNL Experience Cloud] und Adobe Analytics gemeinsam verwendet werden, dürfen nicht mehr als 20 Millionen eindeutige Mitglieder umfassen.
* **Datenschutz**: Zielgruppen werden nicht nach dem Authentifizierungsstatus der Besucher gefiltert. Wenn Besucher Ihre Site sowohl authentifiziert als auch nicht authentifiziert anzeigen können, kann eine Aktion, die ein nicht authentifizierter Benutzer durchführt, dennoch dazu führen, dass der Besucher in die Zielgruppe aufgenommen wird. Lesen Sie sich die [Adobe Experience Cloud-Datenschutzbestimmungen](https://www.adobe.com/de/privacy/experience-cloud.html) durch, um die Auswirkungen der gemeinsamen Nutzung von Zielgruppen auf den Datenschutz zu verstehen.
* Eine Diskussion über die **Unterschiede zwischen Segmenten in [!DNL Adobe Analytics] und [!DNL Audience Manager]** finden Sie [hier](https://docs.adobe.com/content/help/de-DE/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html).

## Timeline für die Segmentveröffentlichung

| Was ist verfügbar? | Wann ist es verfügbar? | Wo ist es verfügbar? |
|---|---|---|
| Metadaten (Segmenttitel und Definition) | Sofort nach der Veröffentlichung | [!DNL Audience Manager], [!UICONTROL Experience Cloud-Zielgruppenbibliothek], [!DNL Target] |
| Verwendbares Segment mit Mitgliedschaft | ~ 8 Stunden nach der Veröffentlichung | Besucherprofil-Betrachter in [!DNL Audience Manager] |
| Eigenschaften- und Mitgliedspopulation | Nach 24–48 Stunden | [!DNL Audience Manager] |

>[!NOTE]
>Einmal pro Woche werden alle Daten vollständig synchronisiert, um alle Unterschiede (Deltas) und Diskrepanzen zu berücksichtigen, die in der Vorwoche nicht erfasst wurden.

## Veröffentlichen von Segmenten im [!UICONTROL Segment Builder]

1. Navigieren Sie zu **[!UICONTROL Analytics > Workspace > Komponenten > Segmente]> +**
1. Erstellen Sie ein Segment im [!UICONTROL Segment Builder].
1. Geben Sie einen Titel und eine Beschreibung für das Segment ein. Andernfalls können Sie es nicht speichern.
1. Aktivieren Sie die Option **[!UICONTROL Dieses Segment in Experience Cloud veröffentlichen (für *Report Suite*)]**.

![](assets/publish-ec.png)

>[!IMPORTANT]
>Stellen Sie sicher, dass Sie „Besucher mit Experience Cloud ID“ verwenden, wenn Sie Segmentvorschauen in Analytics anstelle der Segmentvorschau „Unique Visitors“ insgesamt betrachten, wenn Sie Adobe Analytics-Zahlen mit Audience Manager-Zahlen vergleichen:
>
>![](assets/seg-vis-ecid.png)

| Element | Beschreibung |
|---|---|
| **[!UICONTROL Dieses Segment in Experience Cloud veröffentlichen (für *`<report suite>`*)]** | Wenn diese Option aktiviert ist, werden der Segmenttitel und die Definition (d. h. die Shell-Zielgruppe, wie sie häufig in Anzeigenplattformen verwendet wird) sofort für die Experience Cloud freigegeben, während die Segmentmitgliedschaft ausgewertet und alle 4 Stunden freigegeben wird. <br> Wenn die Zielgruppe einer Aktivität beispielsweise in [!DNL Target] zugewiesen wird, beginnt [!DNL Analytics] damit, IDs für Besucher zu senden, die sich für diese Experience Cloud- und [!DNL Target]-Zielgruppe qualifizieren. Ab diesem Zeitpunkt werden der Zielgruppenname und die zugehörigen Daten auf der Experience Cloud Audiences-Seite angezeigt. </br> |
| **[!UICONTROL Fenster für die Zielgruppenerstellung]** | Der von Ihnen ausgewählte Zeitrahmen wird verwendet, um die Zielgruppe in einem fortlaufenden Kalender zu erstellen. „Letzte 30 Tage“ (Standard) bezieht zum Beispiel Besucher ein, die sich in den letzten 30 Tagen ab dem heutigen Datum für die Zielgruppe qualifiziert haben (NICHT ab dem ursprünglichen Datum, an dem das Segment erstellt wurde). |
| **[!UICONTROL In Zielgruppenbibliothek erstellen]** | Die Segmente, die Sie erstellen und veröffentlichen, können in der Experience Cloud-Zielgruppenbibliothek ohne Latenz zur Verfügung gestellt werden. Sie sind nicht von Analytics-Aktualisierungen abhängig. Diese Segmente werden nicht Ihrer Beschränkung auf 75 veröffentlichte Segmente angerechnet. |
| **[!UICONTROL x von 75 veröffentlicht]** | Zeigt die Anzahl der Segmente an, die Sie in Experience Cloud veröffentlicht haben. Klicken Sie auf den Link, um eine Liste der veröffentlichten Segmente mit zugehöriger Report Suite und Eigentümer anzuzeigen. |
| **[!UICONTROL Speichern]** | Speichert dieses Segment. |

## Rückgängigmachen der Veröffentlichung oder Löschen von Segmenten

Um ein in Experience Cloud veröffentlichtes Segment zu löschen, müssen Sie zuerst die Veröffentlichung rückgängig machen. Um die Veröffentlichung eines Segments rückgängig zu machen, **deaktivieren** Sie einfach das Kontrollkästchen, das Sie zum Veröffentlichen aktiviert haben.

>[!NOTE]
>
>Sie können die Veröffentlichung eines Segments **nicht** rückgängig machen, das aktuell von einer der folgenden Adobe-Lösungen verwendet wird: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (für Kunden von [!DNL Core Service] und [!DNL Audience Manager]) und alle anderen externen Partner (für Kunden von [!DNL Audience Manager]). Die Veröffentlichung eines Segments, das von [!DNL Target] verwendet wird, **kann** rückgängig gemacht werden.

## Anzeigen des Segmentveröffentlichungsstatus im [!UICONTROL Segment-Manager]

1. Navigieren Sie zu [!UICONTROL Analytics > Komponenten > Segmente].
1. Beachten Sie die neue Spalte [!UICONTROL Veröffentlicht]. „Ja“/„Nein“ bezieht sich darauf, ob das Segment in der Experience Cloud veröffentlicht wurde oder nicht.

![](assets/publish-status.png)

## Abrufen der [!DNL Audience Manager]-UUID

Es gibt zwei Möglichkeiten, die AAM-UUID zu erfassen, die derzeit mit dem Browser verknüpft ist:

* Adobe Experience Cloud-Debugger
* Natives Entwicklertool in Browsern (z. B. Chrome Developer Tools)

Die folgenden Screenshots zeigen Ihnen, wie Sie die AAM-UUID in Ihrem Browser abrufen und sie im Audience Manager-Besucherprofil-Betrachter verwenden, um Eigenschaften- und Segmentmitgliedschaften zu validieren.

**Methode 1: Verwenden des Adobe Experience Cloud-Debuggers**

1. Laden Sie den [Adobe Experience Cloud-Debugger](https://docs.adobe.com/content/help/de-DE/analytics/implementation/validate/debugger.html) im Chrome-Webstore herunter und installieren Sie ihn.
1. Starten Sie den Debugger beim Laden einer Seite.
1. Blättern Sie zum Audience Manager-Abschnitt und suchen Sie die AAM-UUID, die auf der aktuellen Browserseite eingestellt ist (`50814298273775797762943354787774730612` im Beispiel unten).

![](assets/debugger.jpg)

**Methode 2: Verwenden von Chrome Developer Tools (oder anderen Browser-Entwicklertools)**

1. Starten Sie Chrome Developer Tools vor dem Laden einer Seite.
1. Laden Sie die Seite und aktivieren Sie „Anwendungen“ > „Cookies“. Die AAM-UUID sollte im Drittanbieter-Demdex-Cookie ([adobe.demdex.net](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/reference/demdex-calls.html) im Beispiel unten) festgelegt sein. Das Feld „demdex“ ist die AAM-UUID-Einstellung im Browser (`50814298273775797762943354787774730612` im Beispiel unten).

![Chrome Developer Tools](assets/ggogle-uuid.png)

## Verwenden des Audience Manager-[!UICONTROL Besucherprofil-Betrachters]

Die AAM-UUID im Browser wird standardmäßig verwendet, wenn der [!UICONTROL Besucherprofil-Betrachter] geladen wird. Wenn Sie Eigenschaftsrealisierungen für andere Benutzer überprüfen, geben Sie eine UUID in das Feld „UUID“ ein und klicken Sie auf [!UICONTROL Aktualisieren]. Weitere Informationen finden Sie unter [Besucherprofil-Betrachter](https://docs.adobe.com/content/help/de-DE/audience-manager/user-guide/features/visitor-profile-viewer.html).

![](assets/aam-vpv.png)

## Anzeigen von Segmenteigenschaften in [!DNL Audience Manager]

In AAM wird die Liste der Besucher mit ECIDs für ein bestimmtes Segment in Form von Streaming ausgewertet, da Analytics Segmente mit Experience Cloud teilt.

1. Gehen Sie in [!DNL Audience Manager] zu [!UICONTROL Zielgruppendaten > Eigenschaften > Analytics-Eigenschaften]. Es wird ein Ordner für jede Analytics Report Suite angezeigt, die mit Ihrer Experience Cloud-Organisation verknüpft ist. Diese Ordner (für Eigenschaften, Segmente und Data Sources) werden erstellt, wenn der Hauptdienst Profile und Zielgruppen/Personen initiiert oder bereitstellt.
1. Wählen Sie den Ordner für die Report Suite aus, in der Sie zuvor das Segment erstellt haben, das Sie für [!DNL Audience Manager] freigeben möchten. Sie sehen das Segment/die Zielgruppe, das/die Sie erstellt haben. Wenn Sie ein Segment freigeben, geschehen in [!DNL Audience Manager] zwei Dinge:
* Eine Eigenschaft wird erstellt, zunächst ohne Daten. Ca. 8 Stunden nach der Veröffentlichung des Segments in [!DNL Analytics] wird die Liste der ECIDs für [!DNL Audience Manager] und andere Experience Cloud-Lösungen integriert und freigegeben.

![](assets/aam-traits.png)

* Es wird ein Segment mit einer Eigenschaft erstellt. Es verwendet die Datenquelle, die mit der Report Suite verknüpft ist, in der Sie das Segment veröffentlicht haben.
* Die Eigenschaft läuft nun nach 16 Tagen ab (zuvor waren es 2 Tage).

## Anzeigen des Segments in [!DNL Adobe Target]

Wenn das Kontrollkästchen [!UICONTROL Dieses Segment in Experience Cloud veröffentlichen] während der Segmenterstellung in Adobe Analytics aktiviert wird, ist das Segment in der benutzerdefinierten Zielgruppenbibliothek von Adobe Target verfügbar. Ein in Analytics oder Audience Manager erstelltes Segment kann für Aktivitäten in Target verwendet werden. Sie können zum Beispiel Kampagnenaktivitäten basierend auf Analytics-Konversionsmetriken und in Analytics erstellten Zielgruppensegmenten erstellen.

1. Klicken Sie auf [!UICONTROL Zielgruppen].
1. Suchen Sie auf der Seite [!UICONTROL Zielgruppen] die aus der [!DNL Experience Cloud] stammende Zielgruppe. Diese Zielgruppen sind für [!DNL Target]-Aktivitäten verfügbar.
