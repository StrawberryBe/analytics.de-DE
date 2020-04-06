---
description: Zeigt Informationen zu Besuchern, wie beispielsweise Besucherzahlen, Kundentreue und Besuchereigenschaften, an.
title: Besucherberichte
topic: Ad hoc analysis
uuid: 3e9b41d1-d6ff-47a8-aa6b-829df1040c34
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Besucherberichte

Zeigt Informationen zu Besuchern, wie beispielsweise Besucherzahlen, Kundentreue und Besuchereigenschaften, an.

## Rückkehrhäufigkeit {#concept_447A99B71E484D27A7A02888CC51FD3D}

Zeigt die Zeitdauer zwischen Besuchen von zurückkehrenden Besuchern und die Anzahl der Besuche, die in die Kategorie mit der jeweiligen Zeitdauer fallen. Verwenden Sie den Bericht, um zu sehen, wie viel Zeit wiederholte Besucher im Durchschnitt verbringen, ohne Ihre Site zu besuchen, und um Trends bei Wiederholungskunden anzuzeigen.

<!-- 

c_reports_return_freq.xml

 -->

Wenn Sie beispielsweise die Metrik &quot;Bestellungen&quot;in diesem Bericht anzeigen, kann eine für den Handel bestimmte Site die effektivste Zeit zwischen den Besuchen bei der Generierung der Umrechnung verstehen. Verwenden Sie diese Informationen, um Besucher, die Ihre Site nicht besuchen, effektiv zu vermarkten.

Sie können:

* die Anzahl der rückkehrenden Besucher sowie die Häufigkeit der erneuten Besuche zu identifizieren.
* Bewerten Sie die Attraktivität und Relevanz Ihrer Website für Besucher im Laufe der Zeit.
* zu erfahren, wie hoch die Stickiness Ihrer Site für die Besucher ist, und wie oft die Besucher geneigt sind, für weitere Interaktion oder Aktualisierung zur Site zurückzukehren.
* Finden Sie heraus, wie sich der Inhalt und die Promotions Ihrer Website auf Ihre Besucher auswirken.

Standardmäßig hat dieser Bericht die folgenden Zeitspannen:

* Weniger als ein Tag
* Ein bis drei Tage
* Drei bis sieben Tage
* Sieben bis vierzehn Tage
* Vierzehn Tage bis ein Monat
* Länger als ein Monat

## Besuchsnummer {#concept_BBB614072FD74379B1A8520ACB75AE9A}

Zeigt, welche Anzahl von Besuchen auf Ihrer Site Ihre Erfolgsmetriken am stärksten beeinflussten. Ein Besucher, der Ihre Site zum ersten Mal besucht, wird im Zeileneintrag &quot;Besuch Nr. 1&quot;gezählt. Besucher, die für einen zweiten Besuch zur Site zurückkehren, werden im Zeileneintrag &quot;Besuch Nr. 2&quot;usw. gezählt.

<!-- 

c_reports_visit_number.xml

 -->

Sie können diesen Bericht als Trichteranalysebericht verwenden, um zu sehen, ob Besucher zurückkehren. Sie können auch eine Umsatzmetrik hinzufügen, um zu sehen, ob Sie mehr Umsatz aus ersten Besuchen oder nachfolgenden Besuchen generieren.

Dieser Bericht könnte beispielsweise folgende Fragen beantworten: Haben Kunden, die beim vierten Besuch gekauft haben, mehr Umsatz generiert als diejenigen, die beim ersten Besuch gekauft haben?

Sie können diesen Bericht nach jedem anderen Bericht oder jeder anderen Variablen aufschlüsseln, um Folgendes festzustellen:

* Wie viele Besuche dauert es normalerweise, bis ein Benutzer, der durch Kampagne XYZ geklickt hat, einen Einkauf tätigt.
* Ob beispielsweise Benutzer in Tokio mehr Besuche machen, bevor sie einen Interessenten generieren, als Benutzer in London.

>[!NOTE] Wenn derselbe Besucher Ihre Website mehrmals im selben Zeitraum besucht, wird jede angegebene Besuchsnummer bei jedem Besuch inkrementiert.

Dieser Bericht basiert auf den Besucher-ID-Daten, die bei jedem Treffer von Besuchern an Adobe übergeben werden. Da diese Daten empfangen werden, vergleicht Adobe sie mit historischen Besucher-ID-Daten, um festzustellen, ob der Treffer:

