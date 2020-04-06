---
description: Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Zuordnungsmodell angeben.
title: Metriktyp und Attribution
uuid: 64649698-df2a-42c3-bb31-938f766e1d1f
translation-type: tm+mt
source-git-commit: e6aaf2754c6a5c33fbe3e093b4d7ca5a375c41e7

---


# Metriktyp und Attribution

Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Zuordnungsmodell angeben.

* [Metriktyp](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_34A86FB402F94E988724232283BF18B7)
* [Spaltenattributionsmodell](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_F9690FD1943B403AB28E2FAC54EFE032)
* [Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1)

## Metriktyp {#section_34A86FB402F94E988724232283BF18B7}

![](assets/cm_type_alloc.png)

| Metriktyp | Definition |
|---|---|
| Standard | Diese Metriken sind dieselben, die auch in der Standard-[!DNL Analytics]-Berichterstellung verwendet werden. Wenn eine Formel aus einer einzelnen Standardmetrik bestand, zeigt sie identische Daten an wie das nicht berechnete MetrikGegenstück. Standardmetriken sind nützlich, um errechnete Metriken zu erstellen, die für jedes einzelne Zeilenelement spezifisch sind. Beispiel: [Bestellungen]/[Besuche] teilt die Bestellungen für diesen Einzelposten durch die Anzahl der Besuche für den Posten. |
| Gesamt | Verwenden Sie die Gesamtsumme für den Berichte in jedem Zeileneintrag. Wenn eine Formel aus einer einzelnen Summenmetrik bestand, wird für jeden Zeileneintrag dieselbe Gesamtanzahl angezeigt. Summenmetriken sind nützlich, um errechnete Metriken zu erstellen, die mit den Gesamtdaten der Site verglichen werden. Beispiel: [Bestellungen]/[Gesamtbesuche] zeigt den Anteil der Bestellungen für ALLE Site-Besuche und nicht nur die Besuche für den speziellen Zeileneintrag. |

## Spaltenattributionsmodell {#section_F9690FD1943B403AB28E2FAC54EFE032}

