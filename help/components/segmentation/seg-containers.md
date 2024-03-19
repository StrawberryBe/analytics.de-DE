---
description: Erfahren Sie mehr über die verschiedenen Segmentierungs-Container und deren Verwendung
keywords: Segmentierung;Segmente
title: Segment-Container
feature: Segmentation
exl-id: f30d525b-32b7-47d5-b92d-24bf86d8a471
source-git-commit: 5a9ba3f9749338c181fbcdc311bd08a92144e698
workflow-type: ht
source-wordcount: '3529'
ht-degree: 100%

---


# Segment-Container

Ein Segment legt Bedingungen für das Filtern von Besuchenden auf der Grundlage ihrer Attribute oder Interaktionen mit Ihrer Site fest. Um in einem Segment Bedingungen festzulegen, legen Sie Regeln für die Filterung von Besuchern auf der Grundlage von Besuchermerkmalen und/oder Navigationsverhalten fest. Um die Besucherdaten weiter herunterzubrechen, können Sie jeden Besucher auf der Grundlage bestimmter Besuche und/oder Seitenansichten filtern. Segment Builder bietet eine einfache Architektur zum Erstellen dieser Untergruppen und das Anwenden von Regeln als verschachtelte hierarchische Container der Form Besucher, Besuch oder Treffer.

Die in Segment Builder verwendete Container-Architektur definiert

- ![Besuchende](https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg) **[!UICONTROL Besuchende]** als äußersten Container, der übergreifende Daten enthält, die für Besuchende über Besuche und Seitenansichten hinweg spezifisch sind.
- ![Besuch](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg) Mit einem verschachtelten Container **[!UICONTROL Besuch]** können Sie Regeln festlegen, um die Besucherdaten auf der Grundlage von Besuchen aufzuschlüsseln, und
- ![Ereignis](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg) mit einem verschachtelten Container **[!UICONTROL Treffer]** können Sie die Besucherinformationen auf der Grundlage einzelner Seitenansichten aufschlüsseln.

Jeder Container ermöglicht Berichte über den Verlauf von Besuchenden, nach Besuch aufgeschlüsselte Interaktionen oder aufgeschlüsselte einzelne Treffer.

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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
</tr>
</table>

<!--![](assets/sequential_segmentation_container_hierarchy.png)-->

Im Folgenden finden Sie eine Videoübersicht über die Segment-Container:

