---
description: 'Informationen '
title: Metriktyp und Attribution
uuid: 64649698-df2a-42c3-bb31-938f766e1d1f
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 97%

---


# Metriktyp und Attribution

Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den Metriktyp und das Attributionsmodell angeben.

## Metriktyp

![](assets/cm_type_alloc.png)

| Metriktyp | Definition |
|---|---|
| Standard | Diese Metriken sind dieselben, die auch in der Standard-[!DNL Analytics]-Berichterstellung verwendet werden. Wenn eine Formel aus einer einzelnen Standardmetrik besteht, zeigt sie die gleichen Daten wie das nicht berechnete Metrikgegenstück an. Standardmetriken eignen sich zum Erstellen berechneter Metriken, die speziell für die einzelnen Einzelposten gelten. Beispiel: [Bestellungen]/[Besuche] teilt die Bestellungen für diesen Einzelposten durch die Anzahl der Besuche für den Posten. |
| Gesamt | Verwenden Sie den Gesamtwert für den Berichtszeitraum in jedem Einzelposten. Wenn eine Formel aus einer einzelnen Gesamtmetrik besteht, zeigt sie dieselbe Gesamtzahl für jeden Einzelposten an. Gesamtmetriken eignen sich für die Erstellung berechneter Metriken, die mit den Gesamtdaten der Site verglichen werden. Beispiel: [Bestellungen]/[Gesamtbesuche] zeigt den Anteil der Bestellungen für ALLE Site-Besuche und nicht nur die Besuche für den speziellen Zeileneintrag. |

## Spaltenattributionsmodell

>[!IMPORTANT]
>
>Im Juli 2018 hat [!DNL Analytics] die Funktion [Attribution IQ](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/attribution/models.html) eingeführt, mit der die Bewertung von Zuordnungsmodellen bei berechneten Metriken geändert wurde. Im Rahmen dieser Änderung wurden berechnete Metriken, die ein nicht standardmäßiges Zuordnungsmodell verwenden, zu neuen, verbesserten Zuordnungsmodellen migriert:
>
>* Eine vollständige Liste der unterstützten nicht standardmäßigen Modelle und Lookback-Fenster finden Sie in der Dokumentation zu [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html).
>* Die Zuordnungsmodelle „Marketing-Kanal – Letztkontakt“ und „Marketing-Kanal – Erstkontakt“ werden in das neue „Letztkontakt“- bzw. in das „Erstkontakt“-Attributionsmodell migriert. (Hinweis: Marketing-Kanäle werden nicht veraltet sein, sondern lediglich die beiden Zuordnungsmodelle, die in berechneten Metriken erscheinen.)
>* Darüber hinaus wird die Methode zur Berechnung der linearen Zuordnung korrigiert. Wenn Kunden berechnete Metriken mit linearen Zuordnungsmodellen verwenden, können sich die Berichte geringfügig ändern, um das neue, korrigierte Attributionsmodell widerzuspiegeln. Diese Änderung an berechneten Metriken wird in Analysis Workspace, Reports &amp; Analysen, der Berichte-API und dem Report Builder übernommen. Weitere Informationen finden Sie unter **Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018**) weiter unten.

>



## Wie die lineare Zuordnung funktioniert (ab 19. Juli 2018)

Im Juli 2018 wurde das Reporting für die lineare Zuordnung bei berechneten Metriken in Adobe geändert. Diese Änderung betrifft Analysis Workspace, Reports &amp; Analytics, Report Builder, Activity Map und die Reporting-APIs. Die Änderung betrifft in erster Linie eVars und andere Dimensionen mit Persistenz. Diese Änderungen treffen nur auf berechnete Metriken zu und haben keinen Einfluss auf andere Berichte, die lineare Zuordnung verwenden (z. B. den Bericht „Seiten“ in Reports &amp; Analytics). Andere Berichte, die die lineare Zuordnung verwenden, werden weiter die aktuelle Methode zur linearen Zuordnung verwenden.

Im folgenden Beispiel soll illustriert werden, wie sich berechnete Metriken mit linearer Zuordnung beim Reporting ändern:

|  | Treffer 1 | Treffer 2 | Treffer 3 | Treffer 4 | Treffer 5 | Treffer 6 | Treffer 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Eingereichte Daten | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |
| Letztkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | 10$ |
| Erstkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | 10$ |
| Beispieleigenschaft | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |

In diesem Beispiel wurden die Werte A, B und C in eine Variable für die Treffer 1, 3, 4 und 6 gesendet, bevor ein Kauf in Höhe von 10 USD bei Treffer 7 getätigt wurde. In der zweiten Zeile werden dieses Werte bei Treffern auf Grundlage von Letztkontaktbesuchen gespeichert. In der dritten Zeile wird das Speichern auf Grundlage des Erstkontaktbesuchs dargestellt. Zu guter Letzt stellt die letzte Zeile dar, wie Daten aus einer Eigenschaft aufgezeichnet würden, bei denen kein Speichern vorgesehen ist.

## Unterschiede in der Funktionsweise der linearen Zuordnung in Reports &amp; Analytics im Vergleich zu Workspace

Es gibt einige Unterschiede in der Funktionsweise der linearen Attribution zwischen diesen beiden Tools:

* In Reports &amp; Analytics ist die (verarbeitete) lineare Attribution immer besuchsbasiert, während sie in Workspace besuchs- oder besuchsbasiert sein kann.
* Wenn in Reports &amp; Analytics beim ersten Treffer eines Besuchs kein Wert übergeben wurde, bleibt der (anfängliche) Wert des vorherigen Besuchs erhalten. Dies ist in Workspace NICHT der Fall (Attribution IQ). Wenn beim ersten Treffer eines Besuchs kein Wert übergeben wird, ist „Keine“ der Ausgangswert.

## Funktionsweise der linearen Zuordnung vor Juli 2018

Vor dem 19. Juli 2018 wurde die lineare Attribution berechnet, nachdem die Erst- bzw. Letztkontakt-Persistenz bereits erfolgt war. Gemäß dem Letztkontakt-eVar wurden die 10 USD daher wie folgt verteilt: A = 10 x (3/6) = 5 USD, B = 10 x (2/6) = 3,33 USD, C = 10 x (1/6) = 1,67 USD.

Gemäß dem oberen Erstkontakt-eVar würden alle 10 USD-Beträge zu A gegeben. Für die Eigenschaft: A = 10 x (2/4) = 5 USD, B = 10 x (1/4) = 2,50 USD und C = 10 x (1/4) = 2.50 USD. Um die frühere Funktionsweise der linearen Zuordnung zusammenzufassen:

| Werte | Aktueller Letztkontakt-eVar | Aktueller Erstkontakt-eVar | Aktuelle Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00$ | 10,00$ | 5,00$ |
| PROMO B | 3,33$ | 0$ | 2,50$ |
| PROMO C | 1,67$ | 0$ | 2,50$ |
| Gesamt | 10,00$ | 10,00$ | 10,00$ |

**Zusammenfassung der Funktionsweise der linearen Zuordnung ab 19. Juli 2018**

Nach dem 19. Juli wurde dieses Verhalten in berechneten Metriken korrigiert. Statt die gespeicherten Werte aufgrund von Letzt- bzw. Erstkontakt zu verwenden, verwendet [!DNL Analytics] nur die Werte, die übertragen wurden (erste Zeile der Tabelle). Daher haben die Dimensions-Zuordnungseinstellungen keinen Einfluss mehr darauf, wie die lineare Zuordnung berechnet wird (d. h. Eigenschaften und eVars werden gleich behandelt), und die Ergebnisse spiegeln wider, was ursprünglich übertragen wurde, statt der möglicherweise gespeicherten Erst- bzw. Letztkontaktwerte. In allen drei Fällen gilt dann: A = 10 x (2/4) = 5 USD, B = 10 x (1/4) = 2,50 USD und C = 10 x (1/4) = 2,50 USD.

| Werte | Neuer Letztkontakt-eVar | Neuer Erstkontakt-eVar | Neue Eigenschaft |
|---|---|---|---|
| PROMO A | 5,00$ | 5,00$ | 5,00$ |
| PROMO B | 2,50$ | 2,50$ | 2,50$ |
| PROMO C | 2,50$ | 2,50$ | 2,50$ |
| Gesamt | 10,00$ | 10,00$ | 10,00$ |

