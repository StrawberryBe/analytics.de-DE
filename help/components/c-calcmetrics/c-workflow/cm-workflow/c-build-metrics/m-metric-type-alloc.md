---
description: Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Attributionsmodell angeben.
seo-description: Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Attributionsmodell angeben.
seo-title: Metriktyp und Attribution
title: Metriktyp und Attribution
uuid: 64649698-df 2 a -42 c 3-bb 31-938 f 766 e 1 d 1 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Metriktyp und Attribution

Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Attributionsmodell angeben.

* [Metriktyp](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_34A86FB402F94E988724232283BF18B7)
* [Spaltenattributionsmodell](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_F9690FD1943B403AB28E2FAC54EFE032)
* [Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018)](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1)

## Metriktyp {#section_34A86FB402F94E988724232283BF18B7}

![](assets/cm_type_alloc.png)

| Metriktyp | Definition |
|---|---|
| Standard | These metrics are the same metrics used in standard [!DNL Analytics] reporting. Wenn eine Formel aus einer einzelnen Standardmetrik besteht, zeigt sie die gleichen Daten wie das nicht berechnete Metrikgegenstück an. Standardmetriken eignen sich zum Erstellen berechneter Metriken, die speziell für die einzelnen Einzelposten gelten. [Bestellungen] / [Besuche] nehmen beispielsweise Bestellungen für diesen Einzelposten auf und dividiert sie durch die Anzahl der Besuche für diesen Einzelposten. |
| Gesamt | Verwenden Sie den Gesamtwert für den Berichtszeitraum in jedem Einzelposten. Wenn eine Formel aus einer einzelnen Gesamtmetrik besteht, zeigt sie dieselbe Gesamtzahl für jeden Einzelposten an. Gesamtmetriken eignen sich für die Erstellung berechneter Metriken, die mit den Gesamtdaten der Site verglichen werden. For example, [Orders] / [Total Visits] shows the proportion of orders against ALL visits to your site, not just the visits to the specific line item. |

## Spaltenattributionsmodell {#section_F9690FD1943B403AB28E2FAC54EFE032}

>[!IMPORTANT]
>
>In July 2018, [!DNL Analytics] introduced [Attribution IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html), which revised the way allocation models in calculated metrics are evaluated. Im Rahmen dieser Änderung wurden berechnete Metriken, die ein nicht standardmäßiges Zuordnungsmodell verwenden, zu neuen, verbesserten Zuordnungsmodellen migriert:
>
>* Eine vollständige Liste der unterstützten nicht standardmäßigen Modelle und Lookback-Fenster finden Sie in der Dokumentation zu [Attribution IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html).
>* Die Zuordnungsmodelle „Marketingkanal – Letztkontakt“ und „Marketingkanal – Erstkontakt“ werden in das neue „Letztkontakt“- bzw. in das „Erstkontakt“-Attributionsmodell migriert. (Hinweis: Marketing-Kanäle werden nicht veraltet sein, sondern lediglich die beiden Zuordnungsmodelle, die in berechneten Metriken erscheinen).
>* Darüber hinaus wird die Methode zur Berechnung der linearen Zuordnung korrigiert. Wenn Kunden berechnete Metriken mit linearen Zuordnungsmodellen verwenden, können sich die Berichte geringfügig ändern, um das neue, korrigierte Attributionsmodell widerzuspiegeln. This change to calculated metrics will be reflected in Analysis Workspace, [!UICONTROL Reports &amp; Analytics], the Reporting API, Report Builder, and Ad Hoc Analysis. Weitere Informationen finden Sie unter [Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018)](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1).
>



## Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018) {#section_EDBB2E14A6C248C5A79C0913C02D7CA1}

Im Juli 2018 hat Adobe geändert, wie die lineare Zuordnung für berechnete Metriken gemeldet wird. This change impacts Analysis Workspace, Ad Hoc Analysis, [!UICONTROL Reports &amp; Analytics], Report Builder, Activity Map, and the Reporting APIs. Die Änderung betrifft in erster Linie eVars und andere Dimensionen mit Persistenz. Note that these changes will only apply to calculated metrics and will not impact other reports using linear allocation (such as the Pages report in [!UICONTROL Reports &amp; Analytics]). Andere Berichte, die die lineare Zuordnung verwenden, werden weiter die aktuelle Methode zur linearen Zuordnung verwenden.

