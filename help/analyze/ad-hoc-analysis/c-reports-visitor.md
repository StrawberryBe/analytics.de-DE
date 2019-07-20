---
description: Zeigt Informationen zu Besuchern an, einschließlich der Besucheranzahl, Kundentreue und Besuchermerkmalen.
seo-description: Zeigt Informationen zu Besuchern an, einschließlich der Besucheranzahl, Kundentreue und Besuchermerkmalen.
seo-title: Besucherberichte
solution: Analytics
title: Besucherberichte
topic: Ad Hoc Analysis
uuid: 3 e 9 b 41 d 1-d 6 ff -47 a 8-aa 6 b -829 df 1040 c 34
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Besucherberichte

Zeigt Informationen zu Besuchern an, einschließlich der Besucheranzahl, Kundentreue und Besuchermerkmalen.

## Rückkehrhäufigkeit {#concept_447A99B71E484D27A7A02888CC51FD3D}

Zeigt Ihnen, wie viel Zeit zwischen Besuchen zurückkehrender Besucher vergeht, sowie die Anzahl der Besucher, die in die einzelnen Zeitkategorien fallen. Verwenden Sie den Bericht, um zu ermitteln, wie lange rückkehrende Besucher im Durchschnitt ihre Website nicht besuchen, und um Trends bei rückkehrenden Besuchern zu sehen.

<!-- 

c_reports_return_freq.xml

 -->

Beispielsweise hilft die Anzeige der Bestellungenmetrik in diesem Bericht Onlinehändlern, die effektivsten Zeiten zur Erzeugung von Konversion zwischen Besuchen zu ermitteln. Verwenden Sie diese Informationen, um effektiv Besucher anzusprechen, die Ihre Website seit einer gewissen Zeit nicht mehr besucht haben.

Sie können:

* die Anzahl der wiederkehrenden Besucher sowie die Häufigkeit der erneuten Besuche identifizieren.
* die Attraktivität und Bedeutung Ihrer Website über einen bestimmten Zeitraum hinweg bewerten.
* erfahren, wie sticky Ihre Site für die Besucher ist, und wie oft die Besucher geneigt sind, für weitere Interaktion oder Aktualisierung zur Site zurückzukehren.
* die Auswirkungen Ihres Website-Inhalts und Ihrer Promo-Aktivitäten auf Ihre Besucher identifizieren.

Standardmäßig umfasst der Bericht die folgenden Zeiträume:

* Weniger als ein Tag
* Ein bis drei Tage
* Drei bis sieben Tage
* Sieben bis vierzehn Tage
* Vierzehn Tage bis ein Monat
* Länger als ein Monat

## Besuchnummer {#concept_BBB614072FD74379B1A8520ACB75AE9A}

Zeigt, welcher Kundenbesuch auf Ihrer Website den größten Einfluss auf Ihre Erfolgsmetriken hatte. Ein Besucher, der Ihre Website zum ersten Mal besucht, wird im Zeileneintrag „Besuch Nr. 1“ gezählt. Besucher, die zum zweiten Mal zur Seite zurückkehren, werden im Zeileneintrag „Besuch Nr. 2“ usw. gezählt.

<!-- 

c_reports_visit_number.xml

 -->

Sie können diesen Bericht als Fallout-Bericht verwenden, um zu sehen, ob Besucher zurückkehren. Sie können auch eine Umsatzmetrik hinzufügen, um zu sehen, ob Sie bei erstmaligen Besuchen oder bei darauffolgenden Besuchen mehr Umsatz generieren.

Mit diesem Bericht könnten Sie beispielsweise Fragen wie diese beantworten: Haben Kunden, die bei ihrem vierten Besuch einen Einkauf tätigten, mehr Umsatz generiert als die, die bei ihrem ersten Besuch einkauften?

Sie können diesen Bericht nach jedem anderen Bericht oder jeder anderen Variable unterteilen, um zu ermitteln,

* wie viele Besuche es üblicherweise braucht, bis ein Besucher, der bei Kampagne XYZ durchgeklickt hat, einen Kauf tätigt.
* ob beispielsweise Benutzer in Tokio mehr Besuche als Besucher in London brauchen, bis ein Lead generiert wird.

>[!NOTE]
>
>Wenn derselbe Besucher Ihre Website mehrmals im selben Zeitraum besucht, wird jede angegebene Besuchsnummer bei jedem Besuch inkrementiert.

