---
description: Schritte zum Ausführen der verschiedenen Berichtstypen.
title: Verschiedene Berichtstypen ausführen
topic: Reports,Reports and analytics
uuid: f59ab2a1-e916-46e8-bb5b-e6361ba00dda
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Verschiedene Berichtstypen ausführen

Schritte zum Ausführen der verschiedenen Berichtstypen.


## Rangbericht ausführen {#task_C570BA4A213F4F2EB7B30E012934BE7D}

In Rangberichten zeigt die Tabelle die Rangfolge der Berichtsseiten im Verhältnis zur Metrik nach Anzahl oder Prozentsatz an. Bei Rangberichten können mehrere Metriken in einem Bericht angezeigt werden.

<!-- 

t_reports_ranked.xml

 -->

1. Erstellen Sie einen Bericht, z. B. [!UICONTROL Pages Report] ( **[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Pages]**).
1. In the report header, click **[!UICONTROL Ranked.]**
1. Klicken Sie auf die Spaltenüberschrift in der Tabelle, um den Bericht nach Rang zu ordnen.

   Rangberichte können bis zu 200 in der Tabelle aufgelistete Elemente enthalten (wie zum Beispiel Produkte, Kategorien, Webseiten usw.) und zehn Metriken (Umsatz, Bestellungen, Ansichten usw.).

## Trendbericht ausführen {#task_F03B4E760B9E4EA29FC3F654E6316887}

Trendberichte zeigen Metriken im Zeitverlauf an. Sie verwenden diesen Berichtstyp, wenn Sie sehen möchten, wie sich ein Segment von einem Zeitraum zum nächsten auswirkt.

<!-- 

t_reports_trended.xml

 -->

Für die meisten Konversions- und Traffic-Berichte steht eine Trendansicht zur Verfügung. Mithilfe des [!UICONTROL Calendar]können Sie Verbesserungen für alle Zeitraumunterteilungen anzeigen, einschließlich Tage eines Monats, Wochen eines Jahres, Wochen eines Quartals, Monate eines Jahres usw. Trendberichte zeigen Trends für eine Metrik (Umsatz, Bestellungen, Ansichten usw.) für bis zu fünf Elemente (z. B. Produkte, Kategorien, Webseiten usw.) an.

**So führen Sie einen Trendbericht aus**

1. Führen Sie einen Konversions- oder Traffic-Bericht aus, z. B. **[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Pages]**.
1. Unter **[!UICONTROL Report Type]** klicken Sie auf **[!UICONTROL Trended.]**

## Konversionstrichterbericht ausführen {#task_B926A74AA6A641138C2986C1635120CB}

Konversionstrichterberichte zeigen den Prozentsatz der Besucher an, die eine Reihe von Ereignissen durchlaufen haben, um eine gewünschte Aktion durchzuführen. Sie können beispielsweise sehen, wie viele Besucher Ihre Webseite aufriefen, Artikel zu einem Einkaufswagen hinzufügten und dann einen Artikel kauften. Dieser Bericht zeigt auch die Anzahl der Personen an, die während des Weges ausfielen.

<!-- 

t_reports_conversion_funnel.xml

 -->

Um diesen Bericht auszuführen, wählen Sie einen Bericht aus, z. B. einen Seitenbericht ( **[!UICONTROL Reports]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Tracking Code]** > **[!UICONTROL Campaign Conversion Funnel]**).