Im folgenden Beispiel soll illustriert werden, wie sich berechnete Metriken mit linearer Zuordnung beim Reporting ändern:

<table id="table_E66D066A3E7B4232BBC220775F8B985A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Treffer 1 </th> 
   <th colname="col3" class="entry"> Treffer 2 </th> 
   <th colname="col4" class="entry"> Treffer 3 </th> 
   <th colname="col5" class="entry"> Treffer 4 </th> 
   <th colname="col6" class="entry"> Treffer 5 </th> 
   <th colname="col7" class="entry"> Treffer 6 </th> 
   <th colname="col8" class="entry"> Treffer 7 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Eingereichte Daten </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> - </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> - </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10 USD </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Letztkontakt-eVar </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> PROMO A </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> PROMO B </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10 USD </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erstkontakt-eVar </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> PROMO A </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO A </td> 
   <td colname="col6"> PROMO A </td> 
   <td colname="col7"> PROMO A </td> 
   <td colname="col8"> 10 USD </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beispieleigenschaft </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> - </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> - </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10 USD </td> 
  </tr> 
 </tbody> 
</table>

In diesem Beispiel wurden die Werte A, B und C in eine Variable für die Treffer 1, 3, 4 und 6 gesendet, bevor ein Kauf in Höhe von 10 USD bei Treffer 7 getätigt wurde. In der zweiten Zeile werden dieses Werte bei Treffern auf Grundlage von Letztkontaktbesuchen gespeichert. In der dritten Zeile wird das Speichern auf Grundlage des Erstkontaktbesuchs dargestellt. Zu guter Letzt stellt die letzte Zeile dar, wie Daten aus einer Eigenschaft aufgezeichnet würden, bei denen kein Speichern vorgesehen ist.

**Zusammenfassung der Funktionsweise der linearen Zuordnung vor Juli 2018**

Vor dem 19. Juli 2018 wurde die lineare Attribution berechnet, nachdem die Erst- bzw. Letztkontakt-Persistenz bereits erfolgt war. Gemäß dem Letztkontakt-eVar wurden die 10 USD daher wie folgt verteilt: A = 10 x (3/6) = 5 USD, B = 10 x (2/6) = 3,33 USD, C = 10 x (1/6) = 1,67 USD.

Gemäß dem oberen Erstkontakt-eVar würden alle 10 USD-Beträge zu A gegeben. Für die Eigenschaft: A = 10 x (2/4) = 5 USD, B = 10 x (1/4) = 2,50 USD und C = 10 x (1/4) = 2.50 USD. Um die frühere Funktionsweise der linearen Zuordnung zusammenzufassen:

| Werte | Aktueller Letztkontakt-eVar | Aktueller Erstkontakt-eVar | Aktuelle Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00 USD | 10,00 USD | 5,00 USD |
| PROMO B | 3,33 USD | 0 USD | 2,50 USD |
| PROMO C | 1,67 USD | 0 USD | 2,50 USD |
| Gesamt | 10,00 USD | 10,00 USD | 10,00 USD |

**Zusammenfassung der Funktionsweise der linearen Zuordnung ab 19. Juli 2018**

Nach dem 19. Juli wurde dieses Verhalten in berechneten Metriken korrigiert. Instead of using the persisted values based on last touch or first touch, [!DNL Analytics] now uses only the values that were passed in (the first row of the top table). Daher haben die Dimensions-Zuordnungseinstellungen keinen Einfluss mehr darauf, wie die lineare Zuordnung berechnet wird (d. h. Eigenschaften und eVars werden gleich behandelt), und die Ergebnisse spiegeln wider, was ursprünglich übertragen wurde, statt der möglicherweise gespeicherten Erst- bzw. Letztkontaktwerte. In allen drei Fällen gilt dann: A = 10 x (2/4) = 5 USD, B = 10 x (1/4) = 2,50 USD und C = 10 x (1/4) = 2,50 USD.