Dieser Bericht basiert auf den Besucher-ID-Daten, die bei jedem Besuch durch einen Besucher an Adobe weitergegeben werden. Nach Empfang dieser Daten vergleicht Adobe sie mit historischen Daten zur Besucher ID, um festzustellen, ob es sich um einen:

* neuen Besucher (Besuchsnummer gleich 1),
* früheren Besucher, der seinen Besuch fortsetzt (Besuchernummer wird nicht inkrementiert), oder einen
* früheren Besucher, der die Website erneut besucht, handelt (Besuchsnummer wird um 1 inkrementiert).

>[!NOTE]
>
>Jede Analytics-Besucher-ID ist mit einem Besucherprofil auf Adobe-Servern verknüpft. Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.

## Kundenloyalität {#concept_991F758BAA304B7B9D48BD73BBB62FE5}

Nutzen Sie diesen Bericht, um zu sehen, ob Ihr Umsatz eher durch neue oder wiederkehrende Kunden zustande kommt.

<!-- 

c_reports_customerloyalty.xml

 -->

Der Bericht [!UICONTROL Kundeloyalität] gibt Aufschluss über Einkaufsmuster von Kunden, wobei vier Loyalitätskategorien zugrunde gelegt werden:

* **Kein Kunde**: Besucher, die nie einen Einkauf getätigt haben
* **Neuer Kunde**: Besucher, die einen einzigen Einkauf getätigt haben
* **Rückkehrender Kunde**: Besucher, die zwei Einkäufe getätigt haben
* **Loyaler Kunde**: Besucher, die mehr als drei Einkäufe getätigt haben

>[!NOTE]
>
>Wenn Sie diese Metriken verwenden, werden alle Benutzerbesuche (oder alle Besucher) in diesem Bericht dargestellt, unabhängig davon, ob der Besuch (oder Besucher) einen Kauf enthielt.

Der Loyalitätsstatus ändert sich nach dem Ende eines Besuchs, bei dem es zu einem Einkaufsereignis gekommen ist. Beispiel: Ein Neukunde (1 Einkauf) tätigt einen Kauf und registriert sich dann innerhalb desselben Besuchs für einen Newsletter. Das Ereignis zur Newsletter-Registrierung wird dennoch als Interaktion mit einem Neukunden betrachtet, da sich der Kundenloyalitätsstatus erst beim nächsten Besuch ändert.

## Besucherprofil{#concept_4D829198CD144DCDA667E0651F93AFC7}   

Zeigt Informationen über die Art von Besuchern an, die Ihre Site aufrufen. Sie können beispielsweise den Standort des Besuchers anzeigen und feststellen, welchen Browser bzw. welche Computerhardware er verwendet, welche Sprache er eingestellt hat und welchen Internetserviceanbieter er benutzt.

<!-- 

c_reports_visitor_profile.xml

 -->

** [!UICONTROL Languages] **: Displays your visitors’ preferred languages, captures the default browser language, and displays the languages that visitors use most often on your site.

** [!UICONTROL Domains] **: Lists the organizations and ISPs your visitors use to access your site. Dieser Bericht unterscheidet sich vom Bericht [!UICONTROL Vollständige Domänen] insofern, als der Bericht Vollständige Domänen die vollständige ISP-Domäne registriert, während dieser Bericht die sekundäre Domäne auflistet.

** [!UICONTROL Top Level Domains] **: Identifies world regions that visitors come from based on their originating domain extension, and shows how many visitors come from these countries. Domänen mit den Erweiterungen kommerzieller Einrichtungen (.com), von Netzwerken (.net), des Bildungswesens (.edu), von Regierungsbehörden (.gov) und Organisationen (.org) befinden sich meistens in den USA und sind gesondert von anderen Domänen aufgeführt.

** [!UICONTROL Visitor ZIP/Postal Code] **: Displays the zip and postal codes that produced the customers that had the greatest effect on purchase success metrics.

## GeoSegmentation {#concept_7C1B930F90F945B49205D3855CAE1813}

<!-- 

c_reports_geosegmentation.xml

 -->

Zeigt die geografische Dynamik Ihrer Besucher in Echtzeit, einschließlich der Länder, Bundesländer (bzw. Bundesstaaten) und Städte, von denen aus sie die Site durchsuchen. Darüber hinaus erhalten Sie einen wichtigen Einblick in die Technologie und Vorlieben der Zielgruppe Ihrer Website.
