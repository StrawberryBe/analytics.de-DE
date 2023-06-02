---
description: Erfahren Sie mehr über die verschiedenen Segmentierungscontainer und deren Verwendung
keywords: Segmentierung;Segmente
title: Segment-Container
feature: Segmentation
exl-id: f30d525b-32b7-47d5-b92d-24bf86d8a471
source-git-commit: 5a9ba3f9749338c181fbcdc311bd08a92144e698
workflow-type: tm+mt
source-wordcount: '3469'
ht-degree: 54%

---


# Segment-Container

Ein Segment legt Bedingungen für die Filterung eines Besuchers auf der Grundlage der Attribute oder Interaktionen des Besuchers mit Ihrer Site fest. Um in einem Segment Bedingungen festzulegen, legen Sie Regeln für die Filterung von Besuchern auf der Grundlage von Besuchermerkmalen und/oder Navigationsverhalten fest. Um die Besucherdaten weiter herunterzubrechen, können Sie jeden Besucher auf der Grundlage bestimmter Besuche und/oder Seitenansichten filtern. Segment Builder bietet eine einfache Architektur zum Erstellen dieser Untergruppen und das Anwenden von Regeln als verschachtelte hierarchische Container der Form Besucher, Besuch oder Treffer.

Die im Segment Builder verwendete Behälterarchitektur definiert

- ![Besucher](https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg) **[!UICONTROL Besucher]** als äußersten Behälter, der übergreifende Daten enthält, die für den Besucher über Besuche und Seitenansichten hinweg spezifisch sind.
- ![Besuch](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg) verschachtelt **[!UICONTROL Besuch]** -Container können Sie Regeln festlegen, mit denen die Besucherdaten auf der Grundlage von Besuchen aufgeschlüsselt werden, und
- ![Ereignis](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg) verschachtelt **[!UICONTROL Treffer]** -Container können Sie die Besucherinformationen auf der Grundlage einzelner Seitenansichten aufschlüsseln.

Jeder Container ermöglicht Berichte über den Verlauf eines Besuchers, nach Besuch aufgeschlüsselte Interaktionen oder aufgeschlüsselte einzelne Treffer.

<table style="table-layout: fixed; border: none;">

<tr>
<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<!--![](assets/sequential_segmentation_container_hierarchy.png)-->

Im Folgenden finden Sie eine Videoübersicht über die Segment-Container:

>[!VIDEO](https://video.tv.adobe.com/v/25401/?quality=12)

## Besuchercontainer

Der Besucher-Container enthält sämtliche Besuche und Seitenansichten für Besucher innerhalb eines bestimmten Zeitraums. Ein Segment auf der Besucherebene gibt die Seite zurück, die die Bedingung erfüllt, sowie alle anderen Seiten, die vom Besucher angesehen wurden (und dies nur durch definierte Datumsbereiche beschränkt). Da es sich um den am weitesten definierten Container handelt, geben Berichte, die auf Besucherbehälterebene generiert werden, Seitenansichten über alle Besuche hinweg zurück und ermöglichen Ihnen die Erstellung einer Analyse mehrerer Besuche. Daher ist der Besucherbehälter am wahrscheinlichsten, dass er sich basierend auf definierten Datumsbereichen ändert.

Besucher-Container können Werte enthalten, die auf dem Gesamtverlauf eines Besuchers basieren:

- Tage bis Erstkauf
- Ursprüngliche Einstiegsseite
- Ursprünglich Referrerdomänen

## Container Besuch

Mit dem Besuchs-Container können Seiteninteraktionen, Kampagnen oder Konversionen für eine bestimmte Websitzung identifiziert werden. Ein Segment auf Besuchsebene gibt die Seite zurück, die die Bedingung erfüllt, sowie alle anderen Seiten, die im Rahmen der Besuchssitzung angezeigt wurden (und nur durch definierte Datumsbereiche eingeschränkt). Der Besuchebehälter ist der am häufigsten verwendete Behälter, da er das Verhalten für die gesamte Besuchssitzung erfasst, sobald die Regel erfüllt ist. Mit dem Besuchebehälter können Sie definieren, welche Besuche beim Erstellen und Anwenden eines Segments ein- oder ausgeschlossen werden sollen. Er kann Ihnen bei der Beantwortung der Frage helfen, wie viele Besucher bei demselben Besuch den Bereich „News und Sport“ angesehen haben. Oder welche Seiten zu einer erfolgreichen Konversion zum Kauf beigetragen haben.

Besuchs-Container enthalten Werte, die auf dem Auftreten pro Besuch basieren:

- Besuchsnummer
- Einstiegsseite
- Rückkehrhäufigkeit
- Beitragsmetriken
- Linear zugeordnete Metriken

## Treffercontainer

Der Treffer-Container definiert, welche Seitenbesuche von einem Segment einbezogen oder ausgeschlossen werden sollen. Der Trefferbehälter ist der engste der verfügbaren Container, mit dem Sie bestimmte Klicks und Seitenansichten identifizieren können, bei denen eine Bedingung wahr ist. Sie können einen einzelnen Trackingcode anzeigen oder das Verhalten innerhalb eines bestimmten Bereichs Ihrer Site isolieren. Sie können auch einen bestimmten Wert erkennen, wenn eine Aktion stattfindet, z. B. den Marketing-Kanal, wenn ein Auftrag platziert wurde.

Treffer-Container enthalten Werte, die auf den Aufschlüsselungen einzelner Seiten basieren:

- Produkte
- Listen-Props
- Listen-eVars
- Merchandising eVars (im Kontext von Ereignissen)

   >[!NOTE]
   >
   >Wenn Sie diesen Container für einen persistenten Wert verwenden, z. B. eine eVar, ruft er jeden Treffer ab, bei dem dieser Wert beibehalten wird. Wenn ein Trackingcode vorhanden ist, der nach einer Woche abläuft, kann dieser Wert über mehrere Besuche hinweg persistent sein.

## Logischer Gruppen-Container

Mit dem logischen Gruppen-Container können Sie einen separaten Container innerhalb der Segmentregeln bereitstellen, um Entitäten zu filtern, die nicht hierarchiebasiert sind. Beispielsweise können Sie einen Container bereitstellen, der innerhalb des Segments verschachtelt ist, das besucherbasiert filtert. Für diesen Logiktyp müssen Sie die Hierarchie unterbrechen (da Sie bereits einen Besucherbehälter der obersten Ebene verwendet haben), um nur nach ausgewählten Besuchern zu filtern. Siehe [Beispiele für logische Gruppen](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md) für weitere Informationen.

## Verschachteln von Containern {#nest-containers}

Wenn Sie Segment-Container innerhalb anderer Container erstellen, erstellen Sie im Grunde ein Segment in einem Segment. Bei verschachtelten Containern wird die folgende Logik angewendet:

1. Bestimmen, welche Daten enthalten sind, indem der äußerste Container verwendet wird. Alle Daten, die nicht mit dieser äußeren Regel übereinstimmen, werden aus dem Segmentbericht ausgeschlossen.
1. Anwenden der verschachtelten Regel auf die verbleibenden Daten. Die verschachtelte Regel gilt NICHT für Treffer, die die erste Regel abgewiesen hat.
1. Wiederholen, bis alle verschachtelten Container-Regeln berechnet wurden. Die verbleibenden Daten werden dann in den resultierenden Bericht einbezogen.

Sie können die Verschachtelung zwischen Behältern und zwischen Regeln innerhalb eines Containers verwenden. Folgende Elemente können in jedem Container verschachtelt werden:

| Container-Name | Was darin verschachtelt werden kann |
|---|---|
| Treffer | Nur Ereignisse |
| Besuch | Treffer-Container, Ereignisse |
| Besucher. | Besuchs-Container, Treffer-Container, Ereignisse |
| logische Gruppe | Besucher-Container, Besuchs-Container, Treffer-Container |

### Mehrere Container in eine einzelne Definition einbeziehen

Indem Sie mehrere Segmente in ein neues verbundenes Segment einbeziehen, können Sie Ihre Daten sogar noch weiter verfeinern. Das Zusammenziehen von zwei vorhandenen Segmenten agiert beim Filtern der Besucher als OR-Anweisung. Alle Container auf der Arbeitsfläche werden gegen alle Daten geprüft und alle Daten, die mit einem der Container übereinstimmen, werden in den Bericht einbezogen.

Wenn Sie z. B. einen Besuchs-Container, in dem gilt „Land = Vereinigte Staaten“ mit einem Besuchs-Container zusammenziehen, in dem „Auftrag = Wahr“ ist,,

```
Country = United States + Order = True
```

erstellt ein Segment, das sich in dieser Reihenfolge verhält:

1. Dieses Segment bezieht sich zunächst auf Ihre gesamten Daten und identifiziert alle Besucher in den Vereinigten Staaten.
2. Das Segment betrachtete dann alle Ihre Daten erneut und suchte danach, ob Besucher eine Bestellung aufgegeben hatten.
3. Beide Datensätze werden dann auf den Bericht angewendet.

## Container für sequenzielle Segmente {#containers-sequential}

Die sequenzielle Segmentierung verwendet dieselben grundlegenden Container wie [!UICONTROL Besucher], [!UICONTROL Besuche] und [!UICONTROL Treffer] (einschließlich Seitenansichten oder andere Dimensionen) hierarchisch verschachtelt.

<table style="table-layout:fixed; border: none;">

<tr>
<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<!--![](assets/nesting_container.png)-->

[!UICONTROL Besucher] stellen den Container mit dem höchsten Rang in der sequenziellen Segmentierung dar. Dabei sind [!UICONTROL Besuche] im [!UICONTROL Besucher-Container] und [!UICONTROL Treffer] in den [!UICONTROL Besucher]- oder [!UICONTROL Besuchs-Containern] enthalten. Diese [Container-Hierarchie](/help/components/segmentation/seg-overview.md#section_7FDF47B3C6A94C38AE40D3559AFFAF70) muss eingehalten werden, um ordnungsgemäß sortierte sequenzielle Segmente zu erstellen.

**So erstellen Sie sequenzielle Segmente**, werden Behälter verschachtelt und die sequenzielle Logik wird mithilfe der [!UICONTROL THEN] -Operator, für den jeder Container erforderlich ist `true` basierend auf der Sequenz des Besuchers.

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DANN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<!--![](assets/sequential_segmentation_nesting_3.png)-->

Die einzige Ausnahme für diese Container-Hierarchie besteht in der Verwendung des [Logischer Gruppen-Container](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md). Mit dem [!UICONTROL logischen Gruppen-Container] können Sie einen Treffer innerhalb eines Containers ohne spezielle Reihenfolge verschachteln, um Ereignisse und Dimensionen zu erfassen, jedoch außerhalb einer sequenziellen Reihenfolge.

<table style="table-layout:fixed; border: none;">

<tr>
<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DANN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Group_18_N.svg"/> Gruppe</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

</table>

<!--![](assets/logic_group_hierarchy.png)-->

## Auf Containerdaten basierende Berichte {#reports}

Mit Containern können Sie unterschiedliche Daten auf der Grundlage von Berichtswerten unterschiedlich filtern, wenn Segmente aufgeschlüsselt und auf Berichte angewendet werden.

Daten, die auf den einzelnen Ebenen der Hierarchie der Container Besucher > Besuch > Treffer erfasst werden, beeinflussen, wie Sie Ihre Segmente erstellen. Wenn Sie dasselbe Segment mit demselben Datensatz auf denselben Bericht anwenden, erhalten Sie unterschiedliche Werte, die auf dem Container basieren, aus dem Sie den Bericht generieren. Faktoren wie die Behälterberichtsebene und die Persistenz von Werten über Treffer hinweg können erhebliche Änderungen an Ihrer Berichtsgenauigkeit bedeuten.

### Grundlagen der Containerdaten {#container-data}

Beispiel: Der unten dargestellte Besucher hat eine Site zum ersten Mal besucht, kam auf der Homepage an und hat dann drei weitere Seiten besucht und aus dem Besuch einen Kauf gemacht. Bei einem anderen Besuch landete der Besucher auf der Produktseite, wechselte dann zur Homepage, zurück zur Produktseite und schloss die Sitzung dann ab, nachdem er sich Wintermützen angesehen hat. Basierend auf den für jeden Behälter für das Segment erfassten Daten werden im Bericht unterschiedliche Werte angezeigt.

Die `Pages equals Winter Coat` Segment unten wird auf die **Seitenbericht**.


Basierend auf dem ausgewählten Container zeigt der Bericht unterschiedliche Ergebnisse für die folgenden Besuche und Seitenansichten eines Besuchers an.

<table style="table-layout:auto; border: 0;">

<tr>
<td style="background-color: #E5E4E2;"></td>
<td style="background-color: #E5E4E2;" colspan="4"><b>Besuch 1</b></td>
</tr>
<tr>
<tr>
<td style="background-color: #E5E4E2;">
<img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/>
</td>
<td style="background-color: #FFFFFF; "><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Startseite </td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Wintermantel</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Kauf: 100 $</td>
</tr>
<tr>
<td colspan="5">
</tr>
<tr>
<td style="background-color: #E5E4E2;"></td>
<td style="background-color: #E5E4E2;"colspan="4"><b>Besuch 2</b></td>
</tr>
<tr>
<tr style="border: 0;">

<td style="background-color: #E5E4E2;">
<img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/>
</td>
<td style="background-color: #FFFFFF; "><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterstiefel</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Winterhaufen</td>

</table>


<!--![](assets/container_overview.png)-->

### Berichte aus dem Treffer-Container

Wenn sich diese Bedingung in einem Treffer-Container befindet, listet der Bericht nur Seiten auf, für die *Seite = Wintermäntel* wahr ist. Da nur eine Seite diese Bedingung in einem Container mit nur einer Seite erfüllt, wird nur die Wintermäntel-Seite angezeigt.

| Seite | Seitenansichten |
|---|--:|
| Wintermantel | 1 |

<!--![](assets/container_overview_PV.png)-->

Die Berichterstellung aus dem Trefferbehälter zeigt, wie sich die Berichterstellung aus verschiedenen Behältern auf die Berichtswerte insgesamt auswirkt. Beachten Sie beim Anzeigen des Segmentberichts, dass die Seitenansichten ungefähr den Besuchen entsprechen (rund 2.000 Besucher haben bei einem Besuch doppelte Seiten gesehen, was zur Gesamtzahl der Seitenansichten addiert wird). Und Unique Visitors entsprechen ungefähr der Anzahl der Besuche (etwa 2.000 Unique Visitors haben mehr als einmal besucht).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **69.252** von 351.292 <br/>**67.554** von 165.175 <br/>**63.541** von 113.169 | **19%**<br/>**40%**<br/>**56%** |


<!--![](assets/container_report_PV.png)-->

>[!IMPORTANT]
>
>Unabhängig davon, wie Sie die Daten anzeigen (aus den Treffer-, Besuchs- oder Besucherbehältern), weisen sie in diesem Beispiel alle dieselbe Anzahl von 63.541 Besuchern auf. Unabhängig davon, wie Sie den Bericht generieren, bleibt die ursprüngliche Besucherbedingung (Besucher, die die Wintermäntel-Seite angesehen haben) intakt. Dies ist die Teilmenge der Daten, mit denen Sie auf den verschiedenen Ebenen Berichte erstellen.

### Berichte aus dem Besuchecontainer

Wenn sich dieselbe Bedingung in einem Besuchs-Container befindet, listet der Bericht alle Seiten des Besuchs auf, für die *Seite gleich Wintermäntel* wahr ist. Sie filtert die Wintermäntel-Seite, erfasst aber auch alle anderen Seiten des Besuchs, bei denen die Bedingung wahr ist. Da der Besucher während des Besuchs auch die Seiten &quot;Home&quot;, &quot;Product&quot;und &quot;Purchase&quot;besucht hat, werden diese zusätzlichen Seiten im Bericht aufgeführt, wenn die Berichte Besuchercontainerdaten verwenden.

| Seite | Seitenansichten |
|---|--:|
| Startseite  | 1 |
| Produkt | 1 |
| Wintermantel | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_visit.png)-->

In den Segmentwerten aus dem Besuchs-Container sehen Sie, dass die Anzahl der Seitenansichten signifikant gestiegen ist. Dieser Anstieg liegt daran, dass die Berichterstellung aus dem Besuchebehälter alle Seiten identifiziert, die die Bedingungen erfüllen, sowie alle anderen beim Besuch angezeigten Seiten (mit allen Seitenansichten, die in jedem Besuchebehälter erfasst werden).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **226.193** von 351.292 <br/>**67.554** von 165.175 <br/>**63.541** von 113.169 | **64%**<br/>**40%**<br/>**56%** |

<!--![](assets/container_report_Visit.png)-->

### Berichte aus dem Besuchercontainer

Wenn sich dieselbe Bedingung in einem Besucher-Container befindet, listet der Bericht alle von einem Besucher angesehenen Seiten auf, für die *Seite gleich Wintermäntel* wahr ist. Diese Bedingung bedeutet, dass, wenn ein Besucher die Wintermäntel-Seite angesehen hat, alle Seiten im Besucherbehälter aufgelistet sind (einschließlich Seitenansichten bei anderen Besuchen). Daher werden Seiten, die nicht mit der Bedingung übereinstimmen, auch im Bericht aufgeführt, da der Besucher sie zu einem früheren Zeitpunkt angezeigt hat. Alle Seiten im Besucherbehälter werden im Bericht aufgelistet, selbst wenn sie zuvor aufgetreten sind und die Bedingungen nicht speziell erfüllen.

| Besuch 1<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Wintermantel | 1 |
| Kauf | 1 |

| Besuch 2<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Winterkleidung | 2 |
| Winterstiefel | 1 |
| Winterhaufen | 1 |

| Besuch 1 + Besuch 2<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Winterkleidung | 3 |
| Startseite  | 1 |
| Wintermantel | 1 |
| Kauf | 1 |
| Winterstiefel | 1 |
| Winterhaufen | 1 |

<!--![](assets/container_overview_visitors.png)-->

Beim Anzeigen von Segmenten aus dem Besucher-Container können Sie sehen, dass die Seitenansichten und die Besuche angestiegen sind. Dieser Anstieg liegt daran, dass, wenn der Besucher die Wintermäntel-Seite nur einmal besucht hat (wodurch die Bedingung wahr ist), alle anderen Seitenansichten und alle anderen Besuche, die für diesen Besucher erfasst wurden.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **240.094** von 351.292 <br/>**83.823** von 165.175 <br/>**63.541** von 113.169 | **68%**<br/>**50%**<br/>**56%** |

<!--![](assets/container_report_Visitor.png)-->

Zusammenfassend wird deutlich, dass das Wissen darüber, wie die Segmentierung bei unterschiedlichen Aufschlüsselungen von Daten funktioniert, bei der Interpretation der gelieferten Daten von entscheidender Bedeutung ist.

## Auf dem Container basierende Berichte {#reporting}

Jede Aufschlüsselung von Segmentdaten hat einen Umfang, auf den diese angewendet wird. Die meisten Aufschlüsselungen basieren auf *Seitenansichten*, wobei jedoch viele wertvolle Segmente auf dem *Besuchecontainer* und in geringerem Umfang auf dem *Besuchercontainer* basieren. Es ist wichtig, dass Sie wissen, wie Berichte funktionieren, die auf dem Umfang Ihres Containers basieren.

Verwenden der `Page equals Winter Coats` Segmentbeispiel unten sind Beispiele für die Ergebnisse dieses Segments, die darauf basieren, wie die Behälterdaten angewendet werden und wie der Umfang der Daten mit dem Segmenttyp übereinstimmt.

### Auf übereinstimmender Segmentregel basierender Segment-Container

Das Anwenden des Segment-Containers auf einen normalen Datenbereich bringt die erwarteten Ergebnisse, in denen die Linienelemente mit der Segmentregel übereinstimmen.

- **Treffer-Container, bei dem Seite gleich „Wintermantel“**: Ein *Seitenbericht* mit diesem Segment liefert nur die Werte, die mit „Wintermantel“ übereinstimmen. Alle anderen Seiten werden aus dem Bericht ausgeschlossen.
- **Besuchs-Container, bei dem Einstiegsseite gleich „Winterkleidung“**: Ein *Einstiegsseiten*-Bericht mit diesem Segment liefert nur den zweiten Besuch, weil dessen Einstiegsseite mit der Segmentregel übereinstimmt.
- **Besuchs-Container, bei dem Besuchsnummer gleich 1**: Alle Seitenansichten des ersten Besuchs sind im Bericht enthalten, weil er mit der Segmentregel übereinstimmt.

### Seitenansichten auf der Besuchs-Container-Ebene

Viele Segmentregeln identifizieren Seitenansichten pro Besuch. Wenn diese Identifizierung erfolgt, wird der gesamte Besucherbehälter angewendet, wenn nur ein einzelner Treffer mit der Regel übereinstimmt. Dieser Segmentbericht ist besonders wertvoll, weil auf Besuchen basierende Seitenansichten Einblick auf der Grundlage von Seitenansichten pro Besuch liefern.

- **Besuchs-Container, bei dem Seite gleich Seite „Wintermantel“**: In einem Seitenbericht auf der Besucher-Container-Ebene werden alle Seitenansichten gezeigt, die eine Ansicht der Seite „Winterkleidung“ enthalten. Wenn eine Seite mit der Segmentregel übereinstimmt, werden alle dem Besuch zugeordneten Seitenansichten in den Bericht aufgenommen.
- **Besuchebehälter, bei dem Seite gleich &quot;Startseite&quot;ist**: In einem Seitenbericht mit diesem Segment werden nur Daten aus dem ersten Besuch angezeigt, da der Besucher beim zweiten Besuch keine &quot;Homepage&quot;angezeigt hat.
- **Besucher-Container, bei dem Seite gleich „Winterkleidung“**: In einem Seitenbericht ruft dieses Segment alle Daten beider Besuche ab, da der Besucher die Seite „Winterkleidung“ gesehen hat.

### Segment-Container, der Treffer identifiziert, die kleiner als Seitenansichten sind

Die Verwendung des Segments mit einem Container, der kleiner als der Aufschlüsselungsbereich ist, liefert überraschende Daten. Bei Verwendung einer kleineren Aufschlüsselung werden weiterhin alle Treffer aus dem Datenbereich einbezogen.

- **Treffer-Container, bei dem Einstiegsseite gleich „Produkt“**: Alle Seiten sind mit der Einstiegsseite des Besuchs verknüpft, wodurch eine besuchsbasierte Aufschlüsselung erfolgt. Bei Verwendung dieses Segments wird nicht nur die Entrypage &quot;Produktseite&quot;abgerufen, sondern auch alle Treffer in diesem Besuch.
- **Treffer-Container, bei dem Listenvariable 1 WertA enthält**: Wenn mehrere Werte für denselben Treffer als Listenvariablen definiert sind, werden alle Variablenwerte in das Segment einbezogen. Es ist nicht möglich, Werte zu separieren, die in derselben Seitenansicht auftreten, da der Treffer-Container der kleinste Segment-Container für das Aufschlüsseln von Treffern ist.
- **Treffer-Container, bei dem Seite gleich „Kauf“**: Bei der Verwendung von Seitenansichten als Metrik wird nur die Kaufseite angezeigt (erwartungsgemäß). Bei Verwendung eines Berichts über den Beitrag am Umsatz erhalten alle Seiten im ersten Besuch 100 $, da Beitragsmetriken besuchsbasiert sind.
- **Treffer-Container, bei dem Seite gleich „Wintermantel“**: Bei der Verwendung von Seitenansichten als Metrik wird nur die Wintermantel-Seite angezeigt (erwartungsgemäß). Bei Verwendung eines Berichts über den Beitrag am Umsatz erhält keine Seite eine Gutschrift, da für diese Dimension eine persistente Dimension erforderlich ist. Die Seitenansicht, auf der der Kauf tatsächlich stattfand (die Kaufseite) ist nicht im Treffer-Container enthalten, weshalb kein Element einen Umsatzbeitrag erhält. Bei einem über den Besuchs-Container ausgeführten Bericht wären jedoch alle Seitenansichten dieses Besuchs enthalten und der Umsatzbeitrag (100 $) würde über alle in der Sitzung gesehenen Seiten verteilt.

## Persistenz über Container hinweg {#persistence}

Die Filterung nach Dimensionen, die über einen Seitenbereich hinweg bestehen bleiben, wie z. B. eine Campaign-eVar oder eine Referrer-Dimension, wirkt sich auf die auf Behälterebene erfassten Daten aus und muss für die Genauigkeit der Berichterstellung verstanden werden.

Segmentdaten können, basierend auf der Persistenz einer Dimension oder einer angewendeten Variablen, über ausgewählte Seiten hinweg variieren. Einige Dimensionen, z. B. die Seitendimension, bieten auf Seitenebene eindeutige Werte und werden auf der Grundlage von Daten aus dem Treffer-Container gefiltert. (Siehe als Beispiel [Auf Container-Daten basierende Berichte](/help/components/segmentation/seg-overview.md)). Andere Dimensionen, z. B. die Dimension „Referrerdomäne“, sind für einen Besuch über mehrere Seiten hinweg persistent. Zum Beispiel: `Referring Domain equals aol.com`. Einige Dimensionen oder angewendete Variablen, z. B. die Besuchsdauer, erstrecken sich über den gesamten Verlauf des Besuchers.

<!--![](assets/RefDomain_aol.png)-->

Im Gegensatz zur Seitendimension ist der Wert „Referrerdomäne“ an jede Seite in diesem Besuch angehängt. Im Beispiel unten kommt der Besucher von einer verweisenden Site auf der Homepage an. Daher wird allen Seiten innerhalb dieses Besuchs derselbe Wert für die Referrer-Domäne zugewiesen.

Die `Referring Domain equals aol.com` Segment unten wird auf die **Seitenbericht**.

<table style="table-layout:fixed; border: 0;">

<tr>
<td style="background-color: #E5E4E2;"></td>
<td style="background-color: #E5E4E2;" colspan="4"><b>Besuch 1</b></td>
</tr>
<tr>
<tr>
<td style="background-color: #E5E4E2;">
<img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/><br/>aol.com
</td>
<td style="background-color: #FFFFFF; "><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Startseite </td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Wintermantel</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Kauf: 100 $</td>
</tr>
<tr>
<td colspan="5">
</tr>
<tr>
<td style="background-color: #E5E4E2;"></td>
<td style="background-color: #E5E4E2;"colspan="4"><b>Besuch 2</b></td>
</tr>
<tr>
<tr style="border: 0;">

<td style="background-color: #E5E4E2;">
<img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/><br/>weather.com
</td>
<td style="background-color: #FFFFFF; "><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterstiefel</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterkleidung</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Winterhaufen</td>

</table>

<!--![](assets/container_overview_persist.png)-->

Bei einem neuen Besuch wird der Besucher von einer anderen Website verwiesen. Daher wird allen Seiten im neuen Besuch der neue Wert für die Referrer-Domäne für jede Seitenansicht zugewiesen.

### Berichte aus dem Treffer-Container

Da allen Seitenansichten innerhalb desselben Besuchs derselbe Wert für die Referrerdomäne zugewiesen wird, erfolgt die Berichterstellung auf Ebene des Trefferbehälters , wobei `Referring Domain equsls 'aol.com'` gibt alle in der folgenden Tabelle aufgeführten Seiten zurück.

| Referrerdomäne gleich &quot;aol.com&quot; | Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Wintermantel | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_persist_Visit.png)-->