| Werte | Neuer Letztkontakt-eVar | Neuer Erstkontakt-eVar | Neue Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00 USD | 5,00 USD | 5,00 USD |
| PROMO B | 2,50 USD | 2,50 USD | 2,50 USD |
| PROMO C | 2,50 USD | 2,50 USD | 2,50 USD |
| Gesamt | 10,00 USD | 10,00 USD | 10,00 USD |

<!-- 

<p>Additionally, as part of this change, [!DNL Analytics] is <b>changing how multiple sequential successes</b> are treated. In the following example, 7 hits occurred in the same visit with two orders, one $10 order on hit 4, and one $5 order on hit 7: </p> 
<table id="table_4647AA466D1447F6961DDC10468FCCE1"> 
 <tgroup cols="8">
  <colspec colnum="1" colname="col1" colwidth="1.00*" />
  <colspec colnum="2" colname="col2" colwidth="1.04*" />
  <colspec colnum="3" colname="col3" colwidth="1.02*" />
  <colspec colnum="4" colname="col4" colwidth="1.02*" />
  <colspec colnum="5" colname="col5" colwidth="1.03*" />
  <colspec colnum="6" colname="col6" colwidth="1.02*" />
  <colspec colnum="7" colname="col7" colwidth="1.02*" />
  <colspec colnum="8" colname="col8" colwidth="1.03*" />
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> </th> 
    <th colname="col2" class="entry"> Hit 1 </th> 
    <th colname="col3" class="entry"> Hit 2 </th> 
    <th colname="col4" class="entry"> Hit 3 </th> 
    <th colname="col5" class="entry"> Hit 4 </th> 
    <th colname="col6" class="entry"> Hit 5 </th> 
    <th colname="col7" class="entry"> Hit 6 </th> 
    <th colname="col8" class="entry"> Hit 7 </th> 
   </tr>
  </thead> 
  <tbody> 
   <tr> 
    <td colname="col1"> <p>Data Sent In </p> </td> 
    <td colname="col2"> PROMO A </td> 
    <td colname="col3"> - </td> 
    <td colname="col4"> PROMO B </td> 
    <td colname="col5"> $10 </td> 
    <td colname="col6"> - </td> 
    <td colname="col7"> PROMO C </td> 
    <td colname="col8"> $5 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p>Last Touch eVar </p> </td> 
    <td colname="col2"> PROMO A </td> 
    <td colname="col3"> PROMO A </td> 
    <td colname="col4"> PROMO B </td> 
    <td colname="col5"> $10 </td> 
    <td colname="col6"> PROMO B </td> 
    <td colname="col7"> PROMO C </td> 
    <td colname="col8"> $5 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p>First Touch eVar </p> </td> 
    <td colname="col2"> PROMO A </td> 
    <td colname="col3"> PROMO A </td> 
    <td colname="col4"> PROMO A </td> 
    <td colname="col5"> $10 </td> 
    <td colname="col6"> PROMO A </td> 
    <td colname="col7"> PROMO A </td> 
    <td colname="col8"> $5 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p>Example prop </p> </td> 
    <td colname="col2"> PROMO A </td> 
    <td colname="col3"> - </td> 
    <td colname="col4"> PROMO A </td> 
    <td colname="col5"> $10 </td> 
    <td colname="col6"> - </td> 
    <td colname="col7"> PROMO C </td> 
    <td colname="col8"> $5 </td> 
   </tr> 
  </tbody> 
 </tgroup> 