>[!VIDEO](https://video.tv.adobe.com/v/25401/?quality=12)

## Besucher-Container

Der Besucher-Container enthält sämtliche Besuche und Seitenansichten für Besucher innerhalb eines bestimmten Zeitraums. Ein Segment auf der Besucherebene gibt die Seite zurück, die die Bedingung erfüllt, sowie alle anderen Seiten, die vom Besucher angesehen wurden (und dies nur durch definierte Datumsbereiche beschränkt). Da es sich um den am breitesten definierten Container handelt, liefern Berichte, die auf der Ebene des Besucher-Containers erstellt werden, Seitenansichten über alle Besuche hinweg und ermöglichen eine Analyse mehrerer Besuche. Der Besucher-Container ändert sich daher auf der Grundlage der definierten Datumsbereiche am wahrscheinlichsten.

Besucher-Container können Werte enthalten, die auf dem Gesamtverlauf eines Besuchers basieren:

- Tage bis Erstkauf
- Ursprüngliche Einstiegsseite
- Ursprünglich Referrerdomänen

## Besuchs-Container

Mit dem Besuchs-Container können Seiteninteraktionen, Kampagnen oder Konversionen für eine bestimmte Web-Sitzung identifiziert werden. Ein Segment auf der Besuchsebene gibt die Seite zurück, die die Bedingung erfüllt, sowie alle anderen Seiten, die von Besuchenden angesehen wurden (und dies nur durch definierte Datumsbereiche beschränkt). Der Besuchs-Container ist der am häufigsten verwendete Container, da er das Verhalten für die gesamte Besuchssitzung erfasst, sobald die Regel erfüllt ist. Mit dem Besuchs-Container können Sie definieren, welche Besuche beim Erstellen und Anwenden eines Segments ein- oder ausgeschlossen werden sollen. Er kann Ihnen bei der Beantwortung der Frage helfen, wie viele Besucher bei demselben Besuch den Bereich „News und Sport“ angesehen haben. Oder welche Seiten zu einer erfolgreichen Konversion zum Kauf beigetragen haben.

Besuchs-Container enthalten Werte, die auf dem Auftreten pro Besuch basieren:

- Besuchsnummer
- Einstiegsseite
- Rückkehrhäufigkeit
- Beitragsmetriken
- Linear zugeordnete Metriken

## Treffer-Container

Der Treffer-Container definiert, welche Seitenbesuche von einem Segment einbezogen oder ausgeschlossen werden sollen. Der Treffer-Container ist der engste der verfügbaren Container, mit dem Sie bestimmte Klicks und Seitenansichten identifizieren können, bei denen eine Bedingung wahr ist. Sie können einen einzelnen Trackingcode anzeigen oder das Verhalten innerhalb eines bestimmten Bereichs Ihrer Site isolieren. Sie können auch einen bestimmten Wert erkennen, wenn eine Aktion stattfindet, z. B. den Marketing-Kanal, wenn ein Auftrag platziert wurde.

Treffer-Container enthalten Werte, die auf den Aufschlüsselungen einzelner Seiten basieren:

- Produkte
- Listen-Props
- Listen-eVars
- Merchandising eVars (im Kontext von Ereignissen)

  >[!NOTE]
  >
  >Wenn Sie diesen Container mit einem persistenten Wert verwenden, z. B. einem eVar, wird jeder Treffer ausgelesen, in dem der Wert persistent ist. Im Fall eines Trackingcodes, der nach einer Woche abläuft, kann dieser Wert über mehrere Besuche hinweg persistent sein.

## Logischer Gruppen-Container

Mit dem logischen Gruppen-Container können Sie einen separaten Container innerhalb der Segmentregeln bereitstellen, um Entitäten zu filtern, die nicht hierarchiebasiert sind. Beispielsweise können Sie einen Container bereitstellen, der innerhalb des Segments verschachtelt ist, das besucherbasiert filtert. Dieser Logiktyp erfordert es, dass Sie die Hierarchie unterbrechen (da Sie bereits über einen Besucher-Container auf der obersten Ebene verfügen), um nur nach ausgewählten Besuchenden zu filtern. Siehe [Beispiele für logische Gruppen](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md) als ergänzende Information.

## Verschachteln von Containern {#nest-containers}

Wenn Sie Segment-Container innerhalb anderer Container erstellen, erstellen Sie im Grunde ein Segment in einem Segment. Bei verschachtelten Containern wird die folgende Logik angewendet:

1. Bestimmen, welche Daten enthalten sind, indem der äußerste Container verwendet wird. Alle Daten, die nicht mit dieser äußeren Regel übereinstimmen, werden aus dem Segmentbericht ausgeschlossen.
1. Anwenden der verschachtelten Regel auf die verbleibenden Daten. Die verschachtelte Regel gilt NICHT für Treffer, die die erste Regel abgewiesen hat.
1. Wiederholen, bis alle verschachtelten Container-Regeln berechnet wurden. Die verbleibenden Daten werden dann in den resultierenden Bericht einbezogen.

Sie können die Verschachtelung zwischen Containern und zwischen Regeln in einem Container verwenden. Folgende Elemente können in jedem Container verschachtelt werden:

| Container-Name | Was darin verschachtelt werden kann |
|---|---|
| Treffer | Nur Ereignisse |
| Besuch | Treffer-Container, Ereignisse |
| Besucher. | Besuchs-Container, Treffer-Container, Ereignisse |
| logische Gruppe | Besucher-Container, Besuchs-Container, Treffer-Container |

### Einbeziehen mehrerer Behälter in eine einzelne Definition

Indem Sie mehrere Segmente in ein neues verbundenes Segment einbeziehen, können Sie Ihre Daten sogar noch weiter verfeinern. Das Zusammenziehen von zwei vorhandenen Segmenten agiert beim Filtern der Besucher als OR-Anweisung. Alle Container auf der Arbeitsfläche werden gegen alle Daten geprüft und alle Daten, die mit einem der Container übereinstimmen, werden in den Bericht einbezogen.

Wenn Sie z. B. einen Besuchs-Container, in dem gilt „Land = Vereinigte Staaten“ mit einem Besuchs-Container zusammenziehen, in dem „Auftrag = wahr“ ist,

```
Country = United States + Order = True
```

wird ein Segment erstellt, das sich wie folgt verhält:

1. Dieses Segment bezieht sich zunächst auf Ihre gesamten Daten und identifiziert alle Besuchenden in den Vereinigten Staaten.
2. Das Segment bezieht sich dann erneut auf Ihre gesamten Daten und prüft, ob Besuchende einen Auftrag erteilt haben.
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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
</tr>
</table>

<!--![](assets/nesting_container.png)-->

[!UICONTROL Besucher] stellen den Container mit dem höchsten Rang in der sequenziellen Segmentierung dar. Dabei sind [!UICONTROL Besuche] im [!UICONTROL Besucher-Container] und [!UICONTROL Treffer] in den [!UICONTROL Besucher]- oder [!UICONTROL Besuchs-Containern] enthalten. Diese [Container-Hierarchie](/help/components/segmentation/seg-overview.md#section_7FDF47B3C6A94C38AE40D3559AFFAF70) muss eingehalten werden, um ordnungsgemäß sortierte sequenzielle Segmente zu erstellen.

**Zum Erstellen sequenzieller Segmente** werden Container verschachtelt und eine sequenzielle Logik verbunden. Dazu wird der [!UICONTROL DANN]-Operator verwendet, für den jeder Container basierend auf der Sequenz der Besucherin oder des Besuchers `true` sein muss.

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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
</tr>
</table>

<!--![](assets/sequential_segmentation_nesting_3.png)-->

Die einzige Ausnahme für diese Container-Hierarchie besteht in der Verwendung des [logischen Gruppen-Containers](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md). Mit dem [!UICONTROL logischen Gruppen-Container] können Sie einen Treffer innerhalb eines Containers ohne spezielle Reihenfolge verschachteln, um Ereignisse und Dimensionen zu erfassen, jedoch außerhalb einer sequenziellen Reihenfolge.

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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
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
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Treffer</td>
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

Daten, die auf den einzelnen Ebenen der Hierarchie der Container Besucher > Besuch > Treffer erfasst werden, beeinflussen, wie Sie Ihre Segmente erstellen. Wenn Sie dasselbe Segment auf denselben Bericht anwenden und dabei denselben Datensatz verwenden, erhalten Sie unterschiedliche Werte, die vom Container abhängen, von dem aus Sie den Bericht erzeugen. Faktoren wie die Container-Berichtsebene und die Persistenz von Werten über Treffer hinweg können wesentliche Veränderungen der Berichtsgenauigkeit verursachen.

### Grundlagen der Containerdaten {#container-data}

Beispiel: Der unten dargestellte Besucher hat eine Site zum ersten Mal besucht, kam auf der Homepage an und hat dann drei weitere Seiten besucht und aus dem Besuch einen Kauf gemacht. Bei einem anderen Besuch landete der Besucher auf der Produktseite, wechselte dann zur Homepage, zurück zur Produktseite und schloss die Sitzung dann ab, nachdem er sich Wintermützen angesehen hat. Basierend auf den für die einzelnen Container für das Segment erfassten Daten, werden im Bericht unterschiedliche Werte angezeigt.

Das Segment `Pages equals Winter Coat` unten wird auf den **Seitenbericht** angewendet.


Der Bericht zeigt basierend auf dem ausgewählten Container unterschiedliche Ergebnisse für die folgenden Besuche und Seitenansichten einer Besucherin oder eines Besuchers an.

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
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterjacke</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Kauf 100 USD</td>
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
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Wintermützen</td>

</table>


<!--![](assets/container_overview.png)-->

### Berichte aus dem Treffer-Container

Wenn sich diese Bedingung in einem Treffer-Container befindet, listet der Bericht nur Seiten auf, für die *Seite = Wintermäntel* wahr ist. Da nur eine Seite diese Bedingung in einem Container mit nur einer Seite erfüllt, wird nur die Wintermäntel-Seite angezeigt.

| Seite | Seitenansichten |
|---|--:|
| Winterjacke | 1 |

<!--![](assets/container_overview_PV.png)-->

Bei Berichten aus dem Treffer-Container können Sie sehen, wie sich Berichte aus unterschiedlichen Containern auf die gesamten Berichtswerte auswirken. Beachten Sie beim Anzeigen des Segmentberichts, dass die Seitenansichten ungefähr den Besuchenden entsprechen (rund 2.000 Besuchende haben bei einem Besuch doppelte Seiten gesehen, was zur Gesamtzahl der Seitenansichten addiert wird). Und Unique Visitors entsprechen ungefähr der Anzahl der Besuche (etwa 2.000 Unique Visitors haben die Seite mehr als einmal besucht).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten <br/>Besuche:<br/>Unique Visitors: | **69.252** von 351.292 <br/>**67.554** von 165.175 <br/>**63.541** von 113.169 | **19 %**<br/>**40 %**<br/>**56 %** |


<!--![](assets/container_report_PV.png)-->

>[!IMPORTANT]
>
>Unabhängig davon, wie Sie die Daten anzeigen (über den Treffer-, Besuchs- oder Besucher-Container), haben in diesem Beispiel alle dieselbe Anzahl von 63.541 Besuchenden. Die ursprüngliche Besucherbedingung (Besuchende, die die Winterjacken-Seite angesehen haben) bleibt unabhängig davon intakt, wie Sie den Bericht erzeugen. Dies ist die Teilmenge der Daten, mit denen Sie auf den verschiedenen Ebenen Berichte erstellen.

### Reporting aus dem Besuchs-Container

Wenn sich dieselbe Bedingung in einem Besuchs-Container befindet, listet der Bericht alle Seiten des Besuchs auf, für die *Seite gleich Wintermäntel* wahr ist. Sie filtert die Wintermäntel-Seite, erfasst aber auch alle anderen Seiten des Besuchs, bei denen die Bedingung wahr ist. Da die Besucherin oder der Besucher bei dem Besuch auch die Start-, Produkt- und die Kaufseite besucht hat, werden diese zusätzlichen Seiten im Bericht aufgeführt, wenn der Bericht mit den Daten des Besucher-Containers erstellt wird.

| Seite | Seitenansichten |
|---|--:|
| Startseite  | 1 |
| Produkt | 1 |
| Winterjacke | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_visit.png)-->

In den Segmentwerten aus dem Besuchs-Container sehen Sie, dass die Anzahl der Seitenansichten signifikant gestiegen ist. Dieser Anstieg hat den Grund, dass ein Bericht aus dem Besuchs-Container alle Seiten identifiziert, die die Bedingungen erfüllen, plus alle anderen beim Besuch angesehenen Seiten (mit allen in jedem Besuchs-Container erfassten Seitenansichten).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **226.193** von 351.292 <br/>**67.554** von 165.175 <br/>**63.541** von 113.169 | **64 %**<br/>**40 %**<br/>**56 %** |

<!--![](assets/container_report_Visit.png)-->

### Reporting aus dem Besucher-Container

Wenn sich dieselbe Bedingung in einem Besucher-Container befindet, listet der Bericht alle von einem Besucher angesehenen Seiten auf, für die *Seite gleich Winterjacke* wahr ist. Diese Bedingung bedeutet, dass, wenn eine Besucherin oder ein Besucher die Winterjacken-Seite angesehen hat, alle Seiten im Besucher-Container aufgelistet werden (einschließlich der Seitenansichten aus anderen Besuchen). Folglich werden im Bericht auch Seiten gelistet, die die Bedingung nicht erfüllen, weil die Besucherin oder der Besucher diese zu einem vorherigen Zeitpunkt gesehen hat. Alle im Besucher-Container enthaltenen Seiten werden im Bericht aufgeführt. Dies betrifft auch Seiten, die vorher aufgetaucht sind und die Bedingungen nicht spezifisch erfüllen.

| Besuch 1<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Winterjacke | 1 |
| Kauf | 1 |

| Besuch 2<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Winterkleidung | 2 |
| Winterstiefel | 1 |
| Wintermützen | 1 |

| Besuch 1 + Besuch 2<br/>Seite | <br/>Seitenansichten |
|---|--:|
| Winterkleidung | 3 |
| Startseite  | 1 |
| Winterjacke | 1 |
| Kauf | 1 |
| Winterstiefel | 1 |
| Wintermützen | 1 |

<!--![](assets/container_overview_visitors.png)-->

Beim Anzeigen von Segmenten aus dem Besucher-Container können Sie sehen, dass die Seitenansichten und die Besuche angestiegen sind. Dieser Anstieg hat den Grund, dass auf der Besucherebene, sobald die Besucherin oder der Besucher die Winterjacken-Seite einmal besucht hat (wodurch die Bedingung wahr ist), alle anderen Seitenansichten und alle anderen Besuche für diese Besucherin oder diesen Besucher erfasst werden.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **240.094** von 351.292 <br/>**83.823** von 165.175 <br/>**63.541** von 113.169 | **68 %**<br/>**50 %**<br/>**56 %** |

<!--![](assets/container_report_Visitor.png)-->

Zusammenfassend wird deutlich, dass das Wissen darüber, wie die Segmentierung bei unterschiedlichen Aufschlüsselungen von Daten funktioniert, bei der Interpretation der gelieferten Daten von entscheidender Bedeutung ist.

## Auf dem Container basierende Berichte {#reporting}

Jede Aufschlüsselung von Segmentdaten hat einen Umfang, auf den diese angewendet wird. Die meisten Aufschlüsselungen basieren auf *Seitenansichten*, wobei jedoch viele wertvolle Segmente auf dem *Besuchecontainer* und in geringerem Umfang auf dem *Besuchercontainer* basieren. Es ist wichtig, dass Sie wissen, wie Berichte funktionieren, die auf dem Umfang Ihres Containers basieren.

Am Beispiel des Segments `Page equals Winter Coats` sind unten Beispiele für die Ergebnisse dieses Segments aufgeführt, die darauf basieren, wie die Container-Daten angewendet werden und wie der Umfang der Daten mit dem Segmenttyp übereinstimmt.

### Auf übereinstimmender Segmentregel basierender Segment-Container

Das Anwenden des Segment-Containers auf einen normalen Datenbereich bringt die erwarteten Ergebnisse, in denen die Linienelemente mit der Segmentregel übereinstimmen.

- **Treffer-Container, bei dem Seite gleich „Wintermantel“**: Ein *Seitenbericht* mit diesem Segment liefert nur die Werte, die mit „Wintermantel“ übereinstimmen. Alle anderen Seiten werden aus dem Bericht ausgeschlossen.
- **Besuchs-Container, bei dem Einstiegsseite gleich „Winterkleidung“**: Ein *Einstiegsseiten*-Bericht mit diesem Segment liefert nur den zweiten Besuch, weil dessen Einstiegsseite mit der Segmentregel übereinstimmt.
- **Besuchs-Container, bei dem Besuchsnummer gleich 1**: Alle Seitenansichten des ersten Besuchs sind im Bericht enthalten, weil er mit der Segmentregel übereinstimmt.

### Seitenansichten auf der Besuchs-Container-Ebene

Viele Segmentregeln identifizieren Seitenansichten pro Besuch. Wenn diese Identifizierung eintritt, wird der gesamte Besucher-Container angewendet, wenn nur ein einzelner Treffer mit der Regel übereinstimmt. Dieser Segmentbericht ist besonders wertvoll, weil auf Besuchen basierende Seitenansichten Einblick auf der Grundlage von Seitenansichten pro Besuch liefern.

- **Besuchs-Container, bei dem Seite gleich Seite „Wintermantel“**: In einem Seitenbericht auf der Besucher-Container-Ebene werden alle Seitenansichten gezeigt, die eine Ansicht der Seite „Winterkleidung“ enthalten. Wenn eine Seite mit der Segmentregel übereinstimmt, werden alle dem Besuch zugeordneten Seitenansichten in den Bericht aufgenommen.
- **Besuchs-Behälter, bei dem Seite gleich „Startseite“ ist**: In einem Seitenbericht mit diesem Segment werden nur Daten aus dem ersten Besuch angezeigt, da die Besucherin oder der Besucher beim zweiten Besuch keine „Startseite“ angesehen hat.
- **Besucher-Container, bei dem Seite gleich „Winterkleidung“ ist**: In einem Seitenbericht ruft dieses Segment alle Daten beider Besuche ab, da der Besucher die Seite „Winterkleidung“ gesehen hat.

### Segment-Container, der Treffer identifiziert, die kleiner als Seitenansichten sind

Die Verwendung des Segments mit einem Container, der kleiner als der Aufschlüsselungsbereich ist, liefert überraschende Daten. Bei Verwendung einer kleineren Aufschlüsselung werden weiterhin alle Treffer aus dem Datenbereich einbezogen.

- **Treffer-Container, bei dem Einstiegsseite gleich „Produkt“**: Alle Seiten sind mit der Einstiegsseite des Besuchs verknüpft, wodurch eine besuchsbasierte Aufschlüsselung erfolgt. Bei Verwendung dieses Segments wird nicht nur die Einstiegsseite „Produktseite“ einbezogen, sondern auch alle Treffer in dem entsprechenden Besuch.
- **Treffer-Container, bei dem Listenvariable 1 WertA enthält**: Wenn mehrere Werte für denselben Treffer als Listenvariablen definiert sind, werden alle Variablenwerte in das Segment einbezogen. Es ist nicht möglich, Werte zu separieren, die in derselben Seitenansicht auftreten, da der Treffer-Container der kleinste Segment-Container für das Aufschlüsseln von Treffern ist.
- **Treffer-Container, bei dem Seite gleich „Kauf“**: Bei der Verwendung von Seitenansichten als Metrik wird nur die Kaufseite angezeigt (erwartungsgemäß). Bei Verwendung eines Berichts über den Beitrag am Umsatz erhalten alle Seiten im ersten Besuch 100 $, da Beitragsmetriken besuchsbasiert sind.
- **Treffer-Container, bei dem Seite gleich „Wintermantel“**: Bei der Verwendung von Seitenansichten als Metrik wird nur die Wintermantel-Seite angezeigt (erwartungsgemäß). Bei Verwendung eines Berichts über den Beitrag am Umsatz erhält keine Seite eine Gutschrift, da für diese Dimension eine persistente Dimension erforderlich ist. Die Seitenansicht, auf der der Kauf tatsächlich stattfand (die Kaufseite) ist nicht im Treffer-Container enthalten, weshalb kein Element einen Umsatzbeitrag erhält. Bei einem über den Besuchs-Container ausgeführten Bericht wären jedoch alle Seitenansichten dieses Besuchs enthalten und der Umsatzbeitrag (100 $) würde über alle in der Sitzung gesehenen Seiten verteilt.

## Persistenz über Container hinweg {#persistence}

Die Filterung nach Dimensionen, die über einen Seitenbereich persistent sind, z. B. ein Kampagnen-eVar oder eine Referrer-Dimension, wirkt sich auf die auf Container-Ebene gesammelten Daten aus und muss im Hinblick auf die Berichtsgenauigkeit nachvollzogen werden.

Segmentdaten können, basierend auf der Persistenz einer Dimension oder einer angewendeten Variablen, über ausgewählte Seiten hinweg variieren. Einige Dimensionen, z. B. die Seitendimension, bieten auf Seitenebene eindeutige Werte und werden auf der Grundlage von Daten aus dem Treffer-Container gefiltert. (Siehe als Beispiel [Auf Container-Daten basierende Berichte](/help/components/segmentation/seg-overview.md)). Andere Dimensionen, z. B. die Dimension „Referrer-Domain“, sind für einen Besuch über mehrere Seiten hinweg persistent. Beispiel: `Referring Domain equals aol.com`. Einige Dimensionen oder angewendete Variablen, z. B. die Besuchsdauer, erstrecken sich über den gesamten Verlauf des Besuchers.

<!--![](assets/RefDomain_aol.png)-->

Im Gegensatz zur Seitendimension ist der Wert „Referrerdomäne“ an jede Seite in diesem Besuch angehängt. Im Beispiel unten kommt der Besucher von einer verweisenden Site auf der Homepage an. Dementsprechend wird allen in diesem Besuch enthaltenen Seiten derselbe Wert für die Referrer-Domain zugewiesen.

Das Segment `Referring Domain equals aol.com` unten wird auf den **Seitenbericht** angewendet.

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
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><img align="right" src="https://spectrum.adobe.com/static/icons/ui_18/ArrowSize100.svg"/><br/>Winterjacke</td>
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Kauf 100 USD</td>
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
<td style="background-color: #FFFFFF;"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg"><br/>Wintermützen</td>

</table>

<!--![](assets/container_overview_persist.png)-->

Bei einem neuen Besuch wird die Besucherin bzw. der Besucher von einer anderen Website verwiesen. Dementsprechend wird allen in dem neuen Besuch enthaltenen Seiten der neue Wert für die Referrer-Domain für jede Seitenansicht zugewiesen.

### Berichte aus dem Treffer-Container

Da allen in demselben Besuch enthaltenen Seitensichten derselbe Wert für die Referrer-Domain zugewiesen wird, werden beim Reporting auf Ebene des Treffer-Containers, bei dem `Referring Domain equsls 'aol.com'`, alle in der folgenden Tabelle aufgeführten Seiten zurückgegeben.

| Referrer-Domain ist gleich „aol.com“ | Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Winterjacke | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_persist_Visit.png)-->

