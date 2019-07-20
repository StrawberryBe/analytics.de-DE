---
description: Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.
seo-description: Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.
seo-title: Umsatz
solution: Analytics
title: Umsatz
topic: 'Berichte    '
uuid: e 5 b 72798-f 5 c 7-440 d-a 62 d -376 bfd 115 ac 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Umsatz

Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.

Verwenden Sie „Umsatz“, um den allgemeinen Erfolg und Trend Ihrer Site anzuzeigen. Zudem können Sie Zeiträume eingrenzen, in denen die Site besonders erfolgreich war, um die Ursache zu ermitteln und für künftige Kampagnen zu nutzen.

## Allgemeine Berichteigenschaften {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* Damit dieser Bericht erfolgreich Daten erfassen kann, müssen bestimmte Anforderungen erfüllt sein. In der Bildanforderung muss Folgendes stattfinden:

   * Ein [!UICONTROL Kaufereignis] muss in der Variablen `s.events`.

   * Die Variable `products` muss mit einer Zahl im Preisfeld definiert werden.
   * Folgendes würde beispielsweise mit 35,99 € im Umsatzbericht ausgewiesen:

      ```js
       s.products="Mens;Shoes;1;35.99"
      ```

      ```js
       s.events="purchase"
      ```

* Wenn mehrere Produkte in der der Variablen [!UICONTROL „s.products“] vorhanden sind, werden alle Produkte im Umsatzbericht erfasst. For example, [!DNL s.products="Mens;Socks;1;4.50,Womens;Socks;1;4.50"] would pass $9 in revenue to reporting.

   >[!NOTE]
   >
   >Der Umsatz wird nicht multipliziert, wenn die Menge in einem einzelnen Produkt erhöht wird. For example, [!DNL s.products="Womens;Socks;5;4.50"] does not pass $22.50 into reporting, it passes $4.50. Make sure your implementation passes the total revenue for the quantity listed ( [!DNL s.products="Womens;Socks;5;22.50"]).

* [!UICONTROL Umsatz] rundet den Gesamtbetrag für einen Zeitraum auf den nächsten Währungsbetrag auf. Es wird nicht jedes einzelne Produkt oder jeder Hit gerundet.
* Da in Analytics-Berichten jeder Tag auf den nächsten vollen Betrag gerundet wird, weicht die Summe der einzelnen Tage im Vergleich zum monatlichen Gesamtbetrag geringfügig ab. Denn der monatliche Gesamtbetrag ist nicht mit dem gerundeten Betrag der einzelnen Tage identisch. Es handelt sich um die absolute Summe, die auf den nächsten vollen Betrag gerundet wird.
* Sie können einen Bericht erstellen, bei dem der Umsatz nicht auf den nächsten vollen Betrag gerundet wird, indem Sie eine [berechnete Metrik](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) verwenden.
* Wenn die Variable `purchaseID` nicht verwendet wird, könnten Benutzer beim Aktualisieren der Seite den Umsatz fälschlicherweise erhöhen, da die Daten mehrmals an Adobe gesendet werden.
* Stündliche Aufschlüsselungen basieren auf der Zeitzone der Report Suite.
* Der Bericht enthält keine Zeileneinträge. Er kann nur als Trendansicht angezeigt werden.
* Eine Granularität wie Stunde, Tag, Woche, Monat, Quartal und Jahr kann angewendet werden. Die Verfügbarkeit dieser Granularitäten hängt vom Datumsbereich der Berichterstellung ab.
* Dieser Bericht kann in die folgenden Berichte aufgeschlüsselt werden (je nach Unternehmens- und Report Suite-Einstellungen).

   * [!UICONTROL Zeit pro Besuch]
   * [!UICONTROL Seiten und Sitebereiche]
   * [!UICONTROL Videos]
   * [!UICONTROL Klicktiefe und Entrypages]
   * In die meisten Berichte zu [!UICONTROL Traffic-Quellen] wie [!UICONTROL „Suchkeywords“], [!UICONTROL „Suchmaschinen“] und [!UICONTROL „Referrer-Domänen“].

   * In den [!UICONTROL Trackingcodebericht] und alle zugehörigen Classification-Berichte.
   * In den [!UICONTROL Produktvariablenbericht] und alle zugehörigen Classification-Berichte. Auch in [!UICONTROL Kategorienberichte].

   * In fast alle [!UICONTROL Besucherprofil]-Berichte mit Ausnahme der [!UICONTROL Geosegmentation]-Berichte.

   * Alle Variablenberichte [!UICONTROL „benutzerspezifische Konversion“] mit grundlegenden Subrelationen.

* Stündliche Aufschlüsselungen sind nicht verfügbar.

## Produktspezifische Eigenschaften {#section_ED87FFD020634453AABE86B0248BE69B}

* This report can be accessed by going to **[!UICONTROL Conversion]** &gt; **[!UICONTROL Purchases]** &gt; **[!UICONTROL Revenue]**.

* Die Berichte zu [!UICONTROL Traffic-Quellen] finden Sie unter [!UICONTROL Suchmethoden].

* This report can be accessed by going to **[!UICONTROL Site Metrics]** &gt; **[!UICONTROL Purchases]** &gt; **[!UICONTROL Revenue]**.

* Abgesehen von den oben aufgeführten Aufschlüsselungen sind auch Aufschlüsselungen zum [!UICONTROL Erst- und Letztkontakt von Marketingkanälen] verfügbar.

* This report can also be accessed by going to **[!UICONTROL Site Metrics]** &gt; **[!UICONTROL Purchases]** &gt; **[!UICONTROL Revenue]**.

* Neben den oben aufgeführten Aufschlüsselungen können auch [!UICONTROL Listenvariablen] und die aktuellen [!UICONTROL Videovariablen] verwendet werden.

* Dieser Bericht kann Segmente verwenden.

* Sie können jedes Element in diesem Bericht nach jedem anderen Bericht und beliebigen Variablen aufschlüsseln, sodass Sie Aufschlüsselungen jeder gewünschten Granularität sehen können.
* Sie können alle [!UICONTROL Konversions]- und [!UICONTROL Traffic]-Metriken mit dem [!UICONTROL Umsatz] verwenden. Für alle [!UICONTROL Konversionsmetriken] sind unterschiedliche Zuordnungen möglich.

* Dieser Bericht kann mehrere hochgradig erweiterte Segmente nutzen.

Wenn sich dieser Bericht nicht an der üblichen Stelle befindet, wenden Sie sich an Ihren Administrator. Möglicherweise wurde die Standardmenüstruktur den Anforderungen Ihrer Organisation entsprechend geändert.
