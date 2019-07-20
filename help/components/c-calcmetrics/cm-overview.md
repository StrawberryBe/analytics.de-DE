---
description: Berechnete und erweiterte berechnete (abgeleitete) Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.
keywords: Berechnete Metriken; Abgeleitete Metriken; Erweiterte berechnete Metriken
seo-description: Berechnete und erweiterte berechnete (abgeleitete) Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.
seo-title: Berechnete und erweiterte berechnete (abgeleitete) Metriken
title: Berechnete und erweiterte berechnete (abgeleitete) Metriken
uuid: 2553 c 115-b 15 a -4109-8 de 2-733 dbc 1 eeb 9 e
translation-type: tm+mt
source-git-commit: fb27d500a725a540e632952295aa2ea3a3a21fb6

---


# Berechnete und erweiterte berechnete (abgeleitete) Metriken

Berechnete und erweiterte berechnete (abgeleitete) Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.

>[!IMPORTANT]
>
>In July 2018, Adobe introduced [Attribution IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html), which revised the way allocation models in calculated metrics are evaluated. Im Rahmen dieser Änderung wurden berechnete Metriken, die ein nicht standardmäßiges Zuordnungsmodell verwenden, zu neuen, verbesserten Zuordnungsmodellen migriert:
>
>* Die Zuordnungsmodelle "Marketingkanal Last Touch" und" Marketingkanal First Touch" wurden in neue Zuordnungsmodelle für Last Touch und First Touch migriert (Hinweis: " Marketingkanäle" wurde nicht mehr unterstützt - es wurden nur die beiden Zuordnungsmodelle in berechneten Metriken angezeigt.
>* Darüber hinaus haben wir korrigiert, wie die lineare Zuordnung berechnet wird. Wenn Kunden berechnete Metriken mit linearen Zuordnungsmodellen verwenden, können sich die Berichte geringfügig ändern, um das neue, korrigierte Attributionsmodell widerzuspiegeln. This change to calculated metrics is reflected in [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], the Reporting API, Report Builder, and Ad Hoc Analysis. Weitere Informationen finden Sie unter [Wie die lineare Zuordnung ab 19. Juli 2018 funktioniert](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1).


Mit unseren Werkzeugen für berechnete Metriken können Sie Metriken auf flexiblere Weise erstellen, verwalten und kuratieren. They allow you as marketers, product managers and analysts to ask questions of the data without having to change your [!DNL Analytics] implementation. The custom metrics available in each [!DNL Analytics] package are:

* Adobe [!DNL Analytics] Foundation: Calculated
* [Adobe Analytics Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html): Berechnet  + Erweitert berechnet
* [Adobe Analytics Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html): Berechnet + erweitert berechnet
* [Adobe Analytics Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html): Berechnet + erweitert berechnet

Hier sehen Sie einen Vergleich zwischen den jeweiligen Möglichkeiten, die berechnete und erweiterte berechnete Metriken bieten:

| Generatoroptionen | Berechnete Metriken | Erweiterte berechnete (abgeleitete) Metriken |
|---|---|---|
| [Formatarten (Dezimal, Zeit, Prozent, Währung)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#concept_5EC82A91EB9C44FC870326C85F9D0B18) | Ja | Ja |
| [Attributionsänderung (Standard, Linear, Teilnahme etc.)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#concept_B7A1FCFEFA9D4C4883208ACE8C9C8E5E) | Ja | Ja |
| [Metriktypen (Standard, Total)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#concept_B7A1FCFEFA9D4C4883208ACE8C9C8E5E) | Ja | Ja |
| Grundrechenarten (Addieren, Subtrahieren, Multiplizieren, Dividieren) | Ja | Ja |
| [Segmente anwenden](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md#concept_21C77BD86E7E45E79AF030D8ED54DB3E) | Nein | Ja |
| [Allgemeine Funktionen (Zählen, Anzeigenwert, Mittel etc.)](../../components/c-calcmetrics/cm-reference/cm-functions.md#concept_E3022D5EEEE145B69A23438BAF7016B2) | Nein | Ja |
| [Erweiterte Funktionen (Regression, Wenn-Dann, T-Transformation etc.)](../../components/c-calcmetrics/cm-reference/cm-adv-functions.md#concept_A5FB9127D70F4E1AA02D1ACBF4F54174) | Nein | Ja |

## Funktionen {#section_A0A5C275B68A4D628950BBB0B1EE631F}

Sie können

* Create metrics across [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], [!UICONTROL Ad Hoc Analysis], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection], and [!UICONTROL Contribution Analysis].
* Segmentierte Metriken erstellen, die zur Berichtslaufzeit abgeleitet werden, [ohne die Implementierung ändern zu müssen](https://youtu.be/CuQTm9RaUpY). Diese Metriken können historisch angezeigt werden, da sie auf Segmenten basieren.
* Metriken über Report Suites hinweg freigeben. Das bedeutet, dass alle neu erstellten Metriken für alle Report Suites in demselben Anmeldeunternehmen gelten.
* (Nur erweiterte berechnete Metriken) Segmente für Metriken. Sie können beispielsweise eine Metrik für „Neue Besucher“ erstellen, mit der Personen gezählt werden, für die dies die erste Sitzung ist.
* (Nur erweiterte berechnete Metriken) Statistische Funktionen miteinbeziehen, um Daten besser beschreiben zu können. Sie könnten beispielsweise die Elemente in einem Bericht zählen oder die Anzahl der Standardabweichungen für jedes Element addieren.
* Utilize metrics created in [!UICONTROL Ad Hoc Analysis] in the other [!DNL Analytics] tools and vice versa.

   >[!NOTE]
   >
   >Sie können weiterhin Metriken in Ad-hoc-Analysen erstellen. Die Benutzeroberfläche des dortigen Generators für berechnete Metriken ähnelt jetzt dem neuen Generator für Metriken.

## Einschränkungen {#section_CB878B02451541D68A68B508D4DBD19A}

Some [!DNL Analytics] features let you use events but not calculated metrics:

* Trichter in Reports &amp; Analytics
* Fallout in Analysis Workspace
* [!UICONTROL Kohortenanalyse in Analysis Workspace]
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segmente]
* [!UICONTROL Echtzeitberichte]
* [!UICONTROL Aktuelle Datenberichte]
* [!DNL Analytics] for [!DNL Target]

## Tools {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Here is a short overview of the [!UICONTROL Calculated Metrics] tools:

<table id="table_520AFE97DB514958ABE23FD3C9CE0ABD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tool </th> 
   <th colname="col2" class="entry"> Funktionen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#concept_5EC82A91EB9C44FC870326C85F9D0B18" format="dita" scope="local"> Aufbau berechneter Metriken</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E6F02AB9DF204C2F9A0AC92A31594B3E"> 
     <li id="li_A4A6E716374243A190C539A3F4A41C0C">Erstellen Sie einfache berechnete Metriken oder erweiterte berechnete Metriken mit erweiterten Zuordnungsmodellen. </li> 
     <li id="li_C8C97BA4E227463E98077ABA5818FFC6">Segmente inline zu Metrik-Formeln hinzufügen. </li> 
     <li id="li_8503D9E06A3C46569B5CDB4B90F72446">Segmente in einem Bericht vergleichen (beispielsweise lokale Besucher mit internationalen Besuchern vergleichen) </li> 
     <li id="li_4B528FDE1F96400DBA0D3276408FF919">Statistische Funktionen verwenden </li> 
     <li id="li_C1162B1EA6784B8189A8A87E2B0DA79A">Detaillierte Metrikbeschreibungen angeben (was die Metrik macht, wo sie verwendet werden sollte, wo sie NICHT verwendet werden sollte) </li> 
     <li id="li_DEA13F5E8BF94AF1B311C467FE6E2A74">Definitionen in neue Metriken kopieren </li> 
     <li id="li_8C21F55015D44910904202D2BF74221C">Eine Inline-Metrikvorschau bereitstellen </li> 
     <li id="li_3704F66C321C477F9D4F52E068C231BD">Die Metrikpolarität festlegen, die angibt, ob es gut oder schlecht ist, wenn ein bestimmtes benutzerspezifisches Ereignis (eine Metrik) steigt </li> 
     <li id="li_9D45319FA965476FB1C90DE8AA72BBD7">Metriken taggen </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="../../components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md#concept_BA6815CB06D842D5825766396B691653" format="dita" scope="local"> Berechnete Metrik – Manager</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E4D20D5DD3904CC6A85785B5BD4C1B1E"> 
     <li id="li_E0B216BA1478406EB6212263DF71D85B">Metriken für andere freigeben </li> 
     <li id="li_96EB16FAF3454211AAEF78EA5B08927F">Metriken genehmigen und kuratieren </li> 
     <li id="li_3ADBD2428EAC4B0AA61222D87C3AF2B7">Metriken organisieren (taggen), damit sie von Benutzern gefunden werden können </li> 
     <li id="li_726F3C3390744E49BA63606FE196880E">Metriken löschen </li> 
     <li id="li_F306BA4FA8AF4A6E987BA62634659A2F">Metriken umbenennen </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Leiste „Metrikauswahl“ </td> 
   <td colname="col2"> <p>Replaces the <span class="uicontrol"> Show Metrics</span> popup in [!UICONTROL Reports &amp; Analytics]. </p> <p>Damit können Sie auch Metriken suchen und diese dem Bericht hinzufügen bzw. darauf anwenden. Außerdem können Sie die <a href="../../components/c-calcmetrics/c-workflow/cm-workflow/cm-finding.md#concept_A09845053A934CB7B755391D76E76C08" format="dita" scope="local">Sortierfolge</a> ändern (Optionen sind: Alphabetisch, Empfohlen, Häufig verwendet, Kürzlich verwendet). Darüber hinaus können Sie nach Report Suites filtern, um nur Metriken anzuzeigen, die in einer bestimmten Report Suite erstellt wurden. </p> <p>Um auf diese Metrikauswahl zuzugreifen, klicken Sie auf das Metriksymbol <img placement="inline"  src="assets/metrics_icon.png" width="30px" id="image_2C6F20B4E634486B95BACD4CA47EF991" /> auf der linken Seite eines Berichts. Die Metrikauswahl sieht wie folgt aus: </p> <p><img placement="break" align="center"  src="assets/metrics_rail.png" width="200px" id="image_379523E9AFEC4CF08D20C42C740AA358" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/README.md" format="https" scope="external"> API für berechnete Metriken</a> </td> 
   <td colname="col2"> <p>Teil des Adobe Analytics 2.0-API-Satzes. </p> </td> 
  </tr> 
 </tbody> 
</table>