Siehe [Konversionsberichte](https://marketing.adobe.com/resources/help/de_DE/reference/reports_conversion.html), um eine Beschreibung anzuzeigen.

## Fallout-Bericht ausführen {#task_8FD97C8260464F9DA731A93DB8F80184}

Die [!UICONTROL Fallout Report] zeigt die Anzahl der Besucher an, die eine vorab festgelegte Seitenfolge besucht haben. Er zeigt außerdem die Konversions- und Trichteranalyseraten zwischen den einzelnen Schritten an.

<!-- 

t_reports_fallout.xml

 -->

Sehen Sie sich das neue Bedienfeld [Fallout-Analyse](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/fallout_flow.html) in Analyse Workspace an!

1. Klicken Sie [!UICONTROL Adobe Analytics]in auf **[!UICONTROL Reports]** > **[!UICONTROL Paths]** > **[!UICONTROL Pages]** > **[!UICONTROL Fallout]**.
1. Klicken Sie auf der [!UICONTROL Fallout Report] Seite auf **[!UICONTROL Launch the Fallout Report Builder]**.

   ![Schritt Ergebnis](assets/fallout_add_items.png)

1. On the [!UICONTROL Define Checkpoints] page, specify the checkpoints that you want to use for the report.
1. Klicken Sie auf **[!UICONTROL Run Report]**.

   ![Schritt Ergebnis](assets/fallout_report.png)

>[!MORELIKETHIS]
>
>* [Fallout-Bericht – Beschreibung](https://docs.adobe.com/content/help/de-DE/analytics/components/variables/dimensions-reports/reports-fallout.translate.html)


## Seitenflussbericht ausführen {#task_133E8B87C3F04DA0A42D10CBA499305B}

Seitenflussberichte zeigen die Reihenfolge an, in der Ihre Besucher auf die Seiten zugreifen und durch Ihre Site navigieren. Dieser Bericht hilft bei der Beantwortung

Sehen Sie sich die neue [Flussvisualisierung](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/flow.html) in Analyse Workspace an!

Führen Sie einen [Pfadbericht](https://marketing.adobe.com/resources/help/de_DE/reference/reports_paths.html) aus.

Klicken Sie beispielsweise auf **[!UICONTROL Reports]** > **[!UICONTROL Paths]** > **[!UICONTROL Pages]** > **[!UICONTROL Next Page Flow]**.

![](assets/page_flow.png)

Sie lesen diesen Bericht von links nach rechts, beginnend mit der gewählten Seite. Die Seiten, die nach der gewählten Seite angezeigt wurden, werden als nach rechts verlaufende Verzweigung dargestellt.

Der Prozentsatz, in dem jede nachfolgende Seite angezeigt wurde, wird neben dem Namen der Seite angezeigt. Die Breite der Linie, die mit der nächsten Seite verbunden ist, zeigt diesen relativen Prozentwert an.

**[!UICONTROL Path Views]**: Gibt an, wie oft eine Seite angezeigt wurde, wenn sie auf die angezeigten Pfade beschränkt ist.

Die Seite &quot;Datenschutzregeln&quot;könnte z. B. insgesamt 10.000 Ansichten aufweisen, aber nur 500 dieser Ansichten erfolgten unmittelbar nach der Startseite. Daher wird der Begriff Pfad Ansicht verwendet.

Der relative Prozentsatz wird durch die relative Breite der Linie dargestellt. Dieser Bericht zeigt standardmäßig fünf Zweitstufenverzweigungen und fünf Drittstufenverzweigungen an. Sie können die Anzahl der Verzweigungen auf bis zu zehn Zweitstufenverzweigungen und fünf Drittstufenverzweigungen erweitern, um eine Ansicht zu erhalten. Dadurch erhöht sich die Höhe des Berichts und es ist höchstwahrscheinlich ein Bildlauf erforderlich, um das gesamte Diagramm Ansicht.

## Trichterbericht ausführen {#task_2BBF6FACD48F479E8B2EE458919941CB}

Sie können Erfolgsereignisse auswählen und sie einem [!UICONTROL Purchase Conversion Funnel] Bericht oder einem [!UICONTROL Product Conversion Funnel] Bericht hinzufügen.

<!-- 

t_reports_funnel.xml

 -->

1. Klicken Sie auf **[!UICONTROL Reports]** > **[!UICONTROL Products]** > [Produktkonversionstrichter](https://marketing.adobe.com/resources/help/de_DE/reference/reports_conversion_funnel.html).

## Marketingkanalbericht ausführen {#task_64ADED5CC75248319E06E3E029B47F78}

Marketing Kanal Berichte bietet einen Übersichtsbericht zur Zuordnung von First Touch- und Last Touch-Kanälen mit Standardmetriken für Berichte wie Umsatz, Bestellungen und Kosten. Mit diesen Berichten können Sie analysieren, wie viel Umsatz die einzelnen Kanal erbringen.

<!-- 

t_reports_marketing_channel.xml

 -->

See the [Marketing Channel](https://marketing.adobe.com/resources/help/de_DE/mchannel/index.html) help system for more information.

## Anomalieerkennungsbericht ausführen {#task_4808C96327354D789C075823F5C3A049}

Beschreibt, wie Sie die Diagramme für die Zusammenfassung und individuelle Metriken bei der Anomalieerkennung interpretieren.

<!-- 

t_anomaly_view.xml

 -->

Sehen Sie sich die neuen Funktionen für [Anomalieerkennung und Beitragsanalyse](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/anomaly_detection.html) in Analysis Workspace an!

**[!UICONTROL Reports]** > **[!UICONTROL Site Metrics]** > **[!UICONTROL Anomaly Detection]** .

>[!NOTE] Die Anomalieerkennung können Sie auch aus Projekten in Analysis Workspace ausführen. [Mehr …](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/anomaly_detection.html)

Informationen zum Einrichten der Anomalieerkennung finden Sie im [Referenzhandbuch](https://marketing.adobe.com/resources/help/de_DE/sc/user/index.html#Setting_up_Anomaly_Detection).

Die Anomalieerkennung zeigt zwei Diagrammtypen an: Ein Zusammenfassungsdiagramm und Diagramme zu einzelnen Metriken. Diagramme zu einzelnen Metriken werden nur angezeigt, wenn mindestens eine Anomalie für diese Metrik erkannt wurde.

<table id="table_88163CD8FC164342855D90D01F9C581A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Diagrammtyp </p> </th> 
   <th colname="col2" class="entry"> <p>Funktionsweise </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Zusammenfassungsdiagramm </p> <p><img placement="break"  src="assets/ad_summary_chart.png" width="570px" id="image_1CD4C4770BAA43C4AD7CBB824AD41338" /> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_D26DA3024CD7468291369F549557B28A"> 
      <li id="li_1C22B6E02FFB479FB71EFAD89EB37A4E">Jedes Feld stellt eine Anomalie dar, die pro Tag verfolgt wird und einer Metrik unten entspricht. </li> 
      <li id="li_8FC587D3FF4E452D83263CC7A10B6675">Grün zeigt Anomalien über der Trendlinie, blau unter der Trendlinie an. </li> 
      <li id="li_25135AB691BF443599AF2A3A60E2E71A">Gibt die Stärke der Anomalie an: Je größer die Anomalie, desto dunkler die Farbe des Datenpunkts und desto weiter entfernt von der Trendlinie. </li> 
      <li id="li_0C42AFA8897D420D8AB1A5D0F65B3B3A">Durch Klicken auf individuelle Anomalien wird das individuelle Metrikdiagramm dieser Anomalie (unterhalb des Zusammenfassungsdiagramms) nach oben gebracht. </li> 
      <li id="li_85C0F426952547B5A75D6BD31DE19CA5">Die Abweichungsprozentwerte (links vom Diagramm) werden wie folgt berechnet: 
       <ul id="ul_BEC0A88BFFAC4CF78BC9885FEB749694"> 
        <li id="li_1BAB2F50482745B69937DFAF1E09982E">Wenn die oberen Grenzen und der erwartete Wert identisch sind, beträgt die Abweichung in % 100 % </li> 
        <li id="li_CA48064F5788448C8646CCE196161237">Andernfalls ist die Abweichung in Prozent ((Istwert – oberer Grenzwert) / (oberer Grenzwert – erwarteter Wert)) * 100 </li> 
        <li id="li_4090357A0D214BC7B1C3DE0615875554">Wenn die unteren Grenzen und der erwartete Wert identisch sind, beträgt die Abweichung in Prozent –100% </li> 
        <li id="li_EF694E1A4E874ECD94E1E8F7302E494F">Andernfalls ist die Abweichung in Prozent ((unterer Grenzwert – Istwert) / (erwarteter Wert – unterer Grenzwert)) * –100 </li> 
       </ul> </li> 
      <li id="li_5C05EF7023484CC993E96D63E842B65C">Durch Klicken auf <span class="uicontrol">Anzeigen Segmente</span> wird die Segmentschiene eingeblendet, die es Ihnen ermöglicht, Segmente auf einen Anomalieerkennungsbericht anzuwenden. <a href="https://marketing.adobe.com/resources/help/de_DE/analytics/segment/"  > Weitere Informationen</a> zur Segmentierung. </li> 
      <li id="li_1B41CABF13D1407886C68EE3BC201E60">Durch Klicken auf <span class="uicontrol">Metriken bearbeiten</span> können Sie Metriken auswählen und die Auswahl für Metriken aufheben, für die Sie Anomalien erkennen möchten. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Diagramm für individuelle Metriken </p> <p><img placement="break"  src="assets/metric_report.png" width="570px" id="image_5BBECFD91CF14478AA4761E6256BBCB9" /> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_739C5687013743A29B63089FDA763F45"> 
      <li id="li_456A0BDA4D4E46CE9CC1C3DBAA1E2220">Zeigt abweichende Datenpunkte für einzelne Trendmetriken (einschließlich berechneter Metriken) als Punkte an. </li> 
      <li id="li_89FD847C65F04F48BCA7CD38D0EC51CD">Zeigt die neueste Anomalie oben und sortiert sekundär nach Anzahl der Anomalien. </li> 
      <li id="li_98B97A9706DE4455B8D8850904CBDE03">Zeigt eine durchgehende Linie an, um die aktuell erfassten Daten anzugeben. Dies wird mit der Prognose und der Fehlermarge verglichen, um abzuleiten, ob Datenpunkte abweichend sind. </li> 
      <li id="li_0EEA38DDDC344BF3879430E67D74EB72">Zeigt eine gepunktete Linie an, die eine auf historischen Daten basierende Prognose darstellt (d. h. den Schulungszeitraum). </li> 
      <li id="li_035BD2725D004AEDB630BF8DFF4DA4F3">Zeigt die oberen und unteren 95 % Konfidenzintervalle/Begrenzungen in einem grauen Farbton an. </li> 
      <li id="li_021A3D1F2EDB4319B9B39620EF1C038A">Ermöglicht das Reduzieren und Erweitern einzelner Berichte durch Klicken auf die Pfeilschaltflächen neben dem Metriknamen nach oben oder unten. </li> 
      <li id="li_722E4B9FC21047AC96D7B143197E293D">Ändert die Reihenfolge, in der die Metrikdiagramme angezeigt werden, indem auf Drilldowns im Übersichtsbericht reagiert wird (siehe oben) </li> 
      <li id="li_A2441169B185475AA68A64F81E6E40B8">Ermöglicht Ihnen das Filtern von Diagrammen anhand von Suchbegriffen, z. B. "Seite"für alle seitenbezogenen Metriken. </li> 
      <li id="li_F1BBBFCA8E2A43C29658E4FCAA36C904">Hier können Sie alle definierten Metriken oder nur solche mit Anomalien anzeigen. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anomalieerkennung einrichten {#task_AF347B34F56E44A6AE70E019B6EB2F08}

Schritte zur Auswahl von Report Suites, Metriken und Schulungs-/Anzeigezeiträumen für die Anomalieerkennung.

<!-- 

t_anomaly_config.xml

 -->

Sie richten die Anomalieerkennung unabhängig für jede Report Suite ein.

1. Navigieren Sie zu **[!UICONTROL Analytics > Reports > Site Metrics > Anomaly Detection]** .
1. Wählen Sie die Report Suite, für die Sie die tägliche Anomalieerkennung verfolgen möchten. Um eine Liste der Report Suites anzuzeigen, klicken Sie auf das Dropdown-Menü der Report Suite-Auswahl.
1. To select the metrics and/or define filtered metrics, click **[!UICONTROL Edit Metrics]** at the top right of the screen:  ![](assets/metrics_icon.png).

   Sie können Metriken aus der Liste mit allen Metriken (einschließlich berechneter Metriken) oder aus einer Liste mit verfolgten Metriken auswählen. Sie können auch nach bestimmten Begriffen filtern, um die Liste einzugrenzen. 1. Once the report has been generated, define the **[!UICONTROL Training Period]** and the **[!UICONTROL View Period]** for anomaly detection. (Den Schulungszeitraum kann man sich als „Lernzeitraum“ für den Algorithmus vorstellen.)

   ![](assets/view_training_periods.png)

   Bedenken Sie Folgendes:

* Der Schulungszeitraum endet unmittelbar vor dem Beginn der Ansicht.
* Die Standardeinstellung für beide Versionen ist 30 Tage und Sie können sie auf 60 oder 90 Tage verlängern.
* Durch die Verlängerung des Schulungszeitraums werden Ihre Daten in einen größeren Kontext gestellt und die Größe einer Anomalie kann verringert werden.

   Der Bericht zu Metriken zur Anomalieerkennung wird bei jeder Änderung eines Parameters aktualisiert.
1. (Optional) Apply segments to the report by clicking **[!UICONTROL Show Segments]** and selecting one or more existing segments or creating a new segment and applying it.

   ![](assets/ad_top_menu.png)

   Weitere Informationen zum Erstellen und Verwalten von Segmenten erhalten Sie im [Leitfaden zur Analysesegmentierung](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/). 1. (Optional) Fügen Sie den Bericht zu den Favoriten hinzu oder setzen Sie ein Lesezeichen.
1. (Optional) Ändern Sie das Enddatum des Anzeigezeitraums. Der Standardwert ist „Gestern“. 
1. Sie können den Bericht nun interpretieren. [Anzeigen von Diagrammen zur Anomalieerkennung](/help/analyze/reports-analytics/t-running-report-types.md#task_4808C96327354D789C075823F5C3A049).

## Echtzeitbericht ausführen {#task_5D25929C918E40B18965222FA94176B0}

Beschreibt, wie Sie Echtzeitberichte anzeigen und interpretieren.

<!-- 

reports_realtime.xml

 -->

**[!UICONTROL Reports > Site Metrics > Real-Time]** .

In Echtzeit-Berichte werden zwei Hauptberichte Angebot - ein Übersichtsbericht und ein Detailbericht. Sie bestehen jeweils aus einer Reihe von Reportlets.

Informationen zum Konfigurieren von Echtzeitberichten finden Sie im [Analytics-Referenzhandbuch](https://marketing.adobe.com/resources/help/de_DE/reference/index.html#RealTime_Reports_Configuration).

1. Take a look at the **[!UICONTROL Overview]** report and its components:  ![](assets/rtr_overview_report.png)

   <table id="choicetable_8586BECF55E843B2B5CD41205567EA32"> 
   <thead class="chhead sthead"> 
   <th class="choptionhd"> UI-Komponente </th> 
   <th class="chdeschd"> Beschreibung </th> 
   </thead> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Report Suite auswählen</strong></td> 
   <td class="chdesc stentry"> Zeigt die Report Suite an, die von diesem Echtzeitbericht behandelt wird. Informationen zum Ändern der Report Suite finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/reference/t_realtime_admin.html"  >Konfiguration von Echtzeitberichten </a>. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Zwischen Berichten wechseln</strong></td> 
   <td class="chdesc stentry"> Damit können Sie zwischen den eingerichteten Berichten (höchstens 3) wechseln. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Zeitraum wählen</strong></td> 
   <td class="chdesc stentry"> Damit können Sie den allgemeinen Zeitraum für alle Reportlets im Bericht wählen. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Berichte konfigurieren</strong></td> 
   <td class="chdesc stentry"> Dieser Zahnradsymbol-Link ist nur sichtbar, wenn Sie über Admin-Rechte verfügen. Wenn Sie darauf klicken, gelangen Sie zum Report Suite-Manager unter <span class="ignoretag"><span class="uicontrol">Admin Tools</span> &gt; <span class="uicontrol">Report Suites</span> &gt; <span class="uicontrol">Einstellungen bearbeiten</span> &gt; <span class="uicontrol">Echtzeit </span> </span>. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Vollbildansicht</strong></td> 
   <td class="chdesc stentry"> Das Symbol für die Vollbildansicht ist nur sichtbar, wenn Ihr Bildschirm auf ein bestimmtes Seitenverhältnis (entweder 16:9 oder 16:10) eingestellt ist UND wenn Ihr Browser die Vollbildansicht unterstützt. Beachten Sie, dass Sie keine Aktionen im Bildschirm ausführen können, während der Vollbildmodus aktiviert ist (drücken Sie <span class="uicontrol">Esc</span>, um diesen zu verlassen). Im Vollbildmodus kommt es zu keinen Timeouts. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Site-Traffic-Bericht</strong></td> 
   <td class="chdesc stentry"> Die Daten zur blauen Trendlinie zeigen die Traffic-Summe für die gesamte Site an. Die X-Achse verwendet wörtliche Beschriftungen (vor 15 Minuten, vor 10 Minuten), mit Ausnahme des aktuellen Ausdrucks, der als Echtzeitwert angezeigt wird. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Site-Summen-Reportlet</strong></td> 
   <td class="chdesc stentry"> Stellt eine Anzahl der Site-Gesamtwerte für die ausgewählte Metrik des Echtzeitberichts für die letzten N Minuten dar. "N"kann über die Zeitraumauswahl konfiguriert werden. <p>Die Farbe und Richtung des Pfeils basieren auf dem folgenden Algorithmus: 
      <ul id="ul_9F40CEA33798467393CB1266BB36D500"> 
      <li id="li_CCD01A44F912487DA5681EA50113643C">Signifikanter Gewinn (Pfeil nach oben): &gt; 100% </li> 
      <li id="li_7402491A9A614851B7F2AE0C77BD9A97">Gewinn (Pfeil nach oben rechts): zwischen 5 % und 100 % </li> 
      <li id="li_BCA79C08B5714D4B9315068112C66107"> Flach (Pfeil nach rechts): zwischen 5 % und -5 % </li> 
      <li id="li_234ECBD7D83A4AE680E4A70BF288681F"> Verlust (Pfeil nach unten rechts): zwischen -5 % und -100 % </li> 
      <li id="li_10C5EA8803604C1CA714D3DB27478B31"> Erheblicher Verlust (Pfeil nach unten): &lt; -100% </li> 
      </ul> </p> <p>Wenn der Site-Gesamtwert in "Instanzen"angegeben wird, spiegeln diese Instanzen die Dimension im primären Reportlet wider. Wenn ein instanzspezifischer Name vorhanden ist (z. B. "Seitenbenennung"), wird dieser Name vom Site-Gesamtwert gemeldet. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Primäres Reportlet</strong></td> 
   <td class="chdesc stentry"> Bericht für die primäre Dimension des Echtzeitberichts und seine Metrik. Zeigt eine Trendlinie für dieses Element für den ausgewählten Zeitraum an. Der Metrikgesamtwert stellt die Summe für die vollständige Trendlinie dar. Der Pfeil zeigt an, ob das Element stark gewinnt, gewinnt, flach, verloren geht oder stark verliert. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Suchdialogfeld</strong></td> 
   <td class="chdesc stentry"> Die Suche wirkt sich auf alle Reportlets aus. Die Suche bleibt bei der Ansicht des Berichts bestehen. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Sortieren nach... Beliebteste/Gewinner/Verlierer</strong></td> 
   <td class="chdesc stentry"> Sie können zwischen der Sortierung nach <span class="uicontrol">Beliebteste</span> (Standard), <span class="uicontrol">Gewinner</span> (Dimensionen mit dem größten Wachstum) und <span class="uicontrol">Verlierer</span> (Dimension mit einem Trend nach unten) umschalten. <p>Hier finden Sie die Formel, mit der Gewinner oder Verlierer bestimmt werden: Das früheste Beispiel wird über eine einfache Berechnung der Prozentsatzänderung mit dem vorletzten Beispiel verglichen. Wenn also „Letzte 15 Minuten“ gewählt ist und n die aktuelle Minute darstellt, wird n-1 mit n-15 verglichen. Die Gewichtung erfolgt derzeit nicht in Echtzeit. Die aktuelle Minute wird ignoriert, weil sie nicht vollständig ist und wahrscheinlich eine Änderung in % bewirken würde. </p> <p>Diese Formel ist für alle im Echtzeitbericht verwendeten Metriken konsistent. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Sekundäres 1 Reportlet</strong></td> 
   <td class="chdesc stentry"> Stellt Echtzeitberichte für die Dimension des zweiten bereitgestellten Berichts und für die Metrik dar. <p>Das sekundäre 1 Reportlet zeigt die ersten 4 Kategorien an. die fünfte ist eine Aggregation aller verbleibenden Werte. Für jede Kategorie wird die gesamte Rohdaten-Ansicht dieser Kategorie bereitgestellt. Außerdem wird die Summe für alle Kategorien in der Mitte angezeigt. </p> <p> Wenn Sie den Mauszeiger über einen Abschnitt bewegen, wird die zugehörige Kategorie hervorgehoben und die Trendlinie der Kategorie unter dem Donut angezeigt. </p> <p> Wenn Sie den Mauszeiger über ein Zeilenelement bewegen, wird der Zeileneintrag sowie der zugehörige Abschnitt hervorgehoben und die Trendlinie der Kategorie unter dem Donut angezeigt. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>Sekundäres 2 Reportlet</strong></td> 
   <td class="chdesc stentry"> Stellt Echtzeitberichte für die Dimension des dritten bereitgestellten Berichts und für die Metrik dar. Wenn Sie den Mauszeiger über die Elementbeschriftung bewegen, wird die Beschriftung nach rechts verschoben und eine Trendlinie für das mit dem Mauszeiger versehene Element eingeblendet. </td> 
   </tr> 
   </table>

1. Click a list item in the Primary Reportlet to launch the **[!UICONTROL Details]** view for that list item:  ![](assets/rtr_detail_report.png)

   | **Elementtrend-Reportlet** | Stellt die Trendlinie des Elements dar, das im Übersichtsbericht für die letzten N Minuten ausgewählt wurde. N kann über die Zeitraumauswahl konfiguriert werden. |
   |---|---|
   | **Reportlet insgesamt** | Stellt eine Gesamtmetrikanzahl für das Element dar, das im Übersichtsbericht für die letzten N Minuten ausgewählt wurde. N kann über die Zeitraumauswahl konfiguriert werden. |
   | **Korreliertes sekundäres 1 Reportlet** | Dieses Reportlet ist dem sekundären 1 Reportlet sehr ähnlich. Der einzige Unterschied ist die Datenquelle, mit der dieser Bericht gefüllt wird: In diesem Beispiel wird die Korrelation (oder Aufschlüsselung) zwischen einer bestimmten Seite (die Sie im primären Reportlet des Übersichtsberichts ausgewählt haben) und den angezeigten Instanzen angezeigt. |
   | **Korreliertes sekundäres 2 Reportlet** | Dieses Reportlet ist dem sekundären 2 Reportlet sehr ähnlich. Der einzige Unterschied ist die Datenquelle, mit der dieser Bericht gefüllt wird: In diesem Beispiel wird die Korrelation (oder Aufschlüsselung) zwischen einer bestimmten Seite (die Sie im primären Reportlet des Übersichtsberichts ausgewählt haben) und der Sprachdimension angezeigt. |
