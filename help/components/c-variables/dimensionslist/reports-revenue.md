---
description: Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.
title: Umsatz
topic: Reports
uuid: e5b72798-f5c7-440d-a62d-376bfd115ac8
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Umsatz

Ermittelt die Höhe der Einnahmen, die mit allen Produkten in einem bestimmten Zeitraum generiert wurden.

Verwenden Sie „Umsatz“, um den allgemeinen Erfolg und Trend Ihrer Site anzuzeigen. Zudem können Sie Zeiträume eingrenzen, in denen die Site besonders erfolgreich war, um die Ursache zu ermitteln und für künftige Kampagnen zu nutzen.

## Allgemeine Berichteigenschaften {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* Damit dieser Bericht erfolgreich Daten erfassen kann, müssen bestimmte Anforderungen erfüllt sein. In der Bildanforderung muss Folgendes stattfinden:

   * Ein [!UICONTROL purchase] Ereignis muss in der `s.events` Variablen ausgelöst werden.

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

* [!UICONTROL Revenue] rundet den Gesamtbetrag für einen Zeitraum auf den nächsten Währungswert. Es wird nicht jedes einzelne Produkt oder jeder Hit gerundet.
* Da in Analytics-Berichten jeder Tag auf den nächsten vollen Betrag gerundet wird, weicht die Summe der einzelnen Tage im Vergleich zum monatlichen Gesamtbetrag geringfügig ab. Denn der monatliche Gesamtbetrag ist nicht mit dem gerundeten Betrag der einzelnen Tage identisch. Es handelt sich um die absolute Summe, die auf den nächsten vollen Betrag gerundet wird.
* Sie können einen Bericht erstellen, bei dem der Umsatz nicht auf den nächsten vollen Betrag gerundet wird, indem Sie eine  [berechnete Metrik](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/cm-overview.html) verwenden.
* Wenn die Variable `purchaseID` nicht verwendet wird, könnten Benutzer beim Aktualisieren der Seite den Umsatz fälschlicherweise erhöhen, da die Daten mehrmals an Adobe gesendet werden.
* Stündliche Aufschlüsselungen basieren auf der Zeitzone der Report Suite.
* Der Bericht enthält keine Zeileneinträge. Er kann nur als Trendansicht angezeigt werden.
* Eine Granularität wie Stunde, Tag, Woche, Monat, Quartal und Jahr kann angewendet werden. Die Verfügbarkeit dieser Granularitäten hängt vom Datumsbereich der Berichterstellung ab.
* Dieser Bericht kann in die folgenden Berichte aufgeschlüsselt werden (je nach Unternehmens- und Report Suite-Einstellungen).

   * [!UICONTROL Time Spent per Visit] zur Verfügung.
   * [!UICONTROL Pages and Site Sections] zur Verfügung.
   * [!UICONTROL Videos] zur Verfügung.
   * [!UICONTROL Page Depth and Entry Pages] zur Verfügung.
   * Die meisten [!UICONTROL Traffic Sources]Berichte, einschließlich [!UICONTROL Search Keywords], [!UICONTROL Search Engines]und [!UICONTROL Referring Domains] Berichte.

   * [!UICONTROL Tracking Code] und alle zugehörigen Klassifizierungsberichte.
   * [!UICONTROL Products variable] und alle zugehörigen Klassifizierungsberichte. Auch [!UICONTROL Categories] Berichte.

   * Nahezu alle [!UICONTROL Visitor Profile] Berichte mit Ausnahme von [!UICONTROL GeoSegmentation] Berichten.

   * All [!UICONTROL Custom Conversion] variables reports with basic subrelations.

* Stündliche Aufschlüsselungen sind nicht verfügbar.

## Produktspezifische Eigenschaften  {#section_ED87FFD020634453AABE86B0248BE69B}

* This report can be accessed by going to **[!UICONTROL Conversion]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* [!UICONTROL Traffic Sources] Unterteilungen finden Sie unter [!UICONTROL Finding Methods].

* This report can be accessed by going to **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* Zusätzlich zu allen zuvor aufgelisteten Aufschlüsselungen stehen [!UICONTROL First and Last Touch Marketing Channel] Aufschlüsselungen zur Verfügung.

* This report can also be accessed by going to **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* In addition to the previously mentioned breakdowns, [!UICONTROL List]variables and the current [!UICONTROL Video] variables can be used.

* Dieser Bericht kann Segmente verwenden.

* Sie können jedes Element in diesem Bericht nach jedem anderen Bericht und beliebigen Variablen aufschlüsseln, sodass Sie Aufschlüsselungen jeder gewünschten Granularität sehen können.
* Sie können alle [!UICONTROL conversion] und [!UICONTROL traffic] Metriken gleichzeitig verwenden [!UICONTROL Revenue]. You can use different allocation for all [!UICONTROL conversion] metrics.

* Dieser Bericht kann mehrere hochgradig erweiterte Segmente nutzen.

Wenn sich dieser Bericht nicht an der üblichen Stelle befindet, wenden Sie sich an Ihren Administrator. Möglicherweise wurde die Standardmenüstruktur den Anforderungen Ihrer Organisation entsprechend geändert.