</table> 
<p> </p> 
<p>Currently (<b>prior to July 19, 2018</b>), linear attribution would carry forward past the initial conversion and persist into the second conversion </p> 
<ul id="ul_FD09813B59F04FF2A96A70BBE0A8F349"> 
 <li id="li_2EC965DDAE334C1795530F7C6F1674C5">In our first-touch eVar example, the total revenue for each promotion would be calculated using the promos prior to conversion on hit 4 for revenue on hit 4, but all promos for the conversion on hit 7. </li> 
 <li id="li_687C03C4B0A941AA800084F324A95FD6">In our last-touch eVar example, this would be: A = (2/3) * 10 + (2/5) * 5 = $8.66, B = (1/3) * 10 + (2/5) * 5 = $5.33, C = (1/5) * 5 = $1.00. In our FT eVar example: A = (3/3) * 10 + (5/5) * 5 = $15.00, and for the prop: A = (1/2) * 10 + (1/3) * 5 = $6.66, B = (1/2) * 10 + (1/3) * 5 = $6.66, and C = (1/3) * 5 = $1.66. </li> 
</ul> 
<p>Resulting in a distribution as follows: </p> 
<table id="table_6A066E602BF641B0BD4B175EE9753C6E"> 
 <tgroup cols="4">
  <colspec colnum="1" colname="col1" colwidth="*" />
  <colspec colnum="2" colname="col2" colwidth="*" />
  <colspec colnum="3" colname="col3" colwidth="*" />
  <colspec colnum="4" colname="col4" colwidth="*" />
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Values </th> 
    <th colname="col2" class="entry"> Current Last Touch eVar </th> 
    <th colname="col3" class="entry"> Current First Touch eVar </th> 
    <th colname="col4" class="entry"> Current Prop </th> 
   </tr>
  </thead> 
  <tbody> 
   <tr> 
    <td colname="col1"> PROMO A </td> 
    <td colname="col2"> $8.66 </td> 
    <td colname="col3"> $15.00 </td> 
    <td colname="col4"> $6.66 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> PROMO B </td> 
    <td colname="col2"> $5.33 </td> 
    <td colname="col3"> $0.00 </td> 
    <td colname="col4"> $6.66 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> PROMO C </td> 
    <td colname="col2"> $1.00 </td> 
    <td colname="col3"> $0.00 </td> 
    <td colname="col4"> $1.66 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> Total </td> 
    <td colname="col2"> $15.00 </td> 
    <td colname="col3"> $15.00 </td> 
    <td colname="col4"> $15.00 </td> 
   </tr> 
  </tbody> 
 </tgroup> 
</table> 
<p> </p> 
<p><b>After July 19, 2018</b>, [!DNL Analytics] will treat each sequence of conversions independently, meaning linear attribution will no longer carry forward from one conversion to another. In the previous example, attribution will always be treated the same way (regardless of the eVar allocation settings as stated above) and will be calculated as follows: A = (1/2) * 10 = $5, B = (1/2) * 10 = $5, and C = (1/1) * 5 = $5. To summarize: </p> 
<table id="table_2D39CCD158BF488EA404324DF50B9579"> 
 <tgroup cols="4">
  <colspec colnum="1" colname="col1" colwidth="*" />
  <colspec colnum="2" colname="col2" colwidth="*" />
  <colspec colnum="3" colname="col3" colwidth="*" />
  <colspec colnum="4" colname="col4" colwidth="*" />
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Values </th> 
    <th colname="col2" class="entry"> New Last Touch eVar </th> 
    <th colname="col3" class="entry"> New First Touch eVar </th> 
    <th colname="col4" class="entry"> New Prop </th> 
   </tr>
  </thead> 
  <tbody> 
   <tr> 
    <td colname="col1"> PROMO A </td> 
    <td colname="col2"> $5.00 </td> 
    <td colname="col3"> $5.00 </td> 
    <td colname="col4"> $5.00 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> PROMO B </td> 
    <td colname="col2"> $5.00 </td> 
    <td colname="col3"> $5.00 </td> 
    <td colname="col4"> $5.00 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> PROMO C </td> 
    <td colname="col2"> $5.00 </td> 
    <td colname="col3"> $5.00 </td> 
    <td colname="col4"> $5.00 </td> 
   </tr> 
   <tr> 
    <td colname="col1"> Total </td> 
    <td colname="col2"> $15.00 </td> 
    <td colname="col3"> $15.00 </td> 
    <td colname="col4"> $15.00 </td> 
   </tr> 
  </tbody> 
 </tgroup> 
</table>

 -->

