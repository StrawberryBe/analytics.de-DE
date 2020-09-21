---
description: Zeigen quantitative Informationen über Ihre Website an, z. B. wie oft Besucher bestimmte Seiten angezeigt haben, die Zahl der insgesamt auf bestimmten Seiten getätigten Käufe, wann sie sich ereigneten und ähnliche quantitative Daten. Jeder dieser Berichte ist eine Metrik, die Sie in anderen elementbasierten Berichten platzieren können.
title: Site-Metrikberichte
topic: Ad hoc analysis
uuid: 0730747a-216f-4a58-b62b-a9812968cde5
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 99%

---


# Site-Metrikberichte

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 zum Lebensende. [Weitere Infos](https://adobe.ly/discoverworkspace)

Zeigen quantitative Informationen über Ihre Website an, z. B. wie oft Besucher bestimmte Seiten angezeigt haben, die Zahl der insgesamt auf bestimmten Seiten getätigten Käufe, wann sie sich ereigneten und ähnliche quantitative Daten. Jeder dieser Berichte ist eine Metrik, die Sie in anderen elementbasierten Berichten platzieren können.

## Site-Metrikberichte {#concept_0639CA16551749A693F49ADED4842CCE}

Zeigen quantitative Informationen über Ihre Website an, z. B. wie oft Besucher bestimmte Seiten angezeigt haben, die Zahl der insgesamt auf bestimmten Seiten getätigten Käufe, wann sie sich ereigneten und ähnliche quantitative Daten. Jeder dieser Berichte ist eine Metrik, die Sie in anderen elementbasierten Berichten platzieren können.

Metrikberichte zeigen einen   Trend über einen Zeitraum. Sie können eine Zeit- und Wochentagsgranularität für diese Berichte anwenden. Alternativ dazu können Sie sich die Besuchszeit auf Ihrer Site, die Käufe, den Umsatz und ähnliche Metriken analysieren.

Die folgenden Site-Metrik-Berichte stehen im Menü [!UICONTROL Site-Metrik] zur Verfügung.

## Bericht „Seitenansichten“ {#concept_5331AFB6948547F7B8DF367B49360E6B}

<!-- 

c_reports_pageviews.xml

 -->

Ein Trendbericht, der anzeigt, wie oft Ihre Webseiten im ausgewählten Zeitraum (Stunde, Tag, Woche, Monat, Quartal oder Jahr) angesehen wurden. Eine [!UICONTROL Seitenansicht] ist eher eine Anforderung eines ganzseitigen Dokuments als eines Elements einer Seite, wie es beispielsweise ein Bild oder ein Video ist. Wenn z. B. ein einzelner Benutzer während eines Besuchs 15 Seiten aufruft, werden 15 Seitenansichten gezählt. Wenn ein Benutzer die gleiche Seite dreimal während eines Besuchs aufruft, werden drei Seitenansichten gezählt. Anhand dieses Berichts können Sie Seitenansichten jeder Seite auf Ihrer Site sowie die Gesamtübersicht der Seitenansichten auf Ihrer gesamten Site zurückverfolgen.

## Bericht „Besuche“ {#concept_50CA55CF2A41430CBC754AEEEE6023A9}

Zeigt die Anzahl der Besuche auf Ihrer gesamten Website während eines bestimmten Zeitraums an. Ein *Besuch* ist eine Sequenz von Seitenansichten. Ein Besuch beginnt, wenn ein Besucher eine Seite lädt, und endet nach 30 Minuten der Inaktivität. Ein Besuch kann mehrere Stunden dauern, solange der Besucher vor der Zeitüberschreitung mindestens eine Seite lädt. Ein Besuch verläuft jedoch nicht unbedingt gleichzeitig mit einer Browsersitzung. Mit anderen Worten, wenn ein Besucher den Browser schließt, ihn erneut öffnet und fünf Minuten später zu Ihrer Website zurückkehrt, wird dies als Fortsetzung des gleichen Besuchs erkannt. Wenn zudem ein Besucher eine Seite 35 Minuten lang liest, wird der Besuch geschlossen und verarbeitet und ein neuer Besuch beginnt, wenn der Besucher zu einer anderen Seite durchklickt. Besuche werden anhand von Cookies nachverfolgt. Ein Besuch wird nach 12 Stunden durchgehender Aktivität beendet.

<!-- 

c_reports_visits.xml

 -->

In „Marketing Reports and Analytics“ können Sie einen [!UICONTROL „Besuche“-Bericht] auf einer ausgewählten Seite ausführen. In Ad Hoc Analysis haben Sie die Möglichkeit, die Daten zu segmentieren, um bestimmte Seiten anzuzeigen.

## Bericht „Unique Visitors“ {#concept_39097C54E46C496CBAD537329DB3C84A}

Ein Trendbericht, der die Anzahl der Unique Visitors anzeigt, die Ihre Website aufgerufen haben. Jeder Besucher wird einmal gezählt, unabhängig davon, wie oft die Person Ihre Website besucht. Adobe verwendet eine „Cookie-Handshake“-Technologie mit angemeldetem Patent, um einen Unique Visitor von einem wiederkehrenden Besucher zu unterscheiden. Der „Cookie-Handshake“ überwindet die Einschränkungen der Browser-Cookie-Technologie des Internets.

<!-- 

c_reports_unique_visitors.xml

 -->

Weitere Verwendungszwecke dieses Berichts:

* Einblick in die Anzahl der verschiedenen Personen, die Ihre Website während eines beliebigen Zeitraums aufsuchten.
* Ansicht von Verkehrsmustern der letzten Zeit und Einblick in die Promo-Aktivitäten, die Unique Visitor zu Ihrer Site bringen.
* Vergleich der Anzahl der Unique Visitors mit der Anzahl der Seitenansichten.

## Bericht „Besucher“ {#concept_7371DAB5DA474D03A2D1448F151E011B}

Zeigt die Zahl der Unique Visitors Ihrer Site in der jeweiligen Stunde bzw. am jeweiligen Tag, der Woche, im Quartal oder im Jahr. Ein Unique Visitor wird für den ausgewählten Zeitraum nur einmal gezählt. Besucher, die zu Ihrer Website zurückkehren, werden erst nach abgelaufenem Zeitraum wieder als Unique User gezählt.

<!-- 

c_reports_visitors.xml

 -->

Der unten in der Tabelle angezeigte Gesamtwert ist die Summe aller Besuche im angegebenen Zeitraum und gibt nicht immer die Zahl der Unique Visitors wieder. Wenn Sie beispielsweise den Bericht [!UICONTROL Unique Visitors pro Tag] für einen Zeitraum von mehreren Tagen ausführen, kann der Gesamtwert rückkehrende Besucher umfassen, da derselbe Besucher möglicherweise am nächsten Tag zurückkehrt und erneut gezählt wird. Wenn Sie jedoch den Bericht [!UICONTROL Unique Visitors pro Monat] ausführen, spiegelt der Wert in der Spalte „Summe“ genau wider, wie viele individuelle Besucher während des Monats die Site aufsuchen.

## Bericht „Zeit pro Besuch“ {#concept_5CDB759F9C9B4002A786A71F2BDBB292}

Zeigt, wie lange ein Besucher Ihre Website während jedes Besuchs angesehen hat. Er enthält außerdem die Statistik „Durchschn. Besuchszeit pro Site“, die die durchschnittliche Dauer des Besuchs Ihrer Site angibt.

<!-- 

c_reports_time_spent_per_visit.xml

 -->

Verwenden Sie diesen Bericht, um:

* zu erkennen, wie lange Besucher in Ihrer Site verweilen.
* den Site-Inhalt und Promo-Aktionen zu identifizieren, die das Interesse der Besucher erwecken.
* zu erkennen, warum Ihr Traffic-Vorkommen hoch ist, aber die Besucher umgehend aussteigen.

## Bericht „Käufe“ {#concept_E3B9AF43CCD24F25A85D05DFB51C4740}

Zeigt zusammenfassende Daten zu Umsatz, Bestellungen und Einheiten an. Sie können auch den Bericht [!DNL Purchase Conversion Funnel] aufrufen.

<!-- 

c_reports_purchases.xml

 -->

* **Umsatz**: Zeigt den Bruttogewinn aus gewählten Zeiträumen an. Dies wäre z. B. der Umsatz im Monat März, die in der letzten Woche getätigten Käufe oder der Umsatz am aktuellen Tag.
* **Bestellungen**: Zeigt die Anzahl der Bestellungen auf Ihrer Website während des angegebenen Zeitraums an. Bestellungen können mehrere Produkte enthalten.
* **Einheiten**: Zeigt die Gesamteinheiten an, die während des angegebenen Zeitraums bestellt wurden.
* **Einkaufskonversionstrichter**: Ideal für die Anzeige von Konversionsereignissen auf Ihrer Site, sofern diesen in einer bestimmten Reihenfolge durchgeführt werden, z. B. bei Einzelhandelseinstellungen. Ein Konversionstrichterbericht zeigt die Konversionsmetriken für jeden Schritt des Konversionsprozesses sowie Bestellungen, Umsätze und Einheiten an.

## Bericht „Warenkorb“ {#concept_6AEC5A6C707B46B790C1A79E72F9A339}

Zeigt die Anzahl der Warenkörbe an, die während des angegebenen Zeitraums geöffnet werden. Sie haben die Möglichkeit, Warenkorbansichten, Zusätze, Entnahmen und Checkouts zu analysieren. Der Warenkorb wird gewöhnlich geöffnet, wenn der Kunde einen Artikel zum Kauf auswählt, das Öffnen kann jedoch auch ohne einen Artikel erfolgen.

<!-- 

c_reports_shopping_cart.xml

 -->

Den [!UICONTROL Bericht „Warenkorb“] können Sie zu folgenden Zwecken einsetzen:

* Bestimmung von Mustern, Höhen und Tiefen in der Anzahl der auf Ihrer Site geöffneten Warenkorb.
* Untersuchung bestimmter Zeiträume, um Einzelheiten zu den Metriken zu erkennen, die spezifisch zur Öffnung des Einkaufswagens beitrugen.

## Bericht „Benutzerspezifische Ereignisse“ {#concept_9337B2FB8A3F417BA8689FE7FD64629F}

Die Konversionsaktionen auf Ihrer Site, die Benutzer ausführen sollen. Dies kann etwa eine Registrierung, ein Abonnement, ein Abschluss des Interessentenformulars, ein gestarteter Chat, ein Kauf, eine Buchung oder die Teilnahme an einer Umfrage sein.

<!-- 

c_reports_custom_events.xml

 -->

Da jede Report Suite der Analysen unterschiedlich ist, wird dieses Berichtsset für jeden Kunden unterschiedlich eingesetzt. Ein [!UICONTROL benutzerspezifisches Ereignis] kann als Zähler verwendet werden, der angibt, wie oft ein Ereignis auftritt. Wenn Sie beispielsweise **[!UICONTROL event1]** (Ereignis1) auf die Zählung von Dokumentladungen einstellen, zeigt der Bericht [!UICONTROL „Benutzerspezifisches Ereignis“] die Gesamtanzahl der aufgetretenen Ereignisse (Ladevorgänge) an. Sie können mehrere benutzerspezifische Ereignisberichte verwenden.

## Konversionsberichte {#concept_BDD3DD8A46F043BB916C7E346E7C314F}

Zeigt den Umsatz, den Sie aus den verschiedenen Aspekten Ihrer Website erhalten. Dazu gehören der Umsatz aus Werbekampagnen, der Umsatz durch Stammkunden im Vergleich zum Umsatz durch Neukunden, eine Aufschlüsselung des Umsatzes nach Produkt und viele weitere Umsatzberichte. Konversionsberichte können außerdem weitere Erfolgsereignisse wie Werbe-Klicks, Downloads oder andere Ereignisse anzeigen.

<!-- 

c_reports_conversion.xml

 -->

Zur Konversionsberichterstellung gehören Echtzeitstatistiken zu allen wichtigen Kundenaktivitäten wie:

* Kaufstrategien des Kunden
* Warenkorbmetriken, einschließlich Abgang
* Kundenkonversionssätze
* Effizienz der Werbung und Kanalpartner
* Erfolg der Online- und Offline-Marketing-Kampagnenleistung
* Kundenloyalitätsmetriken
* Einblick in die Verkaufszyklen

## Marketingkanalberichte {#concept_81FFA8C15A9B4914BFED37488ADD17FD}

Marketingkanalberichte zeigen die Zuordnung der First Touch- und Last Touch-Kanäle. Der Bericht informiert über geschäftskritische Standardmetriken wie Umsatz, Bestellungen und Kosten und zeigt, wie viel Umsatz die einzelnen Kanäle erzielten. Kanaldefinitionsregeln werden in der [!DNL Admin Console] definiert und es stehen speziell für die Kanalberichte geltende APIs bereit.

<!-- 

c_reports_marketing_channel.xml

 -->

**[!UICONTROL First Touch- oder Last Touch-Kanalbericht]**: Zeigt Metriken an, die Daten zu einem bestimmten First Touch- oder Last Touch-Kanal einblenden. In diesen Berichten können Sie einen Kanal unterteilen und die Details der einzelnen Kanäle anzeigen. Wenn Sie AdLens aktiviert haben, sehen Sie Classifications in Ihren Kanalberichten von „Marketing Reports and Analytics“.

**[!UICONTROL First Touch- oder Last Touch-Kanalbericht]**: Zeigt Details wie Seitennamen und verweisende Stellen an. Diese Informationen werden aus den Kanalwerten extrahiert, die Sie beim Konfigurieren von Regeln in der Option [!UICONTROL Den Kanalwert setzen auf] festgelegt haben. Kanaldetailberichte geben Ihnen die Möglichkeit, die Kanaldetailwerte vom Übersichtsbericht sorgfältig zu prüfen.

Detailliertere Informationen zur Konfiguration des Marketingkanals in „Marketing Reports &amp; Analysen“ finden Sie im Hilfesystem zu [Marketingkanal](/help/components/c-marketing-channels/analyze-mc.md).