Bei der Anzeige der Daten aus dem Treffer-Container, wurden über 92.000 Seitenansichten bei über 33.000 Besuchen durch nur etwas mehr als 32.000 Besucher erzeugt. Im Durchschnitt fielen bei jedem Besuch drei Seitenansichten an und nahezu sämtliche Besuche betrafen Unique Visitors.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **98.234** von 351.165 <br/>**33.203** von 165.173 <br/>**32.269** von 113.110 | **27%**<br/>**20%**<br/>**28%** |

<!--![](assets/container_report_persist_PV.png)-->

### Berichte aus dem Besuchecontainer

Wenn dieselbe Bedingung im Besuchebehälter für einen Seitenbericht gefiltert wird, dann werden alle Seiten im Besuch, auf denen `Referring Domain equals 'aol.com'`ist wahr. Da der Wert der Referrerdomäne auf der Besuchsebene festgelegt wird, sind Berichte auf Seitenansichts- und Besuchsebene identisch.

| Referrerdomäne gleich &quot;aol.com&quot; | Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Wintermantel | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_persist_Visit.png)-->

Da alle Seiten basierend auf dem Besuch denselben Wert für die Referrer-Domäne haben, ist der Bericht auf Besuchebehälterebene (fast) mit dem Bericht aus dem Seitenansichtsbehälter identisch. Aufgrund von Datenanomalien gibt es einen leichten Offset (98.234 gegenüber 98.248).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **98.248** von 351.165 <br/>**33.203** von 165.173 <br/>**32.269** von 113.110 | **27%**<br/>**20%**<br/>**28%** |

