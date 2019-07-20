---
description: 'null '
seo-description: 'null '
seo-title: FAQ zu Attribution IQ
title: FAQ zu Attribution IQ
uuid: 09961172-869 d -4 ed 3-aba 5-52374 e 53 b 603
translation-type: tm+mt
source-git-commit: ab2cda6d10bfeee13262581578bcdb4746112296

---


# FAQ zu Attribution IQ

<table id="table_590341C2F0DA4511ADEFDC1DB49CD248"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>F: Warum wird in den neuen Attributionsmodellen dem Zeileneintrag „Keine“ manchmal ein größerer Anteil zugeordnet als erwartet?</b> </p> </td> 
   <td colname="col2"> <p>A: Der Grund liegt wahrscheinlich im von Ihnen ausgewählten Berichtsfenster, das <a href="../../../analyze/analysis-workspace/attribution-iq/attribution.md#section_BC71DA030E45487AA3C3F6ED247A3C4A" format="dita" scope="local">hier</a> beschrieben wird . Dies tritt normalerweise auf, wenn Ihr Berichtsfenster am ersten Tag des Monats beginnt und Sie ein Besucher-Lookback (Berichtsfenster) verwenden. Um zusätzliche Attributions-Lookback-Werte zu erfassen (und den Wert im Zeileneintrag „Keine“ zu reduzieren), geben Sie im Berichtsfenster einen längeren Zeitraum ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Es werden manchmal Datumswerte außerhalb meines Berichtsfensters in meinem Bericht angezeigt, wenn Attributionsmodelle verwendet werden. Warum?</b> </p> </td> 
   <td colname="col2"> <p>A: Diese zusätzlichen Datumswerte sind ein Artefakt des <a href="../../../analyze/analysis-workspace/attribution-iq/attribution.md" format="dita" scope="local">hier</a> beschriebenen Lookback-Fensters für die Besucherberichterstellung . Im Artikel <a href="https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html" format="html" scope="external">Data appearing outside reporting window</a> (Außerhalb des Berichtsfensters angezeigte Daten) wird erläutert, weshalb dies derzeit passiert. Adobe Analytics wird diese zusätzliche Zeilen in einer künftigen Version herausfiltern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Kann ich ein benutzerdefiniertes Lookback-Fenster mit meinen Attributionsmodellen verwenden?</b> </p> </td> 
   <td colname="col2"> <p>A: Currently, attribution models rely on either a visitor or visit lookback window - but either of these lookback windows are adjustable by either changing the reporting date range (for visitor lookback) or by using a custom visit definition as part of Virtual Report Suites and <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-mobile-visit-processing.html" format="html" scope="external"> Context-Aware Sessions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Wann sollte ich einen Attributions-Lookback vom Typ „Besuch“ anstelle eines Attributions-Lookbacks vom Typ „Besucher“ verwenden?</b> </p> </td> 
   <td colname="col2"> <p>A: Die Auswahl des Attributions-Lookbacks hängt von Ihrem Anwendungsfall ab. Wenn Ihre Konversion in der Regel einen längeren Berücksichtigungszyklus aufweist (etwas, was länger dauert als ein einzelner Besuch), sollten Sie einen Besucher-Lookback verwenden oder eine VRS-Instanz mit einem längeren Besuch erstellen, der den Berücksichtigungszyklus genauer widerspiegelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Stehen Attributionsmodelle in „Datenfeeds“ oder in „Data Warehouse“ zur Verfügung?</b> </p> </td> 
   <td colname="col2"> <p>A: Nein. Da Attributionsmodelle zur Berichtszeit mit <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">Berichtszeitverarbeitung</a> berechnet werden, können sie weder in „Datenfeeds“ noch in „Data Warehouse“ berücksichtigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Stehen Attributionsmodelle nur dann zur Verfügung, wenn ich Virtual Report Suite mit aktivierter Berichtszeitverarbeitung verwende?</b> </p> </td> 
   <td colname="col2"> <p>A: Nein. Obwohl Attributionsmodelle die <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">Berichtszeitverarbeitung</a> im Backend verwenden, stehen sie aus Gründen der Benutzerfreundlichkeit in VRS und in Suites mit Basisberichten zur Verfügung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Unterstützt Attribution IQ in Analysis Workspace ein datengesteuertes oder Algorithmusattributionsmodell?</b> </p> </td> 
   <td colname="col2"> <p>A: Dieses steht in Analysis Workspace derzeit nicht zur Verfügung, wird jedoch aktiv in Angriff genommen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Werden irgendwelche Abmessungen oder Metriken durch Attribution IQ nicht unterstützt?</b> </p> </td> 
   <td colname="col2"> <p>A: Zuordnungs-IQ wird für alle Dimensionen unterstützt.</p> 
    <p><u>Nicht</u> unterstützte Metriken (primär, weil sie keinen Sinn ergeben): </p> 
    <ul id="ul_B12A1291DEEF41FDBAD110C4A9265234"> 
     <li id="li_245571C5377C45ADBAE6F735B91FCD1F"> Unique Visitors </li> 
     <li id="li_000CA7680A0745D9860CA7D5F62288D4">Besuche </li> 
     <li id="li_53CAD3ECAE54451BBB0750FB62AF1243">Vorfälle </li> 
     <li id="li_C589008CA92E4C69866E85EEEC88EF90"> Seitenansichten </li> 
     <li id="li_ACF8D24E3AC746E280DB0F71D4B772A3">A4T-Metriken </li> 
     <li id="li_78BFE0A4F8024301A218C0415537F632">Besuchszeitmetriken </li> 
     <li id="li_29774EEFE9A04759B7929EA35AA9BEAD">Absprünge </li> 
     <li id="li_B163C6F24240465F85AB5C9792F0F013">Absprungrate </li> 
     <li id="li_CF065E227A634C77BC2C48C2A6EC849A">Einstiege </li> 
     <li id="li_ED962C5063B047F185EFC58EB43C661F">Ausstiege </li> 
     <li id="li_029F6D09433F48A38303E5C96E77480B">Seiten nicht gefunden </li> 
     <li id="li_8410AF29208247B5B3E49F72208913BA">Suchvorgänge </li> 
     <li id="li_8421F1D5F58148D98B1AB5C04FCCA9CF">Einzelseitenbesuche </li> 
     <li id="li_50D4EA0FF2E6438C8DD2A1B2EAD7B9D7">Einzelzugriff </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Inwiefern unterscheidet sich Attribution IQ von der Attribution in Data Workbench?</b> </p> </td> 
   <td colname="col2"> <p>A: Data Workbench bietet stufenweise Folgendes: </p> 
    <ul id="ul_5A8C979CDCD04FF5B9625C84B2678CC7"> 
     <li id="li_115DC58D4BDF40A4A0036E76F6E64158">Die Fähigkeit, eine Attribution über weitere Datenquellen auf Besucherebene vorzunehmen, beispielsweise Anzeigenimpressionen und Point of Sale. </li> 
     <li id="li_C31891A4D5594D93AF97340F6D3A2E3E">Algorithmusmodellierung (<a href="https://marketing.adobe.com/resources/help/en_US/insight/client/c_attrib_algorithmic.html" format="html" scope="external">beste Anpassung</a>). Attribution IQ umfasst nur regelbasierte Modelle. </li> 
     <li id="li_749D5D11B34E40E9AB53908A38979CAA">Zusätzliche Visualisierungen, beispielsweise <a href="https://marketing.adobe.com/resources/help/en_US/insight/client/c_lat_tbls.html" format="html" scope="external">Wartezeittabellen </a>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Funktioniert Attribution IQ mit Datenquellen?</b> </p> </td> 
   <td colname="col2"> <p>A: Im Moment funktioniert Attribution IQ nur mit Datenquellen, die nicht auf Zusammenfassungsebene vorhanden sind. </p> <p> Da Datenquellen auf Zusammenfassungsebene mit keiner Analytics-Besucherkennnung verknüpft werden können, ist keine erweiterte Attribution möglich. Als Datenquellen werden auch Transaktions-IDs unterstützt, es sei denn sie werden in einer Virtual Report Suite mit aktivierter <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">Berichtszeitverarbeitung</a> verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>F: Funktioniert Attribution IQ mit der <a href="https://marketing.adobe.com/resources/help/en_US/analytics/advertising/overview.html" format="html" scope="external">Advertising Analytics</a>-Integration?</b> </p> </td> 
   <td colname="col2"> <p>A: Die integrierten Metriken – also Impressionen, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung – sind Datenquellen auf Zusammenfassungsebene und daher inkompatibel mit Attribution IQ. Doch die Metadatendimensionen (z. B. Übereinstimmungstyp und Keyword) funktionieren mit der Attribution, wenn sie mit standardmäßigen Analytics-Ereignissen oder -Metriken verwendet werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