Bei der Anzeige der Daten aus dem Treffer-Container, wurden über 92.000 Seitenansichten bei über 33.000 Besuchen durch nur etwas mehr als 32.000 Besucher erzeugt. Im Durchschnitt fielen bei jedem Besuch drei Seitenansichten an und nahezu sämtliche Besuche betrafen Unique Visitors.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **98.234** von 351.165 <br/>**33.203** von 165.173 <br/>**32.269** von 113.110 | **27 %**<br/>**20 %**<br/>**28 %** |

<!--![](assets/container_report_persist_PV.png)-->

### Reporting aus dem Besuchs-Container

Wenn dieselbe Bedingung für einen Seitenbericht im Besuchs-Container gefiltert wird, sind alle Seiten in dem Besuch wahr, bei denen `Referring Domain equals 'aol.com'`. Da der Wert der Referrer-Domain auf der Besuchsebene festgelegt wird, sind Berichte auf Seitenansichts- und Besuchsebene identisch.

| Referrer-Domain ist gleich „aol.com“ | Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Winterjacke | 1 |
| Kauf | 1 |

<!--![](assets/container_overview_persist_Visit.png)-->

Da alle Seiten basierend auf dem Besuch denselben Wert für die Referrer-Domain haben, ist der Bericht auf der Besuchs-Container-Ebene (fast) mit dem Bericht aus dem Seitenansichts-Container identisch. Aufgrund von Datenanomalien gibt es einen leichten Versatz (98.234 gegenüber 98.248).

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **98.234** von 351.165 <br/>**33.203** von 165.173 <br/>**32.269** von 113.110 | **27 %**<br/>**20 %**<br/>**28 %** |