<!--![](assets/container_report_persist_Visit.png)-->

### Berichte aus dem Besuchercontainer

Aus dem Besucherbehälter listet der Seitenbericht alle Seiten auf, die von einem Besucher aufgerufen wurden, bei dem `Referring Domain equals 'aol.com'` ist wahr. Wenn ein Besucher *&#39;aol.com&#39;* jederzeit im Verlauf (innerhalb des definierten Zeitraums) als Referrer-Domäne bezeichnet werden, werden alle Seiten im Besucherbehälter (einschließlich Seitenansichten bei anderen Besuchen) aufgelistet. Selbst Seiten, die nicht mit der primären Bedingung übereinstimmen, werden im Bericht aufgeführt, da diese Seiten im Besucherbehälter enthalten sind. Alle Seiten im Besucherbehälter werden im Bericht aufgelistet, selbst wenn sie zuvor aufgetreten sind und die Bedingungen nicht speziell erfüllen.

In einem Referrer-Domänenbericht: `Referring Domain equals 'aol.com'` ist in vier Seitenansichten wahr, aber `Referring Domain equals "weather.com"` auf den anderen Seiten &quot;true&quot;festgelegt ist, die der Besucher aufgerufen hat. Aus dem Besucherbehälter erhalten Sie eine Liste der Besucher, bei denen &quot;aol.com&quot;wahr ist. Sie erhalten jedoch auch Seiten, auf denen die Referrer-Domäne &quot;weather.com&quot;ist, und nicht den Wert, der Ihrer ursprünglichen Anforderung im Segment entsprach.