* Ein neuer Besucher (Besuchsnummer gleich 1).
* Ein vorheriger Besucher, der einen Besuch fortsetzt (Besuchsnummer wird nicht inkrementiert).
* Ein früherer Besucher, der einen neuen Besuch durchführt (Besuchsnummer wird um 1 inkrementiert).

>[!NOTE] Jede Analytics-Besucher-ID ist einem Besucherprofil auf Adobe-Servern zugewiesen. Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.

## Kundentreue {#concept_991F758BAA304B7B9D48BD73BBB62FE5}

Nutzen Sie diesen Bericht, um zu sehen, ob Ihr Umsatz eher durch neue oder wiederkehrende Kunden zustande kommt.

<!-- 

c_reports_customerloyalty.xml

 -->

Der [!UICONTROL Customer Loyalty] Bericht zeigt Einkaufsmuster von Kunden basierend auf vier Kategorien der Treue an:

* **Kein Kunde**: Besucher, die noch nie gekauft haben
* **Neuer Kunde**: Besucher, die einen einzigen Einkauf tätigten
* **Rückkehrender Kunde**: Besucher, die zweimal gekauft haben
* **Loyaler Kunde**: Besucher, die mehr als drei Einkäufe getätigt haben

>[!NOTE] Bei der Verwendung dieser Metriken werden alle Besuche (oder Besucher) eines Benutzers in diesem Bericht repräsentiert, unabhängig davon, ob im Besuch (oder Besucher) ein Kauf inbegriffen war.

Der Treuestatus ändert sich nach dem Ende des Besuchs, wenn ein Ereignis zum Kauf eintritt. Beispielsweise tätigt ein Neukunde (1 Einkauf) einen Kauf und registriert sich dann während desselben Besuchs für einen Newsletter. Das Ereignis zur Newsletter-Registrierung wird dennoch als Interaktion mit einem Neukunden betrachtet, da sich der Status der Kundenloyalität erst beim nächsten Besuch ändert.

## Besucherprofil {#concept_4D829198CD144DCDA667E0651F93AFC7}

Zeigt Informationen zum Typ des Besuchers an, der Ihre Site aufsucht. Sie können die Lage des Besuchers, die Art der verwendeten Browser und Computerhardware, die verwendeten Sprachen und die Daten des Internet-Dienstleisters für Ihre Besucher sehen.

<!-- 

c_reports_visitor_profile.xml

 -->

**[!UICONTROL Languages]**: Zeigt die bevorzugte Sprache Ihrer Besucher an, zeichnet die Standardsprache des Browsers auf und zeigt an, welche Sprachen Besucher am häufigsten auf Ihrer Site verwenden.

**[!UICONTROL Domains]**: Listen der Organisationen und ISPs, die Ihre Besucher zum Zugriff auf Ihre Site verwenden. This report differs from the [!UICONTROL Full Domains] report in that the Full Domains report registers the full ISP domain, whereas this report lists the secondary domain.

**[!UICONTROL Top Level Domains]**: Identifiziert anhand der ursprünglichen Domänenerweiterung die Regionen in der Welt, aus denen Besucher stammen, und zeigt an, wie viele Besucher aus diesen Ländern kommen. Domänen, die in &quot;Commercial&quot;(.com), &quot;Network&quot;(.net), &quot;Education&quot;(.edu), &quot;Government&quot;(.gov) und &quot;Organization&quot;(.org) enden, sind in der Regel in den Vereinigten Staaten ansässig und werden getrennt von den übrigen Domänen aufgeführt.

**[!UICONTROL Visitor ZIP/Postal Code]**: Zeigt die Postleitzahlen an, aus denen die Kunden stammen, die die Erfolgsmetrik des Kaufs am stärksten beeinflussten.

## GeoSegmentation {#concept_7C1B930F90F945B49205D3855CAE1813}

<!-- 

c_reports_geosegmentation.xml

 -->

Zeigt die geografische Dynamik Ihrer Besucher in Echtzeit an, einschließlich der Länder, Bundesstaaten und Städte, aus denen sie navigieren. Sie können auch wichtige Einblicke in die Technologie und Präferenzen der Audience Ihrer Website gewinnen.