<!--![](assets/container_report_persist_Visit.png)-->

### Reporting aus dem Besucher-Container

Aus dem Besucher-Container listet der Seitenbericht alle Seiten auf, die von einer Besucherin oder einem Besucher angesehen wurden, bei denen `Referring Domain equals 'aol.com'` wahr ist. Wenn daher eine Besucherin oder ein Besucher irgendwann (innerhalb des definierten Zeitraums) im Verlauf *„aol.com“* als Referrer-Domain hatte, werden alle Seiten im Besucher-Container aufgeführt (einschließlich der Seitenansichten bei anderen Besuchen). Auch Seiten, die nicht der primären Bedingung entsprechen, werden im Bericht aufgeführt, da diese Seiten im Besucher-Container enthalten sind. Alle im Besucher-Container enthaltenen Seiten werden im Bericht aufgeführt. Dies betrifft auch Seiten, die vorher aufgetaucht sind und die Bedingungen nicht spezifisch erfüllen.

In einem Bericht „Referrer-Domain“ ist `Referring Domain equals 'aol.com'` bei vier Seitenansichten wahr, bei den anderen Seiten des Besucherzugriffs ist jedoch `Referring Domain equals "weather.com"` wahr. Aus dem Besucher-Container erhalten Sie eine Liste der Besuchenden, bei denen „aol.com“ wahr ist. Sie erhalten jedoch auch Seiten, auf denen die Referrer-Domain „weather.com“ ist, und nicht der Wert, der Ihrer ursprünglichen Anfrage im Segment entsprach.