| Besuch 1<br/>Referrerdomäne gleich &quot;aol.com&quot; | <br/>Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Wintermantel | 1 |
| Kauf | 1 |

| Besuch 2<br/>Referrerdomäne = &#39;weather.com&#39; | <br/>Seitenansichten |
|----|---:|
| Winterkleidung | 2 |
| Wintermantel | 1 |
| Kauf | 1 |

| Besucherbehälter<br/>Referrerdomäne gleich &quot;aol.com&quot; | Seitenansichten |
|----|---:|
| Winterkleidung<br/>Verweisende Domäne: &#39;aol.com&#39; | 1 |
| Winterkleidung<br/>Verweisende Domäne: &#39;weather.com&#39; | 1 |
| Startseite <br/>Verweisende Domäne: &#39;aol.com&#39; | 1 |
| Wintermantel <br/>Verweisende Domäne: &#39;aol.com&#39; | 1 |
| Kauf<br/>Verweisende Domäne: &#39;aol.com&#39; | 1 |
| Winterstiefel<br/>Verweisende Domäne: &#39;weather.com&#39; | 1 |
| Winterhaufen<br/>Verweisende Domäne: &#39;weather.com&#39; | 1 |


<!--![](assets/container_overview_persist_Visitor.png)-->

Beachten Sie, dass bei der Anzeige der Daten aus dem Besucher-Container die Seitenansichten signifikant angestiegen sind (von 98.248 auf 112.925). Dieser Anstieg liegt daran, dass alle Seitenansichten des Besuchers (einschließlich der Seiten mit anderen Werten für die Referrerdomäne, die auf Besucherbehälterebene gespeichert sind) aufgelistet wurden. Und die zusätzlichen Besuche dieses Besuchers, die Besuche von 33.203 auf 43.448 erhöhten.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
|  | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **112.925** von 351.165 <br/>**43.448** von 165.173 <br/>**32.269** von 113.110 | **32%**<br/>**26%**<br/>**28%** |

