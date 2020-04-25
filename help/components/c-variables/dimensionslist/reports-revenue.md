---
description: Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.
title: Umsatz
topic: Reports
uuid: e5b72798-f5c7-440d-a62d-376bfd115ac8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Umsatz

Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.

Verwenden Sie „Umsatz“, um den allgemeinen Erfolg und Trend Ihrer Site anzuzeigen. Zudem können Sie Zeiträume eingrenzen, in denen die Site besonders erfolgreich war, um die Ursache zu ermitteln und für künftige Kampagnen zu nutzen.

## Allgemeine Berichteigenschaften {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* Damit dieser Bericht erfolgreich Daten erfassen kann, müssen bestimmte Anforderungen erfüllt sein. In der Bildanforderung muss Folgendes stattfinden:

   * Ein [!UICONTROL Kaufereignis] muss in der Variablen  `s.events` festgelegt.

   * Die Variable `products` muss mit einer Zahl im Preisfeld definiert werden.
   * Folgendes würde beispielsweise mit 35,99 € im Umsatzbericht ausgewiesen:

      ```js
       s.products="Mens;Shoes;1;35.99"
      ```

      ```js
       s.events="purchase"
      ```

* Wenn mehrere Produkte in der der Variablen [!UICONTROL s.products] vorhanden sind, werden alle Produkte im Umsatzbericht erfasst. Beispiel: [!DNL s.products="Mens;Socks;1;4.50,Womens;Socks;1;4.50"] wird als Umsatz von 9 USD in der Berichterstellung ausgewiesen.

   >[!NOTE]
   >
   >Der Umsatz wird nicht vervielfacht, wenn sich die Menge in einem einzelnen Produkt erhöht. Beispiel: [!DNL s.products="Womens;Socks;5;4.50"] wird nicht als 22,50 USD in der Berichterstellung ausgewiesen, sondern als 4,50 USD. Stellen Sie sicher, dass Ihre Implementierung den Gesamtumsatz für die aufgeführte Menge ausweist ([!DNL s.products="Womens;Socks;5;22.50"]).

* [!UICONTROL Umsatz] rundet den Gesamtbetrag für einen Zeitraum auf den nächsten Währungsbetrag auf. Es wird nicht jedes einzelne Produkt oder jeder Hit gerundet.
* Da in Analytics-Berichten jeder Tag auf den nächsten vollen Betrag gerundet wird, weicht die Summe der einzelnen Tage im Vergleich zum monatlichen Gesamtbetrag geringfügig ab. Denn der monatliche Gesamtbetrag ist nicht mit dem gerundeten Betrag der einzelnen Tage identisch. Es handelt sich um die absolute Summe, die auf den nächsten vollen Betrag gerundet wird.
* Sie können einen Bericht erstellen, bei dem der Umsatz nicht auf den nächsten vollen Betrag gerundet wird, indem Sie eine  [berechnete Metrik](https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics/) verwenden.
* Wenn die Variable `purchaseID` nicht verwendet wird, könnten Benutzer beim Aktualisieren der Seite den Umsatz fälschlicherweise erhöhen, da die Daten mehrmals an Adobe gesendet werden.
* Stündliche Aufschlüsselungen basieren auf der Zeitzone der Report Suite.
* Der Bericht enthält keine Zeileneinträge. Er kann nur als Trendansicht angezeigt werden.
* Eine Granularität wie Stunde, Tag, Woche, Monat, Quartal und Jahr kann angewendet werden. Die Verfügbarkeit dieser Granularitäten hängt vom Datumsbereich der Berichterstellung ab.
* Dieser Bericht kann in die folgenden Berichte aufgeschlüsselt werden (je nach Unternehmens- und Report Suite-Einstellungen).

   * [!UICONTROL Zeit pro Besuch].
   * [!UICONTROL Seiten und Sitebereiche].
   * [!UICONTROL Videos].
   * [!UICONTROL Klicktiefe und Entrypages].
   * In die meisten Berichte zu [!UICONTROL Traffic-Quellen] wie [!UICONTROL Suchkeywords], [!UICONTROL Suchmaschinen] und [!UICONTROL Referrer-Domänen].

   * In den [!UICONTROL Trackingcodebericht] und alle zugehörigen Classification-Berichte.
   * In den [!UICONTROL Produktvariablenbericht] und alle zugehörigen Classification-Berichte. Auch in [!UICONTROL Kategorienberichte].

   * In fast alle [!UICONTROL Besucherprofil]-Berichte mit Ausnahme der [!UICONTROL Geosegmentation]-Berichte.

   * Alle Variablenberichte [!UICONTROL benutzerspezifische Konversion] mit grundlegenden Subrelationen.

* Stündliche Aufschlüsselungen sind nicht verfügbar.

## Produktspezifische Eigenschaften  {#section_ED87FFD020634453AABE86B0248BE69B}

* So greifen Sie auf diesen Bericht zu: **[!UICONTROL Konversion]** > **[!UICONTROL Einkäufe]** > **[!UICONTROL Umsatz]**.

* Die Berichte zu [!UICONTROL Traffic-Quellen] finden Sie unter [!UICONTROL Suchmethoden].

* So greifen Sie auf diesen Bericht zu: **[!UICONTROL Sitemetriken]** > **[!UICONTROL Einkäufe]** > **[!UICONTROL Umsatz]**.

* Abgesehen von den oben aufgeführten Aufschlüsselungen sind auch Aufschlüsselungen zum [!UICONTROL Erst- und Letztkontakt von Marketingkanälen] verfügbar.

* Auch auf diesen Bericht können Sie so zugreifen: **[!UICONTROL Sitemetriken]** > **[!UICONTROL Einkäufe]** > **[!UICONTROL Umsatz]**.

* Neben den oben aufgeführten Aufschlüsselungen können auch [!UICONTROL Listenvariablen] und die aktuellen [!UICONTROL Videovariablen] verwendet werden.

* Dieser Bericht kann Segmente verwenden.

* Sie können jedes Element in diesem Bericht nach jedem anderen Bericht und beliebigen Variablen aufschlüsseln, sodass Sie Aufschlüsselungen jeder gewünschten Granularität sehen können.
* Sie können alle [!UICONTROL Konversions]- und [!UICONTROL Traffic]-Metriken mit dem [!UICONTROL Umsatz] verwenden. Für alle [!UICONTROL Konversionsmetriken] sind unterschiedliche Zuordnungen möglich.

* Dieser Bericht kann mehrere hochgradig erweiterte Segmente nutzen.

Wenn sich dieser Bericht nicht an der üblichen Stelle befindet, wenden Sie sich an Ihren Administrator. Möglicherweise wurde die Standardmenüstruktur den Anforderungen Ihrer Organisation entsprechend geändert.