| Besuch 1<br/>Referrer-Domain gleich „aol.com“ | <br/>Seitenansichten |
|----|---:|
| Startseite  | 1 |
| Winterkleidung | 1 |
| Winterjacke | 1 |
| Kauf | 1 |

| Besuch 2<br/>Referrer-Domain = „weather.com“ | <br/>Seitenansichten |
|----|---:|
| Winterkleidung | 2 |
| Winterjacke | 1 |
| Kauf | 1 |

| Besucher-Container<br/>Referrer-Domain gleich „aol.com“ | Seitenansichten |
|----|---:|
| Winterkleidung<br/>Referrer-Domain: „aol.com“ | 1 |
| Winterkleidung<br/>Referrer-Domain: „weather.com“ | 1 |
| Startseite <br/>Referrer-Domain: „aol.com“ | 1 |
| Wintejacke <br/>Referrer-Domain: „aol.com“ | 1 |
| Kauf<br/>Referrer-Domain: „aol.com“ | 1 |
| Winterstiefel<br/>Referrer-Domain: „weather.com“ | 1 |
| Wintermützen<br/>Referrer-Domain: „weather.com“ | 1 |


<!--![](assets/container_overview_persist_Visitor.png)-->

Beachten Sie, dass bei der Anzeige der Daten aus dem Besucher-Container die Seitenansichten signifikant angestiegen sind (von 98.248 auf 112.925). Dieser Anstieg hat den Grund, dass alle Seitenansichten der Besucherin oder des Besuchers (einschließlich der Seiten mit anderen Werten für die Referrer-Domain, die auf Besucher-Container-Ebene gespeichert sind) aufgelistet wurden. Und die zusätzlichen Besuche dieser Besucherin oder dieses Besuchers, die die Besuche von 33.203 auf 43.448 erhöhten.