>[!IMPORTANT]
>
>Im Juli 2018 hat [!DNL Analytics] die Funktion [Attribution IQ](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/attribution.html) eingeführt, mit der die Bewertung von Zuordnungsmodellen bei berechneten Metriken geändert wurde. Im Rahmen dieser Änderung wurden berechnete Metriken, die ein nicht standardmäßiges Zuordnungsmodell verwenden, zu neuen, verbesserten Zuordnungsmodellen migriert:
>
>* Eine vollständige Liste der nicht standardmäßigen Zuordnungsmodelle und der unterstützten Lookback-Fenster finden Sie in der [Zuordnungs-IQ](https://marketing.adobe.com/resources/help/de_DE/analytics/analysis-workspace/attribution.html) -Dokumentation.
>* Die Zuordnungsmodelle „Marketing-Kanal – Letztkontakt“ und „Marketing-Kanal – Erstkontakt“ werden in das neue „Letztkontakt“- bzw. in das „Erstkontakt“-Attributionsmodell migriert. (Hinweis: Marketing-Kanäle werden nicht veraltet sein, sondern lediglich die beiden Zuordnungsmodelle, die in berechneten Metriken erscheinen.)
>* Darüber hinaus wird die Methode zur Berechnung der linearen Zuordnung korrigiert. Wenn Kunden berechnete Metriken mit linearen Zuordnungsmodellen verwenden, können sich die Berichte geringfügig ändern, um das neue, korrigierte Attributionsmodell widerzuspiegeln. Diese Änderung an den berechneten Metriken betrifft Analysis Workspace, Reports &amp; Analytics, die Reporting-API, Report Builder und Ad Hoc Analysis. For more information, see **How Linear Allocation works (as of July 19, 2018**, below.
>



## Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018) 

Im Juli 2018 wurde die Berichterstellung für die lineare Zuordnung bei berechneten Metriken in Adobe geändert. Diese Änderung betrifft Analysis Workspace, Ad Hoc Analysis, Reports &amp; Analytics, Report Builder, Activity Map und die Reporting-APIs. Die Änderung betrifft in erster Linie eVars und andere Dimensionen mit Persistenz. Diese Änderungen treffen nur auf berechnete Metriken zu und haben keinen Einfluss auf andere Berichte, die lineare Zuordnung verwenden (z. B. den Bericht „Seiten“ in Reports &amp; Analytics). Andere Berichte, die eine lineare Zuordnung verwenden, verwenden weiterhin die vorhandene Methode der linearen Zuordnung.

Das folgende Beispiel zeigt, wie sich berechnete Metriken mit linearer Zuordnung im Berichte ändern:

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
   <td colname="col1"> <p>Daten gesendet in </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> – </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> – </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10$ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Letztkontakt eVar </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> PROMO A </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> PROMO B </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10$ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>First Touch eVar </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> PROMO A </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO A </td> 
   <td colname="col6"> PROMO A </td> 
   <td colname="col7"> PROMO A </td> 
   <td colname="col8"> 10$ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beispieleigenschaft </p> </td> 
   <td colname="col2"> PROMO A </td> 
   <td colname="col3"> – </td> 
   <td colname="col4"> PROMO A </td> 
   <td colname="col5"> PROMO B </td> 
   <td colname="col6"> – </td> 
   <td colname="col7"> PROMO C </td> 
   <td colname="col8"> 10$ </td> 
  </tr> 
 </tbody> 
</table>

In diesem Beispiel wurden die Werte A, B und C bei Treffern 1, 3, 4 und 6 in eine Variable gesendet, bevor ein Kauf im Wert von 10 USD bei Treffer 7 erfolgte. In der zweiten Zeile bleiben diese Werte bei einem Besuch mit Last Touch über Treffer hinweg erhalten. Die dritte Zeile zeigt die Persistenz eines First Touch-Besuchs. Schließlich wird in der letzten Zeile veranschaulicht, wie Daten für eine Eigenschaftsvariable ohne Persistenz aufgezeichnet werden.

## Funktionsweise der linearen Zuteilung vor Juli 2018

Vor dem 19. Juli 2018 wurde die lineare Attribution berechnet, nachdem die Erst- bzw. Letztkontakt-Persistenz bereits erfolgt war. Dies bedeutete, dass für die oben genannte &quot;last touch&quot;-eVar die 10 USD wie folgt verteilt würden: A = 10 * (3/6) = $5, B = 10 * (2/6) = $3.33, C = 10 * (1/6) = $1.67.

Für die oben genannte First Touch eVar würden alle $10 an A übergeben. Für die Eigenschaftsvariable: A = 10 * (2/4) = 5, B = 10 * (1/4) = 2,50 $ und C = 10 * (1/4) = 2,50 $. So fassen Sie die lineare Zuordnung wie zuvor zusammen:

| Werte | Aktuelle Letztkontakt-eVar | Aktuelle eVar für Erstkontakt | Aktuelle Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00$ | 10,00$ | 5,00$ |
| PROMO B | 3,33$ | 0$ | 2,50$ |
| PROMO C | 1,67$ | 0$ | 2,50$ |
| Gesamt | 10,00$ | 10,00$ | 10,00$ |

**Zusammenfassung der Funktionsweise der linearen Zuweisung zum 19. Juli 2018**

Nach dem 19. Juli haben wir dieses Verhalten in berechneten Metriken korrigiert. Statt die gespeicherten Werte aufgrund von Letzt- bzw. Erstkontakt zu verwenden, verwendet [!DNL Analytics] nur die Werte, die übertragen wurden (erste Zeile der Tabelle). Daher haben die Dimensions-Zuordnungseinstellungen keinen Einfluss mehr darauf, wie die lineare Zuordnung berechnet wird (d. h. Eigenschaften und eVars werden gleich behandelt), und die Ergebnisse spiegeln wider, was ursprünglich übertragen wurde, statt der möglicherweise gespeicherten Erst- bzw. Letztkontaktwerte. So, in allen drei Fällen, A = 10 * (2/4) = 5, B = 10 * (1/4) = 2,50 $ und C = 10 * (1/4) = 2,50 $.

| Werte | Neue Letztkontakt-eVar | Neue eVar für Erstkontakt | Neue Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00$ | 5,00$ | 5,00$ |
| PROMO B | 2,50$ | 2,50$ | 2,50$ |
| PROMO C | 2,50$ | 2,50$ | 2,50$ |
| Gesamt | 10,00$ | 10,00$ | 10,00$ |