<!--![](assets/container_report_persist_Visitor.png)-->

## Zusammenfassung

- Der Besucherbehälter gibt alle Seiten zurück, die von einem Besucher gesehen werden, wenn mindestens eine Seite die Kriterien erfüllt. Wenn also eine Seite nur bei Besuch 1 an Tag 1 angezeigt wird, sind alle vom Besucher über mehrere Besuche hinweg angezeigten Seiten in den Daten enthalten.
- Der Besuchebehälter gibt alle bei einem Besuch angezeigten Seiten zurück, für die mindestens eine Seite die Kriterien erfüllt. Wenn daher eine Seite nur bei Besuch 1 am Tag 1 gesehen wurde, werden alle während des gesamten Besuchs gesehenen Seiten in die Daten einbezogen.
- Achten Sie darauf, die für die Segmentierung verwendete Bedingung auf einer eVar oder einem anderen Typ von persistenten Variablen zu basieren. Sie können beispielsweise die Bedingung &quot;Wenn Kampagne E-Mail enthält&quot;verwenden und sie läuft nach sieben Tagen ab. Wenn die Kampagne also beim ersten Besuch festgelegt wird, bleibt sie sieben weitere Tage bestehen. Jeder Besuch ist enthalten, auch wenn die Kampagne nur beim ersten Besuch festgelegt wurde. Die anderen Besuche werden ebenfalls einbezogen (solange sie im Datumsbereich des Berichts liegen). Wenn Sie ausschließen möchten, dass persistente Werte einbezogen werden, können Sie entweder das Ereignis „Instanz von“ oder, sofern verfügbar, eine entsprechende Eigenschaftsvariable verwenden.