| <img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphDonut_18_N.svg"/> | Metrik | # | % |
|---|---|--:|--:|
| | Seitenansichten:<br/>Ansichten:<br/>Unique Visitors: | **112.925** von 351.165 <br/>**43.448** von 165.173 <br/>**32.269** von 113.110 | **32 %**<br/>**26 %**<br/>**28 %** |

<!--![](assets/container_report_persist_Visitor.png)-->

## Zusammenfassung

- Der Besucher-Container gibt alle von einer Besucherin oder einem Besucher gesehenen Seiten zurück, von denen mindestens eine Seite den Kriterien entspricht. Wenn daher eine Seite nur bei Besuch 1 an Tag 1 gesehen wurde, werden alle bei mehreren Besuchen von der Besucherin oder dem Besucher gesehenen Seiten in die Daten einbezogen.
- Der Besuchs-Container gibt alle Seiten zurück, die in einem Besuch gesehen wurden und von denen mindestens eine Seite die Kriterien erfüllt. Wenn daher eine Seite nur bei Besuch 1 an Tag 1 gesehen wurde, werden alle während des gesamten Besuchs gesehenen Seiten in die Daten einbezogen.
- Achten Sie darauf, die Bedingungen, die Sie für die Segmentierung verwenden, auf einer eVar oder einem anderen Typ einer persistenten Variablen basieren zu lassen. Sie könnten z. B. die Bedingung „Wenn Kampagne E-Mail enthält“ verwenden, die nach sieben Tagen abläuft. Wenn die Kampagne daher auf den ersten Besuch gesetzt wird, ist sie anschließend sieben weitere Tage persistent. Jeder Besuch wird einbezogen, auch wenn die Kampagne nur für den ersten Besuch aktiviert war. Auch die anderen Besuche werden einbezogen (solange sie innerhalb des Datumsbereichs des Berichts liegen). Wenn Sie ausschließen möchten, dass persistente Werte einbezogen werden, können Sie entweder das Ereignis „Instanz von“ oder, sofern verfügbar, eine entsprechende Eigenschaftsvariable verwenden.
